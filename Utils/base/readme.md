# ↔️Base
The library provides conversion of numbers between different number systems.

## 📦Avaliable functions
### base-from-dec
This function takes two arguments: base, decimal number and then convert the decimal number to a given base number.
```
  {base-from-dec> 2> 10}
```
> Returns: 1010 (10dec = 1010bin)
```
  {base-from-dec> 8> 15}
```
> Returns: 17
```
  {base-from-dec> 16> 255}
```
> Returns: FF

### base-to-dec
This function takes two arguments: base, number in that base and then converted to decimal base number.
```
  {base-to-dec> 2> 111}
```
> Returns: 7 (111bin = 7dec)
```
  {base-to-dec> 8> 43}
```
> Returns: 35
```
  {base-to-dec> 16> 4E}
```
> Returns: 78 *known bugs, pending fix

## *Macros*
### bin-from-dec
```
  {bin-from-dec> 10}
```
### oct-from-dec
```
  {oct-from-dec> 10}
```
### hex-from-dec
```
  {hex-from-dec> 54}
```

### bin-to-dec
```
  {bin-to-dec> 1011}
```
### oct-to-dec
```
  {oct-to-dec> 71}
```
### hex-to-dec
```
  {hex-to-dec> AB}
```


## 🚛Author
Maciek Bandura, https://github.com/bandurama