# YOLOv8-Train-on-Custom-Datasets
## Installation of Modules
YOLOv8 released a package named “ultralytics”, that you can install with the mentioned command below.
## pip install ultralytics
The above command will install all the packages that are required to use YOLOv8 for detection and training on your own data.

## Creation of Config Files

Creating a custom configuration file can be a helpful way to organize and store all of the important parameters for your computer vision model.

Create a file having the filename “custom. yaml”, inside the current directory where you have opened a terminal/(command prompt). Paste the below code in that file. set the correct path of the dataset folder, change the classes and their names, then save it.

path:  (dataset directory path)
train: (Complete path to dataset train folder)
test: (Complete path to dataset test folder) 
valid: (Complete path to dataset valid folder)

### Classes
nc: 5# replace according to your number of classes

### classes names
replace all class names list with your classes names
names: ['person', 'bicycle', 'car', 'motorcycle', 'airplane']

## Start Training

Once you’ve completed the preprocessing steps, such as data collection, data labeling, data splitting, and creating a custom configuration file, you can start training YOLOv8 on custom data by using mentioned command below in the terminal/(command prompt).

## yolo task=detect mode=train model=yolov8n.pt data=custom.yaml epochs=3 imgsz=640
