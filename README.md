An arabic chatbot that can detect sentiment and reply accordingly.

# Pipeline Steps:

1. Read and merge train and test datasets
2. Combine all contexts into either positive or negative sentiment.
3. Use Arabic library ("qalsadi.lemmatizer") for tokenization, removing stop-words and lemmatization.
4. We create a new replicated column of the available sentences and then we add it to the current dataset but shifted up by 1. 
5. We remove the last sentence from every conversation in the dataset as it doesn’t have a reply (the next sentence will be for another conversation).
6. We divide the dataset into training/testing datasets.
5. Train machine learning Logistic Regression model on the training dataset
6. Run the trained model on the entered query to classify its sentiment.
7. Create Tf-idf for all sentences that have the same sentiment as the query.
8. Create Tf-idf for the entered query
9. Calculate cosine similarity between the entered query and all sentences that have the same sentiment.
10. Choose the sentence with the highest cosine similarity
11. Output the following sentence as it was the reply for the most similar sentence.

# Team Members:
1. Ahmed Osama Mohamed 40-9418 
2. Mostafa walid 40-5470 
3. Omar Khaled Khairy 40-5535 
4. Malak Osama 40-1389
