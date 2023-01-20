


**Janarish Saju C**

AI/ML Engineer

**20th January 2022**

# **PICO Extraction**

# **What is PICO !**

**Participants/Problem (P), Intervention (I), Comparison (C) and Outcome (O)**

Successful evidence-based medicine (EBM) applications rely on answering clinical questions by analyzing large medical literature databases. In order to formulate a well-defined, focused clinical question, a framework called PICO is widely used, which identifies the sentences in a given medical text that belong to the four components: Participants/Problem (P), Intervention (I), Comparison (C) and Outcome (O).

# **Data Source** 
https://github.com/jind11/PubMed-PICO-Detection

# **Original Data Source** 
https://pubmed.ncbi.nlm.nih.gov

**Meta informations about the Data:**

- Structured_abstracts_PICO contains the original abstracts. The line that starts with ### indicates the PMID. After that line, each line contains the original section heading, the assigned gold label for train and test and the section content, separated by the symbol |. To create the gold label, key words in the section heading are checked and the mapping rule can be referred to the paper above-mentioned.

- Structured_abstracts_sentences_PICO is almost the same as structured_abstracts_PICO except that each section content is sentence splitted using the Stanford CoreNLP toolkit so that each line has only one sentence and all numbers have been replaced by @.

- The folder splitted contains the train, validation and test sets that are randomly splitted from the file structured_abstracts_sentences_PICO at the ratio of 8:1:1.


# **IMPLEMENTATIONS**
*(\*written here all the necessary steps carried out in the shared code)*
## **BERT NER**
## **1. Data Preprocessing Steps**
- Data read/import
- Data conversion as per model requirements
- Data formatting
## **2. Feature Engineering Steps**
- Encode the labels to Numeric representation
- Tokenize and embed the datasets
## **3. Model Initialization**
- Initialize the BERT model
- Define the Task Name
- Define the Tokenizer method
## **4. Hyper Parameter Turning**
- The following parameters were used
  - evaluation\_strategy = "epoch",
  - learning\_rate=1e-4,
  - per\_device\_train\_batch\_size=16,
  - per\_device\_eval\_batch\_size=16,
  - num\_train\_epochs=6,
  - weight\_decay=1e-5,
## **5. Train the Model**
- Train the model with the below metrics
  - Train\_dataset,
  - Eval\_dataset,
  - Tokenizer,
  - Compute\_metrics
## **6. Evaluate the Model**
- Evaluation done based on the 20 percent of data extracted for validation purposes from the training data.
## **7. Prediction Module**
- Read the unseen data
- Data Conversion
- Feed the Unseen Data to the fine turned model and Get Predictions
- Get ***Label Predictions***
- Store the results in a DataFrame
## **8. Export the Results**
- Export test results
# **CONCLUSION**
- BERT has the advantage over other Machine Learning and Deep Learning models.
- As it is a transformer technique pretrained with huge datasets.
- And it save us a lot of time for training
- Although it has a disadvantage, Heavier BERT model is computationally expensive


**Number of Total Records: 24668**

**Accuracy (80:20 split): 90.8**


## **REFERENCES & URLs**
## **Online Sources:**

1. <https://docs.google.com/document/d/1dcEGM7NCDqEydBmeH2yCz9gwaA2RISTeA-WoT8DgGyA/edit>
1. https://github.com/jind11/PubMed-PICO-Detection
1. https://pubmed.ncbi.nlm.nih.gov
1. https://medium.com/@andrewmarmon/fine-tuned-named-entity-recognition-with-hugging-face-bert-d51d4cb3d7b5
##
