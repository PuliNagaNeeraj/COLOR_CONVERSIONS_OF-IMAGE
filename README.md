# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Puli Naga Neeraj
### Register Number:  212223240130


## Output:

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('NagaNeeraj.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('NagaNeeraj',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 1](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/97e35251-6e31-4966-a0c2-b3ea0879ce6b)
<br>
<br>

### ii)Write the image
```Python
import cv2
image=cv2.imread('NagaNeeraj.jpg',0)
cv2.imwrite('NagaNeeraj1.1.jpg',image)
```
#### OUTPUT:
![NagaNeeraj1 2](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/ea767b87-c7d2-471e-97db-23f2aa2de3f5)
<br>
<br>

### iii)Shape of the Image
```Python
import cv2
image=cv2.imread('NagaNeeraj.jpg',1)
print(image.shape)
```
#### OUTPUT:
![NagaNeeraj1 3](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/74ca2bc8-0bf8-436d-a5f2-742a326a4ed4)
<br>
<br>

### iv)Access rows and columns
```Python
import random
import cv2
image=cv2.imread('NagaNeeraj.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 4](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/66e2b31b-4607-47c7-8179-52fcf7ab45be)
<br>
<br>

### v)Cut and paste portion of image
```Python
import cv2
     image=cv2.imread('NagaNeeraj.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 5](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/d1ec5f13-1688-467e-b688-fe89dbc29d9a)
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```Python
 import cv2
    img = cv2.imread('NagaNeeraj.jpg',1)
    img = cv2.resize(img,(300,200))
    cv2.imshow('Original Image',img)

    hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
    cv2.imshow('BGR2HSV',hsv1)

    hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
    cv2.imshow('RGB2HSV',hsv2)

    gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
    cv2.imshow('BGR2GRAY',gray1)

    gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
    cv2.imshow('RGB2GRAY',gray2)

    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 6](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/b4a7cb12-53e6-4a59-ab3a-c0bd78de82fe)
<br>
<br>

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('NagaNeeraj.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 7](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/8eea9329-9c0f-4007-8494-4ff8f7cab06e)
<br>
<br>

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('NagaNeeraj.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 8](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/2e3a62c4-bb91-462a-9e65-d60f304d4918)
<br>
<br>

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('NagaNeeraj.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 9](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/618f471b-0c3e-47d8-9fcb-f221dc29e22d)
<br>
<br>

### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("NagaNeeraj.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:
![NagaNeeraj1 10](https://github.com/PuliNagaNeeraj/COLOR_CONVERSIONS_OF-IMAGE/assets/138849173/4db274c5-4fa6-429c-8670-1f774ad548ee)
<br>
<br>
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







