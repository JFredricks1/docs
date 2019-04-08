![SAI-QA Logo](/Capstone-SAIQA/img/logo.png)
### [Main](/Capstone-SAIQA/README.md)
# Overview
This module handles all login and registration logic for the application.  Ensures that users are sent to the correct pages after entering their correct credentials.  An admin will go to the learning page, a guest or a normal user will go to the question panel, and a successful registration would bring the user to the login page.

When registering, uppercase and special characters are counted using Python's regex package.  If any of the rules are not met, or the form is empty, the HTML form will clear, and the error will be logged in the console.

## Registration Rules
- The username must be between 4 - 20 characters
- The password must be between 4 - 20 characters
- The username must have at least two uppercase letters
- The password must have at least two uppercase letters
- The password must have at least two special characters ($&+,=?@`~^*%!-_)
- The two passwords must match each other
- The user must not already be created

# Sequence Diagrams

Below is an overview of how the code runs through the relevant classes.

![Login Sequence Diagram](/Capstone-SAIQA/img/Login_Diagram.png/)
![Registration Sequence Diagram](/Capstone-SAIQA/img/Registration.png/)

# Related Classes
- [QuestionController](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#login-controller)
- [QuestionService](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#services)
- [QuestionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [ConnectionDAO](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#dao)
- [LoggingDecoractor](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#loggingdecorator)
- [UserModel](https://github.com/mark-mo/docs/blob/master/Capstone-SAIQA/docs/ClassDiagram.md#models)