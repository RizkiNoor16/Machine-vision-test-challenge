# Machine-vision-test-challenge
This is a repository for the Machine Vision Test Challenge provided by Formulatrix to provide an automatic vision-based inspection solution. To overcome the problems faced by Fermentic Inc., I propose a solution for an object detection program that can distinguish between good and bad tips. Good tips with perfect tips can be considered premium quality, while bad tips, which are still usable, are considered to be of economy standard.

To differentiate between bad tips and good tips, I have manually labeled the images myself. The bad tips and good tips are distinguishable, as shown in the example below.

![Diagram Tanpa Judul drawio (29)](https://user-images.githubusercontent.com/99520100/224466378-b8bbbe31-e3ae-4142-bb18-964b4eb3f180.png)

## Data Preparation (Augmentation)
To achieve optimal accuracy results, the object detection model requires a large amount of training data to improve its accuracy. With only 24 datasets provided by the challenge, additional datasets are needed.

Image augmentation is a process of increasing the size of a dataset by performing operations such as rotation, flipping, and shifting of images without changing the key information present in the image. Augmentation is a common technique used in image processing to create additional training data to improve the accuracy of a machine learning model. In this project, we will be using augmentation to increase the size of the test set provided by the challenge. Each image in the test set will be augmented 11 times to generate additional data and enhance the accuracy of the object detection model.
