# Computer_Graphics_Lab
Computer Graphics lab project 

#####FIrst of all i have summarized some projects to see how Ai and deep learning works and what approach should i take########

1 - AITrainer_NOTES:
	About The Project:
		Simple AI trainer app using OpenCV Python and MediaPipe Python,
		It detects exercising-pose, which is given realtime, and counts prope" reps.
	About The Data:
		Getting landmarks on the body using MediaPipe: Pose Estimation, Depending on the exercise chosen,
		 it calculates the angles between joints which actually matter ,It only counts "proper" reps, by checking the range of important angle.

	About the model training:
		it is so simple the programmer used MediaPipe.
	**MediaPipe offers cross-platform, customizable ML solutions for live and streaming media.**

	LINK: https://google.github.io/mediapipe/

2 - Exermote_NOTES:
	About the project:
		Exermote is a fitness app prototype, which is capable to detect Burpees, Squats and Situps and to count related repetitions.
		The exercise recognition is done with Convolutional LSTM Neural Networks.

	About The Data:
		To recorde the data the programmer has used 2 different types of devices:
		- Iphone on right upper arm: 12 data features (3x gravity, 3x acceleration, 3x euler angle, 3x rotation rate).
		- 6x Estimote Nearables on chest, belly, hands and feet: each 4 data features (3x acceleration, 1x rssi)

		The Recording frequency was 10 Hz for the reason that Nearable send frequency is limited to this value on hardware side.

	About the model training:
		The Programmer used DeepConvLSTM Neural Networks that were already tested by Francisco Javier Ordóñez and Daniel Roggen for recognizing activities of daily living.
		The model takes time sequences of raw sensor data and outputs the according exercise label.
		About the training:
			The whole training procedure took place in the google cloud, The machine learning framework in use was Keras with TensorFlow as backend.


3 - PushUP_COunter_notes:
	About the Project:
		project aims to build a deep learning solution to count the repetitions of exercises such as push ups or pull ups. 
		A model that can run on phones and that is possible to train with only a few hundred images.

	About The Data:
		the data was constructed from several videos,The videos were processed with the optical flow algorithm. This algorithm allowed to construct
 		a new video with a few colours representing the movement of the subjects in the videos.data
		 was constructed from several videos removed from youtube and some home-made videos.
		The videos were processed with the optical flow algorithm. 
		This algorithm allowed to construct a new video with a few colours representing the movement of the subjects in the videos.

	About the model training:
		The model used was a small convolutional neural network built in Keras. the goal of the model was from the input frames, predict if the subject was moving down, up or not moving.
		**Movement of the subject was analysed frame by frame. And what was considered as a repetition was a change of state**
	

