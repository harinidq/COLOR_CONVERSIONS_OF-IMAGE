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
### Developed By: HARINI M D
### Register Number: 212222230043




### i) Read and display the image                  
                                                      
 
  
 ```
import cv2
image=cv2.imread('dog.jpg',1)
cv2.imshow('sakthi',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
 ```

## Output:
  ![Screenshot 2024-02-15 135726](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/f392ae14-d889-44ea-a995-0ac4f02ada84)


### ii)Write the image                         
                                                      
 ```
import cv2
   image=cv2.imread('dog.jpg',0)
   cv2.imwrite('d.jpg',image)
```
## Output:
  ![Screenshot 2024-02-15 205052](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/65bf2ab2-3200-4738-8b7c-7214838bd2da)

      
### iii)Shape of the Image                           
                                                          
```
 import cv2
    image=cv2.imread('dog.jpg',1)
    print(image.shape)
```
## Output:

![Screenshot 2024-02-15 205157](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/67c8a66c-a100-422a-bb27-d3e297b9eaf3)

                                                     
### iv)Access rows and columns                    
                                                       
```
import random
    import cv2
    image=cv2.imread('dog.jpg',1)
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

## Output:

![Screenshot 2024-02-15 205549](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/975f545e-1ed9-4866-bde9-55bba58322a1)

 
### v)Cut and paste portion of image               
```
     import cv2
     image=cv2.imread('dog.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
 
## Output:
  ![Screenshot 2024-02-15 192945](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/4bce6e90-1af4-4e1d-83c9-018a45ca4615)

### vi) BGR and RGB to HSV and GRAY           
```
import cv2
img = cv2.imread('dog.jpg',1)
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

## Output:
![Screenshot 2024-02-15 140206](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/bfc64452-f9c8-4abe-9982-31b896966ad7)![Screenshot 2024-02-15 140334](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/cd11adf1-a721-4252-b1c3-6bf72675bf6c)

![Screenshot 2024-02-15 140314](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/ff6dc6b3-9372-44fa-b81f-a60ab9ca15f7)
![Screenshot 2024-02-15 140252](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/473dbdc5-6f59-411b-bf86-188d3fabc858)

 ![Screenshot 2024-02-15 140228](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/344caec1-b527-4c8b-abda-8644bc621ce3)




### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dog.jpg')
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
## Output:
![Screenshot 2024-02-15 193353](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/69e07b00-bc24-4656-a5a8-bb45e224758f)![Screenshot 2024-02-15 193413](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/fe0c1c80-9141-4c3b-a06f-0c767b1b5205)

![Screenshot 2024-02-15 193437](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/a5476a64-d3e9-404f-bf3c-fcf50eebc360)



### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dog.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-15 193702](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/c53f3fe3-14fc-4acd-aff8-618be135e08f)
![Screenshot 2024-02-15 193945](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/4be22ab3-c1e7-4c4b-b8fe-f67ac45a8751)
![Screenshot 2024-02-15 193745](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/fd35d2d2-04f0-4e24-95a7-b7d5a5b3a467)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dog.jpg',1)
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
##  Output:
![Screenshot 2024-02-15 194205](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/e1727a1e-d8f0-4f56-baf8-830d13ea6159)![Screenshot 2024-02-15 194148](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/8dbfe2d2-bd72-48a8-bdb5-ced617093eee)

![Screenshot 2024-02-15 194115](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/7e861787-90c5-4592-8183-cabc7e5062d7)
![Screenshot 2024-02-15 194130](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/8a37fe2d-bcb7-408e-b8f1-daa4fbd29860)




### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dog.jpg",1)
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

## Ouput:
![Screenshot 2024-02-15 194454](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/d0680c15-5755-4c0e-bca3-91176b831db5)![Screenshot 2024-02-15 194539](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/bd59bc4a-a0d6-46b5-addf-8821a2809fd6)

![Screenshot 2024-02-15 194523](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/4a3ab9cf-1716-44e5-80de-3273b3d05117)
![Screenshot 2024-02-15 194511](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/f3114856-43fa-4934-9ebd-3525df522645)





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.



