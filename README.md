## Overview

This project detects facial keypoints and let's you overlay snapchat style filters to it.
Facial Keypoint Detection             |  Filter Overlay
:-------------------------:|:-------------------------:
![Facial Keypoint Detection](./images/facial_keypoint_test.gif)  |  ![Snapchat Style Overlay](./images/mr_sunglasses.gif)

## Setup

For better and faster results, GPU support is required. CPU should work fine as well.

1. Clone the repository, and navigate to the downloaded folder.
```
git clone https://github.com/ysharc/Facial-Keypoint-Detector.git
cd Facial-Keypoint-Detector
```

2. Create (and activate) a new environment with Python 3.6 and the `numpy` package.

	- __Linux__ or __Mac__: 
	```
	conda create --name FKD-App python=3.6 numpy
	source activate FKD-App
	```
	- __Windows__: 
	```
	conda create --name FKD-App python=3.6 numpy scipy
	activate FKD-App
	```

3. Install/Update TensorFlow (for this project, you may use CPU only).
	- Option 1: __To install TensorFlow with GPU support__, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system.
	```
	pip install tensorflow-gpu==1.3.0
	```
	- Option 2: __To install TensorFlow with CPU support only__:
	```
	pip install tensorflow==1.3.0
	```

4. Install/Update Keras.
 ```
pip install keras -U
```

5. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.
	- __Linux__ or __Mac__: 
	```
	KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```
	- __Windows__: 
	```
	set KERAS_BACKEND=tensorflow
	python -c "from keras import backend"
	```

6. Install a few required pip packages (including OpenCV).
```
pip install -r requirements.txt
```

## Data

All of the data you'll need to train a neural network is in the AIND-CV-FacialKeypoints repo, in the subdirectory `data`. In this folder are a zipped training and test set of data.

1. Navigate to the data directory
```
cd data
```

2. Unzip the training and test data (in that same location). If you are in Windows, you can download this data and unzip it by double-clicking the zipped files. In Linux/Mac, you can use the terminal commands below.
```
unzip training.zip
unzip test.zip
```

You should be left with two `.csv` files of the same name. You may delete the zipped files.

*Troubleshooting*: If you are having trouble unzipping this data, you can download that same training and test data on [Kaggle](https://www.kaggle.com/c/facial-keypoints-detection/data).

Now, with that data unzipped, you should have everything you need!

## Quick Start

- If you're interested in knowing the whole process, then run the interactive jupyter notebook and follow the instructions.

```
jupyter notebook CV_project.ipynb
```

- Web app [coming soon!]