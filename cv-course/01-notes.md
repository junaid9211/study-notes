# Numpy basics

### Creating array in numpy
```python
# cast python list to numpy array
np.array([1, 2, 3, 4])

# np.arange works similar to python's range function
np.arange(low, high, skip)

np.zeros((row, column))
np.ones((row, column))

# returns an array of n numbers between [low, high) low is inclusive high is exclusive
np.randon.randint(low, high, n)
```


### array operations
```python
arr.max()
arr.min()
arr.mean()
arr.argmax()
arr.argmin()
arr.reshape(row, column)
```

### indexting
```python
arr[row, col]  # returns a value at the location
arr[r0:r1, c0: c1]  # returns a subsection of the array
```