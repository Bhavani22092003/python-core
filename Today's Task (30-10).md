## Conditional Statements 



```python
marks =55

if marks <=60:
    print('screening test')   
elif marks <=70:
    print('first round')
elif marks <=80:
    print('Second round')
else:
    print('study hard')
```

    screening test
    

### Dictionary

* dictionaries are very imp because of it have nested dictionary(dictionary with in a dictionary)
* dict class is a container of tuples 
* Tuples: it only accepting leng of 2 elements 
* only immutable data types are used for values 

* In Python, a dictionary is a built-in data structure used to store collections of data in a key-value pair format. Each element in a dictionary consists of a key and its corresponding value. Keys are unique within a dictionary, and they are used to access the associated values. Dictionaries are often used for fast and efficient data retrieval based on keys.


 * <b>Syntax :</b> my_dict = {}
 


```python
# Creating an empty dictionary
my_dict = {}

# Creating a dictionary with some key-value pairs
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 30,
    "city": "New York"
}

```


```python
person['age']
```




    30



### Dict class

* by using dict class we creating dictionary with some keys and values


```python
x=dict([(1,11),  ##--> creating dictinary by using list
       (2,22)])
x
```




    {1: 11, 2: 22}




```python
x=dict(((1,11),   ##--> dictinary by using tuple,it rises an error if we give more than two elements
       (2,22)))
x

```




    {1: 11, 2: 22}




```python
dir(x)
```




    ['__class__',
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
     '__init__',
     '__init_subclass__',
     '__ior__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__ne__',
     '__new__',
     '__or__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__ror__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'clear',
     'copy',
     'fromkeys',
     'get',
     'items',
     'keys',
     'pop',
     'popitem',
     'setdefault',
     'update',
     'values']




```python
x={'k1':1,
  'k2':2,
  'k3':3}
```

# get 
* In Python, the get() method is used to retrieve the value associated with a given key in a dictionary. This method allows you to access dictionary values in a way that provides a default value if the key does not exist in the dictionary. This is useful to prevent KeyError exceptions when attempting to access a non-existent key.

* They are 2 ways for accessing key values 
1. by calling ('key name') :if the given key was not found it throughs an error
2. get('key name ' ) : if the given key was not found in a dictionary it prints nothing


```python
x['k3']
```




    3




```python
x['k1']
```




    1




```python
## x['k'] ## uncomment to see an error
```


```python
x.get('k2')
```




    2




```python
x.get('k4')
```


```python
x['k4']=4  #3-->one of the  way to adding number to the dictionary
x
```




    {'k1': 1, 'k2': 2, 'k3': 3, 'k4': 4}




```python
x['k5']=5
x
```




    {'k1': 1, 'k2': 2, 'k3': 3, 'k4': 4, 'k5': 5}



### Update 

* In Python, the update() method is used to update the content of a dictionary by adding key-value pairs from another dictionary or an iterable (such as a list of tuples). This method allows you to merge the contents of one dictionary into another. If the key already exists in the original dictionary, the update() method will update the associated value with the new value from the other dictionary.


```python
x.update([('k5',5), #-->adding multiple keys and values ,with in a list or dictionary we can pass the keys and values
          ('k6',6)])
x
```




    {'k1': 1, 'k2': 2, 'k3': 3, 'k4': 4, 'k5': 5, 'k6': 6}



### Keys ( )
*  "keys" typically refer to the unique identifiers used in dictionaries to access their associated values. A dictionary is a built-in data structure that stores collections of data in a key-value pair format, and keys are used to access and retrieve the associated values. Keys must be unique within a dictionary, and they are typically immutable data types, such as strings, numbers, or tuples


```python
x.keys()
```




    dict_keys(['k1', 'k2', 'k3', 'k4', 'k5', 'k6'])



### Values ( )

* In Python, "values" in the context of dictionaries refer to the data associated with keys in a dictionary. Dictionaries are a built-in data structure that stores collections of data in a key-value pair format. The values represent the actual data that you want to store and retrieve, and they are accessed using their corresponding keys.

* syntax 


  dictinary.name.values()


```python
x.values()
```




    dict_values([1, 2, 3, 4, 5, 6])



### Items ( )

* In Python, "items" in the context of dictionaries refer to the key-value pairs within the dictionary. Each key-value pair is considered an "item" in the dictionary. Dictionaries are a built-in data structure that stores collections of data in a key-value pair format, and items represent the combination of keys and their associated values.



```python
x.items()
```




    dict_items([('k1', 1), ('k2', 2), ('k3', 3), ('k4', 4), ('k5', 5), ('k6', 6)])



### pop

* In Python, the pop() method is used to remove and return an item (key-value pair) from a dictionary based on a specified key. This method is commonly used to extract a value from a dictionary while also removing the corresponding key-value pair. If the specified key is not found in the dictionary, you can provide a default value to return, or a KeyError will be raised.

* syntax 

  dictionary.pop(key, default)
  
  where;
* dictionary: The dictionary from which you want to remove and    retrieve the item.
* key: The key of the item you want to remove and retrieve.
* default (optional): The value to return if the key is not found in the dictionary. If this parameter is not provided, a KeyError is raised.



```python
x.popitem() ##-->it poped out last key and values,it doesnt take any arguments
x
```




    {'k1': 1, 'k2': 2, 'k3': 3, 'k4': 4}



### From keys :

* In Python, the fromkeys() method is used to create a new dictionary with specified keys and an optional default value for those keys. This method is useful when you want to initialize a dictionary with a set of keys and assign a default value to each key.

* Syntax :

  dict.fromkeys(keys, value)

where;

* dict: The class name of the dictionary (e.g., dict).
* keys: A sequence (such as a list, tuple, or iterable) of keys that you want to initialize in the dictionary.
* value (optional): The default value to assign to each key. If this parameter is not provided, it defaults to None.




```python
# Create a dictionary using fromkeys() with a list of keys
keys = ["name", "age", "city"]
default_value = "i dont know"
my_dict = dict.fromkeys(keys, default_value)

print(my_dict)

```

    {'name': 'i dont know', 'age': 'i dont know', 'city': 'i dont know'}
    
