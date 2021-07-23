# Roadkill-Avoidance-using-YOLOv5
A Roadkill Avoidance Framework using YOLOv5 and Custom Dataset.  

[This documentation is about an upcoming research-work publication, the custom-data for which will be released soon.]

Millions of animals are killed on roads everyday, all due to collisions/crashes with vehicles. And the situation becomes worrisome as most animal species toggle to endangered mode. Although autonomous vehicles hold out hope for animals on roads, how well can they be trusted when it comes to the lives of endangered beings? There have been instances where even the best-in-the-field of [self driving cars have been confused.](https://www.indiatimes.com/technology/news/autonomous-cars-can-handle-reckless-drivers-but-not-hopping-kangaroos-325092.html)  

Often object detection is used for detecting animals on the road but do we care to check if the data that we are training our object detection model on, is well grounded, valid and justifiable enough? Rarely. 

### What are some of the problems that autonomous vehicles face when it comes to animal detection on road?

1. Lack of open source 'animals-on-road-and along-roadside' data to train the model on.
2. Invalid and inaccurate image data used for training purposes due to (1).
3. Training on complex, heavy (and rather slow) deep learning architectures with lower *detection processing speed*. 

### Through this project we try to overcome the above mentioned drawbacks by proposing a well annotated custom dataset and a fully trained YOLOv5 model.

The flow for the project is as depicted in the block diagram below.

Image data Acquisition → Data pre-processing → Data Augmentation → Data Annotation → Training on YOLOv5

![image](https://user-images.githubusercontent.com/69042198/126728965-23f767d2-9070-48d0-9ed2-801f9eb01643.png)

As already mentioned, Image Data is instrumental in building the framework, we have crafted the image dataset pipeline such that no detail is missed out. 

1. First Data Analysis is done based on published road ecology surveys across continents. Thus, we reach a conclusion of selecting 20 most common animal classes that are prone to road-kills in most of the continents.
2. Based on (1) data acquisition is done in two parts:  
a. Self captured Images  
b. Internet sourced public images
3. Data Preprocessing 
4. Data Augmentation
5. Data Annotation.

![image](https://user-images.githubusercontent.com/69042198/126728977-2415f2fc-996b-45b4-853b-2119f2c408cd.png)

Further, this completely annotated dataset is fed to the two-stage YOLOv5 detector. 

The repo for original Yolov5 architecture→ [https://github.com/ultralytics/yolov5](https://github.com/ultralytics/yolov5)

## RESULTS
![image](https://user-images.githubusercontent.com/69042198/126729062-7376d576-9911-4c65-b32a-f2556589c30e.png) ![image](https://user-images.githubusercontent.com/69042198/126729078-2e4981a3-e1b7-4a34-97ca-473514fb51a4.png)  
![image](https://user-images.githubusercontent.com/69042198/126729084-ddb92ebb-db7d-427a-ac64-c3c5db7f1525.png)

## Performance Metrics
![image](https://user-images.githubusercontent.com/69042198/126729126-0df98ab3-b4bb-4e44-b4bd-748c2d906873.png)  ![image](https://user-images.githubusercontent.com/69042198/126729136-db6f2f44-d022-4157-aa79-74d30b1d1993.png) ![image](https://user-images.githubusercontent.com/69042198/126729138-206d041a-a4f7-406e-a831-3d1e842d3a4c.png)


