# The caries detection web-service using the YOLOv8 neural network

This repository contains the YOLOv8 object detection web service, that detects caries and other teeth deceases on images. Also, it contains additional scripts, that can be used to prepare the source dataset, to train the model and run test predictions.

The DentalAI dataset used to train the model. You can download it from here: https://datasetninja.com/dentalai. If you want to run your own training process, you need to convert it to the YOLOv8 format, using the script in the `convert.ipynb` notebook.

This is a source code for the [Teeth caries detection using YOLOv8 neural network](https://dev.to/andreygermanov/teeth-caries-detection-using-yolov8-neural-network-3fap). Read it to learn in detail how this code created and works.

## Contents

* `convert.ipynb` - The Supervisely to YOLOv8 converter, used to convert the dataset to YOLOv8 format
* `train.ipynb` - The code to train the YOLOv8 model using converted dataset
* `predict.ipynb` - The code, that can be used to run and visualize caries detection on custom images, using the trained model
* `best.pt` - The trained YOLOv8 model on 30 epochs to detect caries, cavity and cracks on teeth
* `object_detector.py` - The backend of a web service
* `index.html` - The frontend of a web service
* `caries.jpg` - Sample teeth with caries image

## Demo

Watch this video: https://youtu.be/OzpPIsxB_4U

## Install

* Clone this repository
* Install dependencies: **pip3 install -r requirements.txt**

## Run web service

* Ensure that the `object_detector.py`, `index.html` and `best.pt` files located in the same folder
* Run

```
python object_detector.py
```

The web interface will be available on **http://localhost:8080** address. You can upload the teeth image and see if it contains caries.
