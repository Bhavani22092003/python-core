### Medium questions (1,2,6,9,4,14)

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
    

### 3. A number is said to be Harshad if it's exactly divisible by the sum of its digits. Create a function that determines whether a number is a Harshad or not.

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
    

### 4.Create a function that takes an integer and outputs an n x n square solely consisting of the integer n.

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
    

### 5. Create a function that takes a list of numbers and return "Boom!" if the digit 7 appears in the list. Otherwise, return "there is no 7 in the list".

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


```

    enter a number:   127
    Boom !
    Boom !
    Boom !
    

### while loop


```python
numbers = [21, 22, 15, 47]
i = 0
x = False
while i < len(numbers):
    if '7' in str(numbers[i]):
        x = True
        break
    i += 1
if x:
    print("Boom!")
else:
    print("There is no 7 in the list")
```

    Boom!
    

### 6.In each input list, every number repeats at least once, except for two. Write a function that returns the two unique numbers.
* example:[2,4,5,2,4,2,4,5,6,4,1,2]-->[6,1]

### for loop 


```python
lists = [2,4,5,2,4,2,4,5,6,4,1,2]
inputlen= len(lists)
unique = []
for i in range(inputlen):
    if lists.count(lists[i]) == 1:
        unique.append(lists[i])
        if len(unique) == 2:
            break
print("The two unique numbers are:", unique)
```

    The two unique numbers are: [6, 1]
    

### while loop ()


```python
lists = [2,4,5,2,4,2,4,5,6,4,1,2]
unique = []
while len(lists) > 0:
    i = lists.pop(0)
    if i in unique:
        unique.remove(i)
    else:
        unique.append(i)
if len(unique) == 2:
    print("The two unique numbers are:", unique)

```

    The two unique numbers are: [6, 1]
    

### 7.Create a function that returns the amount of duplicate characters in a string. It will be case sensitive and spaces are included. If there are no duplicates, return 0.

* example: duplicates("Hello World!") ➞ 3

### for loop


```python
input_string=input('enter a word: ' )
char_count = {}
duplicate_count = 0
for char in input_string:
    if char in char_count:
        char_count[char] += 1 
    else:
        char_count[char] = 1

    for char, count in char_count.items():
        if count > 1:
            duplicate_count += 1

print(duplicate_count)
```

    enter a word: hello
    2
    

### while loop


```python
input_string=input('enter a word: ' )
char_count = {}
duplicate_count = 0

index = 0
while index < len(input_string):
        char = input_string[index]

if char in char_count:
    char_count[char] += 1
else:
    char_count[char] = 1
    index += 1

for count in char_count.values():
    if count > 1:
        duplicate_count += 1

print (duplicate_count)
```

    enter a word: hello
    


    ---------------------------------------------------------------------------

    KeyboardInterrupt                         Traceback (most recent call last)

    Cell In[1], line 6
          3 duplicate_count = 0
          5 index = 0
    ----> 6 while index < len(input_string):
          7         char = input_string[index]
          9 if char in char_count:
    

    KeyboardInterrupt: 


### easy questions: 


### 8.Create a function that takes an array of values resistance that are connected in series, and calculates the total resistance of the circuit in ohms. The ohm is the standard unit of electrical resistance in the International System of Units ( SI ).

* ex:series_resistance([1, 5, 6, 3]) ➞ "15 ohms"

### for loop


```python
resistance = [10, 20, 30]
Sum_of_resistance = 0
for r in resistance:
    Sum_of_resistance = Sum_of_resistance + r
print(f"{Sum_of_resistance}  ohms")    
```

    60  ohms
    

### while loop


```python
resistance = [1, 5, 6,3]
total_of_resistance = 0
x = 0
while x < len(resistance):
    total_of_resistance = total_of_resistance + resistance[x]
    x = x + 1
print(f"{total_of_resistance} ohms")
```

    15 ohms
    

### 9.Create a function which concatenates the number 7 to the end of every chord in a list. Ignore all chords which already end with 7.

* jazzify(["G", "F", "C"]) ➞ ["G7", "F7", "C7"]




```python
x=list(input('enter a number:   '))
for i in range(len(x)):
    if x[i][-1]!='7':
        print((x)[i],"7",end='\t' )
    elif x[i][-1]=='7':
        print((x),sep=" ")
    else:
        print((x))
    

```

    enter a number:   GFC
    G 7	F 7	C 7	

### while loop 


```python
x=(input('enter a number:   '))
y=0
z=" "
while y>len(x):
    y+=1
if x[y]!='7':
    print((x)[y],"7",end='\t' )
elif x[y][-1]=='7':
    print((x),sep=" ")
else:
    print((x))
   
```

    enter a number:   g
    g 7	

### 10.Create a function that takes a string and returns the number (count) of vowels contained within it.
* example : count_vowels("Celebration") ➞ 5


### For loop


```python
vowels = ['a','e','i','o','u']
string=str(input("enter a word:   ")).lower()
total=0

for i in string:
      if i in vowels: 
            total=total+1
print(total)
```

    enter a word:   AEIOU
    5
    

### while loop 


```python
vowels = ['a','e','i','o','u']
string=str(input("enter a word:   ")).lower()
total=0

while total<len(string):
    if i in vowels: 
            total=total+1
print(total)
```

    enter a word:   AEIOU
    5
    

### 11.Hamming distance is the number of characters that differ between two strings.

* example :hamming_distance("abcde", "bcdef") ➞ 5


### for loop


```python
x=(input('enter alphabets:  '))
y=(input('enter alphabets:  '))
count=0
for i in range(len(x)):
    if (x[i]!=y[i]):
        count+=1
print(count)
    
    
```

    enter alphabets:  abcde
    enter alphabets:  bdaec
    5
    

### while loop 


```python
x=(input('enter alphabets:   '))
y=(input('enter alphabets:    '))
count=0
distance=0
while count<len(x):
    if x[count]!=y[count]:
        distance+=1
    count+=1
print(distance)
        

```

    enter alphabets:   abcde
    enter alphabets:    debca
    5
    

### 12.Create a function that takes a list and finds the integer which appears an odd number of times.

* example :find_odd([1, 1, 2, -2, 5, 2, 4, 4, -1, -2, 5]) ➞ -1




### for loop


```python
x=(input('enter  numbers:  '))
for i in set(x):
    if x.count(i)%2==1:
        print((i),end='')
```

    enter  numbers:  1, 1, 2, -2, 5, 2, 4, 4, -1, -2, 5
    -1

### while loop


```python
x=(input('enter  numbers:  '))
while x:
    current_element=x[0]
    count=x.count(current_element)
if x.count%2!=0:
    print(current_element)
print(current_element)
```

### 13.Create a function that takes an array of non-negative integers and strings and return a new array without the strings.

* example:filter_list([1, 2, "a", "b"]) ➞ [1, 2]


### for loop 


```python
array = [1, 2, "a", "b"]
new_array = []
for x in array:
    if isinstance(x, int):
        new_array.append(x)
print(new_array)


```

    [1, 2]
    

### while loop


```python
array = [1, 2, "a", "b"]
new_array = []
i = 0
while i < len(array):
    if isinstance(array[i], int):
        new_array.append(array[i])
    i += 1
print(new_array)
```

    [1, 2]
    

### 14.Create a function that takes a list of non-negative integers and strings and return a new list without the strings.






### for loop 


```python
array = [1, 2, "andhra", "pradesh"]
new_array = []
for x in array:
    if isinstance(x, str):
        new_array.append(x)
print(new_array)
```

    ['andhra', 'pradesh']
    

### while loop 


```python
array = [1, 2, "andhra", "pradesh"]
new_array = []
i = 0
while i < len(array):
    if isinstance(array[i], str):
        new_array.append(array[i])
    i += 1
print(new_array)
```

    ['andhra', 'pradesh']
    

### 15.The solution should be one string with a comma in between every "Hello (Name)".



### for loop 


```python
names = ['bhavani', 'sushma', 'anu']
greetings = ""
for name in names:
    greetings += f"Hello! {name}, "
greetings = greetings[0:]
print(greetings)
```

    Hello! bhavani, Hello! sushma, Hello! anu, 
    


```python
names = ['Bhavani','Anu','Sushma']
greetings = ""
x = 0
while x < len(names):
    greetings += "Hello!" + names[x]
    if x < len(names) - 1:
        greetings += ", "
    x += 1
print(greetings)
```

    Hello!Bhavani, Hello!Anu, Hello!Sushma
    

### 16.Create a function that takes a list of strings and integers, and filters out the list so that it returns a list of integers only.

* example:filter_list([1, 2, 3, "a", "b", 4]) ➞ [1, 2, 3, 4]



```python
names = [1, 'bhavani', 2, 'sushma', 3, 'anii']
num = []
for i in names:
    if isinstance(i, int):
        num.append(i)
print(num)
```

    [1, 2, 3]
    


```python
names = [1, 'bhavani', 2, 'sushma', 3, 'anii']
num = []
x=0
while x < len(names):
    if isinstance(names[x], int):
        num.append(names[x])
    x = x + 1
print(num)
```

    [1, 2, 3]
    




 


```python


```


```python

```
