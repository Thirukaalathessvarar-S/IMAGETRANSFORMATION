# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.

## Program:
```python
Developed By: Thirukaalathessvarar S
Register Number: 212222230161
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("unspash.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()

ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("unspash.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()  


iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("unspash.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()


iv)Image Reflection
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("unspash.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  

v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("unspash.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()     

vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("unspash.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[1000:2500 ,500:2500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![dip1_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/94a1fb0d-c2bf-4b79-931a-e4f00a51310e)


### ii) Image Scaling
![dip2_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/f85318c1-117b-4ef9-b6c4-39efb6140377)



### iii)Image shearing
![dip31_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/748374ae-8629-4779-bd2e-b2697ac39d48)

![dip32_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/01ce014f-e9f3-4b5c-b5cd-15b0d6be0b38)


### iv)Image Reflection
![dip4_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/f3e143ca-8ac2-49e3-b8c7-944703209235)

![dip42_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/c88fd2bb-98ff-4976-aa67-372d40cfec2f)



### v)Image Rotation
![dip5_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/696b7618-cd07-48d5-b77f-d666376466c3)




### vi)Image Cropping
![dip61_exp5](https://github.com/Thirukaalathessvarar-S/IMAGETRANSFORMATION/assets/121166390/d028af2d-a7dc-4520-a2e7-e6bd31bb55f8)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
