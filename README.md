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
```
Developed By: shaik lahir
Register Number: 212224240148
```
##  i)Original Image:
```python
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('cat.jpg',-1)
original = cv2.cvtColor(img , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape
```
## ii)Image Translation
```python
translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## iii)Image shearing
```python
shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## iv)Image Reflection
```python
ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## v)Image Rotation
```python
angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## vi)Image Cropping
```python
cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()

```


## Output:

  ### i)Original image
  
![Screenshot 2025-05-05 095551](https://github.com/user-attachments/assets/c528a6d2-6a4a-4688-9541-7710612a2a74)


### ii)Image Translation

![image](https://github.com/user-attachments/assets/eea4fb52-3682-42d7-9e93-58f0fa1bdfcc)



### iii) Image Scaling


![image](https://github.com/user-attachments/assets/f84947cc-7ad5-47ba-8c0e-12d73656ea6b)



### iv)Image shearing

![image](https://github.com/user-attachments/assets/f584d754-2963-4e8d-9a7a-02fba539664d)



### iv)Image Reflection


![image](https://github.com/user-attachments/assets/ba5de268-1a23-4c2c-a0ac-48c0e21f5657)



### v)Image Rotation

![image](https://github.com/user-attachments/assets/15844e37-2238-4145-b06e-aa22fdd0e921)



### vi)Image Cropping

![image](https://github.com/user-attachments/assets/4092d42c-f226-4eef-83cc-f336e298bd1b)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
