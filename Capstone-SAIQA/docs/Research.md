![SAI-QA Logo](/Capstone-SAIQA/img/logo.png)
### [Main](/Capstone-SAIQA/README.md)
# Research
## Overview

SAI-QA was not something that was created solely out of the knowledge I had gained from my major.  To the point that it is, multiple hours of research were needed so I could have just enough knowledge to get everything working at an acceptable level.  The main two sections that required research was Text Analysis and Natural Language Processing since I already understood the basics of programming.

## Text Analysis

While researching natural language processing, I came across the research paper that lays out the Dynamic Memory Network in full which served the purposes for answering questions.  This research paper was found at the end of a public course syllabus from a public [Stanford course](http://cs224d.stanford.edu/syllabus.html).  There are other algorithms, such as a Dynamic Memory+ which adds an extra element to the architecture to further improve it, the base architecture was used since all that was needed was a way to answer a question.  Once the architecture was found, more research was done to get a better idea of how to create the algorithms required and train them which lead me to a [Dynamic Memory Network Tutorial](https://github.com/Steven-Hewitt/QA-with-Tensorflow/blob/master/QA%20with%20Tensorflow.ipynb), which had to be edited to both only be run once along with be able to work in an application setting instead of as a separate application.

This process led to learning about how Tensorflow's Graphs work along with how the Saver class works.  I also had come across what weights were due to them showing up in several research papers and websites covering artificial intelligence algorithms, allowing me to know better how to best use a trained Dynamic Memory Network to answer questions given it.


## Natural Language Processing

Before concluding to use a [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression), several other regression and classification algorithms were researched, such as k-means and linear regression.  After looking further into these algorithms and seeing an example of sorting images into multiple categories, Multinomial Logistical Regression, or SoftMax Regression proved to be the most effective.

However, now the problem was that the tutorial that was used to create a SoftMax Regression was meant to classify images based off of which number it is.  This required me to take a crash course on Linear Algebra, so the algorithm does not become something completely different while still meeting the requirements put forth by the new input type.

After compiling a dataset and training off of the cost function, the result was subpar with only a 36% accuracy.  To remedy the low accuracy of the classifier, a [Genetic Algorithm](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#genetic-algorithm) was implemented to speed up the training process and lessened the chance of getting stuck at a local maximum instead of finding the global maximum.
