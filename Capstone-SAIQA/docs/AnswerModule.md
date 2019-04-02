![SAI-QA Logo](/img/logo.png)
#Answer Module
##Overview
	Handles answering questions, displaying the past interactions in a paragraph tag using the overflow css property.  Only the last four elements are displayed to not overcrowd the screen.  An entire list of questions asked and the answers to them are also displayed on the left side of the screen.

	A ![Softmax Regression](/Main_Algorithms.md) is used to seperate algorithms between four different categories: time, when things happened; locate, where something happened; property, a fact about the subject; and possession, something the subject owns.  The dataset was self-made and the algorithm was trained using a genetic algorithm.

	A ![Dynamic Memory Network](/Main_Algorithms.md) is used to answer questions based off of the question asked and sentences that were inputed.  Has added functionality to return an entire sentence as an answer.

##Sequence Diagram
![Answer Module Sequence Diagram](/Answer_Module.png)

##Business Rules
![Answer Module Business Rules](/img/Answer_Rules.png)