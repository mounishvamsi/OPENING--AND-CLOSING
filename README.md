# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
```
 Developed by : R Mounish Vamsi Kumar 
 Register number:212224240096 
```

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

# Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```


# Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```




# Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
# Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
# Display the result of Opening
```
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
# Closing is dilation followed by erosion
```
image_close = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```



## Output:

### Display the input Image

<img width="542" height="511" alt="image" src="https://github.com/user-attachments/assets/a9ccd0e1-0bda-4c73-8aea-2d09464308b3" />


### Display the result of Opening

<img width="561" height="523" alt="image" src="https://github.com/user-attachments/assets/737aac51-697d-4410-96d7-e040b765ac06" />


### Display the result of Closing

<img width="534" height="524" alt="image" src="https://github.com/user-attachments/assets/947d5126-7241-4d54-b2be-68bbb0c98321" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
