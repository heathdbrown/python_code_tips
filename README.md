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
