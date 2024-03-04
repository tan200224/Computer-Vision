# Introduction
The goal of this assignment is to count the number of objects of different types in an image, where the objects of different types have different characteristic colors. In this case, the objects are apples, oranges, and bananas, which (supposedly) have different colors (red, orange, and yellow). Specifically, you will write a notebook that finds the locations of oranges, apples, and bananas in images. There are several test images on which you are to run your program.

Your first step is to design a color model. This is just a way to label individual pixels as apple, orange, banana or background. One way to do this is to train a classifier such as a neural network. (This option is not allowed for this project.) An easier way, which we will use here, is simply to use thresholds on the color values. For example in HSV space, maybe every pixel within a certain range of yellowish hues that is saturated enough is considered part of a banana.

You’ll then have to clean up the image using mathematical morphology operations (e.g., opening and closing) primarily and any other rules you need to remove spurious background regions. Note that you may not manually fine tune your algorithm to each test image individually. However, if your algorithm adaptively changes thresholds based on something you compute on the fly from the image (like the average size of the fruit), that’s OK; imaging researchers do this all the time. There is a big difference between the two techniques. Ask if this isn’t clear.

You will then use contours to group adjacent foreground pixels, which will allow you to isolate and count the fruit and find the center coordinates (x, y in pixels) for each one. 

