# ⚡uri
The library provides functions for encoding and decoding URIs. These functions can be used to convert special characters in URIs into their respective encoded representations, or to decode an already encoded uri back into its original format. This allows for proper handling of uris in various applications, such as web development or data processing.

## 🔥Requires
-[base](https://github.com/qs-lang/ext/tree/main/Utils/base) library

## 📦Avaliable functions
### uri-encode
This function returns a encoded string acording to RFC3986 specification. 
```
  {uri-encode> Hello, world!}
```
> Returns: Hello%2C%20world%21

### uri-decode
This function decodes percent-encoded strings.
```
  {uri-decode> Hello%2C%20world%21}
```
> Returns: Hello, world!

### uri-char-to-utf8
This function returns percent-encoded char. 
```
  {uri-char-to-utf8> !}
```
> Returns: %21 

### uri-char-to-utf8
This function returns decoded char. 
```
  {uri-utf8-to-char> %21}
```
> Returns: ! 


## 🚛Author
Maciek Bandura, https://github.com/bandurama
