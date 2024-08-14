Fact-Checking of Claims from Wikipedia
This project was developed as part of the CS 728: Organization of Web Information course, under the guidance of Prof. Soumen Chakrabarti (Jan 2024 - April 2024). The goal was to design a robust system for fact-checking claims using data from Wikipedia, focusing on accurate retrieval and classification of relevant information.

Project Overview
Fact-checking is a critical task in the era of information overload. With the vast amount of data available on platforms like Wikipedia, efficiently verifying the accuracy of claims is essential. This project focuses on building a system that utilizes advanced embedding techniques and natural language processing (NLP) models to verify claims against Wikipedia data.

Key Achievements
High Recall@100: Achieved a strong Recall@100 of 0.707 by retrieving the top 100 candidates for each claim. This metric indicates the system's effectiveness in finding relevant information within the massive Wikipedia dataset.
SentenceTransformer Embeddings: Utilized SentenceTransformer embeddings to encode and index Wikipedia sentences, enabling efficient and accurate retrieval of candidate sentences related to the claims.
Cross-Encoder Re-Ranking: Refined the initial retrieval of candidates through a cross-encoder re-ranker, which further improves the precision of the retrieved information.
NER Enhancements: Implemented Named Entity Recognition (NER) enhancements that significantly improved the classification accuracy for processing claims. By discarding non-relevant sentences, the system achieved a 28% reduction in false positives across all claim types.
Technical Details
Dataset
Source: Wikipedia
Content: Massive collection of sentences extracted from Wikipedia articles, used as the knowledge base for verifying claims.
Model Architecture
Claim Encoding:

Claims were encoded using SentenceTransformer to generate dense embeddings.
The embeddings represent the semantic meaning of the claims for efficient comparison with Wikipedia sentences.
Candidate Retrieval:

Retrieved the top 100 candidates (sentences) from the Wikipedia dataset using the encoded embeddings.
Achieved a Recall@100 of 0.707, indicating a high likelihood of finding relevant information within the top 100 retrieved sentences.
Re-Ranking:

Implemented a cross-encoder re-ranker to refine the list of top candidates.
The cross-encoder re-ranker provided a more precise ranking by evaluating the relevance of each candidate sentence to the claim.
NER Enhancements:

Integrated Named Entity Recognition (NER) to identify and retain only the most relevant sentences, focusing on sentences that contain critical named entities related to the claims.
This step reduced the number of false positives by 28%, improving overall classification accuracy.
Results
Recall@100:
Achieved: 0.707
Reduction in False Positives:
Achieved: 28% reduction across all claim types
The system's performance demonstrates the effectiveness of combining sentence embeddings, efficient retrieval, and enhanced NER for fact-checking tasks.

How to Run
Prerequisites:

Python 3.x
PyTorch
SentenceTransformers
NLTK and other NLP libraries
Setup:

Clone the repository.
Install the required dependencies using pip install -r requirements.txt.
Running the System:

Encode the claims using the SentenceTransformer model.
Retrieve top candidates from the Wikipedia dataset.
Apply the cross-encoder re-ranker for precise retrieval.
Evaluate the results, focusing on Recall@100 and false positive reduction.
Conclusion
This project showcases the effectiveness of advanced NLP techniques, particularly sentence embeddings and cross-encoder re-ranking, in the context of fact-checking claims from large datasets like Wikipedia. The integration of NER further enhances the system's ability to accurately classify relevant information, making it a valuable tool in the domain of information verification.

Acknowledgments
Instructor: Prof. Soumen Chakrabarti
Course: CS 728: Organization of Web Information
Semester: January 2024 - April 2024
For more information or to access the code, please refer to the repository or contact the author.






