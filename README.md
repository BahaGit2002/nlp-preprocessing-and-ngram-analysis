# 📘 **NLP Text Cleaning and N-grams with News API**

This project demonstrates a complete NLP preprocessing pipeline applied to real-time English news articles collected via News API. It covers text extraction, cleaning, tokenization, lemmatization, stopword removal, and N-gram analysis (unigrams, bigrams, trigrams).

All experiments were performed in Google Colab.

---

## 🚀 **Project Goals**

* Collect real-time English news articles using News API
* Clean and normalize the text
* Perform tokenization and lemmatization
* Remove English stopwords
* Generate N-grams (1–3)
* Visualize the most frequent N-grams
* Build a simple and reproducible NLP preprocessing workflow

---

## 📂 **Project Structure**

```
nlp-preprocessing-and-ngram-analysis/
│
├── hw1.ipynb                      # Main Google Colab notebook
├── README.md                      # Project documentation
└── requirements.txt               # Python dependencies
```

---

## 📊 **Dataset**

The raw dataset is collected in real-time from news sources using the **News API**.

**Topics used for data collection:**
* *Artificial intelligence*
* *Machine learning*
* *Data science*

**Data source:** News API (https://newsapi.org)
- Free tier: 100 requests/day
- Up to 30 articles per topic
- Articles from the last 30 days

The text is extracted from article titles, descriptions, and content, then split into sentences and stored in a pandas DataFrame.

---

## 🔑 **Setup Requirements**

### **1. Get a News API Key**
1. Visit https://newsapi.org
2. Sign up for a free account
3. Copy your API key
4. Replace `YOUR_API_KEY_HERE` in the notebook with your actual key

### **2. Install Required Packages**
All installations are handled within the Colab notebook using:
```bash
!pip install newsapi-python
```

---

## 🧹 **Text Cleaning Steps**

Each text entry goes through the following preprocessing pipeline:

1. **Lowercasing** - Convert all text to lowercase
2. **Removing punctuation** - Strip special characters
3. **Removing numbers** - Eliminate numerical digits
4. **Tokenization** - Split text into individual words
5. **Removing stopwords** - Filter common English words
6. **Lemmatization** - Reduce words to base form
7. **Returning clean tokens** - Output processed word list

**Implemented using:**
* `nltk.word_tokenize`
* `nltk.corpus.stopwords`
* `WordNetLemmatizer`

---

## 🔠 **N-gram Generation**

Custom function `get_ngrams(tokens_list, n)` generates:

* **Unigrams (n=1)** - Single words
* **Bigrams (n=2)** - Two-word phrases
* **Trigrams (n=3)** - Three-word phrases

Frequencies are computed using:
```python
from collections import Counter
```

---

## 📈 **Visualization**

The top 10 most frequent:
* Unigrams
* Bigrams
* Trigrams

are visualized using **matplotlib** bar charts with different colors for easy distinction.

---

## 🛠 **Dependencies**

```bash
pip install pandas numpy nltk matplotlib newsapi-python
```

**NLTK data downloads (handled in notebook):**
```python
nltk.download('punkt')
nltk.download('punkt_tab')
nltk.download('stopwords')
nltk.download('wordnet')
```

---

## ▶️ **How to Run**

### **Option 1: Run in Google Colab**
1. Open the notebook: [Open In Colab](https://github.com/BahaGit2002/nlp-preprocessing-and-ngram-analysis/blob/main/hw1.ipynb)
2. Insert your News API key in the designated cell
3. Run all cells sequentially
4. Review the output DataFrames and visualizations

### **Option 2: Run Locally**
1. Clone the repository:
   ```bash
   git clone https://github.com/BahaGit2002/nlp-preprocessing-and-ngram-analysis
   cd nlp-preprocessing-and-ngram-analysis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run the Jupyter notebook
4. Add your News API key when prompted

---

## 📌 **Results**

The project produces:

✔ A cleaned dataset with tokenized and lemmatized text  
✔ Unigram, bigram, and trigram frequency lists  
✔ Visual charts of top N-grams  
✔ A reusable NLP preprocessing pipeline  
✔ Real-time news data analysis capabilities

---

## 🎯 **Customization**

You can easily modify the project to analyze different topics:

```python
topics = ["technology", "climate change", "cryptocurrency"]
```

Or adjust the number of articles per topic:

```python
page_size=50  # Increase up to 100 for free tier
```

---

## 📜 **License**

This project is open-source and available under the MIT License.

---

## 🤝 **Contributions**

Pull requests and improvements are welcome.  
Feel free to fork the project and experiment with other datasets or NLP methods.

---

## 👤 **Author**

**Zhakshylykov Baktiyar**

GitHub: [@BahaGit2002](https://github.com/BahaGit2002)

---

## 🙏 **Acknowledgments**

- News API for providing real-time news data
- NLTK for comprehensive NLP tools
- Google Colab for free computing resources