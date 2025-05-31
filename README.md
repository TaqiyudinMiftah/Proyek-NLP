# 📱 Google Play Review Scraper & Preprocessing ✨

This project aims to **scrape Android application reviews from the Google Play Store** and perform **text preprocessing**, such as normalizing non-standard words (slang). The preprocessed data is then used for sentiment analysis.

## 🎯 Project Objective

The primary goals of this project are:
1.  **Scrape Reviews**: Collect user reviews for a specific Android application (BCA mobile app in this case) from the Google Play Store.
2.  **Text Preprocessing**: Clean and prepare the textual data for analysis. This includes:
    * Removing irrelevant characters, URLs, and numbers.
    * Case folding (converting text to lowercase).
    * Normalizing slang/colloquial Indonesian words to their standard forms.
    * Tokenizing text into individual words.
    * Filtering out stopwords (common words in Indonesian and English).
3.  **Sentiment Analysis**: Perform lexicon-based sentiment scoring to classify reviews as positive, negative, or neutral.
4.  **Preparation for Advanced NLP**: The processed data is ready for further sentiment analysis, visualization, and other advanced Natural Language Processing tasks.

## 🚀 Features

-   **Comprehensive Review Scraping**: Gathers all available reviews for an Android application using its App ID.
-   **Text Processing Pipeline**:
    -   ✅ **Tokenization**: Breaking down text into individual words or tokens.
    -   ✅ **Slang Word Conversion**: Translating non-standard (slang) words into their formal Indonesian equivalents using a lexicon.
-   **Sentiment Classification**: Analyzes sentiment polarity (positive, negative, neutral) based on a predefined lexicon.
-   **Data Visualization**: Includes generation of word clouds and sentiment distribution charts.
-   **NLP Ready**: Outputs clean, structured data suitable for advanced sentiment analysis models, topic modeling, and other NLP applications.

---

## 📚 Libraries Used

The project utilizes the following Python libraries:

* `google-play-scraper`: For scraping reviews from Google Play Store.
* `pandas`: For data manipulation and analysis, especially using DataFrames.
* `numpy`: For numerical operations.
* `matplotlib`: For creating static, animated, and interactive visualizations.
* `seaborn`: For making statistical graphics.
* `nltk` (Natural Language Toolkit): For text processing tasks like tokenization and stopword removal.
* `Sastrawi`: For Indonesian language stemming (though lexicon-based approach was primary for sentiment in the notebook).
* `wordcloud`: For generating word cloud visualizations.
* `scikit-learn` (`sklearn`): For machine learning utilities (though primarily used for `TfidfVectorizer` if a model-based approach was to be extended).
* `requests`: For making HTTP requests (e.g., to fetch lexicons).
* `xgboost`: (Imported in the notebook, potentially for future model-based sentiment analysis).

## ⚙️ How to Run

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/TaqiyudinMiftah/Proyek-NLP.git](https://github.com/TaqiyudinMiftah/Proyek-NLP.git)
    cd Proyek-NLP
    ```

2.  **Set up a Python Environment:**
    It's recommended to use a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install Dependencies:**
    Ensure you have Python installed. Install the required libraries from `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download NLTK Resources:**
    If you haven't already, download the necessary NLTK data. This can be done within a Python interpreter or by adding it to a script:
    ```python
    import nltk
    nltk.download('punkt') # 'punkt_tab' was in notebook, 'punkt' is more general
    nltk.download('stopwords')
    ```

5.  **Run the Jupyter Notebook:**
    The main analysis is performed in the `main.ipynb` Jupyter Notebook. Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
    Then, open and run the cells in `main.ipynb` to see the scraping (if enabled), preprocessing steps, sentiment analysis, and visualizations.

6.  **Data Files:**
    * The notebook loads pre-existing review data from `ulasan_aplikasi_bca.csv`. If you wish to scrape live data, you'll need to modify the scraping part of the notebook.
    * It fetches `colloquial-indonesian-lexicon.csv` from a URL for slang word normalization. Ensure an internet connection for this step if not already downloaded.

---