# QuoraQuestionPair
Kaggle Quora Question Pair Competition

“The goal of this competition is to predict whether a pair of questions are semantically same or not."
	
	Environment:
  
•	numpy 
•	tensorflow 
•	keras
•	pandas
•	python 3.6
•	jupyter notebook

	The Datset was fetched from Kaggle only.
	The Stanford’s GloVe pre-trained word vector ‘glove.840B.300d.txt’ was used for pre-processing
	The code is written in python and was run on Jupyter Notebook. I have used Keras (With Tensorflow as Backend) to build network model.
	The code was run on Kaggle Kernel itself.
	The model was trained with 90% dataset and validated with 10% of dataset.
	I trained the model for 15 epochs.It took about 4hrs to train on Kaggle Kernel.
	The accuracy on validation set was 87.01%

Model's Architecture :


This LSTM based model, takes a pair of question (P and Q) as input and output a probability(y) 	indicating duplicacy.Every pair of question is embedded using Stanford’s Glove pretrained 	vectors. The embedded vectors of each question is fed to individual LSTM network. The 	two representation output from the LSTM is used to calculate two important features. One is 	the distance which is the sum of squared difference between the two representation vectors 	and other is the angle between two vectors which is element wise multiplication of vectors. 	The output of these two features (distance and angle) are concatenated and passes through two 	dense layers (Fully connected layers) with sigmoid activation function. The model is 	trained by minimizing log loss.

![](https://preview.ibb.co/cZoXzx/dia.jpg)

