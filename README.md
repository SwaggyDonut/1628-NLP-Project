# 1628-NLP-Project
MIE1628 Toxic comment classification 

1. Introduction 
Discussing things you care about can be difficult. The threat of abuse and harassment online means that many people stop expressing themselves and give up on seeking different opinions. Platforms struggle to effectively facilitate conversations, leading many communities to limit or completely shut down user comments. 
In this project, we are aimed to develop models to identify different toxic comments including threats, obscenity, insults, and identity-based hate. 
As a course project, all of the models are built based on Pyspark environment. 

2. Dataset Description & Target Defination 
The dataset is twitter context from Kaggle competition. The dataset is 68.8MB, including 159571 columns and 8 rows. 
Table1. Sample Dataset
 
Independent variables:1) ID(user ID), which is an unique value in the dataset. 2) comment_text Response variables: 1) toxic, 2) severe toxic, 3) obscene, 4) threat, 5)insult and 6) identity hat 

From table 2, We can see it’s unbalanced classes, there are 159,571 twitters in total, 162,25/159,571 of them are labelled. Our target is to assign labels for each twitter by natural language processing. One instance(text) can belong to several labels in the same time. It’s multi-label problem. 

When we build our models on school's cluster, it often crashed due to the limitation of memory. Therefore, in our modelling process, we only sample 30000 comments for our tranning set and 20000 comments for test set.
