


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



Number of Records:  24668
Accuracy (80:20 split): 90.8
Git: yet to update
