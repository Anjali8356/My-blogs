---
title: "Working with JSON Files Using Python"
seoTitle: "Working with JSON Files Using Python"
seoDescription: "Working with JSON Files Using Python"
datePublished: Wed May 10 2023 18:59:18 GMT+0000 (Coordinated Universal Time)
cuid: clhi2e731000c09mc0vvfhy10
slug: working-with-json-files-using-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683743080254/3a044c08-336b-4377-aaa1-8e1dcce169ee.jpeg
tags: python, json

---

### What is JSON?

JSON stands for Java-Script Object Notation. it is simply a data representation format just like XML and YAML. it is widely used across the internet for almost every API you access, configurations, games, text editors etc. it is lightweight because of its small file size and easy to read/write as there is not any opening and closing tag like XML. There are some data types which can be used in json.

1. String- "Hello world"
    
2. Numbers = 0, -3. 1000
    
3. Arrays = \[0,1,2\]
    
4. Objects = { "name": "Rick", "profession": "scientist"} or
    
5. null
    

### Why should you learn this?

The ability to process JSON files becomes important for programmers, especially in fields where data is constantly being input and output. In the context of data loading and storing, JSON is the most commonly used format.

Today, We are learning this using Python.

### Working with JSON using Python:

At first, working with `json` data, we will import the build-in module of Python called `json`. `import` is the keyword, used to import any package in Python.

```python
import json
```

Here, a variable named `people_str` contains a list of dictionaries named `people.`

```python
people_str = '''
  "people"=    [ 
  {    
    "name": "John Doe",    
    "age": 25,   
    "city": "New York",  
    "salary": 50000 
  },  

  {    
  "name": "Jane Smith", 
  "age": 30,   
  "city": "Los Angeles",    "salary": 60000 
  }, 

  {   
  "name": "Mark Johnson",   
  "age": 35,   
  "city":"Chicago",   
  "salary": 55000 
  }, 

  {    
  "name": "Sarah Wilson",
  "age": 28,    
  "city": "San Francisco",    
  "salary": 65000  
  }, 

  {    
  "name": "Michael Brown",    
  "age": 32,    
  "city": "Boston",    
  "salary": 70000  
  }
  ]

'''
```

*Hint: You can use any data generator or AI tool such as CHAT-GPT to generate the sample data, in this case, JSON data.*

JSON file must be created with an extension as `.json`.

Now, the First thing we could do is save this data into the JSON file. to do that, we first need to convert this dictionary into JSON objects. `json` module provides a method called `dumps()`, to convert Python dictionaries into json objects.

Let's learn more about it.

### dumps():

We have a built-in function in the `json` module called `dumps()`. What it does is, converts the dictionary into JSON objects.

```python

##dumps takes an actual data object and turn it into string
json_str = json.dumps(people_str,indent=2)
with open('data.json', 'w') as file:
    file.write(json_str)
```

Here, We defined a variable named `json_str` which contains the dictionary format data as a string.

the `dumps()` function takes the first argument `people_str` and the second is the `indent` keyword. `indent` provides some indentation as per the value to make the json data more readable. if we do not do this, it will show the data in a single line in json file.

```python
with open('data.json', 'w') as file:
    file.write(json_str)
```

Here, We are opening a file named `data.json` in writing mode and then writing the data into it. above code will create a file named `'data.json'`, if it doesn't exist already and write the above data into this. (if it exists, it will override that file)

### loads():

loads() is the function provided by `json` module in Python that is used to convert json objects into the dictionary(python's equivalent object).

```python
import json
with open('data.json','r') as file:
    json_obj = json.loads(file.read())
```

The second line in the above code is opening the existing file named `data.json`(in which we have saved the data) in reading mode and loading file data into `json_obj`

```python
print(json_obj)
```

This line will print all the data in `data.json`, as the dictionary.

Output:

```python
"people"=    [ 
  {    
    "name": "John Doe",    
    "age": 25,   
    "city": "New York",  
    "salary": 50000 
  },  

  {    
  "name": "Jane Smith", 
  "age": 30,   
  "city": "Los Angeles",    "salary": 60000 
  }, 

  {   
  "name": "Mark Johnson",   
  "age": 35,   
  "city":"Chicago",   
  "salary": 55000 
  }, 

  {    
  "name": "Sarah Wilson",
  "age": 28,    
  "city": "San Francisco",    
  "salary": 65000  
  }, 

  {    
  "name": "Michael Brown",    
  "age": 32,    
  "city": "Boston",    
  "salary": 70000  
  }
  ]
```

We can try printing other things as well.

```python
print(json_obj['people'])
print(json_obj['people'][0]['name'])
```

This is going to print the list and first name respectively.

Now, Let's take an object-oriented example to understand this more.

```python
import json
class person:
    def __init__(self,name, age, city, salary):
        self.name = name
        self.age = age
        self.city = city
        self.salary = salary
   
```

After importing the `json` module, We created a class named `person` which has a constructor. in short, A constructor is used to initialize data members. This constructor is having data members as `name`, `age`, `city` and `salary`.

```python
def display(self):
        print(self.name, self.age, self.city, self.salary)
```

This is the `display()` function which will display the values of the `name`, `age`, `city` and `salary`.

### Exporting data into json file:

Now let's export this data into a json file.

```python
def export_to_json(self, filename):
     person_dict = {'name':self.name, 'age':self.age,'city':self.city,'salary':self.salary}
     
```

Here, we created a function named `export_to_json()` and passed the `filename` as an argument. our next move is to define a variable named `person_dict` which contains nothing but the data which we are exporting.

```python
with open(filename, 'w') as f:
        f.write(json.dumps(person_dict, indent = 2))
```

If you are reading this blog, you must be aware of the next line, We are opening a file in writing mode, here. It will create a file named `filename` and Write the data into it, with an indentation of 2. Indentation is optional, but it is a good practice to keep the data more readable.

```python
def load_from_json(self,filename):
        with open(filename, 'r') as f:
            data = json.loads(f.read())
        self.name= data['name']
        self.age= data['age']
        self.city = data['city']
        self.salary = data['salary']
```

As we did before, here we are exporting json data into a Python dictionary.

```python
p1 = person("Rick", 70, "Seattle", 200)
p1.display()
p1.export_to_json("demo.json")
```

We created an object named `p1` of class `person` and called the functions. when we run the above code. it will create a file, named `demo.json` if it doesn't exist already . and write the data into it.

Output Window:

```python
Rick 70 Seattle 200
```

json file:

```json
## demo.json
{
  "name": "Rick",
  "age": 70,
  "city": "Seattle",
  "salary": 200
}
```

Thank you for taking the time to read this blog post. I sincerely hope that the information provided here proves to be helpful to you.