# 🧬Binary
The library provides bitwise operations such as and, or, xor and not. Additionaly contains few helper functions.

## 📦Avaliable functions
### bin-and
```
  {bin-and> 0101> 1010}
```
> Returns: 0 (Conjunction of two binary numbers)

### bin-or
```
  {bin-or> 0101> 1010}
```
> Returns: 1111 (Disjunction of two binary numbers)

### bin-xor
```
  {bin-xor> 0101> 1010}
```
> Returns: 1111 (Exclusive disjunction of two binary numbers)

### bin-not
```
  {bin-not> 1010}
```
> Returns: 101 (Negation of binary number)

### bin-pad
Takes two binary numbers stored in variables named: a, b and padds them with zeros, to the same length.
```
  {def> a> 101}
  {def> b> 1010}
  {bin-pad}
```
> appends zero to the value inside a, a := 0101

### bin-del-zeros
Removes proceeding zeros from a given binary number
```
  {bin-del-zeros> 00101}
```
> Returns: 101 (without proceeding zeros)

## 🚛Author
Maciek Bandura, https://github.com/bandurama