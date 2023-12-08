# Rooftop Counting System using Satellite Images

This repository contains code for a rooftop counting system that utilizes satellite images to accurately estimate the number of rooftops in a given area. The system employs a combination of image processing techniques and machine learning algorithms to achieve precise results.

## Getting the Images

To obtain the necessary images for training and testing, QGIS (Geographic Information System) is used in conjunction with Google satellite maps. The marking of each rooftop is done by placing dots on a separate layer positioned above the satellite map. 

## Image Export

Once the rooftops are marked, the system exports the satellite images with the following specifications:
- Scale: 1:2500
- Resolution: 96 dpi
- Width x Height: 1056 px x 816 px
   

## Dots Extraction and Density Map Generation

The exported images with marked dots are processed using Python code. The code (01_create_cssv) extracts the dots' coordinates from each dbf files and saves them in csv format. These CSV files are then utilized to replot the dots onto new images. The system employs a K-Tree algorithm to generate a density map based on the replotting of the dots. These density maps serve as the ground truth for the system.

## CSRNet Integration

After generating the density maps, the system follows the CSRNet code. CSRNet (Convolutional Social Pooling) is a powerful crowd counting model that has been adapted for rooftop counting in this project. By integrating the CSRNet code, the system performs further analysis and processing on the density maps to accurately estimate the number of rooftops in the given area.

With this repository, you can explore the code, replicate the system's functionality, and adapt it to your own projects involving rooftop counting from satellite images. The clear instructions and provided dataset make it easier to understand and implement the system.

**Note:** Proper attribution and acknowledgment of the original CSRNet code are included in this repository.

We welcome contributions, bug reports, and feature requests. Feel free to open issues or submit pull requests to help enhance the system.

Get started with rooftop counting using satellite images today!
