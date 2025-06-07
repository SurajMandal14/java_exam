# NLP Assignment Answers

## Section A: NLP Pipeline and Concepts

### 1. Phases of NLP Pipeline

#### a. List and briefly describe five distinct phases commonly found in an NLP pipeline (e.g., Lexical Analysis, Syntactic Analysis, etc.).

1.  **Lexical Analysis:** This is the first phase, involving the identification and analysis of the structure of words. It includes tokenization, stemming, and lemmatization.
2.  **Syntactic Analysis:** This phase focuses on the arrangement of words to form phrases and sentences. It involves parsing and dependency analysis to understand the grammatical structure.
3.  **Semantic Analysis:** This phase derives the meaning of sentences by analyzing the relationships between words and phrases. It involves word sense disambiguation and semantic role labeling.
4.  **Discourse Integration:** This phase considers the context of the text and the meaning of sentences in relation to each other. It involves co-reference resolution and discourse parsing.
5.  **Pragmatic Analysis:** This final phase deals with the interpretation of the text in its intended context, considering the speaker's intentions and the overall communicative goal.

#### b. For each phase, explain its primary goal and provide a concrete example using the sentence: "The cat sat on the mat."

1.  **Lexical Analysis:**
    *   **Goal:** To break down the sentence into individual words (tokens) and analyze their basic properties.
    *   **Example:**
        *   Tokens: "The", "cat", "sat", "on", "the", "mat"
        *   Identifying "cat" and "mat" as nouns.
2.  **Syntactic Analysis:**
    *   **Goal:** To determine the grammatical structure of the sentence.
    *   **Example:**
        *   Parsing the sentence to identify the subject (The cat), verb (sat), and prepositional phrase (on the mat).
3.  **Semantic Analysis:**
    *   **Goal:** To understand the meaning of the sentence.
    *   **Example:**
        *   Understanding that "sat" describes an action performed by "cat" on "mat".
4.  **Discourse Integration:**
    *   **Goal:** To understand how this sentence relates to other sentences in a larger text.
    *   **Example:**
        *   If a previous sentence mentioned "a fluffy animal," understanding that "The cat" refers to the same animal.
5.  **Pragmatic Analysis:**
    *   **Goal:** To understand the intended meaning of the sentence in a real-world context.
    *   **Example:**
        *   Understanding that the sentence is a simple statement of fact, not a metaphor or a question.

#### c. Discuss how errors in earlier phases can impact the later stages of the NLP pipeline.

Errors in earlier phases can propagate and compound in later phases, leading to incorrect interpretations. For example, if tokenization incorrectly splits a word, syntactic analysis will fail to parse the sentence correctly. Similarly, if syntactic analysis misidentifies the grammatical structure, semantic analysis will derive an incorrect meaning. These errors can cascade through the pipeline, resulting in a complete misunderstanding of the text.

### 2. NLP Tasks and the Role of Knowledge

#### a. Identify and describe at least four different NLP tasks (e.g., Named Entity Recognition, Sentiment Analysis, Machine Translation, etc.).

1.  **Named Entity Recognition (NER):** Identifying and classifying named entities in text, such as people, organizations, locations, dates, and quantities.
2.  **Sentiment Analysis:** Determining the emotional tone or attitude expressed in a piece of text (e.g., positive, negative, neutral).
3.  **Machine Translation:** Automatically translating text from one language to another.
4.  **Text Summarization:** Generating a concise summary of a longer text while preserving its key information.

#### b. Explain the role of background knowledge (such as world knowledge or domain knowledge) in improving the performance of NLP systems.

Background knowledge provides context and information that is not explicitly stated in the text, but is necessary for accurate interpretation. World knowledge includes general facts about the world, while domain knowledge is specific to a particular field or subject. For example, in sentiment analysis, knowing that "amazing" is a positive word requires world knowledge. In medical text analysis, understanding the relationships between diseases and symptoms requires domain knowledge.

### 3. Ambiguity in NLP

#### a. Define ambiguity in the context of NLP.

Ambiguity in NLP refers to the situation where a word, phrase, or sentence can have multiple possible interpretations. This can arise at different levels of linguistic analysis.

#### b. Provide examples of ambiguity that can occur at different phases of the NLP pipeline.

1.  **Lexical Ambiguity:** A word has multiple meanings.
    *   **Example:** "bank" can refer to a financial institution or the side of a river.
2.  **Syntactic Ambiguity:** A sentence can have multiple possible grammatical structures.
    *   **Example:** "I saw the man on the hill with a telescope." (Who has the telescope?)
3.  **Semantic Ambiguity:** The meaning of a sentence is unclear due to the ambiguity of the words or phrases.
    *   **Example:** "The chicken is ready to eat." (Is the chicken ready to be cooked, or ready to be eaten?)
4.  **Pragmatic Ambiguity:** The intended meaning of the speaker is unclear.
    *   **Example:** "Can you pass the salt?" (Is this a genuine question about ability, or a request?)

## Section B: Applications and Challenges

### 4. NLP Applications

#### a. Identify and describe five real-world applications of NLP across different industries.

1.  **Customer Service Chatbots:** Automating customer support by understanding and responding to customer inquiries.
2.  **Sentiment Analysis in Marketing:** Analyzing customer reviews and social media posts to understand brand perception and customer satisfaction.
3.  **Machine Translation for Global Communication:** Enabling communication and content localization across different languages.
4.  **Information Extraction in Healthcare:** Extracting relevant information from medical records and research papers to improve patient care and accelerate research.
5.  **Spam Detection in Email:** Filtering out unwanted and malicious emails based on their content and structure.

#### b. For one application of your choice, list potential data sources that could be used to train and operate the NLP system.

**Application:** Sentiment Analysis in Marketing

**Data Sources:**

1.  **Customer Reviews:** Online reviews from e-commerce platforms (e.g., Amazon, Yelp) and review websites.
2.  **Social Media Posts:** Tweets, Facebook posts, and other social media content mentioning the brand or product.
3.  **Surveys:** Customer feedback collected through surveys and questionnaires.
4.  **Customer Service Interactions:** Transcripts of chat logs and recordings of phone calls with customer service representatives.
5.  **News Articles and Blog Posts:** Media coverage and online commentary about the brand or product.

### 5. NLP Challenges

#### a. List and explain four significant challenges faced in NLP research and applications.

1.  **Ambiguity:** Natural language is inherently ambiguous, making it difficult for NLP systems to accurately interpret the meaning of text.
2.  **Context Dependence:** The meaning of words and sentences can vary depending on the context in which they are used, requiring NLP systems to have a strong understanding of context.
3.  **Sarcasm and Irony:** Detecting sarcasm and irony is challenging for NLP systems because they often rely on subtle cues and background knowledge.
4.  **Low-Resource Languages:** Developing NLP systems for languages with limited data and resources is difficult due to the lack of training data and linguistic tools.

#### b. For two of these challenges, suggest possible strategies or research directions to address them.

1.  **Ambiguity:**
    *   **Strategy:** Develop more sophisticated models that can consider multiple levels of linguistic analysis and integrate background knowledge to disambiguate text.
    *   **Research Direction:** Explore the use of deep learning techniques, such as attention mechanisms and transformers, to capture long-range dependencies and contextual information.
2.  **Context Dependence:**
    *   **Strategy:** Incorporate contextual information from multiple sources, such as surrounding sentences, documents, and external knowledge bases, to improve the accuracy of NLP systems.
    *   **Research Direction:** Investigate the use of knowledge graphs and semantic networks to represent and reason about contextual information.

## Section C: Text Preprocessing and Representation

### 6. Tokenization, Stemming, and Lemmatization

#### a. Define tokenization and describe three types (word, sentence, subword). Provide examples using the text: "NLP is fascinating! It's used in many cutting-edge applications."

**Tokenization:** The process of breaking down a text into individual units called tokens.

**Types of Tokenization:**

1.  **Word Tokenization:** Splitting the text into individual words.
    *   **Example:** \["NLP", "is", "fascinating", "!", "It's", "used", "in", "many", "cutting-edge", "applications", "."]
2.  **Sentence Tokenization:** Splitting the text into individual sentences.
    *   **Example:** \["NLP is fascinating!", "It's used in many cutting-edge applications."]
3.  **Subword Tokenization:** Splitting the text into subword units, such as morphemes or character n-grams.
    *   **Example:** \["NL", "P", "is", "fas", "cin", "ating", "!", "It", "'s", "used", "in", "many", "cut", "ting", "-", "edge", "app", "lic", "ations", "."]

#### b. Define stemming and lemmatization.

**Stemming:** The process of reducing words to their root form by removing suffixes.

**Lemmatization:** The process of reducing words to their base or dictionary form (lemma) by considering the word's meaning and context.

#### c. Show the output for the words "running", "better", and "studies" after applying a common stemmer and a lemmatizer.

| Word      | Stemmer Output | Lemmatizer Output |
| --------- | -------------- | ----------------- |
| running   | run            | running           |
| better    | better         | good              |
| studies   | studi          | study             |

#### d. Discuss when you would choose stemming over lemmatization, and vice versa.

*   **Stemming:** Choose stemming when speed and simplicity are more important than accuracy. Stemming is faster and requires less computational resources, but it can produce incorrect or non-words.
*   **Lemmatization:** Choose lemmatization when accuracy and meaningful base forms are important. Lemmatization is slower and requires more computational resources, but it produces more accurate and linguistically valid results.

### 7. Inflectional vs. Derivational Morphology

#### a. Define inflectional and derivational morphology.

**Inflectional Morphology:** The process of modifying a word to express grammatical features such as tense, number, and gender, without changing the word's core meaning or category.

**Derivational Morphology:** The process of creating new words from existing words by adding prefixes or suffixes, often changing the word's meaning or category.

#### b. Provide examples for each.

**Inflectional Morphology:**

*   walk -> walks (number)
*   walk -> walked (tense)

**Derivational Morphology:**

*   happy -> unhappy (meaning change)
*   write -> writer (category change)

## Section D: Text Representation and Vocabulary

### 8. Vocabulary Construction and Zipf’s Law

#### a. Explain what a "vocabulary" is in NLP and how it is constructed from a corpus.

In NLP, a "vocabulary" is the set of unique words or tokens present in a corpus of text. It is constructed by:

1.  **Tokenizing** the corpus into individual words or tokens.
2.  **Removing** punctuation, special characters, and stop words (optional).
3.  **Lowercasing** all words to treat different cases as the same word (optional).
4.  **Counting** the frequency of each word or token.
5.  **Selecting** the most frequent words to include in the vocabulary (optional).

#### b. Discuss the implications of vocabulary size and how out-of-vocabulary (OOV) words are handled.

*   **Implications of Vocabulary Size:**
    *   **Large Vocabulary:** Can capture more nuances and information, but requires more memory and computational resources.
    *   **Small Vocabulary:** Requires less memory and computational resources, but may miss important information and lead to OOV issues.
*   **Handling OOV Words:**
    *   **Ignore:** Simply ignore OOV words, which can lead to information loss.
    *   **Replace with UNK Token:** Replace all OOV words with a special "unknown" token, which allows the model to handle them without knowing their specific meaning.
    *   **Subword Tokenization:** Use subword tokenization to break down OOV words into smaller units that are already in the vocabulary.

#### c. State Zipf’s Law and explain its significance in NLP.

**Zipf’s Law:** States that the frequency of a word is inversely proportional to its rank in the frequency table. In other words, the most frequent word appears approximately twice as often as the second most frequent word, three times as often as the third most frequent word, and so on.

**Significance in NLP:**

*   **Vocabulary Distribution:** Zipf's Law highlights the skewed distribution of words in natural language, with a few words occurring very frequently and many words occurring rarely.
*   **Vocabulary Size:** It helps in determining the optimal vocabulary size for NLP models, as including very rare words may not significantly improve performance.
*   **Data Sparsity:** It contributes to the data sparsity problem in NLP, where many words have limited occurrences, making it difficult to train robust models.

### 9. Bag of Words (BoW) and TF-IDF

#### a. Explain the Bag of Words model and construct BoW vectors for the documents:

*   Doc1: "The quick brown fox"
*   Doc2: "The lazy brown dog"

**Bag of Words (BoW) Model:** A simple text representation technique that represents a document as an unordered collection of words, ignoring grammar and word order.

**BoW Vectors:**

*   Vocabulary: \["The", "quick", "brown", "fox", "lazy", "dog"]
*   Doc1: \[1, 1, 1, 1, 0, 0]
*   Doc2: \[1, 0, 1, 0, 1, 1]

#### b. List two limitations of the BoW model.

1.  **Ignores Word Order:** The BoW model does not consider the order of words in a document, which can lead to loss of important information.
2.  **Ignores Semantics:** The BoW model treats all words as independent and does not capture the semantic relationships between them.

#### c. Define Term Frequency (TF) and Inverse Document Frequency (IDF).

**Term Frequency (TF):** The number of times a term appears in a document.

**Inverse Document Frequency (IDF):** A measure of how rare a term is across a corpus of documents. It is calculated as the logarithm of the total number of documents divided by the number of documents containing the term.

#### d. Given the corpus:

*   Doc A: "NLP is fun fun fun"
*   Doc B: "Deep learning is fun"
*   Doc C: "NLP and deep learning"

Calculate the TF-IDF score for the term "fun" in Doc A

**Calculations:**

*   TF("fun", Doc A) = 3 / 5 (3 occurrences of "fun" in Doc A, 5 total words in Doc A)
*   IDF("fun") = log(3 / 2) (3 total documents, 2 documents containing "fun")
*   TF-IDF("fun", Doc A) = TF("fun", Doc A) * IDF("fun") = (3 / 5) * log(3 / 2) ≈ 0.243

### 10. Regular Expressions in NLP

Write regular expressions for the following:

#### a. All strings with two consecutive repeated words.

`\b(\w+)\s+\1\b`

#### b. Date strings in the format YYYY-MM-DD.

`\d{4}-\d{2}-\d{2}`

#### c. The word "book" or "books" (case-insensitive).

`[Bb]ooks?`

#### d. Nepal Telecom phone numbers.

`98[4-6]\d{7}`

### 11. Short Notes

Write short notes (3-5 sentences each) on:

#### a. NLP Challenges

NLP faces several challenges, including ambiguity, context dependence, and the need for large amounts of training data. Ambiguity arises from the multiple possible interpretations of words and sentences, making it difficult for NLP systems to accurately understand text. Context dependence requires NLP systems to consider the surrounding text and background knowledge to correctly interpret the meaning of words and sentences. The need for large amounts of training data can be a barrier to developing NLP systems for low-resource languages and specialized domains.

#### b. NLP Applications

NLP has a wide range of applications across different industries, including customer service, marketing, healthcare, and finance. Customer service chatbots use NLP to understand and respond to customer inquiries, automating support and improving customer satisfaction. Sentiment analysis in marketing uses NLP to analyze customer reviews and social media posts, providing insights into brand perception and customer preferences. Information extraction in healthcare uses NLP to extract relevant information from medical records and research papers, improving patient care and accelerating research.

#### c. The use of Python in NLP

Python is a popular programming language for NLP due to its ease of use, extensive libraries, and large community support. Libraries such as NLTK, spaCy, and scikit-learn provide a wide range of tools and resources for NLP tasks, including tokenization, stemming, lemmatization, and machine learning. Python's clear syntax and extensive documentation make it easy for developers to learn and use, while its large community provides ample support and resources for solving NLP problems.
