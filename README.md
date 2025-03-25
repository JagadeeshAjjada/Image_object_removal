# object-remove

A system for removing objects from images using deep learning-based image segmentation and inpainting techniques.

## Overview

Object removal from an image involves two steps: detecting and removing the object.

First, the user selects the object by drawing a box around it. Instead of removing everything inside the box, Mask-RCNN is used to create an exact mask of the object.

Next, DeepFillv2, a deep learning inpainting model, fills in the missing area using a gated convolution system.

The final result is a clean image with the object removed.

<p align ="center">
    <img src="/Test_img/Lowfidality_diagram.png" width="1000" />
    <em></em>
</p>

## Usage

The DeepFillv2 model requires pretrained weights from a PyTorch reimplementation of DeepFillv2. The model's code was taken from that repository with minor changes.

Place the .pth weights file inside the models/ folder before running the program.

```
app.py [path of image]
```

## Results
Here are some examples of the system's output. The images show the user-selected bounding box, the masked version, and the final inpainted result.

<p align ="center">
  <img src="/results/example1.png" width="1000" />
  <em></em>
</p>
<p align ="center">
  <img src="/results/example2.png" width="1000" />
  <em></em>
</p>
