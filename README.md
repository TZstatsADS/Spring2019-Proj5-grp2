# ADS Project 5: 

Term: Spring 2019

+ Team #2
+ Projec title: Jigsaw Unintended Bias in Toxicity Classification
+ Team members
	+ Fei Zheng fz2277@columbia.edu
	+ Shengjie Sun ss5593@columbia.edu
	+ Xiaoxi Zhao xz2740@columbia.edu
	+ Zeyu Yang zy2327@columbia.edu  

Our kernel: https://www.kaggle.com/zhengfei/simple-lstm  

+ Project summary: This project is a [Kaggle competition](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification)(*Jigsaw Unintended Bias in Toxicity Classification*). First we did Exploratory Data Analysis about the comments data. And then we did the train and prediction. Below is the competition summary:  

	When the Conversation AI team first built toxicity models, they found that the models incorrectly learned to associate the names of frequently attacked identities with toxicity. Models predicted a high likelihood of toxicity for comments containing those identities (e.g. "gay"), even when those comments were not actually toxic (such as "I am a gay woman"). This happens because training data was pulled from available sources where unfortunately, certain identities are overwhelmingly referred to in offensive ways. Training a model from data with these imbalances risks simply mirroring those biases back to users. In this competition, you're challenged to build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. You'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bias. Develop strategies to reduce unintended bias in machine learning models, and you'll help the Conversation AI team, and the entire industry, build models that work well for a wide range of conversations.  

	We built a bidirectional LSTM model to predict whether the comments are toxic or not. Based on the fundamental model, we used some methods to improve model performance and reached 0.93365 score.  
	**Strategies**:  
	+ adjusted the train target and loss function, which combines main binary train loss function and an auxilary train loss function
	+ adjusted the examples' weights to make it fit for the evaluation of the competition
	+ used bucketing strategy to reduce the training time from around 590s to around 440s each epoch
	+ made a lot of word-level correction

	
**Contribution statement**: Fei Zheng adjusted the loss function and train the model with wighted examples.

Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.
