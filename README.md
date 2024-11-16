# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:HARINI M D
### Register Number: 212222230043


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('dq.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 160830](https://github.com/user-attachments/assets/05083cd0-f15b-4867-b4d2-b806c05d4cc4)


<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("dq.jpg")
res = cv2.line(img, (0, 0), (1029,686), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![Screenshot 2024-09-09 161510](https://github.com/user-attachments/assets/8fe6f559-b304-401a-afbe-cb983bb182b5)


ii)Draw a circle at the center of the image.
```
import cv2

# Load the image
img = cv2.imread("dq.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 161800](https://github.com/user-attachments/assets/cc67dd17-3945-49e6-8167-0c6ece986016)


iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("dq.jpg")
start=(100,100)
stop=(500,600)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/69d91f54-e41e-4856-92ce-10684732f686)




iv)Add the text "DULQUER" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("dq.jpg")

# Define the text to be added and its position
text = "DULQUER"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 162644](https://github.com/user-attachments/assets/eef01774-f4a3-42bf-b570-451deca69c4a)


<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('dq.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162723](https://github.com/user-attachments/assets/44f0acdf-d526-4e9b-a210-3589019d6b21)
![Screenshot 2024-09-09 162733](https://github.com/user-attachments/assets/88d0b038-2696-4d8d-bd96-da0bd6b67867)


ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('dq.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162818](https://github.com/user-attachments/assets/d09c8a0c-49a4-4096-a129-a72d6975677f)
![Screenshot 2024-09-09 162829](https://github.com/user-attachments/assets/3c2af990-db70-4661-b17a-76e0fc6cf0af)

iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('dq.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162902](https://github.com/user-attachments/assets/52b6792f-1bbc-4bff-b354-28efb510741d)
![Screenshot 2024-09-09 162911](https://github.com/user-attachments/assets/c843cc16-261f-465c-82ce-efdfc59fb855)


iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('dq.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 163019](https://github.com/user-attachments/assets/a05d490a-936c-426e-b788-be3f9c5fa86b)

![Screenshot 2024-09-09 163026](https://github.com/user-attachments/assets/7e84976c-ecfa-4c4a-949e-315028b467b3)

<br>
<br>

### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('dq.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![Screenshot (147)](https://github.com/user-attachments/assets/0d087bcd-eb88-4f08-a202-55d4cdfad17e)

![Screenshot 2024-09-09 175700](https://github.com/user-attachments/assets/e5186feb-564b-421d-a0ad-6aaa79d1a01f)

![Screenshot 2024-09-09 175711](https://github.com/user-attachments/assets/6bf33faa-2a22-4c45-8bb5-a13e74df3a5d)


<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot (138)](https://github.com/user-attachments/assets/430eb402-6dc0-4a6b-b7bb-875b661edc89)


<br>
<br>

### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('dq.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 400, 400

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot (142)](https://github.com/user-attachments/assets/e1729816-c5a5-4a4d-bd70-88ac7f481461)


<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("dq.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot (143)](https://github.com/user-attachments/assets/c03d5c1e-4c6b-4366-a378-b627b33711f1)

ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("dq.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot (145)](https://github.com/user-attachments/assets/cc72ef58-d554-468d-bd47-14f750888823)


<br>
<br>

### viii)Write and Save the Modified Image
```
 cv2.imwrite('dq.jpg',image)
```
![image](https://github.com/user-attachments/assets/a2ab057a-430d-492a-be5b-988cc0ccde5d)

<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.











