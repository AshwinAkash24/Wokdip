# Workshop-1: Working On The Images
# Name : Ashwin Akash M
# Register Number: 212223230024
# Department : Artificial Intelligence And Data Science
# Aim :
Load two images of the same size.<br>
Divide each image into four equal regions (quadrants) based on specific row and column coordinates.<br>
Save the eight individual regions, labeling them as R1, R2, R3, R4 for the first image and R5, R6, R7, R8 for the second image.<br>
Swap the regions as follows:<br>
R1 with R8<br>
R2 with R7<br>
Resize the final images to dimensions specified by the last four digits of your registration number, ensuring the number is even.<br>
# Code:
```
import cv2
image=cv2.imread('Dip.jpg')
image1=cv2.imread('Dip1.jpg')
```
```
image.shape
image1.shape
```
```
cv2.imshow('Image',image)
cv2.imshow('Image1',image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
row_mid=250
col_mid=250
```
```
R1=image[0:row_mid,0:col_mid]
R2=image[0:row_mid,col_mid:500]
R3=image[row_mid:500,0:col_mid]
R4=image[row_mid:500,col_mid:500]
R5=image1[0:row_mid,0:col_mid]
R6=image1[0:row_mid,col_mid:500]
R7=image1[row_mid:500,0:col_mid]
R8=image1[row_mid:500,col_mid:500]
```
```
cv2.imwrite('R1.jpg',R1)
cv2.imwrite('R2.jpg',R2)
cv2.imwrite('R3.jpg',R3)
cv2.imwrite('R4.jpg',R4)
cv2.imwrite('R5.jpg',R5)
cv2.imwrite('R6.jpg',R6)
cv2.imwrite('R7.jpg',R7)
cv2.imwrite('R8.jpg',R8)
```
```
cv2.imshow('R1',R1)
cv2.imshow('R2',R2)
cv2.imshow('R3',R3)
cv2.imshow('R4',R4)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
cv2.imshow('R5',R5)
cv2.imshow('R6',R6)
cv2.imshow('R7',R7)
cv2.imshow('R8',R8)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
image[0:row_mid,0:col_mid]=R8
image1[row_mid:500,col_mid:500]=R3
```
```
cv2.imshow('Reimage',image)
cv2.imshow('Reimage1',image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Output:
![dip1](https://github.com/user-attachments/assets/15278848-614d-40fd-8214-15c5587d4904)

![dip3](https://github.com/user-attachments/assets/165ad92c-979f-430c-83d3-7e57393a1a91)

![dip](https://github.com/user-attachments/assets/782524c1-9301-42ca-9eca-f5238815cb91)
# Result:
Swaping For The Images at given loction has been swaped successfully.
