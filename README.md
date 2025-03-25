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
