# How to Annotate Keypoints Using Roboflow

### Intro

Object detection is a powerful tool in hands of computer vision engineer.

However, object detection models, like Yolo5, can just identify the coordinates of the bounding box of an object, but they can't provide any information about object's orientation in space.

Such information can be provided by coordinates of the object's keypoints.

I was interested to get to know how to trainin a keypoint detection model, Keypoint RCNN, on a custom dataset. For that, I needed to create a simple dataset with objects related to one class, where each object was annotated with 2 keypoints, which would be enough to identify its orientation in space.

Glue tube was the ideal candidate to become such object. So, I've made 134 photos and annotated them in [Roboflow](https://roboflow.com/).

Roboflow doesn't provide keypoint annotation functionality, but this task can be easily done by annotating keypoints with small rectangles.

With help of a custom script, we can convert these annotations

![](https://miro.medium.com/max/2000/1*fj_k-Fy8xlILZT5a1z_GnA.png)

into these annotations

![](https://miro.medium.com/max/3600/1*kGvS_5DgueggsDkGfm1PBA.png)

Tutorial on how to make rectangle annontations in Roboflow and convert them into keypoints is [here](https://medium.com/@alexppppp/how-to-annotate-keypoints-using-roboflow-9bc2aa8915cd)

Tutorial on how to train a custom keypoint detection model is [here](https://medium.com/@alexppppp/how-to-train-a-custom-keypoint-detection-model-with-pytorch-d9af90e111da)

---

### Detailed explanation

https://medium.com/@alexppppp/how-to-annotate-keypoints-using-roboflow-9bc2aa8915cd  

---

### Important!

This repository contains two folders.

[glue_tubes](glue_tubes) is a folder with the original dataset (only images). This dataset should be labeled in Roboflow. To save your time, you don't need to label this dataset by yourself. It's already labeled and is placed in [Glue Tubes Keypoints Project.v1-version-1.yolov5pytorch](Glue%20Tubes%20Keypoints%20Project.v1-version-1.yolov5pytorch) folder.

[Glue Tubes Keypoints Project.v1-version-1.yolov5pytorch](Glue%20Tubes%20Keypoints%20Project.v1-version-1.yolov5pytorch) is a folder with Roboflow-labeled dataset (images and txt-files with coordinates of rectangles). Rectangle labels in txt-files are ready to be transformed into keypoints and bounding boxes.
