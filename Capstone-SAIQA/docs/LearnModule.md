![SAI-QA Logo](/Capstone-SAIQA/img/logo.png))
### [Main](/Capstone-SAIQA/README.md)
# Learning Module
## Overview
Handles taking sentences, cleaning them of extra characters, finds each of the sentence's subjects, and categorizes them before storing the outcome in a database.  Uses Regex to clean up sentences along with separating input into separate sentences.  Can only be access by admins.

A [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression) is used to separate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made, and the algorithm was trained using a genetic algorithm.

Finding a subject is handled by SpaCy, a Natural Language Processing library for Python.  The subject is found by scanning the noun chunks in a sentence and find which one contains a word bearing the 'nsubj' tag.

## Sequence Diagram
![Sequence Diagram](/Capstone-SAIQA/img/Learn_Module.png)

## Business Rules
![Business Rules](/Capstone-SAIQA/img/Learn_Rules.png)

## Related Classes
- QuestionController
- QuestionService
- QuestionDAO
- ConnectionDAO
- LoggingDecoractor
- InputHandler
- softmaxR
- importData
- UserModel
- Sentence