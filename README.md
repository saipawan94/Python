# Python

*Reserved words

Variable, Operator, Constant, Reserved Words.

conditional steps.
if, elif, elif,else.

Intendation.

Repeated steps (while loop, for).

Sequential

Constants -- Fixed values such as numbers, strings, letters. String constants use single quotes & double quotes.

Reserved words -- print, if, else, while,...

Variables is a name place where we can store data and use it later. x=1, y=2.
Should start with letter or underscore. Case sensitive, must consist of letters, numbers & underscores.

Operators --

![image](https://github.com/saipawan94/Python/assets/82724257/35ffce32-6ed3-41d3-8109-66638e732e8d)


```
xx=2

xx = xx + 2

print(xx)

yy = 440 * 12

print(yy)

zz = yy / 1000

print(zz)

jj = 23
kk = jj % 5

print(kk)
```

Order of precedence --
Paranthesis
Power(**)
Multiplication
Addition
Left to Right

1 + 2 ** 3 / 4 * 5 --> 11.0

Data types:
-----------

d = 1 + 4 by default these are considered as integers.
e = 'hello ' + 'there' --> hello there

Type always matters and some operations are prohibited.

```
e = 'hello ' + 'there'
e = e + 1
This gives error Can't convert 'int' object to str implicitly.
```

```
eee='hello'
eee = eee + 1

    eee = eee + 1
          ~~~~^~~
TypeError: can only concatenate str (not "int") to str
>>> type(eee)
<class 'str'>
```

Integer, String, float,
```
converting integer to floatingpoint
i = 10

f = float(i)

print(f)
10.0
```

>> Integer division in python 3 always gives floating point result.
```
i = 10

print(i/2)
5.0
```

String conversions:

We can use int() and float() to convert between strings and integers. we will get an error if the string does not contain numeric values.

sval = '123'
print(sval + 1) --> error

ival = int(sval)
print(ival + 1) --> 124

nsv = 'hello'
niv = nsv + 1 --> error.
niv = int(nsv) --> error.


INPUT:
------

We can intruct python to read data from the user using input() function.

```
name = input('Who are you?')
print('Welcome', name);
WHo are you? Pavan
Welcome Pavan
```

Converting User Input:
------------------------

Whenever we are reading from input from user it an string, we must convert to other datatypes based on the requirement.

Example:
-
Europe floor converter to US(0 -->1, 1--> 2, 2-->3).

```
euf = input('Enter floor number: ')
usf = int(euf) + 1
print('Entered floor number is: ', usf)
Enter floor number: 0
Entered floor number is:  1
```

Comments in Python are useful to know whats there in code and helps as a heading.


COnditional Execution:
------------------------
If we give two if statements in a program it will execute both the If clauses.

```
x = 5
if x < 10:
    print ('Smaller')
if x > 20:
    print('Bigger')
print('Finish')

Smaller
Finish
```

Comparision Operators:
------------------------
<, <=, >, >=, ==, !=

```
x = 5
if x == 5:
    print('Equals to 5')
if x > 4:
    print('Greater than 4')
if x >=5:
    print('Greater than or equal to 5')
if x <=6:
    print('Less than or equal to 6')
if x < 6:
    print('Less than 6')
if x!=6:
    print('Not equal to 6')

Equals to 5
Greater than 4
Greater than or equal to 5
Less than or equal to 6
Less than 6
Not equal to 6
```

Nested decissions:
-

```
x = 42
if x > 1:
    print('More than one')
    if x < 100:
        print('Less than 100')
print('All done')

More than one
Less than 100
All done
```

Two-way decission:
---

If we use 2 if's in a program both will get executed, but if-else will make either 'if' will be executed or 'else' will be executed.
```
x = 4
if x > 2:
    print('Bigger')
else:
    print('Smaller')
print('All done')

Bigger
All done
```

Multi-way decission:
---

**elif will be executed only when if condidion fails.**
```
x = -1
if x > 2:
    print('Bigger')
elif x < 10:
    print('Medium')  
else:
    print('Smaller')
print('All done')
```

Try/ Except:
-

If first condition fails the other dependent conditions also fails.
eg.

```
astr = 'Hello'
istr = int(astr)
print('First', istr)
astr = '123'
istr = int(astr)
print('Second', istr)

    istr = int(astr)
           ^^^^^^^^^
ValueError: invalid literal for int() with base 10: 'Hello'
```

This can be overcome by using try, except.

```
astr = 'Hello'
try:
    istr = int(astr)
except:
    istr = -1
print('First', istr)

astr = '123'
try:
    istr = int(astr)
except:
    istr = -1
print('Second', istr)

First -1
Second 123
```

So first block fails then its entering into except otherwise it will execute try.

Functions:
--

Funtions can be created by using "def", functions just like a placeholder which holds the program lines.
Main use of function is create once and use it multiple times by calling it.
We can define function using def word.
Some functions can also take arguments as an input.

```
def thing():
    print('This is a function')

thing()

This is a function
```

There are two typles of function.
1. Built-in functions. --> print(), input(), type(), float(), int()
2. Defined functions.

Built-in functions are like reserved words.

```
big = max('Hello world')
print(big)

tiny = min('Hello world')
print(tiny)

w

```

Here max(), min() are reserved words.

