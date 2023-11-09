### Lists :

* Hetrogeneous sequencial data type,it is mutable
* "heterogeneous"=diff diff data types
* it can be indexable ,slicing (postive and negative)
* pos index="start=0,end=len of the string(n),step size=(+1)"
* neg index="start=-1,end=-(n+1),step size=(-1)"
* lists are dynamic in nature 


```python
x=[1,2,2,3+3j,'four',print,range]
```


```python
print(x,type(x),id(x),sep='\n')
print(x[0],x[-1])
print(x[::],x[::-1],sep='\n')
len(x)
```

    [1, 2, 2, (3+3j), 'four', <built-in function print>, <class 'range'>]
    <class 'list'>
    2167858285696
    1 <class 'range'>
    [1, 2, 2, (3+3j), 'four', <built-in function print>, <class 'range'>]
    [<class 'range'>, <built-in function print>, 'four', (3+3j), 2, 2, 1]
    




    7




```python
y='string'
y[0],y[::],y[::-1]
len(y)
```




    6



###  empty list :
* a list where we dont have any elements is called an empty list

### List -class
* elements with in a container
* It can be sequential or non-sequential


```python
l=list()
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    []
    <class 'list'>
    0
    0x1f8be2bedc0
    


```python
l=['string']
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    ['string']
    <class 'list'>
    1
    0x1f8bf329b40
    


```python
l=list('string')
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    ['s', 't', 'r', 'i', 'n', 'g']
    <class 'list'>
    6
    0x1f8bf309040
    

#### sets:
* it removes duplicates 
#### set (list) :
* it separates each word in a data type and gives only unique values


```python
l=list({100,1,45,9999})
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    [1, 100, 45, 9999]
    <class 'list'>
    4
    0x1f8be6c6280
    

###  nested list :



```python
x=[1,2,3,[4,5,6]]
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    [1, 100, 45, 9999]
    <class 'list'>
    4
    0x1f8be6c6280
    


```python
x[3]
x[3][::-1]
```




    [6, 5, 4]




```python
x[3][::-2]
```




    [6, 4]



### Range ( ):
* <b>syntax</b> range(start,end,step,) --> end means till
* type casting :changing


```python
r=range(1,11)
print(r,type(r),len(r),hex(id(r)),sep='\n')
```

    range(1, 11)
    <class 'range'>
    10
    0x1f8be7ec240
    


```python
list(r)
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]




```python
r=range(1,11,2)
print(r,type(r),len(r),hex(id(r)),sep='\n')
```

    range(1, 11, 2)
    <class 'range'>
    5
    0x1f8be7ee7f0
    


```python
list(r)
```




    [1, 3, 5, 7, 9]




```python
r=range(10,2,-1)
list(r)
```




    [10, 9, 8, 7, 6, 5, 4, 3]




```python
list(r)
```




    [10, 9, 8, 7, 6, 5, 4, 3]




```python
r=range(1,10,-1)
list(r)
```




    []




```python
l
```




    [1, 100, 45, 9999]




```python
dir(l)
```




    ['__add__',
     '__class__',
     '__class_getitem__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__getstate__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']



### append ( )
 * it adds only one value
 * it will be printed that one value at the very end of the list


```python
x=[]
x
print(x,type(x),len(x),hex(id(x)),sep='\n')
```

    []
    <class 'list'>
    0
    0x1f8bf32ae80
    


```python
x.append(100)
print(x,type(x),len(x),hex(id(x)),sep='\n')
```

    [100, [], [4, 5, 6], [4, 5, 6], 100, [4, 5, 6], 100]
    <class 'list'>
    7
    0x1f8bf32ae80
    


```python
x.append([4,5,6])
x
```




    [100, [], [4, 5, 6], [4, 5, 6], 100, [4, 5, 6], 100, [4, 5, 6]]




```python
help(list.append)
```

    Help on method_descriptor:
    
    append(self, object, /)
        Append object to the end of the list.
    
    

### extend ( ):

*  it will add multiple values ,that multiple values will be printed at the very end of the list


```python
x.extend([2,3,7])
print(x,type(x),len(x),hex(id(x)),sep='\n')
```

    [100, [], [4, 5, 6], [4, 5, 6], 100, [4, 5, 6], 100, [4, 5, 6], 2, 3, 7, 2, 3, 7, 2, 3, 7]
    <class 'list'>
    17
    0x1f8bf32ae80
    


```python
[1,2,3,1,4,1,9].count(1)
```




    3



### Insert ( ) :
* it will add the value at the index postion you gave 


```python
x.insert(-2,'aaaa')
x
```




    [100,
     [],
     [4, 5, 6],
     [4, 5, 6],
     100,
     [4, 5, 6],
     100,
     [4, 5, 6],
     2,
     3,
     7,
     2,
     3,
     7,
     2,
     'aaaa',
     'aaaa',
     'aaaa',
     3,
     7]



### pop and remove 

* these methods are used for removing the values

### remove ( )
*  works with an element,it removes the first occurence of the particular letter you give



```python
y=list('malayalam')
y
```




    ['m', 'a', 'l', 'a', 'y', 'a', 'l', 'a', 'm']




```python
y.remove('a')
y
```




    ['m', 'l', 'y', 'a', 'l', 'a', 'm']




```python
v=[0,1,2,3,4,5]
v.pop(4)
```




    4




```python
a=v.pop()
a,v
```




    (4, [0, 1, 2, 3])




```python

```
