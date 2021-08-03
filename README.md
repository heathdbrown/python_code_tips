# python_code_tips

# python_code_tips

1. Use .join for concatenating strings
```python

strings_to_join = ["Join", "this", "string"]
message = " ".join(strings_to_join)
print(message)

Join this string
```

2. List comprehension
```python

connections = [conn for conn in some_list]
```

3. Generator comprehensions
```python

connections = (conn for conn in some_list)
```
