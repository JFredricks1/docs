![SAI-QA Logo](/Capstone-SAIQA/img/logo.png)
### [Main](/Capstone-SAIQA/README.md)
# Learning Module
## Overview
The Learning Module handles taking sentences, cleaning them of extra characters, finds each of the sentence's subjects and categorizes them before storing the outcome in a database.  Uses Regex to clean up sentences along with separating input into separate sentences.  Can only be accessed by admins.

A [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression) is used to separate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made, and the algorithm was trained using a genetic algorithm.

Finding a subject is handled by SpaCy, a Natural Language Processing library for Python.  The subject is detected by scanning the noun chunks in a sentence and find which one contains a word bearing the 'nsubj' tag.

## Sequence Diagram

Below is an overview of how the code runs through the relevant classes.

![Sequence Diagram](/Capstone-SAIQA/img/Learn_Module.png)

## Business Rules

An overview of the rules of the module.

![Business Rules](/Capstone-SAIQA/img/Learn_Rules.png)

## Related Classes
- [QuestionController](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#question-controller)
- [QuestionService](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#services)
- [QuestionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [ConnectionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [LoggingDecoractor](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#loggingdecorator)
- [InputHandler](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#inputhandler)
- [SoftmaxR](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#softmaxr)
- [ImportData](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#importdata)
- [UserModel](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#models)
- [Sentence](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#models)
