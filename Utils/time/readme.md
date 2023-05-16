# ⌛time
The library provides functions for working with dates and timestamps. It offers a variety of functionalities such as converting dates to timestamps, converting timestamps back to dates in the appropriate format, and retrieving the current date from the system. It also provides functions to perform basic operations on those dates, that is adding and substracting entire dates, hours, seconds and so on.

The conversion functions enable you to convert a specific date into a timestamp, which represents the number of seconds or milliseconds since a particular reference point (usually the Unix epoch). This is useful for storing and manipulating dates in a numeric format.

Conversely, you can convert a timestamp back into a human-readable date format using the appropriate formatting function. This allows you to display timestamps in a more understandable and visually appealing manner.

Additionally, the library provides a function to retrieve the current date and time from the system. This feature is helpful when you need to work with the current date for various purposes like logging, time tracking, or scheduling events.


## 📖Documentation
###Formating standard acording to POSIX.
| Formatter | Description |
| :-: | --- |
| `%a` | shortened **week** name (eg. Mon) |
| `%A` | full **week** name (eg. Monday) |
| `%u` | day of the week #1 (1 - monday.. 7 - sunday) |
| `%w` | day of the week #2 (0 - sunday.. 6 - monday) |
| `%d` | two digit **month** (eg. 01, 02, ..., 31) |
| `%b` | shortened **month** name (eg. Jan) |
| `%B` | full **month** name (eg. January) |
| `%m` | number of **month** (from 01st january, up to 12th december) |
| `%y` | two digit **year** number (eg. 21 for 2021) |
| `%Y` | four digit **year** number (eg. 2021) |
| `%H` | 24 **hour** format |
| `%h` | 12 **hour** format  |
| `%p` | **hour** sufix (either AM or PM) |
| `%M` | **minute** |
| `%s` | **second** |
| `%z` | time zone name |
| `%t` | timestamp |

###Time calculations
During addition and substraciotns (leep year isn't taken into account):
  1 year - 365 days
  1 month - 30 days

###Internal time representation (**ITR**)
Internal functions utilises this format to store and process date and time information.
```
  %Y;%m;%d;%H;%M;%s
```


## 📦Avaliable functions
### time
This function takes formated string and supply it with time and date information.
```
  {time> Today is %Y/%m/%d }
```
> Returns: Today is 2023/05/16

### time-date-val
This function takes formated string and according to that string rest of the time information as separate arguments. Returns ITR.
```
  {time-date-val> Ymd> 2020> 8> 25}
```
> Returns: 2020;8;25;0;0;0

### time-date-to-timestamp
This function takes ITR and returns converted timestamp.
```
  {time-date-to-timestamp: {time-date-val> YmdHMs> 2020> 8> 25> 14> 30> 50}}
```
> Returns: 1598365850

### time-date-from-timestamp
This function timestamp and returns ITR.
```
  {time-date-from-timestamp> 1598365850}
```
> Returns: 2020;8;25;14;30;50

### time-clc
This function takes first ITR, operator and second ITR. Returns a result of either addition (+) or substraction (-) of two dates.
```
  {time-clc: {time-date-val> YmdHM> 2020> 8> 25> 10> 15}> +: {time-date-val> mH> 2> 10}}
```
> Returns: 2020;10;24;20;15;0

### time-gen
This function retrives time and date from system and stores it in **time-val** array.
```
  {time-gen}
```
> Defines array with actual time and date.

### time-conv
This function converts formatting symbol into a value from **time-val** array.
```
  {time-conv> d}
```
> Returns: Actual day from **time-val** array.

### time-leap-year
This predicate returns one if given year is leep or 0 otherwise.
```
  {time-leap-year> 2023}
```
> Returns: 0.

## *Macros*
### time-date-add
```
  {time-date-add: {time-date-val> Ymd> 2020> 8> 25}: {time-date-val> s> 3600}}
```

### time-date-sub
```
  {time-date-sub: {time-date-val> Ymd> 2020> 8> 25}: {time-date-val> s> 3600}}
```

### time-date-days-add
```
  {time-date-add-days: {time-date-val> Ymd> 2020> 8> 25}> 5}
```

### time-date-days-sub
```
  {time-date-add-days: {time-date-val> Ymd> 2020> 8> 25}> 5}
```

## 🚛Author
Maciek Bandura, https://github.com/bandurama