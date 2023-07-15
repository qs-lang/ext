
# scheduler for qs21 lang
## About
Simple scheduler, provides higher abstraction layer.
Might be incorporated to *qvm* directly in C.
It pretty much mimics all of the functionality of 
the og scheduler.

Originally i was planning to ship qs with built
in scheduler, but essentially i've decided to
drop it out, as it adds unnecesair complexity
to the qvm, and according to *qs21* ideology
everything that's unnecesair has to be cut out
from the final project.

Non the less, from the perspective of qs21 developer,
a scheduler is an extremally usefull piece of software.
So here is a pure qs21 implementation of it.


## Usage
The end user might want to *yield* the executiong of something
in time, hence:
```
    {yield> time-in-seconds> expression}
```

For instance:
```
    {yield> 3> {puts: Hello World!{nl}}}
```

And this should be *enaugh*, unless *qvm* doesn't support
scheduling right out of the box. In such case user might
want to *use* sched.q file, and actually create a loop
that will proc *sched*uler to work. In such case:
```
    {use> ./lib/sched}

    {yield> 3> {puts> PASS!}}


    {while> {if-gt: {SCHED-len}> 0}>
        {sched}
    }
```

Scheduler is particularly usefull with *call builders* like `qq`:
```
    {use> ./lib/core}
    {use> ./lib/sched}

    {def> say-hello> nth>
        {puts: {SCHED-len} Hello! {nth} {nl}}
        {if: {nth}> )> 0>
            {yield> 1: {qq> say-hello: {clc: {nth}> -> 1}}}
        >}
    }

    {say-hello> 10}

    {while> {if-gt: {SCHED-len}> 0}>
        {sched}
    }
```

## Source
For simplicity reason, scheduler consists of two *index linked* arrays:
`SCHED` and `SCHEDEXPR`, first one contains timings and the second one
contains expressions that are yielded in time. 

`yield` pushes elements to their respective arrays, `expr` is not changed,
however `time` has the actuall timestamp added to it's value, and is later
used to determine when-to executed expression from respective SCHEDEXPR array.
`sched` loops throught SCHED array and checks if time has come, to evaluated
yielded expressions, if so it does so, and then removes both elements from
both arrays.