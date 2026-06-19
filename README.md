# 🧠 Emotion-Aware System

A Flask web app that detects the emotion in your text and responds with a matching motivational quote.

``

## Dataset
Source: https://www.kaggle.com/datasets/prajwalnayakat/text-emotion

The original dataset contains multiple emotion categories. To improve class balance and simplify the classification task, several labels were merged during preprocessing:

    Original Label	Mapped Label
    fun	happiness
    enthusiasm	happiness
    relief	happiness
    empty	sadness
    Final emotion classes:

    anger
    happiness
    hate
    love
    neutral
    sadness
    surprise

``
## How It Works

1. User submits a text input
2. Text is preprocessed and vectorized
3. A trained ML model predicts the emotion
4. A relevant quote is fetched and displayed

**Detected emotions:** `happy` · `sad` · `angry` · `fear` · `surprise`

## Project Structure

```
emotion-aware-system/
├── app.py              # Flask app & prediction logic
├── utils.py            # Text preprocessing
├── model.pkl           # Trained ML model
├── vectorizer.pkl      # TF-IDF vectorizer
├── quotes.csv          # Emotion-tagged quotes
└── templates/          # HTML templates
```

## Setup

```bash
# Clone the repo
git clone https://github.com/m4hbuhs/emotion-aware-system.git
cd emotion-aware-system

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
```

Then open `http://localhost:10000` in your browser.

## Tech Stack

- **Python** · Flask · scikit-learn · pandas
- **Frontend** · HTML/CSS 