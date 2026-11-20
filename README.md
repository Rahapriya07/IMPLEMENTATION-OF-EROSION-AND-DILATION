# EXPERIMENT 9 – IMPLEMENTATION OF EROSION AND DILATION
## Name: Raha Priya Dharshini M
## Reg No. : 212224240124

## Aim
To implement morphological operations such as erosion and dilation on an image using OpenCV and Python.

## Software Requirements
- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Procedure

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Create a blank image of size 500 × 500 using NumPy.
3. Add text to the image using the `cv2.putText()` function.
4. Display the input image with text using Matplotlib.
5. Create a 3 × 3 kernel using `np.ones()`.
6. Apply **Erosion** using `cv2.erode()` to shrink the white text.
7. Display the eroded image.
8. Apply **Dilation** using `cv2.dilate()` to expand the white text.
9. Display the dilated image and compare the results.

## Code:
```

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(
    image,
    'Raha Priya Dharshini M',
    (100, 250),
    font,
    1,
    (255, 255, 255),
    2,
    cv2.LINE_AA
)

# Display the input image
plt.figure(figsize=(8, 6))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
plt.show()

# Create a 3x3 kernel
kernel = np.ones((3, 3), np.uint8)

# Apply erosion
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.figure(figsize=(8, 6))
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
plt.show()

# Apply dilation
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.figure(figsize=(8, 6))
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
plt.show()
```

## Output

### 1. Input Image with Text
<img width="1353" height="552" alt="image" src="https://github.com/user-attachments/assets/d6c3bb8b-3120-4b9a-aca5-a55be667a1fa" />


### 2. Eroded Image
<img width="1363" height="553" alt="image" src="https://github.com/user-attachments/assets/9869a0db-50b2-47db-be15-68c25d910002" />


### 3. Dilated Image
<img width="1361" height="556" alt="image" src="https://github.com/user-attachments/assets/d10712c2-4194-439a-932c-aadc11802d81" />


## Result
Thus, the morphological operations of erosion and dilation were successfully implemented using OpenCV and Python.
