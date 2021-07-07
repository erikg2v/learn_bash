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
there are several (many) operators that you can enter in an IF statement which return true/false based on [ condition ]. some examples are -e (file exists), -d (file is directory), -s (file is of nonzero size), and -O (you are owner). the ! character reverses the sense of these tests, and returns true if [ condition ] is absent.
## 7.3. other comparison operators
binary comparison operators compare two variables or quantities. note that integer and string comparisons use different operators (because bash).
string comparisons use the typical =, <, ==, etc operators, whereas integer comparisons use things like -eq (equal), -gt (greater than), and -ge (greater than or equal to). for strings, -z tests if null, and -n tests for not null. a practice is to always quote strings under test, because bash.
## 7.4. nested if/then condition tests
condition tests using if/then statements may be nested. this is in effect equivalent to using &&. cool. 
i think the only purpose of this is to increase readability and reduce the bash-ness of the script. 
## 7.5. testing your knowledge of tests
if - tests if the xclients file is executable from $HOME path
elif - goes to where the file is stored in files and executes it directly
else - does some random xterm bullshit and then netscapes the index.html file which is probably an error message