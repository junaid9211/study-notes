# Image processing 
## Changing colorspaces
There are 3 most common color spaces
- RGB
- HSL
- HSV
<br>

To change color space
```python
img2 = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

## Blending images in cv2
The following arithmetic operation is performed on each pixel to perform blending.

$$  img1 * \alpha  + img2 * \beta  + \gamma $$

Make sure that the shape and size of both images is the same otherwise you would get an exception

```python
# read the images
img1 = cv2.imread('../DATA/dog_backpack.jpg')
img2 = cv2.imread('../DATA/watermark_no_copy.png')

# change the colorspace
img1 = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
img2 = cv2.cvtColor(img2, cv2.COLOR_BGR2RGB)

# resize the images so that they are the same size
img1_resize = cv2.resize(img1, (1000, 1000))
img2_resize = cv2.resize(img2, (1000, 1000))

# perform blending operation
blended = cv2.addWeighted(src1=img1, alpha=0.5, 
                          src2=img2, beta=0.5, 
                          gamma=0)
```

## Overlaying images

```python
img1 = cv2.imread('../DATA/dog_backpack.png')
img2 = cv2.imread('../DATA/watermark_no_copy.png')
img2 = cv2.resize(img2, (600, 600))

img1 = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
img2 = cv2.cvtColor(img2, cv2.COLOR_BGR2RGB)

large_img = img1
small_img = img2

# math magic, we are just replacing pixels of larger image with the pixels of small image using assignment operation
x_offset, y_offset = 0, 0
x_end = x_offset + small_img.shape[1]
y_end = y_offset + small_img.shape[0]

large_img[y_offset: y_end, x_offset: x_end] = small_img   
```




