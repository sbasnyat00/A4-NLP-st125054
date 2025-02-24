# A4-NLP-st125054
Assignment 4 NLP 2025 Asian Institute of Technology

For this assignment:

Task1: Trained a BERT model from scratch using a suitable dataset from BookCorpus on Kaggle <https://www.kaggle.com/datasets/nishantsingh96/refined-bookcorpus-dataset>, learning contextual word representations through masked language modeling (MLM) and next sentence prediction (NSP).


Task2: Implemented the trained BERT model within a Siamese network (SBERT) to generate semantically meaningful sentence embeddings, allowing sentence similarity comparisons for the Natural Language Inference (NLI) task on the SNLI dataset

<img width="432" alt="Screenshot 2025-02-23 at 18 41 14" src="https://github.com/user-attachments/assets/fc118963-f74c-44ee-8af4-addf25dfce20" />


Task3: Our SBERT model had 68% accuracy. Possible reasons could be:
1. Used only 50K samples instead of the full 570K SNLI dataset.
2. Trained BERT from scratch instead of using a pretrained model.
3. Used a small batch size (8) due to GPU limitations.


Limitations and possible Improvements:

Training a transformer-based model like SBERT was GPU-intensive, causing CUDA Out of Memory (OOM) errors. To prevent crashes, I reduced the batch size to 8, optimizing memory usage while maintaining stable training.

Using only 50K samples instead of the full dataset limited generalization, but helped speed up training while testing the model's effectiveness.
