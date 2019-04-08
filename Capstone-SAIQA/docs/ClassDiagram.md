![SAI-QA Logo](/Capstone-SAIQA/img/logo.png))
### [Main](/Capstone-SAIQA/README.md)
# Class Breakdown

This project follows a Model-View-Controller (MVC) architecture.

## Class Diagram

An overview of all classes for the application.  All Controllers, Services, and DAOs will implement the decorator class LoggingDecorator so that logging the flow of the application will be encapsulated into a single class, with any extra logging done throughout the classes.  An overview for each class is below the diagram

![Class Diagram](img/Class_Diagrams.png)

## Models

UserModel is used to store information on a user, allowing for this information to be easily transferred around the application.

Sentence is used to package a sentence's subject, category, and sentence.

## Controllers
### Login Controller

Allows for the user to login and register.  After logging in, takes the user to the correct page.

### Main Controller

Clears the previous session and loading the initial page the user will see.

### Question Controller

Controls both the Answer and Learning Modules.  This is the main Controller that handles a bulk of the application.

## Services

All services act as an in-between for their respective Controller and DAO class.

## DAO

All DAOs, Data Access Objects, handle the logic for the database using the CRUD methods: Create, Read, Update, and Delete.  Both DAOs are subclasses of ConnectionDAO which handles the connection to the database.

## Utility
### LoggingDecorator

Handles logging to the console.  This includes exiting, entering, and error logging.

### InputHandler

Both cleans up the input of any unwanted characters using Regex and finds the subject of a sentence using SpaCy.

### GloveHandler

Attempts to find the nearest word when a subject is not found.

## Training
### softmaxR

Gets the category of a sentence using a [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression) algorithm.  Also has code to train the algorithm.

### importData

Contains helper methods for the [Softmax Regression](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#softmax-regression) algorithm.

### DMNInner

Locates the answer to a question based off of the input given by using the [Dynamic Memory Network](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/MainAlgorithms.md#dynamic-memory-network).