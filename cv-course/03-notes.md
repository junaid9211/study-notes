# More on Opencv

### drawing shapes on images
shapes are drawn inplace on the image arrays.
<br>
There are 3 most shapes 
- rectangle
- circle
- line

<br>

Keep in mind that the top left corner of an image is (0, 0)
and bottom right corner is (width, height)

```python
# draw a rectangle using top left and bottom right points
cv2.rectangle(img, pt1=(x1, y1), pt2=(x2, y2), color(r, g, b), thickness=px)

# draw a circle given center and radius
cv2.circle(img, center=(x, y), radius=px, color(r, g, b), thickness=px)

# draw a line between two points
cv2.line(img, pt1=(x1, y1), pt2=(x2, y2), color=(r, g, b), thickness=px)
```