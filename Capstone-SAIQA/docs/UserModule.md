![SAI-QA Logo](Capstone-SAIQA/img/logo.png)
Handles all login and registration logic for the application.  Ensures that users are sent to the correct pages after entering their correct credentials.  An admin will go to the learning page, a guest or a normal user will go to the question panel, and a successful registration would bring the user to the login page.

When registering, uppercases and special characters are counted using Python's regex package.  If any of the rules are not met, or the form is empty, the form will clear, and the error will be logged in the console.

..* Registration Rules
1. The username must be between 4 - 20 characters
2. The password must be between 4 - 20 characters
3. The username must have at least 2 uppercase letters
4. The password must have at least 2 uppercase letters
5. The password must have at least 2 special characters ($&+,=?@`~^*%!-_)
6. The two passwords must match each other
7. The user must not already be created

# Sequence Diagrams
![Login Sequence Diagram](/Capstone-SAIQA/img/Login_Diagram.png/)
![Registration Sequence Diagram](/Capstone-SAIQA/img/Registration.png/)

..* Related Classes
1. LoginController
2. UserService
3. UserDAO
4. ConnectionDAO
5. LoggingDecorator
6. UserModel