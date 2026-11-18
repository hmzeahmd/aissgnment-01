# Assignment 1 -- NLP Foundations

## 1. Natural Language Processing and Its Relationship to AI and Machine Learning

Natural Language Processing (NLP) is a field of computer science and
artificial intelligence (AI) that enables computers to process,
understand, interpret, and generate human language. It works with both
written text and spoken language.

NLP is a branch of AI because it aims to make computers perform tasks
that normally require human language abilities. Machine Learning (ML) is
one of the main approaches used in NLP. Instead of programming every
language rule manually, machine-learning models learn patterns from
examples and data.

For example, a mobile-money company could use NLP to understand customer
messages written in Somali. The system might identify whether a message
is a complaint, a request for help, or a question about an account. This
can help the company direct messages to the correct support team.

## 2. Basic NLP Terminology

The following terms are commonly used in NLP:

-   **Corpus:** A large, organized collection of texts used for language
    research or model training.
-   **Document:** One individual text item in a corpus, such as a
    review, article, or message.
-   **Token:** A unit of text produced by tokenization. A token may be a
    word, part of a word, or punctuation mark.
-   **Vocabulary:** The set of unique tokens found in a text collection.
-   **Feature:** A measurable property or numerical representation used
    by a machine-learning model.
-   **Label:** The correct category or answer assigned to an example
    during supervised learning.

### Example

Consider these three Somali restaurant reviews:

1.  "Cuntadu waa macaan."
2.  "Adeeggu waa fiican yahay."
3.  "Cuntadu ma fiicna."

If we tokenize the reviews by separating words and ignore punctuation,
the combined collection contains **10 word tokens**. The vocabulary
contains **10 unique words**:

`Cuntadu, waa, macaan, Adeeggu, fiican, yahay, ma, fiicna`

Correction: the list above contains 8 unique forms as written. If
capitalization is normalized and the words are counted exactly as they
appear in the three sentences, the vocabulary is:

`cuntadu, waa, macaan, adeeggu, fiican, yahay, ma, fiicna`

Therefore, the vocabulary size is **8**.

A possible label for each review could be `positive` or `negative`. The
first two reviews are positive, while the third is negative.

## 3. Common NLP Tasks

NLP includes several important tasks:

1.  **Text classification:** Assigning a category to a complete text.
    For example, classifying a Somali customer message as a complaint,
    question, or praise.
2.  **Sequence labeling:** Assigning a label to each token in a
    sentence. Named Entity Recognition (NER), which identifies names of
    people, places, and organizations, is one example.
3.  **Information retrieval and text similarity:** Finding documents
    relevant to a user's query or identifying texts with similar
    meanings. A search engine is a common example.
4.  **Text generation:** Producing human-readable text, such as
    answering questions, summarizing documents, or generating responses
    in a chatbot.

## 4. Supervised, Unsupervised, and Self-Supervised Learning

**Supervised learning** uses examples that contain both input data and
correct labels. For example, a model can learn to classify Somali
messages when each training message is marked as `positive`, `negative`,
or `neutral`.

**Unsupervised learning** uses data without manually supplied labels.
The system attempts to discover patterns or groups in the data. For
example, it could group Somali news articles by topic without being told
the topic of each article.

**Self-supervised learning** creates learning targets from the data
itself. For example, a language model may learn by predicting a missing
or next word in a sentence. This approach is useful because large
amounts of text can be used without manually labeling every example.

## 5. Numerical Text Representation and Bag of Words

Machine-learning algorithms generally require numerical input. NLP
therefore converts text into numerical representations.

One simple method is **Bag of Words (BoW)**. It represents a document by
counting how often each vocabulary word appears. The method does not
preserve word order or grammar.

For example, consider:

-   "Nin baa libaax dilay."
-   "Libaax baa nin dilay."

Both sentences contain the same words, so a basic Bag-of-Words
representation gives them the same word counts. However, their meanings
are different because the word order changes who performed the action.
This demonstrates one limitation of Bag of Words.

Other text-representation methods include TF-IDF, word embeddings, and
contextual embeddings produced by modern language models.

## 6. Challenges of Building NLP Systems for Somali

Somali NLP faces several challenges:

1.  **Limited training data:** There are fewer large, publicly available
    Somali datasets than datasets for widely resourced languages such as
    English.
2.  **Morphological complexity:** Somali words can contain prefixes and
    suffixes that affect their form and meaning. This makes tokenization
    and stemming or lemmatization more difficult.
3.  **Spelling variation:** People may write the same word in different
    ways, especially in informal online communication.
4.  **Dialect variation:** Differences between regional varieties can
    make it difficult to build one system that performs equally well for
    all speakers.
5.  **Code-switching:** Somali speakers sometimes mix Somali with
    English or Arabic, particularly in social media and everyday digital
    communication.
6.  **Limited language tools:** There are fewer mature Somali resources
    for spell-checking, tokenization, speech recognition, and other NLP
    tasks.

These challenges can be reduced by collecting representative data,
documenting spelling conventions, including different dialects, and
developing open-source Somali language resources.

## 7. Case Study: Somali Information Retrieval Corpus

Badel et al. (2023) introduced the **Somali Information Retrieval
Corpus**, a resource designed to support information retrieval research
for the Somali language.

The corpus contains **2,335 Somali documents** collected from sources
that include Somali news websites and poetry books. The research
addresses the shortage of dedicated Somali information-retrieval
resources.

The study also investigates query expansion using **pseudo-relevance
feedback (PRF)**. In this approach, a search system first retrieves
documents for an initial query. It then uses information from documents
judged to be relevant by the system to expand or improve the query. The
expanded query can help retrieve additional useful documents.

This work is important because it provides a resource for evaluating
Somali search systems and demonstrates methods that can improve
information retrieval in a low-resource language.

## References

-   Badel, A., et al. (2023). *Somali Information Retrieval Corpus:
    Bridging the Gap between Query Translation and Dedicated Language
    Resources*. Proceedings of the 2023 Conference on Empirical Methods
    in Natural Language Processing.
-   Bird, S., Klein, E., & Loper, E. (2009). *Natural Language
    Processing with Python*. O'Reilly Media.
-   Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent Dirichlet
    Allocation. *Journal of Machine Learning Research, 3*, 993--1022.
-   Devlin, J., Chang, M.-W., Lee, K., & Toutanova, K. (2019). BERT:
    Pre-training of Deep Bidirectional Transformers for Language
    Understanding. *Proceedings of NAACL-HLT*.
-   Hedderich, M. A., et al. (2021). A Survey on Recent Approaches for
    Natural Language Processing in Low-Resource Scenarios. *Proceedings
    of NAACL-HLT*.
-   Hirschberg, J., & Manning, C. D. (2015). Advances in Natural
    Language Processing. *Science, 349*(6245), 261--266.
-   Jurafsky, D., & Martin, J. H. (2026). *Speech and Language
    Processing* (3rd ed. draft).
-   Salton, G., Wong, A., & Yang, C. S. (1975). A Vector Space Model for
    Automatic Indexing. *Communications of the ACM, 18*(11), 613--620.
