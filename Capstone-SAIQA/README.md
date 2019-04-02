![SAI-QA Logo](/img/logo.png)
#**Abstract**

	Sima: Artificial Intelligence for Question Answering (further referred to as SAI-QA) is an artificial intelligence that learns information from training documents and uses the data to answer questions provided to it.  This project’s name is derived from the mathematic symbol Sigma since it is only as good as what is available to it, being able to better answer questions the more training documents feed into it.  Its purpose is to aid researchers and student who want to find information without having to spend hours going through documents and websites for a specific piece of information.

## Video Overview
![Loom Video](https://www.useloom.com/share/1a54c14bdeae4cca9cc123498b5a778f)

##General Overview

	The primary purpose of this project was to combine what I have learned through my major (creating databases, AJAX-enabled web pages, and web applications) and what I have taught myself (Regex, Artificial Intelligence, and Python).  The outcome is a decent web application that can answer questions with relative accuracy as long as the subject has at least one entry in the  database.  Along the way, I also learn about and implemented several artificial intelligence alogirthms which wil be further talked about.  The main areas of of Artificial Intelligence that are used are text analysis and natural language processing (NLP).

###Class Diagram
![Class Diagram](/img/Class_Diagrams.png)

###Logical Architecture
![Logical Architecture Diagram](/img/Logical_Architecture.png)

###Physical Architecture
![Physical Architecture Diagram](/img/Physical_Architecture.png)

###Deployment Diagram
![Deployment Diagram](/img/Deployment_Diagram.png)

###Database
![ER Diagram](/img/ER_Diagram.png/))

###Sitemap
![Sitemap Diagram](/img/Sitemap.png)

..*Modules
1. User Module
2. Learning Module
3. Answer Module

## Conclusions

	Artificial Intelligence is a powerful tool for those who know how to properly use it, something that is not difficult for those with a good mathematic and programming background.  With sites such as Kaggle and companies making their datasets public, most problems can be solved with some form of artificial intelligence without having to create an entire new dataset.

..*Future Ideas
1. Cross-check to correct data: Compare data to rest of database and remove false information.  False information is information that does not match other information that were found from more trustworthy sources.
2. Keep track of unknown subjects: Have a list of all nouns found while learning that are not subject in the database.
3. Auto-learn information from unknown nouns: Check the list of unknown nouns for any that are a neighbor to a known subject using Gensim.
4. Extract questions from images: Tell the user a fact about one of the objects in an image.

..*References
1. ![Dynamic Memory Network Tutorial](https://github.com/Steven-Hewitt/QA-with-Tensorflow/blob/master/QA%20with%20Tensorflow.ipynb)
2. ![Softmax Regression Tutorial](https://gist.github.com/awjuliani/5ce098b4b76244b7a9e3#file-softmax-ipynb)