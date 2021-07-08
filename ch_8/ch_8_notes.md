# chapter 8. operations and related topics
## 8.1. operators
bash supports 64-bit integers, but does not understand floating point arithmetic. it treats numbers containing a decimal point as strings. floats will be handled in ch. 16. \
bitwise operators rarely make appearances in shell scripts, but logical (boolean) ones are common in if/then statements. \
the comma operator , chains together two or more arithmetic operations, but comes with some side effects (TBD) \
## 8.2. numerical constants
shell scripts interpret numbers as base 10 by default. a number preceeded by a 0 is osctal, and 0x is hex. a number with an embedded # evaluates as base#number. \
## 8.3. the double-parenthesis construct
the (( ... )) construct permits arithmetic expansion and evaluation, just like in C. \
## 8.4. operator precedence
my dear aunt sally - multiply, divide, add, subtract. \
compound logical operators (&& || -a -o) have low precedence. \
order of evaluation of equal-precedence operators is "usually" left-to-right. \
note - to avoid confusion or error in complex operators, break it up into bracketed sections. use [[ ... ]] to separate different sections. \