# Sentence Semantic Similarity with BERT
## Introduction
Semantic Similarity is the task of determining how similar two sentences are, in terms of what they mean. This example demonstrates the use of SNLI (Stanford Natural Language Inference) Corpus to predict sentence semantic similarity with Transformers. 
## Model Description
In this project, we use BERT to compute semantic similarity between two pieces of text. Here's how BERT helps with this task:

**1. Contextualized Embeddings:** BERT generates embeddings that capture not only the meaning of individual words but also their meaning in the context of the sentence.

**2. Pre-trained Model:** We use a pre-trained BERT model (such as bert-base-uncased) from Hugging Face's transformers library to leverage this capability without needing extensive retraining.

**3.	CLS Token Representation:** When processing text, BERT adds special tokens to the beginning ([CLS]) and end ([SEP]) of each sentence. The [CLS] token is designed to capture the overall sentence-level meaning. We use the embedding of the [CLS] token as the sentence representation for computing similarity between two texts.

**4.	Cosine Similarity:** After obtaining the embeddings of the [CLS] token for both sentences, we compute the cosine similarity between these embeddings. Cosine similarity is a common metric for measuring the similarity between two vectors, where a score of 1 indicates perfect similarity, and a score of 0 indicates no similarity.
## Dataset
This example demonstrates the use of the Stanford Natural Language Inference (SNLI) Corpus to predict semantic sentence similarity with Transformers.

•	Total train samples: 100000

•	Total validation samples: 10000

•	Total test samples: 10000

Here are the "similarity" label values in SNLI dataset:

**•	Contradiction:** The sentences share no similarity.

**•	Entailment:** The sentences have a similar meaning.

**•	Neutral:** The sentences are neutral.

## Architecture
This model uses BERT to extract sentence embeddings. The architecture involves:

**1.	BERT Layer:** A pretrained BERT model (from Hugging Face) is used to extract contextual embeddings for each sentence.

**2.	Pooling Layer:** The output embeddings are pooled to get a fixed-size representation of each sentence.

**3.	Similarity Function:** The similarity between the two sentences is computed using a distance metric such as cosine similarity or Euclidean distance.

**4.	Dense Layers:** Additional dense layers are used to fine-tune the model for the specific task.


