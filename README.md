# 🚗 Car-ing is Sharing - AI Chatbot



An AI-powered chatbot prototype for automotive sales and rental services using Hugging Face LLMs.

## 🌟 Features

| Feature          | Model Used                                 | Example Use Case              |
|------------------|--------------------------------------------|-------------------------------|
| Sentiment Analysis | `distilbert-base-uncased-finetuned-sst-2-english` | Classify customer reviews      |
| Translation      | `Helsinki-NLP/opus-mt-en-es`               | Translate English reviews to Spanish |
| Q&A              | `deepset/minilm-uncased-squad2`            | Answer customer questions     |
| Summarization    | `facebook/bart-large-cnn`                  | Condense lengthy reviews      |

## 🛠️ Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-repo/car-ing-ai.git
   cd car-ing-ai
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Jupyter Notebook**
   ```bash
   jupyter notebook notebook.ipynb
   ```

## 📂 File Structure

```bash
.
├── notebook.ipynb             # Main notebook with all functionality
├── data/
│   ├── car_reviews.csv        # Review dataset (format: Review;Class)
│   └── reference_translations.txt  # Translation references
├── requirements.txt           # Python dependencies
├── README.md                  # This documentation
└── car.jpeg                   # Brand image
```

## 📊 Performance Metrics

| Task               | Metric      | Score  |
|--------------------|-------------|--------|
| Sentiment Analysis | F1 Score    | 0.857  |
| Translation        | BLEU Score  | 0.602  |

## 💻 Code Examples

**Sentiment Analysis**
```python
sentiment = sentiment_model("The ride quality is exceptional")
# {'label': 'POSITIVE', 'score': 0.998}
```

**Translation**
```python
translated = translator("Comfortable seats and great mileage", max_length=50)
# {'translation_text': 'Asientos cómodos y gran kilometraje'}
```

## 🤖 Model Details

| Model      | Task              | Input               | Output            |
|------------|-------------------|---------------------|-------------------|
| DistilBERT | Sentiment Analysis | Customer review     | POSITIVE/NEGATIVE |
| OPUS-MT    | Translation        | English text        | Spanish text      |
| MiniLM     | Q&A               | (question, context) | Answer            |
| BART       | Summarization     | Long review         | Short summary     |


## 📜 License

Proprietary software - © 2023 Car-ing is Sharing LLC
