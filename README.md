# Medical CT image processing 

The code to use is the pressure integration jupyter notebook. This has the automated centering script. The other files are for manual selection of centering parameters. 

A Python library for processing and analyzing DICOM images of rock samples in CT scans.

## Overview

This library provides tools for loading, processing, and analyzing DICOM images, with specific functionality for rock samples in CT scan data. It enables automated processing of scan sequences with features for:

- Directory navigation and file management
- DICOM file reading with metadata extraction
- Rock sample centering and mask application
- Multi-scan averaging and CT number calculations
- Time-sequence analysis

## Features

- **Folder and File Management**: Automatically locate and process experiment folders
- **DICOM Reading**: Extract image data and acquisition timestamps from DICOM files
- **Sample Centering**: Apply automatic centering correction to rock samples
- **Batch Processing**: Process multiple scans with consistent parameters
- **Statistical Analysis**: Calculate CT numbers and other metrics from processed images
- **Time Series Support**: Track changes across time-sequenced scans
## Usage 

The user must provide the file path for their experiments. Then the user must define the input parameters. As an example: 
input_parameters = {
    'CT_water': 0,
    'CT_air': -1000,
    'coarse': 8,
    'rockin': 10,
    'rockout': 162,
    'num_slices': 166,
    'Slicethick': 0.625,
    'Voxsize': 0.1875,
    'cr': 105
}

The script requires the seperate folders for the images where the rock is fully saturated with air, where the rock is fully saturated with water, and the flow experiments you are analyzing. 
It creates 3D maps: 
![image](https://github.com/user-attachments/assets/0297f093-41bd-4919-a84e-b293181622f8)

You can control how many scans you average over for the analysis and how many voxels you average to improve the signal to noise ratio. 


Some examples of this are in the following paper: 
The role of injection method on residual trapping: Insights into bridging
scales and heterogeneity
https://doi.org/10.1016/j.advwatres.2025.104913
