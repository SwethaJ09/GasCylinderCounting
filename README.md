# GasCylinderCounting
This repository contains a Python script for detecting circles (representing gas cylinders) in one image and rows and columns (representing lines) in another image using OpenCV and Gradio. The script processes the images to detect these elements and provides a Gradio interface for easy interaction
# Requirements
Python 3.6+
OpenCV
NumPy
Gradio

# Installation
Clone the repository or download the script file.
Install the required libraries using pip:
bash
Copy code
pip install opencv-python-headless numpy gradio

# Usage
Upload images:

The first image should contain circular objects (gas cylinders) to be detected.
The second image should contain lines for row and column detection.
Run the script:

You can run this script in a Google Colab notebook. Follow these steps:

Running in Google Colab
Open Google Colab: Google Colab

Create a new notebook.

Install the required libraries by running the following command in a code cell:

python
Copy code
!pip install opencv-python-headless numpy gradio
Copy the provided code into a code cell in the Colab notebook.

Run the code cell.

After running the code, a Gradio interface link will be provided. Click on the link to access the Gradio interface for uploading images and viewing the results.

# Script Explanation
The script defines two main functions: detect_circles and detect_rows_and_columns.

detect_circles(image)
Converts the image to grayscale.
Applies Gaussian blur to reduce noise.
Uses the Hough Transform to detect circles.
Draws detected circles and prints the radius on the image.
Returns the number of detected circles and the processed image.
detect_rows_and_columns(image)
Resizes the image while maintaining the aspect ratio to fit within the display window.
Converts the image to grayscale and applies Gaussian blur.
Uses the Canny edge detector to find edges in the image.
Applies the Hough Line Transform to detect lines.
Filters out horizontal and vertical lines.
Draws detected lines on the image.
Returns the number of detected rows, columns, and the processed image.
Gradio Interface
The Gradio interface allows users to upload two images and view the results of circle detection and row/column detection.

# Example Output
The output will display:

Number of circles detected in the first image.
Processed image with detected circles.
Number of rows detected, total cylinders calculated in the second image.
Processed image with detected rows and columns.
# Conclusion
This script provides an easy way to detect circles and rows/columns in images using OpenCV and Gradio. By running the script in a Google Colab notebook, you can quickly get a Gradio interface link to interact with the detection results.
