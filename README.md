# EX-5 IMAGE TRANSFORMATION
### Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
### Software Required:
- Anaconda - Python 3.7

### Algorithm:
- Step1: Import numpy,cv2,matplotlib.pypolt packages.
- Step2: Load the image file in the program.
- Step3: Use the Translation,Scaling,Shearing,Reflection,Rotation,Cropping using OpenCV and Python.
- Step4: Display the modified image output.
- Step5: End the program.
### Program:
```
Developed By: ROHIT JAIN D
Register Number: 212222230120
```
#### Reading the Original Image:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.imshow(img)
plt.show()
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174322](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/7bc5ec36-8f8a-4d06-b7ff-b4d09d087d0f)
#### i)Image Translation:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M=np.float32([[1,0,-250],
              [0,1,250],
              [0,0,1]])
trans=cv2.warpPerspective(img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans)
plt.show() 
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174154](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/e68c0107-df13-4e7f-bb27-5947e99d9d97)

#### ii) Image Scaling:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M=np.float32([[1.5,0,0],
              [0,1.3,0],
              [0,0,1]])
scaled=cv2.warpPerspective(img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled)
plt.show()  
````
- OUTPUT:<br>
<img height=13% width=35% src="https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/96e0743f-c76f-4f42-9b9b-9661b1f95ec1">

#### iii)Image shearing:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174225](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/16bdf223-cf59-4be5-90f0-262c62bceb97)
#### iv)Image Reflection:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M_x=np.float32([[1, 0,0   ],
                [0,-1,rows],
                [0, 0 ,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0   ],
                [ 0,0,1   ]])
reflect_x=cv2.warpPerspective(img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174236](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/5b0956c7-bc1f-46ba-b444-197e4a5c822b)
#### v)Image Rotation:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()     
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174248](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/4a8bef19-490e-4c81-b897-bb5ef7e1c64f)
#### vi)Image Cropping:
```Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("blue.jpg")
img = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
cropped_img=img[200:500,800:1100]
plt.imshow(cropped_img)
plt.show()
````
- OUTPUT:<br>
![Screenshot 2023-09-13 174301](https://github.com/ROHITJAIND/TRANSFORMATION-OF-IMAGE/assets/118707073/3c7e6fcc-b1bb-414a-8297-61bb7e2a5d86)
### Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
