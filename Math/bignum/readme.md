# 💪bignum
The library included with the programming language is specifically designed for working with large numbers that exceed the range of typical numeric data types like int or long. The library provides a set of mathematical operations allowing basic arithmetic operations on these large numbers. The supported operations include addition, subtraction, multiplication, division, modulo, and comparison.

## 📦Avaliable functions
### big-add
This named expression adds two (big) numbers
```
  {big-add> 9999999999> 2}
```
> Returns: 10000000001

### big-sub
This named expression substracts two (big) numbers
```
  {big-sub> 10000000001> 3}
```
> Returns: 9999999998

### big-mul
This named expression multiplies two (big) numbers
```
  {big-mul> 9999999> 9999999}
```
> Returns: 99999980000001

### big-div
This named expression divides two (big) numbers
```
  {big-div> 99999999999> 9}
```
> Returns: 11111111111

### big-mod
This named expression returns the reminder of two (big) numbers division
```
  {big-mod> 99999999999> 2}
```
> Returns: 1

### big-if-gt
This predicate returns truth if left number is greater then right
```
  {big-if-gt> 99999999999> 88888888888}
```
> Returns: 1

### big-if-ls
This predicate returns truth if left number is lesser then right
```
  {big-if-ls> 99999999999> 88888888888}
```
> Returns: 0

### big-if-eq
This predicate returns truth if both numbers are equal
```
  {big-if-eq> 99999999999> 88888888888}
```
> Returns: 0

### big-clc
This named expression is an analogue to the clc function from standard library - works with big numbers.
```
  {big-clc> 99999999999> -> 88888888888> /> 2}
```
> Returns: 5555555555

### big-del-zeros
This named expression removes preciding zeros
```
  {big-del-zeros> 0000099999999}
```
> Returns: 99999999

### big-is-neg
This predicate returns truth if number is negaitve
```
  {big-is-neg> -99999999999}
```
> Returns: 1

### big-rs
This named expression removes sign from number
```
  {big-rs> -99999999999}
```
> Returns: 99999999999

### big-abs
This named expression returns absolute value of a number
```
  {big-abs> -99999999999}
```
> Returns: 99999999999

## ⚠️Notice
Named expressions: ```uadd```, ```usub```, ```umul```, ```umod``` and ```udiv``` works only with unsigned numbers.


## 🚛Author
Maciek Bandura, https://github.com/bandurama