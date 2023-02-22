# NLP-Preprocessing-Techniques
BOW, N-Grams, TF-IDF, Part of Speech (POS) Tagging

Note: Bag of Words is just a special case of N-Grams where n=1


## Bag of Words (BOW)
BOW is a technique used in natural language processing to represent text as a collection of words, ignoring the order of the words. It creates a histogram of the frequency of each word in a document or a corpus. 

### Example:
Consider the following two sentences: 
- Sentence 1: "The cat is sleeping on the couch."
- Sentence 2: "The dog is playing in the park."

The BOW representation for these two sentences would be: 

| Word  | Sentence 1 | Sentence 2 |
|-------|------------|------------|
| The   | 1          | 1          |
| cat   | 1          | 0          |
| is    | 1          | 1          |
| sleeping | 1          | 0          |
| on    | 1          | 0          |
| the   | 1          | 0          |
| couch | 1          | 0          |
| dog   | 0          | 1          |
| playing | 0          | 1          |
| in    | 0          | 1          |
| park  | 0          | 1          |
