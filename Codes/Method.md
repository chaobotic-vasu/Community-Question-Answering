Assumption is that Community forum’s data is usually related and contextual in manner, and has the capacity to span the spectrum of a particular question or domain or category (which ever dependent variable might be)- so, the focus here is to learn contextualized embeddings using sequential networks. 

Motivated from the formerly explored methods, we experiment on BiLSTM model as it has been promising for sequence modeling, so forth, open-domain QA task. The network implementation is rather simple. 

Flow of the program is as follows:
![image](https://user-images.githubusercontent.com/48856742/136375830-e023930c-e3de-4dd7-a257-c9c46749fc60.png)



Vector representations for texts, say, input question and related questions/answers (or other pairs as per subtask) are generated separately here to capture sequential information attribute wise. Essentially, the problem has been treated as a Classification Problem so for each of (oQ, relQ), (relQ, A) and (oQ, A) new embeddings are computed to label them as 0, 1, 2 ( 0 for bad, 1 for useful and 2 for Good) 

We assume such content-rich embeddings (or data-dependent features) are bound to improve the Q-A pair information hence, better feature engineering as possible. For eg. Subject and Category words such as “Visa” and “Month” will appear in responses (questions or answers) and having such words can be treated as good aspects or features for an answer about booking and locations of visa appointments and hearings. This also infers that topics which are talked about can be found out and with such feature columns (subject/category here), it can be fruitful to predict subset of documents inside that topic. Traditionally comparing, you can see it is not much different than using LDA (Latent Dirichlet Allocation) which is known for topic modeling. Naturally, the aim is to find good results (just) for the given dataset to facilitate better learning question-dependent attributes as feature themselves, data attributes are used as separate features, hence have their own embeddings. 


The output retrieved is essentially, a vector of probabilities of each class for the given particular sequence pair or text pair. They imply how likely the (q, a) or (f, q, a) pair belongs to the Classes (0, 1 and 2 here). 
