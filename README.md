# American sign language detector using YOLOV5
This is an object detection project for detecting American sign language (ASL) alphabets using the YOLOV5 model.
## Table of Contents
- [Introduction](#introduction)
- [How to use](#how-to-use)
-  [Importance](#importance)
## Introduction
This project uses the YOLOV5 model, a popular object detection model with great speed and accuracy. Here I used the model to detect the English alphabets with American sign language.
## How-to-use
### First: Using my weights
1-Clone this repository to your local machine:

 ```shell
   git clone https://github.com/yourusername/ASL_detector.git
   ```
2-Install requirements:
 ```shell
   pip install -r requirements.txt
   ```
3-Open the notebook and only run the last line (don't forget to put the paths of required files) then your webcam opens and let the magic begin:
```shell
   !python "path of your detect.py file" --weights "path of your best.pt file aka your weights" --source 0
   ```
### Second: Using your own weights
1-Run the first block in the notebook to install requirements

2-Get your own dataset or you can use this dataset from roboflow and get the download code:
```shell
  https://public.roboflow.com/object-detection/american-sign-language-letters
```
3-Train your model in the next block:
```shell
  !python train.py --img 416 --batch 16 --epochs 150 --data {dataset.location}/data.yaml --weights yolov5s.pt --cache
```
4-Test your model in the next block but in order to use your webcam you must run this line locally:
```shell
  !python "path of your detect.py file" --weights "path of your best.pt file aka your weights" --source 0
```

## Importance
This model can be a foundational step towards the development of a comprehensive sign language recognition system for the deaf and hard-of-hearing community Also it can facilitate communication for ASL learners and instructors, making it easier to practice and teach individual letters accurately. 
