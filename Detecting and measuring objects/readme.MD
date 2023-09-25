# Computer Vision

## Description of Image Processing and Annotation Code

This code snippet performs image processing tasks and annotates the processed image with the dimensions of identified objects. Here's a breakdown of the key steps:

1. **Image Preprocessing:**
   - The code reads an input image specified by `img_path`.
   - It resizes the image to a desired height while maintaining the aspect ratio.
   - The image is then converted from the BGR color space to the HSV color space.



2. **Adjusting Saturation:**
   - The saturation channel of the HSV image is modified to control the saturation level.
   - A `saturation_factor` is applied to the saturation channel.

3. **Edge Detection:**

   - The Canny edge detection algorithm is applied to the modified image.
   - Edges are dilated to connect nearby points and eroded to remove noise.

4. **Contour Detection:**

   - Contours are identified in the processed image using the edge-detected image.
   - These contours represent objects or shapes in the image.

5. **Drawing Rotated Rectangles and Annotation:**

   - For each identified contour, a rotated bounding rectangle is drawn around it.
   - The width and height of the rectangle are calculated in centimeters based on a pixel-to-centimeter conversion factor.
   - The dimensions are annotated on the image at the bottom-right corner of each rectangle.

6. **Display and Save:**

   - The resulting image with annotated rectangles and dimensions is displayed using OpenCV.
   - The annotated image is saved as 'output_image.jpg' in the current directory.

7. **Clean Up:**

   - All OpenCV windows are closed after displaying the final annotated image.

This code can be used for object detection, dimension measurement, and annotation in images, which can be useful in various computer vision and image analysis applications.
