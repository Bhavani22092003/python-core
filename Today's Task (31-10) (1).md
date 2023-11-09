## Today mandatory task :


* Write a Python program that asks the user for their age and prints "You are an adult" if the age is 18 or older, otherwise prints "You are a minor'.


```python
x=int(input('enter age'))

if x <=0:
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




* Write a program that takes a numerical grade (out of 100) as input and prints the corresponding letter grade according to the following scale:
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

    enter number90
    A
    

* x=int(input('enter age'))
here x is accessing input that input should only accepting integer only.

* if x >100:
the given output should not be more than 100 because,here we declare grades by using marks.
if the given number is more than 100 it executes print statement.

* elif x>=90:
here 'A'-Grade was declare to which students has score 90-100, for knowing the given number is in between 90-100,we should use x>=90 (x should be greater than or equal to 90 )Then only it executes print statements.

* like above statements it will check all the elif statements.
* if any of if and elif statement will true then executes its particular print statement otherwise it prints else statement. 



* Write a program that calculates the Body Mass Index (BMI) of a person. The user should input their weight in kilograms and height in meters. The program should then print whether the person is underweight, normal weight, overweight, or obese


```python
x=int(input('your weight in kg'))
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
    

* Write a program that asks the user for three numbers and prints the maximum of the three.


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

    enter first number4
    enter second number5
    enter third number9
    Third number is Highest 9
    

* Write a program that asks the user for a temperature (in Celsius) and prints "It's freezing" if the temperature is below 0, "It's cool" if it's between 0 and 10, "It's warm" if it's between 10 and 20, and "It's hot" if it's above 20


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
    

* Write a program that asks the user for a number (1-7) and prints the corresponding day of the week.



```python
D=int(input('enter Number '))
if D >=7 and D<=1: ##--> the given number should be from (1,7)
    print('enter valid number') 
elif D==1:         ##--> if the given number is equal to 1 then it will executes print statement
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
    print('FRIDAY')  ##-->if and elif statements will not correct then it executes else statement
else:
    print('SATURDAY')
```

    enter Number 1
    SUNDAY
    

* Write a program that asks the user for a number and prints "In range" if the number is between 10 and 20 (inclusive), and "Out of range" otherwise.



```python
x=int(input('enter a number   '))

if x in range(9,21):  ##-->it checks the range ,if the the given number is in range then it will executes the print statement
    print('the given number is inclusive') ##-->if the given number is in between (10,20) ,it prints inclusive 
else:
    print('out of range')
```

    enter a number   10
    the given number is inclusive
    

* Write a program that asks the user for an integer and prints whether it's even or odd.


```python
x=int(input('enter the number   '))

if x%2==0:
    print('the given number is a   ' 'EVEN') ##-->if the given number was divisible by 2 ,then it is even number otherwise odd number
else:
    print('the given number is'   'ODD')
          
```

    enter the number   2
    the given number is a   EVEN
    


* Write a Python program to add 'ing' at the end of a given string (string length should be equal to or more than 3). If the given string already ends with 'ing' then add 'ly' instead.If the string length of the given string is less than 3, leave it unchanged



```python
y=input('enter a string  ')

if len(y)==2:  #3-->it checks len of elements in the given input ,whether len is equal to 2 or not if yes it will executes its print statement.
    print((y))
elif y.endswith('ing'): ##--> when y is endswith --> that mean if y is ended with ing it executes print statement
    print((y).replace('ing','ly')) ##-->if input was ended with 'ing',it replaces 'ly' in the place of 'ing'
else:
    print((y)+('ing'))

```

    enter a string  string
    strly
    




```python

```
