# VIA Dataset

The repository contains:

* Procedures to use VIA Dataset with two tasks: Object detection and semantic segmentation.
* How to implement into your custom dataset.

### Download datasets

* [Object detection](https://drive.google.com/file/d/1NGrKWHc1z_4bOh2huWHC8kZsUZFXOku-/view)
* [Semantic segmentation](https://drive.google.com/file/d/1EKA7VGdKjevT855ycYW0BOaI8u0r2Sa_/view)

### Documentation

#### Object detection
Object detection folder contains: dataset folder, two files .csv (test.csv, train.csv). The train.csv has 12,764 images and the test.csv has 2561 images. 

The structure of .csv: 

| filename | xmin | ymin | xmax | ymax | class_id |
| -------- | -------- | -------- | -------- | -------- | -------- |
| 00072.jpg     | 148     | 53     | 159     | 63     | 4     |

In object detection task, we have 6 traffic signs (6 classes): Turn left, Turn Right, Straight, Stop, No Turn Left, No Turn Right. 

![](https://i.imgur.com/jrmCOEW.png)

#### Semantic segmentation


Website: https://via.makerviet.org/

