# python_code_tips

## From 11 python_code_tips
> https://www.youtube.com/watch?v=8OKTAedgFYg

1. Iterate with enumerate instead or range(len(x))

2. Use list comprehension instead of raw for loops
```python

connections = [conn for conn in some_list]
```

3. Sort complex iterables with sorted()

4. Store unique values with Sets
5. Save memory with Generators
```python

connections = (conn for conn in some_list)
```

6. Use collections.Counter to count things in objects
7. Merge two dicts together using {**d1, **d2}
8. Define default values in Dictionaries with .get() and .setdefault()
9. Count hashable objects with collections.Counter
https://docs.python.org/3/library/collections.html#collections.Counter

```python
from collections import Counter

for word in ['red', 'blue', 'red', 'green', 'blue', 'blue']:
   cnt[word] += 1
   
print(cnt)
Counter({'blue': 3, 'red': 2, 'green': 1})
```
8. Format strings with f-Strings (Python 3.6+)
9. Concatenate strings with .join()
```python

strings_to_join = ["Join", "this", "string"]
message = " ".join(strings_to_join)
print(message)

Join this string
```

10. Merge dictionaries with {**d1, **d2} (Python 3.5+)

https://towardsdatascience.com/merge-dictionaries-in-python-d4e9ce137374

```python

```

11. Simplify if-statements with if x in list

## Random items

Use vars() to enuermtae objects with properties into dictionaries

```python
class Example:

   def __init__():
      self._name = None
      
   @property
   def name(self)
		try :
			return self._name
		except Exception as e:
			raise e

example = Example()
print(vars(example))

{"_name" : None }

```

## From 10 Python Tips and Tricks for Writing Better Code
> https://www.youtube.com/watch?v=C-gEQdGVXbk

1.) Ternary Conditionals
Instead of the following
```python
condtion = True
if condition:
   x = 1
else:
   x = 0
```
You can write this one oneline with Ternary Conditionals
```python
condition = True
x = if condition else 0
```

2.) Unerscore Placholers with large numbers
```python
num1 = 10_000_000_000
```
Seperators in output
```python
num1 = 10_000_000_000
num2 = 100_000_000
total = num1 + num2
print(f'{total:,}')

10,100,000,000
```
3.) Context Managers
Bad smell, the code works but you want to use context managers for auto closing
```python
f = open('test.txt', 'r')

file_contents = f.read()

f.close()

words = file_contents.split(' ')
word_count = len(words)
print(word_count)

```
Context manager
```python
with open('test.txt', 'r') as f:
   file_contents = f.read()
   
words = filel_contents.split(' ')
word_count = len(words)
print(word_count)
```
**not just for files, can be with databases or anything with managing resources and requiring some type of setup and shutdown.
