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

### How to use VIA Dataset

#### Object detection

In VIA experiment, we implement Single Shot Detection (SSD). You do not need to follow our instructions if you want to handle the data for only your purposes.

1. Upload **VIA Dataset** to Google Drive
2. Upload **object_detection.ipynb** to Google Colab 
3. Modify your dataset locate path in Google Drive and your dataset path link to images and .csv files.

You can run notebook in local with requirements: Keras version 2.2.4, Tensorflow version 1.15 and git clone this repository: 

``` git clone https://github.com/pierluigiferrari/ssd_keras ```

### How to implement into your custom dataset

1. Label
2. Use labeled dataset in internet

Website: https://via.makerviet.org/

