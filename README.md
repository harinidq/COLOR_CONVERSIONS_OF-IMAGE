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

### Program:
### Developed By:HARINI M D
### Register Number:212222230043
i) Read and display the image
```
import cv2
image=cv2.imread('harini.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('harini md',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:

### i) Read and display the image
![Screenshot 2024-09-07 223035](https://github.com/user-attachments/assets/0e08c7f7-4e6c-4eb6-82c6-9b1496a60c2c)



<br>
<br>

### ii)Write the image
```
 cv2.imwrite('b.jpg',image)
```
## OUTPUT:
![Screenshot 2024-09-07 232541](https://github.com/user-attachments/assets/c7a7b1f5-2d69-4f6f-9c2d-d913610a3a8f)



<br>
<br>

### iii)Shape of the Image
```
print(image.shape)
```
## OUTPUT:
![Screenshot 2024-09-07 232551](https://github.com/user-attachments/assets/21d981d8-4dfd-4c13-9e81-1912f31e8178)


<br>
<br>

### iv)Access rows and columns
```
import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('harini-1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-07 223201](https://github.com/user-attachments/assets/b1bcc08c-6713-41bf-abc0-d37dbabbf8c5)


<br>
<br>

### v)Cut and paste portion of image
```
image=cv2.imread('swathi.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('harini-2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-07 223336](https://github.com/user-attachments/assets/424c63d5-fc05-45e3-b4d5-b44c29153470)


<br>
<br>

### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('harini.jpg',1)
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
## OUTPUT:
![Screenshot 2024-09-07 223529](https://github.com/user-attachments/assets/9b9dfbcf-7c8b-4101-9296-22b917cef838)
![Screenshot 2024-09-07 223546](https://github.com/user-attachments/assets/b5e0b68f-e0c3-4e10-8e11-06d974f1879a)

![Screenshot 2024-09-07 223601](https://github.com/user-attachments/assets/7246567a-1a28-4d5f-9438-e2402c02eb4d)
![Screenshot 2024-09-07 223614](https://github.com/user-attachments/assets/3000e2e4-d6f6-4ffc-9b9d-c59632209d1c)
![Screenshot 2024-09-07 223630](https://github.com/user-attachments/assets/a0bc9870-f9d5-421b-866a-ead217360e4e)





<br>
<br>

### vii) HSV to RGB and BGR
```
img = cv2.imread('harini.jpg')
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
## OUTPUT:
![Screenshot 2024-09-07 223743](https://github.com/user-attachments/assets/5fe5559c-7e9c-4d72-bf3d-1ea5b8040b7a)
![Screenshot 2024-09-07 223802](https://github.com/user-attachments/assets/8dfb15db-bc02-49eb-878f-81ddfe4b4188)
![Screenshot 2024-09-07 223818](https://github.com/user-attachments/assets/71110843-c907-4e60-a3e2-33957256ded9)





<br>
<br>

### viii) RGB and BGR to YCrCb
```
img = cv2.imread('harini.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![Screenshot 2024-09-07 223918](https://github.com/user-attachments/assets/2ca6bdea-73bb-4c5e-abd4-a423964bb3f4)
![Screenshot 2024-09-07 223933](https://github.com/user-attachments/assets/a037170f-8ea1-41fb-94e6-55a5cff01cdc)
![Screenshot 2024-09-07 223945](https://github.com/user-attachments/assets/b3228c30-cea6-4e64-ab93-d847479b3962)




<br>
<br>

### ix) Split and merge RGB Image
```
img = cv2.imread('harini.jpg',1)
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
## OUTPUT:
![Screenshot 2024-09-07 224049](https://github.com/user-attachments/assets/179af4b5-7d0d-430d-b1f5-ab496aa73099)
![Screenshot 2024-09-07 224109](https://github.com/user-attachments/assets/3421dda3-e5a3-4012-b3a5-75cc35b252f8)
![Screenshot 2024-09-07 224123](https://github.com/user-attachments/assets/2e7f2ba3-6812-4989-98c5-72efeb8dc6bd)
![Screenshot 2024-09-07 224137](https://github.com/user-attachments/assets/c7d055ce-def8-48fb-894d-ed3e42736e8b)



<br>
<br>

### x) Split and merge HSV Image
```
img = cv2.imread("harini.jpg",1)
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
## OUTPUT:
![Screenshot 2024-09-07 224226](https://github.com/user-attachments/assets/84ced323-85df-4bed-9677-74ff480edd5f)

![Screenshot 2024-09-07 224240](https://github.com/user-attachments/assets/4ab4e159-1ade-4dfa-8df5-397042f40230)

![Screenshot 2024-09-07 224250](https://github.com/user-attachments/assets/91e116bc-d11d-4a1d-97d2-a1eb0f90cfc2)

![Screenshot 2024-09-07 224306](https://github.com/user-attachments/assets/ce835dc3-9735-4be6-bed6-aac22e001b64)


<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








