# 🎲Rand
The library provides random number generator along with bunch of usefull macros. It uses [Linear congruential generator](https://en.wikipedia.org/wiki/Linear_congruential_generator).

## 📦Avaliable functions
### rand
This function returns a random number 
```
  {rand}
```
> Returns: 1843498746 (random value)

### rand-range
This function returns a random number in range between min and max value (both inclusive). 
```
  {rand-range> 1> 10}
```
> Returns: 5 (random value in range)

### rand-arr
This function returns a random element from a given array.
```
  {arr-def> tab> A> B> C}
  {rand-arr> tab}
```
> Returns: B (random value from tab array)

### rand-shuffle
This functions shuffles given array
```
  {arr-def> tab> A> B> C}
  {arr-shuffle> tab}
```
> Tab has been shuffled 

## 🌎globals
### rand-seed
Seed used by RNG. Uses epoch time. Works only on Windows and Linux.

## 🚛Author
Maciek Bandura, https://github.com/bandurama
