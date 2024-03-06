# Histograms, Thresholding, and Morphology

### Image
* Color: Width * Hight * Channels, 256 Values per channel
  * RGB
  * HSV
* Grayscale: Width * Hight, 256 Values
  * "Black and White"
  * Single-channel
* Binary: Width * Hight, 2 value
  * Actually black and white
  * Mask
  * Thresholding image

**Intensity in Grayscale image refers to the amount of light; a high intensity means there is a spot of the grayscale image that is very white or bright**

<img width="472" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/83906e25-e3ae-4b6b-bc8a-6837efa25a2c">

In this case, the intensity at 200 with the most number of pixels refers to the white background of the image. The intensity around 50 - 150 indicates the count of pixels for the coins.

## Threshold
We can set a value for the threshold to create a mask for the object that we are trying to look for from the image

<img width="470" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/a5afda39-5219-4e21-8f8a-0e19330d0330">

<img width="463" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/545c23c4-2d65-4770-b413-18a6936f9d8b">

**Not Options**
* cv2.THRESH_BINARY: Use it when the foreground is brighter
* cv2.THRESH_BINARY_INV: Use it when the foreground is darker

## Morphology
* Open: Remove small white noise
* Closing: Remove small black noise
  
<img width="328" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/69561fe0-3714-4d3a-b3af-7fe09c0c10b6">

### Steps to create a good Mask

<img width="570" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/1c7e5aec-47c2-4637-92da-b98d25641cd1">

# Color Thresholding and HSV

## Color Thresholding
Sometimes it is hard to identify the threshold directly from the histogram

<img width="622" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/108d64b8-73d0-4566-bb9f-d7e4f6fc4ed7">

**The result of the 135 threshold value:**

<img width="496" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/7607946a-17a9-40b2-9f46-cab1e4dc45ff">

#### We can try with RGB

<img width="628" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/20bba0a3-ea4b-4ca3-b4c3-928d97155962">

The images above shows that the blue channel might be a good one to separate the orange and the light blue background, therefore we can set a thresold for the blue channel.

<img width="494" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/9e2ad0d0-1ffd-4290-b225-8325855f7233">

#### Comparison of the Result

<img width="508" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/6b5859a9-e20b-4e91-ba0e-db504ee9aa05">

# HSV

<img width="626" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/92949521-ae24-4330-a737-4df9c09b9687">

### Hue represents the color being displayed

<img width="230" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/66ff1eea-0c67-4ff3-8c47-5a3316bf0808">

### Saturation is between 0 and 255; it encodes how much color there is.

<img width="623" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/7cb94830-d045-4757-98f5-287dc16925e9">

### The Vlaue channel is essentially the "gray" version of the image

<img width="623" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/80b5d441-0d59-4518-b1e8-23a19092a4bc">


# Filtering

<img width="491" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/0acbd79e-e0b7-4624-a11f-c8fcb1dea25f">

### Box Filter

<img width="488" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/e414e0b8-2b47-4be0-9fb2-b669590ea63c">

### Gaussian Distribution

<img width="655" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/2a2fd572-260e-4714-be88-08b26cef303a">
<img width="122" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/0034b966-46bd-440d-a0ac-90f7783e007c">
<img width="107" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/50373441-7cd7-4605-9307-bb9bf82e516e">
<img width="214" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/480cbf32-9e49-41db-b116-2a5d0f99a67a">

### More types of filters
* Median filtering: take the middle pixel value in the neighborhood
* Bilateral filtering: only average similar looking neighbors
* Non-local means: only average pixels with a similar local neighborhood

Denoising Method Comparison
<img width="605" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/a72a7bb5-3c30-4012-9520-38ac863a3110">

# Gradients and Edges
#### Practice with linear filters
<img width="431" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/7104334e-e487-4939-a53d-50f602595938">

<img width="408" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/b94ca762-e939-42ea-aa2c-972633a83703">

<img width="463" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/f89a1b1f-a9c9-4ed0-8a1a-63070a949b56">

<img width="405" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/e8b45e49-ad2a-4311-b91f-a5dd8d44e605">

### Sobel X and Y
<img width="587" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/0452b277-8fc9-4783-b81f-4b25d338d63d">

<img width="581" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/d8a68df2-02a7-4824-8a6f-916b2452fd17">

### Gradients
<img width="355" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/83903fb6-0b96-4a30-8c18-3d050550d047">

<img width="271" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/eeade0bc-8b46-4abb-b6be-fe4ef24a7529">

    img = cv2.imread('coins01.jpg')
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    sob_x = cv2.Sobel(gray, cv2.CV_64F, 1, 0)
    sob_y = cv2.Sobel(gray, cv2.CV_64F, 0, 1)
    grad_mag = np.sqrt(sob_x**2 + sob_y**2)

### From Gradient Magnitude to Edges
<img width="653" alt="image" src="https://github.com/tan200224/Computer-Vision/assets/68765056/9b3c0245-43e5-4ab9-b577-1cb860aabcdd">




