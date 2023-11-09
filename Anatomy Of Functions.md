## Functions

* A function is a reusable block of code that performs a specific task or set of tasks. Functions are a fundamental concept in programming and are used to encapsulate and organize code for better modularity, readability, and reusability.

<b>Syntax</b> : def function_name(parameters):

* def: This keyword is used to define a function in Python.

* function_name: Choose a name for your function that follows Python's naming conventions. Function names should be descriptive and follow lowercase_with_underscores (snake_case) naming style.

* parameters: These are placeholders for values that you can pass into the function as input. Parameters are enclosed in parentheses and separated by commas.



![image.png](attachment:image.png)

#### A small program for calling a function


```python
def foosum(a,b): ##-->a,b are parameters
    print(a+b)
```


```python
# we can use this function multiple times by calling functiona name 
foosum(1,3) ##-->1,2 are arguments,
```

    4
    


```python
foosum(-3,-5)
```

    -8
    

### Arguments

* An argument is a value that is passed to a function when it is called. It might be a variable, value or object passed to a function or method as input. They are written when we are calling the function.



* In python,function supports 3 types of arguments :
1. Positional argument.
2. Keyword argument.
3. Default argument.

### Positional Arguments:
* positional arguments are a type of argument passed to a function or method in a specific order based on their position or order in the function’s parameter list.


* When you define a function, you specify its parameters in a particular order, and when you call the function, you provide arguments that correspond to those parameters in the same order. Python uses this positional information to match the arguments with the parameters.

![image.png](attachment:image.png)

#### Example of positional argument :


```python
def foodivision(n:float,d:float):#3-->n-is first parameter,d-is second parameter
    print(n/d)
```


```python
foodivision(n=10,d=2) ##-->here 10 is passed to n-parameter,and 2 value is passed to d parameter
```

    5.0
    

### Keyword Arguments :
* keyword arguments (also known as keyword parameters) are a way to pass arguments to a function by specifying the parameter names along with their values when calling the function.
* keyword arguments allow you to specify the parameter names explicitly. This can make your code more readable and flexible, as it’s not dependent on the order of the parameters.

![image.png](attachment:image.png)

#### Example of keyword arguments :

### Default Arguments :
* Default arguments are parameters of a function that have a predefined default value. When you define a function and specify default values .
* For certain parameters, it means that those parameters can be omitted when calling the function, and Python will use the default values instead.

![image.png](attachment:image.png)

#### Example For Default Argument :


```python
def foopotentialenergy(m,h,g=9.8):
    print(m*h*g)

```


```python
foopotentialenergy(10,5)
```

    490.00000000000006
    


```python
foopotentialenergy(10,5,g=10)
```

    500
    


```python
def fooconcatenationofstring(s1:str,s2:'',n=1): #-->here s1 accepting string
    print((s1+s2)*n) 
```


```python
fooconcatenationofstring('he',s2='hahaha',n=5)
```

    hehahahahehahahahehahahahehahahahehahaha
    

### Document String :

* A “docstring” (short for “documentation string”) is a special type of string literal that is used to document a module, class, function, or method.
* Docstrings are intended to provide information about the purpose, usage, and behavior of the code they document. They serve as documentation for the code and are used to help other developers (including your future self) understand how to use and work with your code.
* A docstring is typically placed as the first statement in a module, class, function, or method and is enclosed in triple quotes (either single or double quotes).



```python
def foodivision(n:float,d:float):#3-->n-is first parameter,d-is second parameter
    ''' d=denominator
         n=numerator
         '''
    print(n/d)
```


```python
print(foodivision.__doc__)
```

     d=denominator
             n=numerator
             
    
