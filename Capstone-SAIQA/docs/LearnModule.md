![SAI-QA Logo](/img/logo.png)
#Learning Module
##Overview
	Handles taking sentences, cleaning them of extra characters, finds each of the sentence's subjects, and categorizes them before storing the outcome in a database.  Uses Regex to clean up sentences along with seperating input into seperate sentences.  Can only be access by admins.

	A ![Softmax Regression](/Main_Algorithms.md) is used to seperate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made and the algorithm was trained using a genetic algorithm.

	Finding a subject is handled by SpaCy, a Natural Language Processing library for Python.  The subject is found by scanning the noun chuncks in a sentence and find which one contains a word bearing the 'nsubj' tag.

##Sequence Diagram
![Sequence Diagram](/img/Learn_Module/)

##Business Rules
![Business Rules](/img/Learn_Rules)

..*Related Classes