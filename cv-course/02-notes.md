# Opencv basics

### Reading an image
```python
# import opencv
import cv2

# read the image as BGR
img = cv2.imread("IMAGE_PATH")

# read the image as grayscale
img = cv2.imread('IMAGE_PATH', cv2.IMREAD_GRAYSCALE)
```

### Color channels
- opencv reads images as BGR channels
- matplotlib reads images as RGB channels
```python
# change the color channels
img2 = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

### resize image
```python
cv2.resize(img, (new_width, new_height))
```

### flipping images
pos can be 1 of 3 values
- 0 : vertical flip
- 1 : horizontal flilp
- -1 : both vertical and horizontal flips
```python
cv2.flip(img, pos)
```