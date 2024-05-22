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

> Argument is a value we pass into the function as its input when we call the function.
> We use arguments so we can direct function to do differnt kinds of work when we call it different times.
max('Hello world')
>

```
def greet(lang):
    if lang == 'es':
        print('Hola')
    elif lang == 'fr':
        print('Bonjour')
    else:
        print('Hello')
        
greet('es')

Hola
```

Return Values:
-

Return statement is used to return a value once we called the function.

```
def greet():
    return "Hello"
print(greet(), "Pavan")

Hello Pavan
```


```
def greet(lang):
    if lang == 'es':
        return 'Hola'
    elif lang == 'fr':
        return 'Bonjour'
    else:
        return 'Hello'

print(greet('es'), 'Pavan')

Hola Pavan
```

We can pass multiple parameters to a function.

```
def addtwo(a,b):
    added = a + b
    return added

x = addtwo(1,2)
print(x)

3
```

Loops and Iteration:
-----

While --

Until the condition is false the loop will iterate continuously.

```
n = 5

while n > 0:
    print(n)
    n = n -1
print('Loop Completed')
print(n)

```

This loop iterates until n = 0.
If the condition fails it wont touch the block of code inside the loop. In this condition its similar to IF statement because If will fail if condition is false.

**break** statement will break the loop and comes out of loop immediately.
break should be used with in a loop.

```
while True:
    line = input('> ')
    if line == 'done':
        break
    print(line)
print('Done')

> done
Done
```

```
line = input('> ')
if line == 'done':
    break

"break" can be used only within a loopPylance
```

**continue** ends the current iteration and jumps to top of the loop and starts next iteration.

```
while True:
    line = input('> ')
    if line[0] == '#':
        continue
    if line == 'done':
        break
    print(line)
print('Done')

> 1
1
> done
Done
```

While loop is a **indefinite loop**, because they keep going until a logic condition becomes False.

**Definite Loops**(for):
----

For loop is an definite loop becuase it will run exact number of times which we define. 
This will have iteration variable, which will helps to iterate.
For loop will decide how many times it should run the loop.

```
for i in [3,2,1]:
    print(i)
print('ENd of for loop')

3
2
1
ENd of for loop
```

```
friends = ['Pavan', 'Sai', 'Gani']

for friend in friends:
    print('Hello: ', friend)
print('Welcome!')

Hello:  Pavan
Hello:  Sai
Hello:  Gani
Welcome!
```

**Largest Number**
```
a = [3,41,12,9,74,15]
b = 0

for i in a:
    if i > b:
        b=i
print('Largest is:', b)

Largest is: 74
```

Count of numbers:
-
```
a = 0
b = [1,2,3,4]

for i in b:
    a = a + 1
    print(a, i)
print('Count is: ', a)

1 1
2 2
3 3
4 4
Count is:  4
```

Summing using loop:
-
```
a = 0
b = [1,2,3,4]

for i in b:
    a = a + i
    print(a, i)
print('Count is: ', a)

1 1
3 2
6 3
10 4
Count is:  10
```

Average in a Loop:
-
```
count=0
sum=0

print('Before', count, sum)
for value in [1,2,3,4]:
    count = count + 1
    sum = sum + value
    print(count, sum, value)
print('After', count, sum, sum/count)

Before 0 0
1 1 1
2 3 2
3 6 3
4 10 4
After 4 10 2.5 
```

Filtering in a Loop:
-
```
print('Before')
for value in [1,2,3,4,5]:
    if value > 3:
        print('Large number is: ', value)
print('After')

Before
Large number is:  4   
Large number is:  5   
After
```

Search using a Boolean Variable:
-
```
found = False

print('Before', False)

for value in [9, 41, 12, 3, 74, 15]:
    if value == 3:
        found = True
        print(value, found)
    else:
        found = False
        print(value, found)
print('After', found)

Before False
9 False    
41 False   
12 False   
3 True     
74 False   
15 False   
After False
```

Smallest value using for, if.

**None** datatype means empty.

```
smallest = None
print('Before')

for value in [9, 41, 12, 3, 74, 15]:
    if smallest == None:
        smallest = value
    elif value < smallest:
        smallest = value
    print(smallest, value)
print('Smallest is:', smallest)

Before
9 9
9 41
9 12
3 3
3 74
3 15
Smallest is: 3
```

**is and is not Operators**
These are used in logical expressions, it is stronger than "==".
0 == 0.0 --> True
0 is 0.0 --> false

```
smallest = None
print('Before')

for value in [9, 41, 12, 3, 74, 15]:
    if smallest is None:
        smallest = value
    elif value < smallest:
        smallest = value
    print(smallest, value)
print('Smallest is:', smallest)

Before
9 9
9 41
9 12
3 3
3 74
3 15
Smallest is: 3
```

Strings:
--

> It is a sequence of characters.
> We can use single-quotes or double-quotes.
> For strings, + means concatenation.
> If a string contains numbers, it is still a string.
> We can convert numbers in a string to numbers using int().
> Reading input from user is always string, we have to parse and convert the data.
>

```
name = input('Enter: ')
print(name)

Enter: Pavan
Pavan  

apple = input('Enter: ')

x = apple - 10

print(x)

Enter: 100
Traceback (most recent call last):
  File "c:\Users\veprathi\Downloads\print('Hello World').py", line 6, in <module>
    x = apple - 10
        ~~~~~~^~~~
TypeError: unsupported operand type(s) for -: 'str' and 'int'

apple = input('Enter: ')

x = int(apple) - 10

print(x)

Enter: Pavan
Pavan
Enter: 100
90
```

Here apple = 100 is string type, so its failing if we substract with numeric values before converting to int.

* We can get any single character from the string by using index values.
* String index starts with zero.

![image](https://github.com/saipawan94/Python/assets/82724257/d7039f75-38c8-4392-a279-ca8d66c9082a)

```
fruit = 'banana'

letter = fruit[1]
print(letter)

a
```

len():
-
print(len(fruit))
6

Looping through Strings:
-

```
#fruit = 'banana'
index = 0

while index < len(fruit):
    letter = fruit[index]
    print(index, letter)
    index = index + 1

0 b
1 a
2 n
3 a
4 n
5 a
```
```
fruit = 'banana'
index = 0
for letter in fruit:
    print(index, letter)
    index = index + 1

0 b
1 a
2 n
3 a
4 n
5 a
```
Count letters in a string:
-
```
fruit = 'banana'
count = 0

for letter in fruit:
    if letter == 'a':
        count = count + 1
print(count)

3

fruit = 'banana'
index = 0
count = 0

while index < len(fruit):
    letter = fruit[index]
    index = index + 1
    if letter == 'a':
        count = count + 1
print(count)
```

**in will iterate each letter its pointing to**

String Slicing:
--

We can slice a string using **colon operator**

```
s = 'Venkata Sai Pavan'

print(s[0:7])

# If we are beyond the index limit example 100, it wont through any error.
print(s[0:100])

# If we remove start or end of the slice it assume the beginning or end of string.

print(s[:2])

print(s[8:])
print(s[:])
```

[0:7] --> 0 is tee starting and 6 will be the ending.


String concatenation:
-
```
a = 'Hello'

b = a + 'There'

print(b)

c = a + ' ' + 'There'

print(c)
```
By using + we can concatenate the string.

**in** is alogical operator which results in True Or False.

```
fruit = 'banana'

print('n' in fruit)

if 'a' in fruit:
    print('Found It')

True
Found It
```

