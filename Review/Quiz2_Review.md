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

# Color Thresholding, HSV, and Contours

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














