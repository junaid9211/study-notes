# Drawing on Images

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

### writing on image
org is coordinates for the bottom left of the text

```python
cv2.putText(img, 
        text='JUNAID', 
        org=(400, 100), 
        fontScale=4,
        color=(255, 255, 255),
        thickness=5,
        fontFace=cv2.FONT_HERSHEY_SIMPLEX, 
        lineType=cv2.LINE_AA
        )
```

### draw on image using mouse
```python
import cv2
import numpy as np

# callback function to draw on the image
def draw(event, x, y, flag, param):
    if event == cv2.EVENT_LBUTTONDOWN:
        cv2.rectangle(img, pt1=(x-50, y-50), pt2=(x+50, y+50), color=(0, 255, 0), thickness=5)


# create image
img = np.zeros((1000, 1000, 3), dtype=np.uint8)
img_ref = 'my_window'

# add reference
cv2.namedWindow(winname=img_ref)

# add event listener
cv2.setMouseCallback(img_ref, draw)

# display the image
while True:
    cv2.imshow(winname=img_ref, mat=img)
    
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
        
cv2.destroyAllWindows()
    
```


### drawing using a mouse example 2
Script draws a rectangle using drag
```python
import cv2
import numpy as np
from random import choice

drawing = False
ix, iy = -1, -1

def draw_rect(event, x, y , flag, params):
    global drawing, ix, iy
    
    if event == cv2.EVENT_LBUTTONDOWN:
        drawing = True
        ix, iy = x, y
        
    elif event == cv2.EVENT_MOUSEMOVE:
        if drawing:
            c = [(0, 0, 255), (0, 255, 0), (255, 0, 0)]
            cv2.line(img, (ix, iy), (x, y), choice(c), 5)
            ix, iy = x, y
        
    elif event == cv2.EVENT_LBUTTONUP:
        drawing = False
    
    

img = np.zeros((512, 512, 3), np.uint8)
img_ref = 'my_window'

cv2.namedWindow(winname=img_ref)
cv2.setMouseCallback(img_ref, draw_rect)

while True:
    cv2.imshow(img_ref, img)
    
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cv2.destroyAllWindows()

```