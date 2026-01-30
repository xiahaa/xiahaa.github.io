---
title: RS_IEKF
summary: Parameter estimation using IEKF for Rolling Shutter camera and IMU calibration.
tags:
  - Computer Vision
  - Sensor Fusion
  - SLAM
  - Kalman Filter
date: '2020-10-01T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Multistate Constrained Invariant Kalman Filter illustration
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/xiahaa/RS_IEKF
url_code: 'https://github.com/xiahaa/RS_IEKF'
url_pdf: 'https://github.com/xiahaa/RS_IEKF/blob/master/Jacobian-derivation.pdf'
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

## Overview

RS_IEKF is a MATLAB implementation for parameter estimation using Invariant Extended Kalman Filter (IEKF) for Rolling Shutter (RS) camera and IMU calibration. This project implements the multistate constrained invariant Kalman filter for accurate camera-gyroscope calibration.

![Filter Architecture](https://raw.githubusercontent.com/xiahaa/RS_IEKF/master/figs/filter2.png)

## Key Features

- **IEKF-based Parameter Estimation**: Robust estimation of camera-IMU extrinsic parameters
- **Rolling Shutter Camera Support**: Handles rolling shutter effects in modern cameras
- **Multi-dataset Validation**: Tested on multiple public datasets with excellent results
- **Complete Implementation**: Includes source code, datasets, and documentation

## Technical Details

The filter estimates several critical parameters:
- **tr**: Readout time
- **td**: Time delay between camera and gyroscope
- **wd**: Gyroscope bias
- **Ric**: Rotation matrix between camera and IMU

## Results

The implementation has been validated on public datasets with high accuracy:

### RCCar Dataset
- Estimated readout time: 0.0294 s (Reference: 0.0316734 s)
- Time delay: 5.2006 s (Reference: 5.20867 s)

### Rotation Dataset
- Estimated readout time: 0.0315 s (Reference: 0.0316734 s)
- Time delay: 2.8005 s (Reference: 2.83819 s)

### Walk Dataset
- Estimated readout time: 0.0309 s (Reference: 0.0316734 s)
- Time delay: 3.3904 s (Reference: 3.38581 s)

## Source Code

The `src` folder contains all MATLAB source code for the filter implementation. The main entry point is `main.m` where you can configure the filter type through `config.m`.

## Dependencies

The project uses datasets from:
- [Camera-Gyroscope Calibration Dataset](http://users.ece.utexas.edu/~bevans/projects/dsc/software/calibration/)
- Public datasets from Ovrén & Forssén's gyroscope-based video stabilization work

## Citation

If you use this code, please cite:

> Hu, X., Olesen, D. and Knudsen, P., 2020, October. Multistate Constrained Invariant Kalman Filter For Rolling Shutter Camera And Imu Calibration. In 2020 IEEE International Conference on Image Processing (ICIP) (pp. 56-60). IEEE. [DOI: 10.1109/ICIP40778.2020.9191166](https://doi.org/10.1109/ICIP40778.2020.9191166)

**BibTeX:**
```
@inproceedings{hu2020multistate,
  title={Multistate Constrained Invariant Kalman Filter For Rolling Shutter Camera And Imu Calibration},
  author={Hu, Xiao and Olesen, Daniel and Knudsen, Per},
  booktitle={2020 IEEE International Conference on Image Processing (ICIP)},
  pages={56--60},
  year={2020},
  organization={IEEE},
  doi={10.1109/ICIP40778.2020.9191166}
}
```
