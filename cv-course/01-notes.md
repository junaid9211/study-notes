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


### working with images
image has 3 dimentions (height, width, color)
1. height
2. width
3. color channels

for example the shape (1280, 720, 3)
- 1280 is height
- 720 is width
- is the rgb color channels


```python
# imports
import matplotlib.pyplot as plt
from PIL import Image

# open image
pic = Image.open('image/path')

# convert image to np array
pic_arr = np.asarray(pic)

# display image
plt.imshow(pic_arr)
```