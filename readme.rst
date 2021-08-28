Question Answering using document retrieval
############

The dataset we have colleted has this format:
   {
      x:   question
      
      y:   exact answer,
      
      z:   passage/document

   }
   
   
Encoding
############
We need to convert document i.e z  and question i.e x to embedding/vector.

Document encoding
****************

What is  document enconding for?
------------------
To  convert each text document/passage in our dataset to an embedding vector.

How to do document encoding?
------------------
Using a model which takes the text as input and provides a single vector as output.



Which model to use for document encoding?
------------------
A pretrained BERT Model. The CLS token of BERT model could be treated as document embedding/vector.


Quentions encoding
****************

What is  question enconding for?
------------------
To  convert a question to an embedding vector.  The answer to this qustion lies in documents. The question  vector should help us in selecing few documents carrying answer.
The similarity score of this vector should be higher for document vectors corresponding to answer.

How to do question encoding?
------------------
Using a model which takes the text as input and provides a single vector as output. This time model should be trainable. 


Which model to use for document encoding?
------------------
A  BERT Model. The CLS token of BERT model could be treated as question embedding/vector. We will be uing same pretrained BERT model as in document encoder. This time it is trained.

  
