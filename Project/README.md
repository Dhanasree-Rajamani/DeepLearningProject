# Object-Detection-Web-App-Using-YOLOv7-and-Flask



## Description

This project utilizes the YOLOv7 deep learning model for object detection. The YOLOv7 model is trained on a custom dataset using the Grocessory dataset, labeled using Roboflow. The trained model is then used to perform object detection on test images and videos. Additionally, a Flask application has been developed to facilitate uploading images and videos for real-time detection.

## Features
- Object detection using the YOLOv7 model
- Training on a custom dataset
- Integration with Roboflow for labeling
- Real-time detection in a Flask application
- Support for image and video uploads
- Compare the object detection accuracy when using a pretrained YOLOv7 model vs. using our custom dataset trained model
- Gradio UI for user to Input the Search Item and obtain object detection Output(for pretrained and custom model) 
- Web UI using flask to perform object detection(for custom model)

## Installation
- Clone the Repository: git clone https://github.com/username/YOLOv7.git
`cd YOLOv7`
- Set Image Paths: Edit the YAML file (data.yaml) to specify the paths of your train and test images.
- Training: Train the YOLOv7 model with the custom dataset using the following command:
`python train.py --img 640 --batch 16 --epochs 50 --data data.yaml --weights yolov7x.pt --cache`
Monitor the training progress and adjust the parameters as needed.

## Object Detection
- Once training is complete, locate the best weights file (best.pt) in the runs/exp/ directory.
- Since the weights file is too big to push to git. I have copied it to drive. Please find link here:
`https://drive.google.com/file/d/1TeOIEfY2de_mEEObZjReO9VIcOt0ilVA/view?usp=sharing`
- Use the best weights to perform object detection on a test image using the following command:
`python detect.py --weights runs/train/exp/weights/best.pt --img 640 --conf 0.25 --source test.jpg`

## Flask Application
- Set up a virtual environment and install the necessary dependencies:
`virtualenv env` \
`source env/bin/activate` \
`pip install -r requirements.txt`
- Run the Flask application:
`python webapp.py`
- Access the application in a web browser at http://localhost:5000 and upload images or videos for object detection.

Steps to use:

1- Setup the environment to run yolov7 and flask.

2- Clone this github repo.

3- Paste your custom model in the cloned repo.

4- Run :  python webapp.py

5- Open 127.0.0.1:5000

<img width="368" alt="image" src="https://github.com/SravaniThota96/DeepLearning/assets/111466561/6c48e38c-8291-4c33-a8de-b4d5ced8a03a">


6- Upload Image or video to test.

![image3](https://github.com/SravaniThota96/DeepLearning/assets/111466561/3fc38386-afd1-4e86-a01b-7663ec62ef56)

![image6](https://github.com/SravaniThota96/DeepLearning/assets/111466561/17fc7359-865e-4464-8c38-ab0dcf0aa42a)

![image8](https://github.com/SravaniThota96/DeepLearning/assets/111466561/34d016b3-1717-4c6f-9895-bc04df282e8f)


## Gradio UI

Gradio UI has been developed for the custom trained YOLOv7 model and Pretrained YOLOv7 model. The custom trained model was able to identify and label more items(such as meat, cheese, yogurt etc.) than the pretrained model.

Snapshots of the application : 

Custom trained model :

![ss4](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss9.png)

![ss5](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss10.png)

![ss7](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss13.png)

![ss8](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/SS8.png)

Pretrained Model : 

![ss1](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss2.png)

![ss2](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss4.png)

![[ss6](https://github.com/Dhanasree-Rajamani/DeepLearningProject/blob/main/Project/images_ds/ss12.png)

