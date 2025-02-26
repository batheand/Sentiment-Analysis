# Sentiment-Analysis
A model where you give a text input and the model outputs the emotion presented in the text.

- For the dataset we use the sentiment 140 dataset which has tweets mapped with sentiments Negative, Neutral and Positive. We will only use Negative and Positive for our models. 
- For the model we'll, at core, use a bidirectional LSTM. Which will traverse through the tokens from the start to the end then from the end to the start to make sense of it.
- The standard model has been trained with 20 epochs and to 85% accuracy, I believe 10-20 is good if you wish to change the model up and retrain.
  
# How to Run?
You can run the Jupyter notebook, skip training if you wish to (there's a pre trained model in the repository for that case!), and finally experiment with your own sentences in the testing module.

# How to proceed and Improve?
Note: the raw output of the model is between 0 (negative) and 1 (positive) and we determine the result by looking at whichever is the closest. The dataset is arranged so that the negative texts have 0 weighting and the positive texts have 1.

After testing on it myself, I developed the Positive-Negative index (the raw output of the model*100) which often is able to give even more information. The texts have spectrums of sentiments, two texts can be negative and one can be drastically more negative (e.g.: I did't enjoy the drink vs I hated everything about this meal). 

Therefore, for future development, maybe we can lean more into improving the index by adding the neutral data as well with with 0.5 weighting, so that it captures the qualities of neutrality as well. 
