# chapter 7. tests
## 7.1. test constructs
double bracket ((...)) and let ... constructs expands and evaluates *arithetic expressions*. exit stati, if successfull will be 0, and unsuccessful tests be nonzero. the equivalent of a bare exit is exit $?.
bitwise vs logical OR: logical operators short-circuit, whereas bitwise never does. by the principle of least astonishment, use the logical OR.
if-then-else conditions are useful if you are not sure what the output will be. a useful contraction for else if is elif.
put your if conditions in square brackets [ ... ].
the test command is the exact same as the left bracket [, so if test condition is the same as if [ condition ].
double square brackets [[ ... ]] is the extended test command. using this syntax can prevent logic errors, as ||, &&, < and > will throw errors in [ ... ] but work in [[ ... ]]
if COMMAND returns exit status of COMMAND, you don't *need* to put it in brackets, it's just common practice. so do it.
the exit status given by (( ... )) is the opposite of the status given by [[ ... ]]
## 7.2. file test operators