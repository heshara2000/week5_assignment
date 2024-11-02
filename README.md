# week5_assignment
Named Entity Extraction with BERT

This project implements a Named Entity Recognition (NER) model using the HuggingFace transformers library. The model is trained on the CoNLL-2003 dataset. The project walks through data preprocessing, model training, and evaluation steps.
Load the CoNLL-2003 Dataset
We use the CoNLL-2003 dataset for training the NER model. The dataset is automatically loaded using the HuggingFace Datasets library.
Data Preprocessing
Data preprocessing includes tokenizing the input sentences and aligning the labels with the tokens. We use a pretrained tokenizer from the transformers library to prepare the data.

Tokenize the sentences
Align token labels with tokenized input
Split the dataset into training, validation, and test sets

Create Data Loaders
After preprocessing, we create PyTorch data loaders to facilitate batch processing during training.


Model Implementation

We define a custom NER model using a pretrained transformer model from the HuggingFace library. The model architecture is built upon a BertModel, and a classification head is added on top for NER classification.

Training Loop
The training loop includes forward pass, loss computation, and gradient updates. The loop tracks the loss at each step to monitor progress.
Evaluation Metrics
For evaluation, we use standard NER metrics such as accuracy, precision, recall, and F1-score.
