![SAI-QA Logo](/Capstone-SAIQA/img/logo.png)
All text is converted into octal decimal to remove the need of having a large word vector model.  Another reason for using octal decimal instead of another Unicode format is due to most letters being three digits, allowing for the conversion between text and numbers.  The reason why text needs to be converted is because the algorithms cannot interact with text directly.

# SoftMax Regression:

A SoftMax Regression, or a Multinomial Logistical Regression algorithm, is used for classifying sentences into four categories.  This algorithm is used over other classification algorithms since it is both able to have multiple categories and can learn from previously unknown categories.  Modified off a MNIST classification tutorial (https://gist.github.com/awjuliani/5ce098b4b76244b7a9e3#file-softmax-ipynb).

..* Categories
1. Time: When something happened to the subject
2. Location: Where the subject did something or where something happened to the subject
3. Property: What or who the subject is.  This is the most common category
4. Possession: Something that the subject owns, i.e. California owns San Francisco

## Algorithm
### Base algorithm
  
  
  

### Cost Function
 
W = W - LR * GR

# Genetic Algorithm:

	The reason why a genetic algorithm is used is to improve the accuracy of the classifier despite the small dataset.  By using the SoftMax regression's cost function as the fitness function, the genetic algorithm is able to gain a higher accuracy than the SoftMax regression was able to obtain itself.  After the gradient is found, the weight, or what allows for the algorithm to correctly classify a sentence, is adjusted six different ways and then all the weights are checked for accuracy.

..* Adjusted Weight (W)
1. W1 = W - learning_rate * gradient
2. Randomly switch around numbers from W1
3. Randomly switch around numbers from W1
4. W2 = W - learning_rate * gradient
5. Randomly switch around numbers from W2
6. Randomly switch around numbers from W2

After the two most accurate weights are found, they are stitched together in four different ways with one being chosen at random.  This process continues until the algorithm reaches a certain level of accuracy, which is 60.6% accuracy.  From testing, this is the highest accuracy that was reached.

# Dynamic Memory Network:

This architecture was chosen since it increases the benefits of a Recurrent Neural Network using an Attention Mechanism.  It also uses ADAM optimizer for training the weights, which are saved and reloaded using TensorFlow’s Saver class.
![DMN Model](/Capstone-SAIQA/img/DMN_Model.jpg/)
Based off the research paper referenced (Kumar et al., 2015) as well as a tutorial QA with TensorFlow and modified to run a single time without retraining.  Tensorflow handles a majority of the code, resulting in a response from the algorithm to take roughly 8 seconds.


..* Reference
1. Kumar, A., Irsoy, O., Ondruska, P., Iyyer, M., Bradbury, J., Gulrajani, I., … Socher, R. (2015). Ask Me Anything: Dynamic Memory Networks for Natural Language Processing. ArXiv:1506.07285 [Cs]. Retrieved from http://arxiv.org/abs/1506.07285
2. ![Dynamic Memory Network Tutorial](https://github.com/Steven-Hewitt/QA-with-Tensorflow/blob/master/QA%20with%20Tensorflow.ipynb)