![SAI-QA Logo](/Capstone-SAIQA/img/logo.png))
### [Main](/Capstone-SAIQA/README.md)
# Learning Module
# General Approach

The primary architecture, the Dynamic Memory Network, is being used to determine the answer based on the information that it has stored in its database.  This process is done by using a Recurrent Neural Network called a Gated Recurrent Unit which can remember previous input and output information to focus on.  Due to how this neural network works, it is also used for sentiment analysis, determining if a document has a positive or negative view on a subject.  The architecture is put into place to build upon the benefits of the Gated Recurrent Unit, ensuring that relevant information discovered at the beginning of a run-through is not forgotten.

SoftMax Regression, a type of multinomial logistical regression which is a generalization of logistical regression so that it can handle multiple categories, will be used to classify sentences based on how the subject relates to the rest of the sentence.  The groups being used are time, location, property, and possession, all of which relate to the five basic questions which (possession), what (property), when (time), where (location), and why (property).

Octal decimal is used to convert words into a number format so that any of the prediction algorithms can handle them.  This is used over both any of the other ASCII types and word vectors due to Azure limiting space down to 1 GB as well as word vectors require new words to be added constantly.  In the long run, octal decimal would allow for less backend and storage.
Whenever a user asks a question, the subject they asked about will be remembered in the database.  This will allow for the application to keep track of which topic the user is most interested in and can provide random facts based off of the user’s interests.  Despite being a static way of personalizing the user’s experience, it aids in the primary purpose of the application of helping people find information and learn.
Trust is added to all sources for a future feature that will review the facts it has to decrease the chance of false information being in the database.  How this would work is that if there are several sources of information all saying one thing, for example, the moon orbits the earth and another that states that the moon is a myth, the source with the lower trust will be ignored to get rid of most edge cases.

After registering, a user will not be able to update their username and password outside of creating a new user entirely.

# Major Libraries
## Django 2.1.7: The framework for the web application.
Django was picked due to the simplicity of the framework, allowing for a web application to be created without having to spend more time learning a complicated web framework that might have only provided a minimal increase to the overall flow of the application.
## MySQL: The database language used.
## NumPy 1.15.1: Included with TensorFlow and used for handling matrices.
## Python 3.6.4: The programming language.
## SpaCy 2.0.16: Used to handle natural language processing such as a Lemmatizer.
## TensorFlow 1.10.0: Requires Python 3.6

TensorFlow, this will be used due to it both containing multiple well-made classes for programming an artificial intelligence and being made by Google, a fact that increases the reliability of the library.  By using a library for artificial intelligence, more complex and essential equations such as the Adam Optimizer will be optimized, theoretically decreasing the overall error rating of the application.

# Standards
## Project Structure

SAI-QA uses both Django's default project structure and the MVC framework.  This allows for the encapsulating of code.