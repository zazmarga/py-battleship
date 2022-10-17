# Сheck Your Code Against the Following Points

### 1. One function - one purpose.

Remember the principle that one function is one purpose. So if it is 
needed - put some code into a separate method, feel free about it.

### 2. Don't use redundant statements.

Don't use a redundant `return` statement if it doesn't do anything.

Good example:
```python
def change_item(self) -> None:
    self.length += 2
```

Bad example:
```python
def change_item(self) -> None:
    self.length += 2
    return
```

Also, don't use an empty `return` if you have multiple conditions and an
`elif` statement can be used.

Good example:
```python
if a == b:
    # do something
elif a == c:
    # do something
elif a == d:
    # do something
```

Bad example:
```python
if a == b:
    # do something
    return
if a == c:
    # do something
    return
if a == d:
    # do something
    return
```

### 3. Don't use redundant `elif`.

Don't use redundant `else` if a non-empty `return` is used:

Good example:
```python
if a == b:
    if a == c:
        return "Yes"
    return "Maybe"
return "No"
```

Bad example:
```python
if a == b:
    if a == c:
        return "Yes"
    else:
        return "Maybe"
else:
    return "No"
```

### 4. Remove unused attributes.

Check that all the attributes you define in the `__init__` method are used.

