# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>
Import cv2 and save an image as scolor.jpeg.

### Step2:
<br>
Use imread to read and display the image.

### Step3:
<br>
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
<br>
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
<br>
End the program and view the output image windows.

## Program:
```python
# Developed By:ROSHINI R K
# Register Number: 212222230123
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('aa.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()

# i) Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()


#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()


#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR
#HSV TO RGB

rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2.destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image
# SPLIT AND MERGE RGB IMAGE

blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()




# v) Split and merge HSV Image
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()




```
## Output:
### Original image:

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/c82b3206-b60b-43d8-939e-8906be32e6c4)


### 1. BGR and RGB to HSV and GRAY
### i)BGR TO HSV

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/effb46a5-2226-4fb7-acb7-de3ee34431cf)

### ii)BGR TO GRAY

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/85e65342-8826-48d4-8880-40ac9605f5cd)

### iii)RGB TO HSV
![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/dd35f060-b884-4815-aa44-c160e0847fde)


### iv)RGB TO GRAY:
![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/8fa712f2-8b5b-484f-80b6-8843ed9b9943)



### 2. HSV to RGB and BGR
### i) HSV TO RGB

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/33b1d16a-2e63-464e-bcf4-5ac12a921b4b)

### ii) HSV TO BGR

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/aa60add2-f792-44e8-b5dd-6c142c7f1b71)

### 3.RGB and BGR to YCrCb
### i) BGR TO YCrCb

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/c775b4b1-691b-44fe-9e2d-0f8aacd3f65b)


### ii)RGB TO YCrCb

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/035f89b7-bcea-41dc-9a94-1b200d4e1c6e)


### 4. Split and merge RGB Image

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/9dac8c91-c1ad-4a63-b680-f4cd8282bead)


### 5. Split and merge HSV Image

![image](https://github.com/roshiniRK/COLOR-CONVERSION/assets/118956165/d692690b-5063-4998-a55e-a7fa0877079b)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
