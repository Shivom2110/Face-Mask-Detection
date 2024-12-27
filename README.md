# Face Mask Detection

This project aims to detect whether a person is wearing a face mask or not using a deep learning model. The project includes training a model, detecting masks in images, and detecting masks in real-time video streams.

## Project Structure

```
.DS_Store
.idea/
	.gitignore
	Face-Mask-Detection-master.iml
	inspectionProfiles/
		profiles_settings.xml
	misc.xml
	modules.xml
dataset/
	with_mask/
	without_mask/
detect_mask_video.py
face_detector/
	deploy.prototxt
	res10_300x300_ssd_iter_140000.caffemodel
FrontEnd.py
mask_detector.model
requirements.txt
train_mask_detector.py
```

## Requirements

Install the required packages using the following command:

```sh
pip install -r requirements.txt
```

## Training the Model

To train the face mask detection model, run the 

train_mask_detector.py

 script:

```sh
python train_mask_detector.py
```

This script will:
1. Load and preprocess the dataset.
2. Train a MobileNetV2 model on the dataset.
3. Save the trained model as 

mask_detector.model

.

## Detecting Masks in Video Streams

To detect masks in real-time video streams, run the 

detect_mask_video.py

 script:

```sh
python detect_mask_video.py
```

This script will:
1. Load the face detector model from 

deploy.prototxt

 and 

res10_300x300_ssd_iter_140000.caffemodel

.
2. Load the face mask detection model from 

mask_detector.model

.
3. Start the video stream and detect masks in real-time.

## Frontend

To run a simple frontend that captures video from the webcam, run the 

FrontEnd.py

 script:

```sh
python FrontEnd.py
```

## Dataset

The dataset should be organized as follows:

```
dataset/
	with_mask/
	without_mask/
```

Each folder should contain images of people with and without masks, respectively.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements

- The face detection model is based on the Single Shot MultiBox Detector (SSD) framework with a ResNet-10 architecture.
- The face mask detection model is based on the MobileNetV2 architecture.
