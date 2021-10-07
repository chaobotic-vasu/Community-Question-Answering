## Original Source
https://alt.qcri.org/semeval2017/task3/index.php?id=data-and-tools

## Dataset Description
The IR part i.e., the retrieval of CQA knowledge base already carried out by SemEval. It provided Qatar Living Forum’s dataset training data for English and Arabic languages. Qatar living forum is an open-domain forum for people to pose questions from multiple aspects of their daily life. Provided by SemEval 2016 in this collection, the threads are independent of each other and the lists of comments are chronologically sorted and contain additional information (e.g., date, user, topic, etc.) 

The dataset contains about 200 Original questions. Each Original Question Oq has been given 10 related Questions, and these 10 related questions have 10 answers each respectively.
As Each of these combinations come with its respective retrieved Relevance label.  
However, since the labels of Questions to Answers and Question to Questions had different names in the dataset, they have been renamed as such for classification task:
  Bad (0), Good (2) or Potentially Useful (1) AND Perfect Match	(2), Irrelevant	(0), Relevant	(1)

  
  
## Subtasks

The task has been divided into three subtasks: Subtask A, Subtask B and Subtask C. 
The goal is to classify the relevance of the data pair into Bad (0), Good (2) or Potentially Useful (1) class i.e., classify corresponding data pair like (x, y) into a class label which depicts the relevance of the pair. 
 
Subtask A	: (Related Question, Answer)	i.e., 1 relatedQuestion - 10 answers
Subtask B	: (Original Question, Related Question)	i.e., 1 originalQuestion - 10 relatedQuestions
Subtask C	: (Original Question, Answer)	i.e., 1 originalQuestion - 100 answers


## Present data format
For three subtasks A, B, C:
- There are three files each (train, test, validation) for the cleaned data. This has all information needed only as per the Tasks.
  
 

