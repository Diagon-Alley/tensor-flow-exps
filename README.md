# tensor-flow-exps
experiments on tensorflow. This repo can be used for experimenting with various modules of tensorflow

### Reinforcement learning

Reinforcement learning works through trial and error which actions yield the greatest rewards. Used in places where we have a computer learning to play a video game, or a machine learning to drive a car and so on. 

#### Components of Reinforcement learning

* Agent: Learning/Decision maker
* Environment: What the agent interacts with
* Actions: What the agent can do

So what happens in case of reinforcement learning is that the agent chooses actions that maximizes some reward metric over a given amount of time. Basically learning the **`best policy`**

## General steps in machine learning

`Note that general steps in Machine learning do not always comply with reinforcement learning. The steps in reinforcement learning are a little different on its own`

### Supervised learning

* Data acquisition
* Data cleaning(normalization and so on)
* Train, Test split(30%, 70% ---30 % being test and the other being train)
* Train model
* Evaluate model(using test set). Based on the evaluation results we may need to adjust the model parameters
* Deploy model on new incoming data

### Unsupervised learning

* Data acquisition
* Data Cleaning(normalization and so on)
* Prepare the train data
* Train model
* Evaluate model and adjust model parameters and then evaluate again
* Deploy model 

### Hold out sets

Here we actually divide the data into 3 sets: a train set, a test set and a holdout set. The holdout set is used to get a true sense of how the model is going to perform in case of data that has never been seen before. After training the model we are going to test the model using the test set. Based on the test results we are going to adjust the parameters of our model and retrain and test the model. This is a cycle and we can go over this again and again until we are satisfied. However this test data too is not giving us a true measure of how the model is preforming in case of new and unseen data. So basically this hold-out data is going to give us a sense of how the model going to perform when deployed and it sees data that it has never seen before.

We are not allowed to change the parameters once we have found the results for the hold-out data.

## Supervised: Classification Evaluation metrics

* Accuracy, recall, precision

Accuracy is the most common metric which is simply the total number of correctly classified examples divided by the total number of training examples.

## Supervised: Regression Evaluation metrics

* MAE, MSE, RMSE: mean average error, mean squared error and root mean squared error. 

Basically on avearge how far are you from the correct continuous value.

## Unsupervised: Evaluation

* Cluster homogenity, Rand index

