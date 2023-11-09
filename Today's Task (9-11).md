## Lambda Function :

 * A lambda function is a small anonymous function defined using the lambda keyword. It's also known as a lambda expression. Lambda functions are often used for short, simple operations that can be defined in a single line of code.
 * It returns value without return value
 

<b> Syntax </b> lambda arguments: expression


![image.png](attachment:image.png)

![image.png](attachment:image.png)

* Here, arguments are the input parameters, and expression is the operation performed by the function. The result of the expression is implicitly returned.



* For example, a lambda function that add two numbers:


```python
add =( lambda x, y: x + y)(3,2)
add
```




    5



### Printing even and odd numbers by using lambda Function



```python
(lambda x: 'even' if x%2==0 else 'odd')(3) 
```




    'odd'




```python
(lambda x,y:([ele for ele in range(x,y+1) if ele%2==0],[ele for ele in range(x,y+1) if ele%2!=0])) (20,30)
```




    ([20, 22, 24, 26, 28, 30], [21, 23, 25, 27, 29])



### exponential by using lambda


```python
c=(lambda x,y:x**y)(2,3)
c
```




    8



* The main difference is that lambda functions are more concise and are often used in situations where a short, throwaway function is needed. They are commonly used with functions like <b> map(), filter(),</b> and <b>reduce().</b>


* Keep in mind that lambda functions are limited in terms of complexity compared to regular functions, and they are generally best suited for simple operations.

### Map ( )

* The map function is a built-in function that applies a specified function to all the items in an iterable (e.g., a list) and returns an iterator that produces the results. When used in conjunction with a lambda function, it allows you to apply a quick, one-time operation to each element in the iterable.
* <b>Syntax</b> map(func,iterator)
*  map takes 2 inputs(values),1st is a function and 2nd one is iterator


![image.png](attachment:image.png)

* Here, a lambda function is defined to calculate the square of a given number x.


```python
z=map(lambda x:x**2,[1,5,10]) ## -->we store the function in map with some variable 
z  
```




    <map at 0x2a192cb3b20>




```python
list(z) ##-->when we type casting the map function it prints the values
```




    [1, 25, 100]



#### printing ascii values of given letters


```python
y=map(ord,'abc')
list(y)
```


```python
z=map(lambda x:x/0,[1,2,3])  ##---> its going to give an error while run time
z 
```




    <map at 0x2a192e48100>




```python
# list(z) #-->un comment to see an error 
```

#### adding numbers


```python
a=map(lambda x,y:x+y,[1,2,3],[10,20,30])
list(a)
```




    [11, 22, 33]



#### it prints exponential of given number(x^x)


```python
c=map(lambda x:x**x,[1,2,3])
list(c)
```




    [1, 4, 27]



### Filter ( )

* The filter function in Python is another built-in function that, similar to map, operates on an iterable (e.g., a list) and returns an iterator. It filters the elements of an iterable based on a function (usually a lambda function) that returns either True or False.
* If the given condition is true it prints the values,if it is false does not print values

![image.png](attachment:image.png)

#### printing only even numbers


```python
list(filter(lambda x:True if x%2==0 else False ,[1,2,3,4,5]))
```




    [2, 4]



#### it gives only vowels which are in the given "string"


```python
x=filter(lambda x  :True if x in 'aeiouAEIOU' else False,'AStrIno')
list(x)
```




    ['A', 'I', 'o']



#### it gives only numbers and alphabets, which are in the given string 


```python
y=filter(lambda x:True if x.isalnum() else False,'###123abc')
list(y)
```




    ['1', '2', '3', 'a', 'b', 'c']



####  it prints only special character 


```python
a=filter(lambda x:True if x.isalnum() is False else False,'$$$abc123' )
list(a)
```




    ['$', '$', '$']



### Reduce ( )

* The reduce function in Python is part of the functools module and is used to perform a cumulative operation on the items of an iterable, from left to right, and reduce the iterable to a single accumulated result. When used with a lambda function, it allows you to specify the operation to be applied.
* Note that reduce is not a built-in function in Python 3 anymore, so you need to import it from the functools module.




```python
import functools 
from functools import reduce
```


```python
add = lambda x, y: x + y

```


```python
numbers = [1, 2, 3, 4, 5]

```


```python
sum_result = reduce(add, numbers)
sum_result

```




    15




```python

```


```python

```
