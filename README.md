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


<br><br>

## N-Grams
N-grams are a contiguous sequence of n items from a given sample of text, where n refers to the number of words in the sequence. N-grams are useful in language modeling, text generation, and machine translation.

### Example:
Consider the sentence "The quick brown fox jumps over the lazy dog." The bigrams (2-grams) for this sentence would be:

| 2-grams | Count |
|---------|-------|
| The quick | 1     |
| quick brown | 1     |
| brown fox | 1     |
| fox jumps | 1     |
| jumps over | 1     |
| over the | 1     |
| the lazy | 1     |
| lazy dog | 1     |

<br><br>

## TF-IDF (Term Frequency-Inverse Document Frequency)
TF-IDF is a statistical measure used to evaluate the importance of a term within a document or a corpus. It measures the frequency of a term in a document against the frequency of the same term in the corpus. This helps in identifying the importance of a term in a particular document in comparison to its importance in the corpus as a whole.

### Example:
Consider a corpus of two documents:
- Document 1: "The cat is sleeping on the couch."
- Document 2: "The dog is playing in the park."

The TF-IDF representation for the word "cat" in Document 1 would be:

TF (Term Frequency) = (Number of times the term "cat" appears in the document) / (Total number of terms in the document)

TF("cat", Document 1) = 1/7 = 0.14

IDF (Inverse Document Frequency) = log_e(Total number of documents in the corpus / Number of documents with the term "cat")

IDF("cat") = log_e(2/1) = 0.69

TF-IDF("cat", Document 1) = TF("cat", Document 1) * IDF("cat") = 0.14 * 0.69 = 0.097

<br><br>

## Part of Speech (POS) Tagging

POS tagging is the process of labeling each word in a sentence with its corresponding part of speech (noun, verb, adjective, etc.). This is a crucial step in natural language processing as it helps to understand the meaning of a sentence and how its words are related to each other.

### Example:
Consider the sentence: "The cat is sleeping on the couch."

A POS tagger would label each word in the sentence with its corresponding part of speech, as follows:

| Word     | POS Tag |
|----------|---------|
| The      | DT      |
| cat      | NN      |
| is       | VBZ     |
| sleeping | VBG     |
| on       | IN      |
| the      | DT      |
| couch    | NN      |
| .        | .       |

In this example, DT stands for determiner, NN stands for noun, VBZ stands for verb (3rd person singular present), VBG stands for verb (present participle), IN stands for preposition/subordinating conjunction, and . stands for punctuation mark. 

This POS tagging helps to identify the grammatical structure of the sentence and can be used for tasks such as text classification, sentiment analysis, and machine translation.

