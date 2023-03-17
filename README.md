# Project_Real_Time_Hand_Gesture_Detection_using_YOLOV5


# Object-Detection-using-Yolov5

# Yolov5 Custom Dataset Training Dataset Creation

capture images for custom dataset training.(size and resolution of the image dosent matter)
run to capture images capture_image.py

# Labelling the images 

use labelImg tool in python to label images 

# Dataset Preparation

* prepare dataset 
* divide in test , train and val and data.yaml file
* each test and train will contain images and label.
* for training we need 80% of images we collected and for validation the remaining 20% image needed ( train=80% and validation=20% ).
* copy 80% of images from dataset to train folder in location dataset\images\train
* copy corresponding yolo file of the image used for train to location dataset\labels\train
* copy remaining images from dataset to validation folder in location dataset\images\val
* copy corresponding yolo file of the image used for validation to location dataset\labels\val

# Yaml file editing

* open the folder data in yolov5\data and open custom_dataset.yaml in notpad.
* change the value of nc to the no of classes present in our dataset
* replace the classnames with our class names
* save the file

# Yolov5 training and detecting

* open command prompt in folder yolov5 then type "pip install -r requirements.txt" for installing requirement for yolov5
* cd yolov5
* python run.py
* for training open command prompt in folder yolov5 then type "python train.py --img416  --batch 16 --epochs 300 --data custom_dataset.yaml --weights yolov5s.pt --cache"
* after training it will create weight in folder yolov5/runs/train/exp/weights/best.pt
* for detecting images copy some images for testing in folder yolov5\data\images
* open command prompt in folder yolov5 then type "python detect.py --weights best.pt --img 416 --conf 0.5 --source 0t"
* after completing detection it gives results in folder yolov5/runs/detect


# download and install python

* create a folder in our local disk
* open newely created folder in command prompt
* type "python -m venv virtual_environment_name" in the place of virtual_environment_name we can give our own virtual environment name by replacing it
* type "virtual_environment_name\Scripts\activate" for activating the virtual environment
* type "deactivate" for deactivating virtual environment



# References

python : https://www.python.org/downloads/
labelImg : https://github.com/tzutalin/labelImg
yolov5 : https://github.com/ultralytics/yolov5
https://github.com/ultralytics/yolov5
https://github.com/roboflow-ai

# Thanks for Reading

