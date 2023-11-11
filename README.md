# Object-Tracking-DeepSORT-YOLO-v3
## Introduction
This repository contains code and datasets for a basic evaluation of object tracking with the DeepSORT tracker. It was utilized for assessing the performance of the DeepSORT tracker in conjunction with a YOLOv3 implementation, for vision applications in autonomous vehicles.
> Note: Majority of this code is borrowed from the original DeepSORT github repository. `DeepSORT_Tracking` was created for educational purposes to learn about DeepSORT and evaluate its performance. Please take a look at the [original repository](https://github.com/nwojke/deep_sort).

## Repo Structure
```
├── DeepSORT_Tracking.ipynb
├── mars-small128.pb
├── testing
│   ├── challenge.mp4
│   ├── challenge_video.mp4
│   ├── harder_challenge_video.mp4
│   ├── project_video.mp4
│   ├── solidWhiteRight.mp4
│   └── solidYellowLeft.mp4
└── yolov3.weights

```
- `testing` is the directory contains the various video files on which tracking evaluation can be done.
- `yolov3.weights` is the file containing the weigths used by the YOLO-v3 for object detection.
- `mars-small128.pb` is the file containing the weights used by the DeepSORT algorithm for tracking and inferencing.
- `DeepSORT_Tracking` is a Jupyter Notebook containing the code and documentation related to performing object tracking tasks on the provided dataset.

## Dependencies
Install all of the following libraries. 
```py
import struct
import numpy as np
import colorsys
from keras.layers import Conv2D
from keras.layers import Input
from keras.layers import BatchNormalization
from keras.layers import LeakyReLU
from keras.layers import ZeroPadding2D
from keras.layers import UpSampling2D
from keras.layers import add, concatenate
from keras.models import Model
```

## Results
![Screencast from 2023-11-11 12-54-36.webm](https://github.com/dawn-mathew/Object-Tracking-DeepSORT-YOLO-v3/assets/150279674/4c8df4a9-105f-4ab4-b214-13a8f6b0c5bf)

![Screencast from 2023-11-11 13-02-28.webm](https://github.com/dawn-mathew/Object-Tracking-DeepSORT-YOLO-v3/assets/150279674/5af96e1c-a767-4162-b274-7bf77e7774a2)

![Screencast from 2023-11-11 13-05-37.webm](https://github.com/dawn-mathew/Object-Tracking-DeepSORT-YOLO-v3/assets/150279674/b73386bf-0642-4420-969a-2ae7f1a35f0e)
- The obtained results, while promising, exhibit areas for improvement. The tracking performance can be described as average, with instances of undetected targets and occasional tracking errors, which may impact overall accuracy. To enhance the tracking capabilities, future improvements could focus on refining object detection, optimizing hyperparameters, and exploring more advanced filtering and data association techniques. These refinements have the potential to elevate the system's accuracy and mitigate the issues observed during evaluation.

