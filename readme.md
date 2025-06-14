# Aceh Political Sentiment Analysis Application

## 📊 Overview

This web application performs sentiment analysis on tweets related to local political parties in Aceh, Indonesia. It analyzes public sentiment towards Aceh's political landscape using both traditional machine learning and advanced deep learning approaches. The dataset consists of 8,000+ tweets collected from the X platform (formerly Twitter), covering the period from the 2019 Election (April 17, 2019) to the 2024 Aceh Pilkada (November 27, 2024).

## 🚀 Features

- **Sentiment Analysis**: Analyze tweets using two models:
  - **Naive Bayes**: Classic machine learning approach for text classification
  - **IndoBERT**: Advanced deep learning model specifically trained for Indonesian language
  - **Comparison Mode**: Compare results from both models side by side

- **Interactive Dataset Exploration**:
  - Browse and search through the tweet dataset
  - Filter tweets using regex, exact match, or contains methods
  - Select any tweet for immediate sentiment analysis

- **Topic Modeling**: Discover key themes in political discussions using Latent Dirichlet Allocation (LDA)

- **Visualization**: View data distribution and word frequency visualizations

## 🔧 Installation

```bash
# Clone the repository
git clone [repository-url]
cd Streamlit-Web-Twitter-Aceh-Another-GH

# Create and activate a virtual environment (optional but recommended)
python -m venv venv
# On Windows
venv\Scripts\activate
# On Unix/MacOS
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## 🔑 Configuration

The application requires API keys for the IndoBERT model. Create a `.env` file with:

```
api_url=your_indobert_api_url
api_key=your_indobert_api_key
```

## 🖥️ Usage

```bash
streamlit run main.py
```

Navigate to the provided local URL (typically http://localhost:8501) in your web browser.

## 📂 Project Structure

- `main.py`: Main Streamlit application
- `indobert.py`: IndoBERT model implementation
- `data/database.csv`: Dataset of political tweets
- `image/`: Directory containing visualizations

## 🔍 Data Processing Pipeline

1. **Data Collection**: Tweets gathered using the Twitter API with specific parameters
2. **Preprocessing**:
   - Data cleaning (removing irrelevant elements)
   - Case folding (converting to lowercase)
   - Tokenization using NLTK
   - Normalization of non-standard words
   - Stopwords removal using NLTK
   - Stemming using Sastrawi

## 💻 Technology Stack

- **Frontend**: Streamlit
- **Machine Learning**: Naive Bayes, IndoBERT
- **NLP Processing**: NLTK, Sastrawi
- **Data Analysis**: pandas, NumPy
- **Visualization**: Matplotlib, Streamlit native components

## 📣 Acknowledgments

- Dataset collected ethically in accordance with platform policies
- Special thanks to contributors and the Aceh community
