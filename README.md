

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules.

### Step2:
Choose an image and save it as filename.jpg.

### Step3:
Use imread to read the image.

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image.

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image
## Program:

Developed By:Mathiyazhagan.A


Register Number: 212222240063

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,114],[0,1,-230],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()

```

iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()

```



iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```




v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```




vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("mountain.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[100:800,20:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```






### Output:
## i)Image Translation
![Screenshot 2024-03-12 114241](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/a859bd31-e4c7-4f90-8c7c-8365635d9450)


## ii) Image Scaling
![Screenshot 2024-03-12 114336](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/9f9c3403-e949-4138-a369-9f914eee72a6)


## iii)Image shearing
![Screenshot 2024-03-12 114413](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/91ce4ef6-ba10-4058-9527-4a763bb4843e)


## iv)Image Reflection
![Screenshot 2024-03-12 114501](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/054ff9fa-c6fc-43d2-b384-f263733cf304)


## v)Image Rotation
![Screenshot 2024-03-12 114536](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/8c2d72c7-713f-4d67-a2d7-771056547459)


## vi)Image Cropping

![Screenshot 2024-03-12 114616](https://github.com/Mathiofficial/IMAGE-TRANSFORMATIONS/assets/118787327/b458879f-d1a9-4aa8-b42a-5316277fe634)



### Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
