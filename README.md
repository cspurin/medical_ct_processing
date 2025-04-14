# Medical CT image processing 

A Python library for processing and analyzing DICOM images of rock samples in CT scans.

## Overview

This library provides tools for loading, processing, and analyzing DICOM images, with specific functionality for centering rock samples in CT scan data. It enables automated processing of scan sequences with features for:

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
