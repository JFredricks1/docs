![SAI-QA Logo](/Capstone-SAIQA/img/logo.png)
### [Main](/Capstone-SAIQA/README.md)

# Octal Decimal

All text is converted into octal decimal to remove the need of having a large word vector model.  Another reason for using octal decimal instead of another Unicode format is due to most letters being three digits, allowing for the conversion between text and numbers.  The reason why text needs to be converted is because the algorithms cannot interact with text directly.

```python
ans = []
for line in x:
    number = ord(line)
    convNum = oct(number)
    convNum = int(convNum[2:])
        
    ans.append(convNum)
return ans
```

# SoftMax Regression:

A SoftMax Regression, or a Multinomial Logistical Regression algorithm, is used for classifying sentences into four categories.  This algorithm is used over other classification algorithms since it is both able to have multiple categories and can learn from previously unknown categories.  Modified off a MNIST classification tutorial and trained off a custom dataset (https://gist.github.com/awjuliani/5ce098b4b76244b7a9e3#file-softmax-ipynb).  All percentages are based off of 1000 entries that this algorithm has gone over.

## Categories
- Time: When something happened to the subject. Lowest likelihood of appear at 0.1%
- Location: Where the subject did something or where something happened to the subject.  Second least likely to appear at 0.39%
- Property: What or who the subject is.  This is the most common category at 97.69%
- Possession: Something that the subject owns, i.e. California owns San Francisco.  This is the second most likely to appear at 1.16%

## Algorithm
### Base algorithm
![Base Algorithm](/Capstone-SAIQA/img/Softmax_Base_Algorithm.jpg/)

### Cost Function
![Cost Function](/Capstone-SAIQA/img/Softmax_Cost_Function.jpg/)

# Genetic Algorithm:

The reason why a genetic algorithm is used is to improve the accuracy of the classifier despite the small dataset.  By using the SoftMax regression's cost function as the fitness function, the genetic algorithm is able to gain a higher accuracy than the SoftMax regression was able to obtain itself.  After the gradient is found, the weight, or what allows for the algorithm to correctly classify a sentence, is adjusted six different ways and then all the weights are checked for accuracy.

## Adjusted Weight (W)
1. <img src="https://latex.codecogs.com/gif.latex?W1=W-learningrate*gradient"/>
2. Randomly switch around numbers from W1
3. Randomly switch around numbers from W1
4. <img src="https://latex.codecogs.com/gif.latex?W2=W-learningrate*gradient"/>
5. Randomly switch around numbers from W2
6. Randomly switch around numbers from W2

After the two most accurate weights are found, they are stitched together in four different ways with one being chosen at random.  This process continues until the algorithm reaches a certain level of accuracy, which is 60.6% accuracy.  From testing, this is the highest accuracy that was reached.

# Dynamic Memory Network:

This architecture was chosen since it increases the benefits of a Recurrent Neural Network using an Attention Mechanism.  It also uses ADAM optimizer for training the weights, which are saved and reloaded using TensorFlow’s Saver class.

![DMN Model](/Capstone-SAIQA/img/DMN_Model.jpg/)

Based off the research paper referenced (Kumar et al., 2015) as well as a tutorial QA with TensorFlow and modified to run a single time without retraining.  Tensorflow handles a majority of the code, resulting in a response from the algorithm to take roughly 8 seconds.  Trained using the bAbi dataset's first task, which trains only to answer off of a single fact.


# Reference
- Kumar, A., Irsoy, O., Ondruska, P., Iyyer, M., Bradbury, J., Gulrajani, I., … Socher, R. (2015). Ask Me Anything: Dynamic Memory Networks for Natural Language Processing. ArXiv:1506.07285 [Cs]. Retrieved from http://arxiv.org/abs/1506.07285
- [Dynamic Memory Network Tutorial](https://github.com/Steven-Hewitt/QA-with-Tensorflow/blob/master/QA%20with%20Tensorflow.ipynb)