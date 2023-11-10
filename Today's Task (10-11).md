## Reduce :

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
reduce(lambda x,y:x+y,[1,2,3,4])
```




    10




```python
reduce(lambda x,y:x*y,[2,3],'hi')  
```




    'hihihihihihi'




```python
def triangle(x,y):
    for i in range(1,x+1):
        for j in range(i): 
            print(y,end=' ')
        print()
triangle(5,'*')
```

    * 
    * * 
    * * * 
    * * * * 
    * * * * * 
    


```python
def triangle(x,y):
    for i in range(x,0,-1):
        for j in range(1,i+1): 
            print(y,end=' ')
        print()
triangle(5,'*')
```

    * * * * * 
    * * * * 
    * * * 
    * * 
    * 
    

#### program for square


```python
def triangle(x,y):
    for i in range(x,0,-1):
        for j in range(x): 
            print(' ',y,end=' ')
        print()
triangle(5,'*')
```

      *   *   *   *   * 
      *   *   *   *   * 
      *   *   *   *   * 
      *   *   *   *   * 
      *   *   *   *   * 
    

#### program for pyramid


```python
def triangle(x):
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print('*',end=' ')
        for j in range (i+1):
            print('*',end=' ') 
        print()
triangle(5)        
    
```

              * 
            * * * 
          * * * * * 
        * * * * * * * 
      * * * * * * * * * 
    

#### program for reverse pyramid


```python
def ReversePyramid(x):
    for i in range(x-1,-1,-1):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range(i):
            print('*',end=' ')
        for j in range(i+1):
            print('*',end=' ')
        print()
ReversePyramid(5)
       
```

      * * * * * * * * * 
        * * * * * * * 
          * * * * * 
            * * * 
              * 
    

#### program for pyramid with numbers



```python
def triangle(x):
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range(i):
            print(int(1+j),end=' ')
        for j in range(i+1):
            print(int(1+j),end=' ')
        print()
triangle(5)
        
    
```

              1 
            1 1 2 
          1 2 1 2 3 
        1 2 3 1 2 3 4 
      1 2 3 4 1 2 3 4 5 
    

#### program for reverse pyramid with numbers


```python
def ReversePyramid(x):
    for i in range(x-1,-1,-1):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range(i):
            print(int(1+j),end=' ')
        for j in range(i+1):
            print(int(1+j),end=' ')
        print()
ReversePyramid(5)
```

      1 2 3 4 1 2 3 4 5 
        1 2 3 1 2 3 4 
          1 2 1 2 3 
            1 1 2 
              1 
    

#### program for reverse pyramid with alphabets



```python
def ReversePyramid(x):
    for i in range(x-0):
        for j in range(i):
            print(' ',end=' ')
        for k in range(2*(x-i)-1):
            print(chr(65+k),end=' ')
        print()
ReversePyramid(5)
```

    A B C D E F G H I 
      A B C D E F G 
        A B C D E 
          A B C 
            A 
    

#### program for pyramid with alphabets



```python
def triangle(x):
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range(i):
            print(chr(65+j),end=' ')
        for j in range(i+1):
            print(chr(65+j),end=' ')
        print()
triangle(5)
```

              A 
            A A B 
          A B A B C 
        A B C A B C D 
      A B C D A B C D E 
    

#### program for parallelogram with alphabets



```python
def triangle(x):
    for i in range(x):
        for j in range(x-i-1):
            print(' ',end=' ')
        for k in range(2*i+1):
            print(chr(65+k),end=' ')
        for k in range(2*(x-i)-1):
            print(chr(65+k),end=' ')
        print()
triangle(5)
        
```

            A A B C D E F G H I 
          A B C A B C D E F G 
        A B C D E A B C D E 
      A B C D E F G A B C 
    A B C D E F G H I A 
    

#### program for rohmbus with alphabets



```python
def triangle(x):
    for i in range(x):
        for j in range(x-i-1):
            print(' ',end=' ')
        for j in range(2*i+1):
            print(chr(65+j),end=' ')
        print()
    for i in range(x-1):
        for j in range (i+1):
            print(' ',end=' ')
        for j in range(2*(x-i-1)-1):
            print(chr(65+j),end=' ')
        print()
triangle(5)    
```

            A 
          A B C 
        A B C D E 
      A B C D E F G 
    A B C D E F G H I 
      A B C D E F G 
        A B C D E 
          A B C 
            A 
    

#### program for rohmbus with character ' * ' 


```python
def rows(x):
    for i in range(1, x + 1):
        print(' ' * (x - i) + '* ' * i)

    for i in range(x-1, 0, -1):
        print(' ' * (x - i) + '* ' * i)
rows(10)
```

             * 
            * * 
           * * * 
          * * * * 
         * * * * * 
        * * * * * * 
       * * * * * * * 
      * * * * * * * * 
     * * * * * * * * * 
    * * * * * * * * * * 
     * * * * * * * * * 
      * * * * * * * * 
       * * * * * * * 
        * * * * * * 
         * * * * * 
          * * * * 
           * * * 
            * * 
             * 
    

#### sanglass with character ' * '


```python
def SanGlass(x):
    for i in range(x-1,-1,-1):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print('*',end=' ')
        for j in range (i+1):
            print('*',end=' ')
        print()
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print('*',end=' ')
        for j in range (i+1):
            print('*',end=' ')
        print()
SanGlass(10)
        

```

      * * * * * * * * * * * * * * * * * * * 
        * * * * * * * * * * * * * * * * * 
          * * * * * * * * * * * * * * * 
            * * * * * * * * * * * * * 
              * * * * * * * * * * * 
                * * * * * * * * * 
                  * * * * * * * 
                    * * * * * 
                      * * * 
                        * 
                        * 
                      * * * 
                    * * * * * 
                  * * * * * * * 
                * * * * * * * * * 
              * * * * * * * * * * * 
            * * * * * * * * * * * * * 
          * * * * * * * * * * * * * * * 
        * * * * * * * * * * * * * * * * * 
      * * * * * * * * * * * * * * * * * * * 
    

#### program for san glass with numbers 


```python
def SanGlass(x):
    for i in range(x-1,-1,-1):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print(int(i+1)+1,end=' ')
        for j in range (i+1):
            print(int(i+1)+1,end=' ')
        print()
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print(int(i+1)+1,end=' ')
        for j in range (i+1):
            print(int(i+1)+1,end=' ')
        print()
SanGlass(8)
```

      9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        8 8 8 8 8 8 8 8 8 8 8 8 8 
          7 7 7 7 7 7 7 7 7 7 7 
            6 6 6 6 6 6 6 6 6 
              5 5 5 5 5 5 5 
                4 4 4 4 4 
                  3 3 3 
                    2 
                    2 
                  3 3 3 
                4 4 4 4 4 
              5 5 5 5 5 5 5 
            6 6 6 6 6 6 6 6 6 
          7 7 7 7 7 7 7 7 7 7 7 
        8 8 8 8 8 8 8 8 8 8 8 8 8 
      9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
    

#### program for sanglass with alphabets


```python
def SanGlass(x):
    for i in range(x-1,-1,-1):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print(chr(65+j),end=' ')
        for j in range (i+1):
            print(chr(65+j),end=' ')
        print()
    for i in range(x):
        for j in range(i,x):
            print(' ',end=' ')
        for j in range (i):
            print(chr(65+j),end=' ')
        for j in range (i+1):
            print(chr(65+j),end=' ')
        print()
SanGlass(5)
```

      A B C D A B C D E 
        A B C A B C D 
          A B A B C 
            A A B 
              A 
              A 
            A A B 
          A B A B C 
        A B C A B C D 
      A B C D A B C D E 
    


```python

```


```python

```
