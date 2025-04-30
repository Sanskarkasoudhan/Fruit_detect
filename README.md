Fruit Detection and Classification
This project combines CNN-based fruit classification with YOLOv4 object detection to identify and locate fruits in images.
Installation
bashgit clone https://github.com/AlexeyAB/darknet.git
wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights
pip install opencv-python tensorflow numpy matplotlib pandas scikit-learn
Dataset Structure
Fruit-Images-Dataset/
├── Training/  # 300 images per class
├── Test/      # 50 images per class
└── test-multiple_fruits/
Features

CNN Classification: 131 fruit classes, 100x100px input, 3 conv blocks + 3 dense layers
YOLOv4 Detection: 608x608px input, confidence threshold 0.5, NMS threshold 0.4

Known Issues

Test data assignment bug: X_test = np.array(X_train) instead of X_test = np.array(X_test)
Duplicate model definition in code
Generic object labels in YOLO detection output

Usage
Run the script to load data, train the CNN model, and perform object detection on test images.
