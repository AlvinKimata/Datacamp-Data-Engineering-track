## Definitions.
***
###`Nested function.`
#### A `nested function` is a function defined inside another function.
```python
#outer function
def parent():
    #Nested function.
    def child():
        pass
    return child
```
***
### `Nonlocal variables`
#### A `nonlocal variable` is a variable defined in the parent function that are used by the child function.

```python
def parent(arg_1, arg_2):
    #from child()'s point of view, 
    #'value' and 'my_dict' are nonlocal variables,
    #as are 'arg_1' and 'arg_2'
    
    value = 22
    my_dict = {'chocolate': 'yummy'}
    
    def child():
        print(2 * value)
        print(my_dict['chocolate'])
        print(arg_1 + arg_2)
        
    return child
```

### Closures.
#### A `closure` is a nonlocal variable attached to a returned function.

```python
def parent(arg_1, arg_2):
    #from child()'s point of view, 
    #'value' and 'my_dict' are nonlocal variables,
    #as are 'arg_1' and 'arg_2'
    
    value = 22
    my_dict = {'chocolate': 'yummy'}
    
    def child():
        print(2 * value)
        print(my_dict['chocolate'])
        print(arg_1 + arg_2)
        
    return child

new_function = parent(3, 4)

print([cell.cell_contents for cell in new_function.__closure__])