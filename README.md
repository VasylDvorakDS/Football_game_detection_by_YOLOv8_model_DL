# Task

The goal of this work is to develop and train a computer vision model based on the YOLOv8 architecture for detection and classification of objects in sports images, specifically football. The model should be able to recognize several classes:

ball,

goalkeeper,

player,

referee.

For this purpose, a dataset with YOLO-format annotations was used, uploaded and prepared using the Roboflow platform. The work includes the following stages:

Loading and visualizing labeled data,

Performing inference (predictions) on test images,

Training the model with specified parameters (epochs, batch size, image size),

Validating the model with evaluation of detection quality using precision, recall, and mAP metrics.

Football dataset is available from [football_dataset]( https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc/dataset/2 )

# Conclusions

The YOLOv8 model was successfully trained and is capable of detecting objects in images with varying degrees of accuracy for each class.

The detection quality for players is high — mAP50 around 0.95, indicating reliable recognition and localization.

Goalkeepers and referees are recognized with satisfactory accuracy, but there is room for improvement.

The ball is detected the worst, with low mAP values, which may be due to an insufficient number of examples or the complexity of the object.

The processing time per image is quite fast (~27 ms), allowing the model to be used in real-time applications.

To improve ball detection quality, it is recommended to increase the amount of training data for this class and consider further training using a more balanced dataset.

The best optimizer turned out to be SGD with an average mAP50-95 metric across all classes of 0.3576.

<img width="1246" height="829" alt="изображение" src="https://github.com/user-attachments/assets/63dea645-ff9c-41db-8242-9bce91214896" />

