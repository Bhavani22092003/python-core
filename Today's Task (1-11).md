## Today mandatory task :


#### 1. Write a Python program that asks the user for their age and prints "You are an adult" if the age is 18 or older, otherwise prints "You are a minor'.


```python
x=int(input('enter age'))

if x <=0 or x<100:
    print('enter correct age') ##-->print statement execute only when the above if statement is satisfied
elif x>=18:
    print('you are an adult') ##-->print statement executes only when the given input is greater than or equal to 
else:
    print('you are minor') ##-->when  the above 2 statements are not satisfied then it will print else statement
```

    enter age18
    you are an adult
    

* x=int(input('enter age'))
here x is accessing input that input should only accepting integer only.


* if x <=0:
here x is must be greater than 0 ,because here we comaparing age of a person. 
if the given integer is less than 0 ,then it will print else statement i.e ;enter correct age.

* elif x>=18:
here x is must be greater than 18 or equal to 18,if the condition is true then it will print elif statement.otherwise prints else statement.




#### 2. Write a program that takes a numerical grade (out of 100) as input and prints the corresponding letter grade according to the following scale:
 90-100: A
 80-89: B
 70-79: C
 60-69: D
 Below 60: F



```python
x=int(input('enter number'))

if x >100:
    print('please enter valid')
elif x>=90:
    print('A')
elif x>=80:
    print('B') ##-->the print statement will be printed only when the given condition was true ,here x should be greater than or equal to 80,otherwise it goes for next elif statenent,if there is no elif statements it will directly prints else statement
elif x>=70:
    print('C')
elif x>=60:
    print('D')
else:
    print(f)

```

    enter number111
    please enter valid
    

* x=int(input('enter age'))
here x is accessing input that input should only accepting integer only.

* if x >100:
the given output should not be more than 100 because,here we declare grades by using marks.
if the given number is more than 100 it executes print statement.

* elif x>=90:
here 'A'-Grade was declare to which students has score 90-100, for knowing the given number is in between 90-100,we should use x>=90 (x should be greater than or equal to 90 )Then only it executes print statements.

* like above statements it will check all the elif statements.
* if any of if and elif statement will true then executes its particular print statement otherwise it prints else statement. 



#### 3. Write a program that calculates the Body Mass Index (BMI) of a person. The user should input their weight in kilograms and height in meters. The program should then print whether the person is underweight, normal weight, overweight, or obese


```python
x=float(input('your weight in kg'))
y=float(input('your height in cm'))
z=x/ y*y    ##-->bmi formula
format=print(f'the BMI of a person whose x and y are {x}and{y}respectively is{z}')
if z<18.5:     ##-->it checks directly bmi value       
    print('underweight')
elif z>=18.5 and z<24: 
    print('normal weight')
elif z==25 and z<=29.9:
    print('over weight')
else:
    print('obesity')


```

    your weight in kg200
    your height in cm5
    the BMI of a person whose x and y are 200and5.0respectively is200.0
    obesity
    

#### 4. Write a program that asks the user for three numbers and prints the maximum of the three.


```python
x=int(input('enter first number'))
y=int(input('enter second number'))
z=int(input('enter third number'))
if x>y and x>z:
    print('first number is highest',(x))  
elif y>x and y>z:
    print('Second NUmber is highest',(y))
else:
    print('Third number is Highest',(z))

```

    enter first number-2
    enter second number-3
    enter third number-5
    first number is highest -2
    

#### 5. Write a program that asks the user for a temperature (in Celsius) and prints "It's freezing" if the temperature is below 0, "It's cool" if it's between 0 and 10, "It's warm" if it's between 10 and 20, and "It's hot" if it's above 20


```python
c=float(input('enter temperature in celsius  '))
y=(c* 1.8) + 32
if y>0 or y<0:
    print('its freezing')
elif y in range(0,10):
    print('its cooling')
elif y in range(10,20):    ##-->it checks if and elif conditions (range) ,if the given number is not in range it will print else statement
    print('its Warm')
else:
    print('its hot')
          
```

    enter temperature in celsius  0
    its freezing
    

#### 6. Write a program that asks the user for a number (1-7) and prints the corresponding day of the week.



```python
D=int(input('enter Number '))
if D in range (0,8): ##--> the given number should be from (1,7)
    if D==1:         ##--> if the given number is equal to 1 then it will executes print statement
        print('SUNDAY')
    elif D==2:
        print('MONDAY') 
    elif D==3:
        print('TUESDAY')
    elif D==4:
        print('WEDNESDAY')
    elif D==5:
        print('THURSDAY')
    elif D==6:
        print('FRIDAY')
    elif D==7: ##-->if and elif statements will not correct then it executes else statement
        print('SATURDAY')
else:
    print('please enter 1-7 numbers')
```

    enter Number 8
    please enter 1-7 numbers
    

#### 7.Write a program that asks the user for a number and prints "In range" if the number is between 10 and 20 (inclusive), and "Out of range" otherwise.



```python
x=int(input('enter a number   '))

if x in range(9,21):  ##-->it checks the range ,if the the given number is in range then it will executes the print statement
    print('the given number is inclusive') ##-->if the given number is in between (10,20) ,it prints inclusive 
else:
    print('out of range')
```

    enter a number   10
    the given number is inclusive
    

#### 8. Write a program that asks the user for an integer and prints whether it's even or odd.


```python
x=int(input('enter the number   '))

if x%2==0:
    print('the given number is a   ' 'EVEN') ##-->if the given number was divisible by 2 ,then it is even number otherwise odd number
else:
    print('the given number is'   'ODD')
          
```

    enter the number   2
    the given number is a   EVEN
    


#### 9. Write a Python program to add 'ing' at the end of a given string (string length should be equal to or more than 3). If the given string already ends with 'ing' then add 'ly' instead.If the string length of the given string is less than 3, leave it unchanged



```python
y=input('enter a string  ')

if y.isalpha():
    if len(y)==2:  #3-->it checks len of elements in the given input ,whether len is equal to 2 or not if yes it will executes its print statement.
        print((y))
    elif y.endswith('ing'): ##--> when y is endswith --> that mean if y is ended with ing it executes print statement
        print((y).replace('ing','ly')) ##-->if input was ended with 'ing',it replaces 'ly' in the place of 'ing'
    else:
        print((y)+('ing'))
else:
    print('please enter string')

```

    enter a string  5
    please enter string
    



#### 12. Manoj Kumar has family and friends. Help him remind them who is who. Given a string with a name, return the relation of that person to Manoj Kumar.,
 * Person Relation,
 Shiva father ,Letha mother, Tarun brother,Kavitha sister ,,Strange Coder.



```python
v,w,x,y,z='','shiva','letha','tarun','kavitha'

a=str(input('enter name  ')) ##-->it accepts string input

if a==w:      ##--->it checks the values of a and w ,a-->value is our input and w--> value is in given string ,it checks both the values if both values are equal then it executes print statement
    print('he is your father')
elif  a==x:
    print( 'she is your mother')
elif  a==y:
    print('he is your brother')
elif  a==z:
    print('she is your sister')
elif  a.isalpha():
    print('coder') ##-->if we give input that not in given values ,then it checks whether it may be string or not ,if string it prints coder ,if not it goes for else statment
else:
    print('enter string') ###--->if above all if and elif statements are wrong,then it executes else print statement-

```

    enter name  ramu
    coder
    

#### 10. Create rock-paper-scissors by using the if condition.



```python
import random
b=list('rps')
random.shuffle(b) ##-->here computer will choose one randomly
b=b[0]
a=input('player-I: ').lower() ##-->it converted the given input into small letters 
if(a =='p' and b =='r') or (a =='s' and b =='p') or (a =='r' and b =='s'):
    print('a win')
elif a == b:
    print('tie')
else:
    print('b wins')
```

    player-I: r
    tie
    

#### 11. Create a dynamic calculator which asks for numbers and operator and return the answers,
Example
Input: Type first number: 10",
Type any of this (+, -, *, /, %, **): ,*
Assignment-2 ,
Type second number: 19,
Output:Answer is 190



```python
x=int(input('enter a first number'))
y= input(" operator choosen,'+','-','*','/','%','**' ") ##-->we have to choosen one  operator
x2=int(input('type second number'))
if y =='+':
    print('out put is:' ,  x+x2) ##--->it checks wheather our choosen operator is equal to + or not ,if yes it add the x (the first number),x2(the second number).If they are not equal it goes for next elif statements.
elif y=='-':
    print('out put is:',   x-x2) 
elif y=='*':
    print('out put is:',    x*x2)
elif y=='/':
    print('out put is:',    x/x2)
elif y=='%':
    print('out put is:',    x%x2)
elif y=='**':
    print('out put is:',    x**x2)
else:
    print('enter valid number')

    

    
```

    enter a first number2
     operator choosen,'+','-','*','/','%','**' -
    type second number2
    out put is: 0
    

#### 13. Write a python program that takes in a word and determines whether or not it is plural. A plural word is one that ends with “s”


```python
x=input('enter a word   ')
if x.endswith('s'): ##-->it executes print statment only when the given x(input) is endswith 's',if it does not ends with 's',it prints else statment
    print((x))
else:
    print((x)+'s')
```

    enter a word   welcome
    welcomes
    

#### 15. Take values of length and breadth of a rectangle from the user and check if it is square or not.


```python
w,x,y,z=float(input('enter 1st length')),float(input('enter 1st breadth')),float(input('enter 2nd length  ')),float(input('enter 2nd breadth   '))

if w==x==y==z:          ##---> when all sides are equal then it is called square
    print('it is a square') ##--->here all the given four inputs should be equal then only it executes print statement,otherwise prints else statement
else:
    print('it is not a square')
                                       
```

    enter 1st length20
    enter 1st breadth10
    enter 2nd length  20
    enter 2nd breadth   10
    it is not a square
    

#### 16.Accept any city from the user and display the momentum of the city 
Hyderabad       : “charminar”
“Delhi”         : “red fort
“Agra           : Taj mahal
If the city name is not given correctly, give him a warning message.



```python
x=['hyderabad','delhi','Agra']
y=input('enter city name    ')
if y.isalpha():
    if y==x[0]:
        print('Charminar') ##-->it checks 0th index of x ,if it is equal to given input then,it executes print statement.
    elif y==x[1]:
        print('red fort')
    elif y==x[2]:
        print('Agra')
    else:
        print('please given correct city') ##-->if the  input is not in the given list it gives a warning msg like"plese given correct city
else:
    print('please enter string')
```

    enter city name    hyderabad
    Charminar
    

#### 17. Write a program to check whether a person is eligible for voting or not  (voting age>=18).


```python
x=int(input('enter age'))
if x>100 or x<=0:               ##-->given number should be greater than o and less than 100
    print('enter valid age')  
elif x>=18:                 ##-->the person age should be equal or greater than 18,then only person was eligible for vote ,otherwise it executes else statement 
    print('you are eligible to vote') 
else:                    
    print('you are not eligible for vote')
```

    enter age18
    you are eligible to vote
    

#### 18. Accept three sides of the triangle and check whether the triangle is possible or not.(Triangle is possible only when the sum of any two sides is greater than 3 rd side).




```python
x,y,z=int(input('enter first side of triangle')),int(input('enter second side of triangle')),int(input('enter third side of triangle'))
if x + y>z or y+z>x or z+x>y:        ##--->Triangle : sum of 2 sides are greater then other side
    print('it form a triangle')      ##--->it checks input wheather sum of any 2 numbers greater than another number then it prints :it form a triangle
else:                                ##-->if not it prints else statement. 
    print('it is not possible to triangle') 




```

    enter first side of triangle4
    enter second side of triangle5
    enter third side of triangle2
    it form a triangle
    

#### 14.   A company decided to give a bonus of 5% to employees if his/her year of service is more than 5 years.Ask user for their salary and year of service and print the net bonus amount.


```python
salary =int(input('enter salary'))
service=int(input('enter the year of service')) ##-->5% of bonus--->1/100*5*salary.
if service>=5:  ##-->here first it checks service is equal to or greater than 5.
    print('your net bonus amount is:',salary+(5/100*salary)) ##-->if yes it adds salary to the 5% bonus.
else:
    print('your net bonus salary is:', (salary)) ##-->if not it prints same current salary
```

    enter salary20000
    enter the year of service4
    your net bonus salary is: 20000
    


```python

```


```python

```
