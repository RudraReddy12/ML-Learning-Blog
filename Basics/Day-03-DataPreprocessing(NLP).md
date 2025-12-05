# **Text Data Preprocessing**

## **1. Text Cleaning**
- Lowercasing – ensures uniformity  
- Removing punctuation – commas, periods, symbols, etc.  
- Removing numbers (depending on context)  
- Removing URLs, email IDs, hashtags, mentions  
- Removing extra whitespace  

---

## **2. Tokenization**
- Tokenization breaks text into smaller units called *tokens*.  
- Word Tokenization splits the sentence into words (tokens).  

---

## **3. Stopword Removal**
- Stopwords are common words like *"is"*, *"the"*, *"and"* that do not add meaning.  
- Helps reduce dimensionality by removing low-value words.  

---

## **4. Stemming & Lemmatization**
- **Stemming**: Removes endings of words using heuristic rules.  
  - Example: *"studies"*, *"studying"* → **"studi"**  
- **Lemmatization**: Converts words to their dictionary (root) form.  
  - Example: *"studies"*, *"studying"* → **"study"**  
- Normalizes word variations and improves model learning.

---

# **Key Points About Text Preprocessing & NLP**
- Text preprocessing is the first and most important step in any NLP pipeline.
- Raw text contains noise — cleaning removes punctuation, numbers, URLs, and unnecessary symbols.
- Lowercasing ensures uniformity and prevents treating "Apple" and "apple" as different words.
- Tokenization splits text into words or sentences so models can read them as structured units.
- Stopword removal eliminates frequent but non-informative words (the, is, in).
- Stemming reduces words to crude forms, while lemmatization provides accurate dictionary roots.
- Normalization techniques reduce vocabulary size and improve model generalization.
- Machine learning models cannot understand raw text — text must be converted into numerical vectors.
- Common vectorization methods include Bag-of-Words, TF-IDF, and word embeddings.
- Modern NLP uses Transformer-based models like BERT for contextual understanding.
- Good preprocessing improves accuracy, reduces noise, and speeds up training.
- NLP tasks include text classification, sentiment analysis, NER, summarization, translation, etc.
- Consistent preprocessing is essential — usually handled using ML pipelines.
- The quality of preprocessing directly affects the performance of NLP models.
