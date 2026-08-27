# Implementation of Erosion and Dilation Using OpenCV
## Developed By

### Name : Titus Ratna Kumar Karivella 
### Register number : 212224230292
## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program



## Output:
```import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((400, 600), dtype=np.uint8)

cv2.putText(img, "IMAGE PROCESSING", (80, 200),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 3)

kernel = np.ones((5, 5), np.uint8)

erosion = cv2.erode(img, kernel, iterations=1)

dilation = cv2.dilate(img, kernel, iterations=1)

plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap="gray")
plt.title("Original")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(erosion, cmap="gray")
plt.title("Erosion")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilation, cmap="gray")
plt.title("Dilation")
plt.axis("off")

plt.tight_layout()
plt.show()
```


### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

  
<img width="501" height="504" alt="image" src="https://github.com/user-attachments/assets/e59eadc0-9d1d-4a51-bb93-d02e7e390826" />



### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
- 

<img width="520" height="506" alt="image" src="https://github.com/user-attachments/assets/760a4a1a-687e-4737-bcbe-07207e379a27" />



### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.
  

<img width="489" height="511" alt="image" src="https://github.com/user-attachments/assets/01d5e8fc-d067-4190-adbd-eaacc3066869" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
