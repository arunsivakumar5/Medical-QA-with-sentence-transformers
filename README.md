# Medical-QA-with-sentence-transformers
Created medical Q&A models by utilizing sentence transformers models on medical data.

Description:
This GitHub repository contains code for a medical question and answer (Q&A) system that utilizes sentence transformers to provide answers to user queries based on medical documents. The code demonstrates how to encode medical documents, user queries, and find the most similar answers using cosine similarity scores. It also includes a feature for answering questions related to the diseases treated by specific drugs.

Key Features:

Loading and Preprocessing Data: The code loads a dataset of 2967 rows of side effects data from drugs.com and transforms it to include descriptive phrases like "side effect" to enhance answer readability. Rows with missing side effect data are dropped.

Encoding Medical Documents: The code encodes the side effects data using a Sentence Transformer model and prepares embeddings for end-user queries.

Answering User Queries: The code uses cosine similarity to find the most similar embeddings in medical documents for user queries. It provides answers to user questions regarding drug side effects, with the option to retrieve the top two most similar answers if a direct match is not found.

Additional Feature: Disease Treated: The code extends functionality to answer questions about the diseases treated by specific drugs. It encodes data related to both side effects and diseases treated and provides answers based on user queries.

Conclusion:
This code showcases a basic medical Q&A system using sentence transformers and cosine similarity. It suggests opportunities for improvement, such as customizing answers to popular questions and expanding the model's capabilities to handle more detailed queries and newer drugs. Additionally, it highlights the potential to integrate multimodal models like CLIP to provide image examples of diseases in response to user queries, enhancing the overall user experience.

Note: Users are encouraged to ensure comprehensive coverage of user queries to avoid situations where the model returns the most similar match when a specific drug is not present in the dataset.
