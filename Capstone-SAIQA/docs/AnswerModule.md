![SAI-QA Logo](/Capstone-SAIQA/img/logo.png))
# [Main](/Capstone-SAIQA/README.md)
# Answer Module
## Overview
Handles answering questions, displaying the past interactions in a paragraph tag using the overflow CSS property.  Only the last four elements are displayed not to overcrowd the screen.  An entire list of questions asked and the answers to them are also displayed on the left side of the screen.

A [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression) is used to separate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made, and the algorithm was trained using a genetic algorithm.

A [Dynamic Memory Network](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#dynamic-memory-network) is used to answer questions based off of the question asked and sentences that were inputted.  Has added functionality to return an entire sentence as an answer.

## Sequence Diagram

Below is an overview of how the code runs through the relevant classes.

![Answer Module Sequence Diagram](/Capstone-SAIQA/img/Answer_Module.png)

## Business Rules

Below is an overview of the rules of the module.

![Answer Module Business Rules](/Capstone-SAIQA/img/Answer_Rules.png)

## Related Classes
- [QuestionController](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#question-controller)
- [QuestionService](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#services)
- [QuestionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [ConnectionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [LoggingDecoractor](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#loggingdecorator)
- [InputHandler](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#inputhandler)
- [GloveHandler](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#glovehandler)
- [SoftmaxR](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#softmaxr)
- [ImportData](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#importdata)
- [DMNInner](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dmninner)
- [UserModel](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#models)
- [Sentence](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#models)