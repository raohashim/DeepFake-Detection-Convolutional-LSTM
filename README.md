# DeepFake-Detection-Convolutional-LSTM
This project aims to predict synthetic media generated using various techniques and distinguish them as real or fake. 

To achieve this goal, the project proposes a detection system that uses Convolutional LSTM (C-LSTM), which is an end-to-end trainable recurrent deepfake video detection system. The system is composed of a convolutional LSTM structure that processes frame sequences. 

A convolutional LSTM has two essential components that enable it to function effectively.

**1)CNN for frame feature extraction.**

**2)LSTM for temporal sequence analysis.**


##Training via Google Colaboratory Pro.

Step1. ## Dataset
	 - Download the processed dataset from 'https://seafile.idmt.fraunhofer.de/u/d/b639276d15b9423bb11f/'.

	-Some of the dataset we used are listed below:
  	- [FaceForensics++](https://github.com/ondyari/FaceForensics)
  	- [Celeb-DF](https://github.com/yuezunli/celeb-deepfakeforensics)
  	- [Deepfake Detection Challenge](https://www.kaggle.com/c/deepfake-detection-challenge/data) 

Step2. ## Preprocessing  (Use Pre-processing.ipynb file for pre-processing.)
 	 - Load the dataset
  	 - Split the video into frames
  	 - crop the face from each frame
  	 - save the face cropped video

Step3. ## Model and train (Use Model_train.ipynb file for model training.)
  	- It will load the preprocessed video and labels from a csv file.
  	- Create a pytorch model using transfer learning with RestNext50 and LSTM.
  	- Split the data into train and test data
  	- Train the model
  	- Test the model
  	- save the model in .pt file

Step4.  ## Predict   (Use Prediction.ipynb file for prediciton of unseen videos.)
  	- Load the saved pytorch model
  	- Predict the output based in trained weights.
 
