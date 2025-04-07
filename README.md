# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules

### Step2:

Choose an image and save it as filename.jpg

### Step3:

Use imread to read the image

### Step4:

Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

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

### Step11:

End the program
## Program:
```python
Developed By:shaik lahir
Register Number:212224240148

i)Image Translation


import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("dip.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()

iii)Image shearing

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

iv)Image Reflection

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()


v)Image Rotation

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)


vi)Image Cropping

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Cropping:")
plt.imshow(translated_image)
plt.show()



```
## Output:
### i)Image Translation

![image](https://github.com/user-attachments/assets/b46d225d-9dc4-4a97-bd88-cab58c02e6b1)


### ii) Image Scaling

![image](https://github.com/user-attachments/assets/64083618-05bd-499b-9431-9a4213e526ec)



### iii)Image shearing

![image](https://github.com/user-attachments/assets/dbd040e2-99f7-4c7a-9552-3625ed81dba1)



### iv)Image Reflection

![image](https://github.com/user-attachments/assets/59791c08-1a4c-449c-a815-ea4a852d76ee)




### v)Image Rotation

![image](https://github.com/user-attachments/assets/410d13e9-33d9-47c7-9128-891e8ccc5612)



### vi)Image Cropping

![image](https://github.com/user-attachments/assets/cde23a10-7ea5-4846-93c1-1885980dca78)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
