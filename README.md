# Medical-QA-with-sentence-transformers
Created medical Q&A models by utilizing sentence transformers models on medical data.

# Introduction:
This GitHub repository presents a comprehensive medical question and answer (Q&A) system powered by state-of-the-art Sentence Transformers. The primary objective of this project is to enable users to obtain accurate and contextually relevant answers to medical queries by leveraging a vast corpus of medical documents. The system excels in providing insights into drug side effects and the diseases treated by specific medications.

# Key Features:

## 1. Data Loading and Preprocessing
The code begins by loading a rich dataset comprising 2967 rows of drug-related side effects data, which was sourced from drugs.com. The dataset can be accessed here. Notable steps include:

Transformation of data to include user-friendly phrases like "side effect" for enhanced answer readability.
Removal of rows with missing side effect data to ensure robust responses.

## 2. Encoding Medical Documents
The heart of the system lies in its ability to encode medical documents effectively. This is accomplished by utilizing a pre-trained Sentence Transformer model. Key steps include:

Downloading and initializing the Sentence Transformer model (paraphrase-MiniLM-L6-v2) specifically fine-tuned for natural language understanding.
Encoding the side effects data from the dataset, effectively converting it into a rich, numerical representation using the initialized model.
Preparing embeddings for end-user queries, ensuring that the system can process and match user questions.

## 3. Answering User Queries
The repository demonstrates the core functionality of the Q&A system, which is answering user queries accurately. This is achieved by employing cosine similarity as a scoring mechanism to find the most similar embeddings within the medical documents for each user query. Key highlights include:

Finding the top match for each user query based on cosine similarity scores.
Handling scenarios where an exact match is not found by returning the top two most similar answers from the medical documents.
Presenting answers in a structured format, along with their respective scores, to assist users in understanding the relevance of the responses.

## 4. Additional Feature: Disease Treated
In addition to drug side effects, the system can also answer questions about the diseases treated by specific medications. This feature is made possible through the encoding of data related to both side effects and the diseases treated. The process includes:

Creating a new corpus that includes information about both side effects and the diseases treated for each drug.
Allowing users to ask questions related to the diseases treated by specific drugs, thus expanding the system's versatility.

# Conclusion
This repository serves as a robust foundation for building an advanced medical Q&A system. While it excels in answering questions related to drug side effects and diseases treated, there is significant potential for improvement and expansion:

Customizing answers to cater to popular and specific queries.
Handling more complex and detailed medical inquiries.
Incorporating information about newly introduced drugs.
Extending the system with multimodal capabilities, such as providing images related to diseases in response to queries.
The Q&A system showcased here demonstrates the potential to revolutionize medical information retrieval by providing quick and accurate responses from extensive medical documents.
