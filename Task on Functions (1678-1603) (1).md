###  1678 Leetcode goal parser interpreter

You own a Goal Parser that can interpret a string command. The command consists of an alphabet of "G", "()" and/or "(al)" in some order. The Goal Parser will interpret "G" as the string "G", "()" as the string "o", and "(al)" as the string "al". The interpreted strings are then concatenated in the original order.

Given the string command, return the Goal Parser‘s interpretation of command.


```python
def fooGoalParser(s):
    ''' 
    This is a docstring for the fooGoalParser.
    
    The Goal Parser interprets the alphabet "G" as the string "G",
    "()" as the string "o", and "(al)" as the string "al". The interpreted
    strings are then concatenated in the original order.
    
    parameters :
    
    --->s : the input string ,to be interpreted.
    
    Return :
    
   ----> x: the interpreted as per the goal parser rules.
    
    '''
    x = s
    alCount, pCount = s.count('()'), s.count('(al)')
    for i in range(alCount):
        x = x.replace('(al)', 'al')
        
    for j in range(pCount):
        x = x.replace('()', 'o')
    return x    
        
    
```


```python
print(fooGoalParser.__doc__)
```

     
        This is a docstring for the fooGoalParser.
        
        The Goal Parser interprets the alphabet "G" as the string "G",
        "()" as the string "o", and "(al)" as the string "al". The interpreted
        strings are then concatenated in the original order.
        
        parameters :
        
        --->s : the input string ,to be interpreted.
        
        Return :
        
       ----> x: the interpreted as per the goal parser rules.
        
        
    


```python
fooGoalPraser("G()(al)")
```




    'Goal'




```python
fooGoalPraser("(al)G(al)()()G")
```




    'alGalooG'



### 1672 leetcode Richest Customer Wealth

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the ith customer has in the jth bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

* <b>Example</b>  Input: accounts = [[1,2,3],[3,2,1]]
Output: 6
Explanation:
1st customer has wealth = 1 + 2 + 3 = 6
2nd customer has wealth = 3 + 2 + 1 = 6
Both customers are considered the richest with a wealth of 6 each, so return 6.


```python
def RichestWealth(p,s):
    
    '''
    
    This is a docstring for the Richest Customer wealth.
     
     parameters:
     
   ----->  p,s: customers wealth.
       
       x --->x gives sum of p(adding all elements in "p")
       y --->y gives sum of s(adding all elements in "s")
    
     return :
     
   ------>  richest: it gives maximum of p and s 
   
   '''
    
    x=sum(p)
    y=sum(s)
    richest=max(x,y)
    for i in p:
        if x==y:
            print(f'both customers are considered as the richest with a wealth of {richest} each ,so return {richest}')
        elif x>y:
            print(f'1st customer has richest wealth: {richest}')
        else:
            print(f'2nd customer has richest wealth: {richest}')

```


```python
print(RichestWealth.__doc__)
```

    
        
        This is a docstring for the Richest Customer wealth.
         
         parameters:
         
       ----->  p,s: customers wealth.
           
           x --->x gives sum of p(adding all elements in "p")
           y --->y gives sum of s(adding all elements in "s")
        
         return :
         
       ------>  richest: it gives maximum of p and s 
       
       
    


```python
Richest([1,2,8],[1,2,6])
```

    1st customer has richest wealth: 11
    1st customer has richest wealth: 11
    1st customer has richest wealth: 11
    

### 1662 leet code check if two string arrays are equivalent 
* Given two string arrays word1 and word2, return true if the two arrays represent the same string, and false otherwise.A string is represented by an array if the array elements concatenated in order forms the string.

* <b>example</b>Input: word1 = ["ab", "c"], word2 = ["a", "bc"]
* Output: true
* Explanation:
word1 represents string "ab" + "c" -> "abc"
word2 represents string "a" + "bc" -> "abc"
The strings are the same, so return true.


```python
def equivalent(x:str,y:str):
    
    '''
    
      This is a docstring for the Richest Customer wealth.
      
    parameters:
    
    --->x: str  (accept string from user input)
        y:str   (accept string from user input)
    Return :
    
    ---->it checks condition, it prints the statements according to the condition.
    ---->word : it concatinates x and y.
    
    '''
    str1=''.join(x)
    str2=''.join(y)
    word=[str1]+[str2]
    if x==y:
        print('both strings are same')
    else:
        print('strings are different')
    return word
    
```


```python
equivalent(["ab","c"],["a","bc"])
```

    strings are different
    




    ['abc', 'abc']



### 1656 leet code  Design an ordered Stream 

* There are n (id, value) pairs, where id is an integer between 1 and n and value is a string. No two pairs have the same id.

* Design a stream that takes the n pairs in an arbitrary order, and returns the values over several calls in increasing order of their ids.

* Implement the OrderedStream class:

OrderedStream(int n) Constructs the stream to take n values and sets a current ptr to 1.
String[] insert(int id, String value) Stores the new (id, value) pair in the stream. After storing the pair:
If the stream has stored a pair with id = ptr, then find the longest contiguous incrementing sequence of ids starting with id = ptr and return a list of the values associated with those ids in order. Then, update ptr to the last id + 1.
Otherwise, return an empty list. 

### 1623 leet code All valid triplets that can represent a country

* 

### 1603 leet code Design parking system 

* 


```python

```
