# Machine-vision-test-challenge
This is a repository for the Machine Vision Test Challenge provided by Formulatrix to provide an automatic vision-based inspection solution. To overcome the problems faced by Fermentic Inc., I propose a solution for an object detection program that can distinguish between good and bad tips. Good tips with perfect tips can be considered premium quality, while bad tips, which are still usable, are considered to be of economy standard.

To differentiate between bad tips and good tips, I have manually labeled the images myself. The bad tips and good tips are distinguishable, as shown in the example below.

![Diagram Tanpa Judul drawio (31)](https://user-images.githubusercontent.com/99520100/224526359-99d86f8c-33ab-4118-a960-2d2801fa35bb.png)


## Data Preparation (Augmentation)
To achieve optimal accuracy results, the object detection model requires a large amount of training data to improve its accuracy. With only 24 datasets provided by the challenge, additional datasets are needed.

Image augmentation is a process of increasing the size of a dataset by performing operations such as rotation, flipping, and shifting of images without changing the key information present in the image. Augmentation is a common technique used in image processing to create additional training data to improve the accuracy of a machine learning model. In this project, we will be using augmentation to increase the size of the test set provided by the challenge. Each image in the test set will be augmented 11 times to generate additional data and enhance the accuracy of the object detection model.

![Diagram Tanpa Judul drawio (30)](https://user-images.githubusercontent.com/99520100/224467330-2b61fcaf-8456-4a9d-b87d-8a7762e330eb.png)

## Label images(Bounding Box)
Labeling bounding boxes is an essential step in object detection. The process of labeling bounding boxes helps the model learn to identify objects of interest and their location in the image.

The platform used to perform bounding box labeling is [makesense.ai](https://www.makesense.ai/). This platform provides an intuitive interface that allows users to draw bounding boxes around objects in an image and assign labels to them. 

## Training model(Yolo v8)
The purpose of object detection model training is to create a model that is able to recognize objects in images and place bounding boxes around them. This is done by teaching the model to recognize specific patterns and features of the objects to be detected.

[Yolo v8](https://github.com/ultralytics/ultralytics) is one of the deep learning models used for object detection. This model uses a convolutional neural network (CNN) architecture designed specifically for fast and accurate object recognition in images. Yolo v8 is capable of real-time object detection with high accuracy, making it ideal for applications that require fast and accurate object detection.

## Performance
**Confussuion Matrix ** 
![image](https://user-images.githubusercontent.com/99520100/224525872-f24b9412-aeed-4754-a08a-d5b07236a17e.png)

**Validation Label** BEFORE

![image](https://user-images.githubusercontent.com/99520100/224525897-39022514-8fa5-4956-9eab-c6b54ba23dba.png)

**Validation Predictions** AFTER
![image](https://user-images.githubusercontent.com/99520100/224525923-ca6dbbee-6d53-4012-b892-49cd1399fdfe.png)

## Predictions
**NOT GO PREDICTIONS**
This model can predictt Corrupted images (NOT GO)
![image](https://user-images.githubusercontent.com/99520100/224526074-9d4be470-1716-4f8e-be7c-85d382f77fca.png)

**BAD TIP PREDICTION**
Perfectly detect a bad tip
![image](https://user-images.githubusercontent.com/99520100/224526080-c9645b48-fba0-41b5-9471-d66b77e14875.png)

**GOOD TIP PREDICTIONS**
This model can detetct a good tip
![image](https://user-images.githubusercontent.com/99520100/224526248-ff66899c-0d6b-43fe-b2e9-6ba4f4d36273.png)




