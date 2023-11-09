### Medium questions (1,2,6,9,18,21,14,19)

### 1. Create a function that takes two numbers as arguments (num, length) and returns a list of multiples of num until the list length reaches length.

* example: 
list_of_multiples(12, 10) ➞ [12, 24, 36, 48, 60, 72, 84, 96, 108, 120]

### for loop


```python
num,length=int(input('enter number:  ')),int(input('enter multiplier:  '))
z=[]
for i in range(1, length+1):
    z.append(num*i)
print(z)
   

```

    enter number:  10
    enter multiplier:  5
    [10, 20, 30, 40, 50]
    

### while loop


```python
x,y=int(input('enter number:    ')),(input('enter multiplier:    '))
a=[]
i=1
while len(a)<10:
    a.append(x*i)
    i+=1
print(a)   
```

    enter number:    10
    enter multiplier:    10
    [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]
    

### 2.Write a function that accepts the height and width (m, n) and an optional proc s and generates a list with m elements. Each element is a string consisting of either:

The default character (hash #) repeating n times (if no proc is given).
The character passed in through the proc repeating n times.

* example:make_rug(3, 5, '#') ➞ [ "#####", "#####", "#####"]

### for loop 


```python
x,y,z=int(input('enter number')),int(input('enter number')),input('enter any special symbol')
a=[]
for i in range(x):
    a.append(z*y)     
print(a)
    


```

    enter number8
    enter number5
    enter any special symbol*
    ['*****', '*****', '*****', '*****', '*****', '*****', '*****', '*****']
    

### while loop 


```python
x,y,z=int(input('enter number:  ')),int(input('enter number:  ')),input('enter any special symbol:  ')
a=[]
while len(a)<x:
    a.append(z*y)
print(a)
```

    enter number:  10
    enter number:  5
    enter any special symbol:  @
    ['@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@', '@@@@@']
    

### 6. A number is said to be Harshad if it's exactly divisible by the sum of its digits. Create a function that determines whether a number is a Harshad or not.

* example : is_harshad(171) ➞ True
* 1 + 7 + 1 = 9
* 9 exactly divides 171



### for loop


```python
x=int(input('give any 3 digit number:  '))
d=0

for i in range(x):
    if x%sum([int(i) for i in str(x)])!=0:
        print('it is not divisible by'+ (x))
else:
    print('it is divisible by',(x))
```

    give any 3 digit number:  171
    it is divisible by 171
    

### while loop


```python
x=int(input('give digit number:  '))
d=0

while x%sum([int(i) for i in str(x)])!=0:
     print('it is not divisible by'+ (x))
else:
    print('it is divisible by',(x))
```

    give any 3 digit number:  171
    it is divisible by 171
    

### 9.Create a function that takes an integer and outputs an n x n square solely consisting of the integer n.

* example: square_patch(3) ➞ [[3, 3, 3],[3, 3, 3],[3, 3, 3]]

### For loop 


```python

x=int(input('enter number:  '))
y=[]
for i in range(x):
        y.append([x]*x)
    
print(y)

```

    enter number:  3
    [[3, 3, 3], [3, 3, 3], [3, 3, 3]]
    

### while loop


```python
x=int(input('enter number:  '))
y=[]
while x>len(y):
    y.append([x]*x)
print(y)
```

    enter number:  3
    [[3, 3, 3], [3, 3, 3], [3, 3, 3]]
    

### 21. Create a function that takes a list of numbers and return "Boom!" if the digit 7 appears in the list. Otherwise, return "there is no 7 in the list".

* example: seven_boom([1, 2, 3, 4, 5, 6, 7]) ➞ "Boom!"
 7 contains the number seven.


### For loop


```python
x=input('enter a number:   ')
for i in (x): 
    if "7" in x:
        print("Boom !")
    else:
        print("there is no 7 element in the list")
print(x)

```

    enter a number:   127
    Boom !
    Boom !
    Boom !
    127
    

### while loop

### 





### easy questions:


### 1.Create a function that takes an array of values resistance that are connected in series, and calculates the total resistance of the circuit in ohms. The ohm is the standard unit of electrical resistance in the International System of Units ( SI ).

* ex:series_resistance([1, 5, 6, 3]) ➞ "15 ohms"


```python
x=input('enter numbers')
for i in x:
     x+=i
if x>=1:
    (y)+'ohms'
else:
    (y)+'ohm'
print(i)
    
```

    enter numbers123
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[160], line 4
          2 for i in x:
          3      x+=i
    ----> 4 if x>=1:
          5     (y)+'ohms'
          6 else:
    

    TypeError: '>=' not supported between instances of 'str' and 'int'



```python

```
