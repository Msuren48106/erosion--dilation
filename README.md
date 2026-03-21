# Exp-9-Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:

Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.
### Step 2:

Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.
### Step 3:

Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.
### Step 4:

Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.
### Step 5:

Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.
### Step 6:

Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.
### Step 7:

Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.

## REG NO: 212223230222
## NAME : M.SUREN.
## Program:
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype="uint8")
```


### Create the Text using cv2.putText
```
text = "M.SUREN."
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```

### Create the structuring element

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

```


### Original image
```

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```

### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```



### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```


## Output:

### Display the input Image
<br>
<br>
<br>

<img width="516" height="515" alt="Screenshot 2026-03-21 122240" src="https://github.com/user-attachments/assets/ab316f8b-78cc-487e-bce8-0bb88cbd7fe5" />


<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<img width="511" height="501" alt="Screenshot 2026-03-21 122247" src="https://github.com/user-attachments/assets/e4f0050c-5054-4d80-a12d-1e4526345998" />



<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<img width="529" height="507" alt="Screenshot 2026-03-21 122255" src="https://github.com/user-attachments/assets/b81c7333-d8ef-49be-b991-427fb47d3335" />



<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
