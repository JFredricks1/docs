![SAI-QA Logo](/Capstone-SAIQA/img/logo.png))
# [Main](/Capstone-SAIQA/README.md)
# Answer Module
## Overview
Handles answering questions, displaying the past interactions in a paragraph tag using the overflow css property.  Only the last four elements are displayed to not overcrowd the screen.  An entire list of questions asked and the answers to them are also displayed on the left side of the screen.

A [Softmax Regression](/Capstone-SAIQA/docs/MainAlgorithms.md) is used to seperate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made and the algorithm was trained using a genetic algorithm.

A [Dynamic Memory Network](/Capstone-SAIQA/docs/MainAlgorithms.md) is used to answer questions based off of the question asked and sentences that were inputed.  Has added functionality to return an entire sentence as an answer.

## Sequence Diagram
![Answer Module Sequence Diagram](/Capstone-SAIQA/img/Answer_Module.png)

## Business Rules
![Answer Module Business Rules](/Capstone-SAIQA/img/Answer_Rules.png)

## Related Classes
1. QuestionController
2. QuestionService
3. QuestionDAO
4. ConnectionDAO
5. LoggingDecoractor
6. InputHandler
7. GloveHandler
8. softmaxR
9. importData
10. DMNInner
11. UserModel
12. Sentence