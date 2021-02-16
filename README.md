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

```
Object Detection 
    │─── Data
         |───000000_10.png
         |───000001_10.png
         |─── ...
    │─── test.csv
    │─── train.csv
```

The structure of .csv: 

| filename | xmin | ymin | xmax | ymax | class_id |
| -------- | -------- | -------- | -------- | -------- | -------- |
| 00072.jpg     | 148     | 53     | 159     | 63     | 4     |

In object detection task, we have 6 traffic signs (6 classes): Turn left, Turn Right, Straight, Stop, No Turn Left, No Turn Right. 

![](https://i.imgur.com/jrmCOEW.png)

#### Semantic segmentation

Setup sementation data folders

```
Segmentation
    │─── GGDataSet
         |─── train_frames
             |─── train
                 |─── train_0000001.png
         |─── train_masks
             |─── train
                 |─── train_0000001.png         
         |─── val_frames
             |─── val
                 |─── val_0000001.png         
         |─── val_masks
             |─── val
                 |─── val_0000001.png         
         |─── label_colors.txt
    │─── model_pb
    │─── models
    │─── train.py
    │─── convert_pb.py
```

VIA segmentation dataset has 6,240 training images, 1,448 validation images. In our task, we have to predict 3 classes: Background, Line, Road. 
The label_colors.txt contains RGB color code of classes and we handle it to convert classes into one-hot vector. 

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

