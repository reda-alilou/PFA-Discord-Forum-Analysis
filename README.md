# PFA: Discord Forum Analysis

## Analyzing Forum Interactions: Categorization on Discord Technical Communities

A comprehensive data analysis project focused on understanding engagement patterns, user behavior, and question categorization in Discord-based technical communities, specifically targeting the FreeCodeCamp server.

## 🎯 Project Overview

This project analyzes scraped discussions from Discord technical forums to:

- **Classify types of technical questions** using machine learning
- **Predict potential engagement levels** based on content and posting patterns
- **Understand community dynamics** through temporal and behavioral analysis
- **Identify optimal response strategies** for forum moderators and active users

## 📊 Dataset Overview

### Data Volume (as of June 2025)

- **Categories**: 4 (JavaScript, HTML, CSS, Python)
- **Threads**: 1,062 total discussions
- **Answers**: 8,290 community responses
- **Time Span**: September 2022 - June 2025

### Database Schema

The project uses three main tables:

- `categories` - Topic classifications (HTML, CSS, JS, Python)
- `threads` - Original questions and metadata
- `answers` - Community responses with timestamps

## 📁 Project Structure

```
PFA/
├── data/
│   ├── manual_labels/
│   │   └── questions_to_label.csv
│   └── processed/
│       ├── answers_clean.csv
│       ├── categories.csv
│       ├── threads_clean.csv
│       └── user_stats.csv
├── notebooks/
│   ├── 01-cleaning.ipynb
│   ├── 02-eda-visualizations.ipynb
│   └── 03-question-classification.ipynb
└── reports/
    ├── [19 visualization files]
    └── top_20_threads_by_replies.csv

```

## 🔧 Setup and Installation

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Required packages (see requirements below)

### Installation

```bash
git clone https://github.com/yourusername/PFA.git
cd PFA
pip install -r requirements.txt

```

### Key Dependencies

```
pandas
numpy
matplotlib
seaborn
scikit-learn
wordcloud
spacy
nltk
plotly

```

## 🚀 Usage

### 1. Data Cleaning and Preprocessing

```bash
jupyter notebook notebooks/01-cleaning.ipynb

```

- Text sanitization and normalization
- User activity metrics calculation
- Bot detection and filtering
- Timestamp standardization

### 2. Exploratory Data Analysis

```bash
jupyter notebook notebooks/02-eda-visualizations.ipynb

```

- Temporal pattern analysis
- Content metrics and word clouds
- User behavior analysis
- Engagement metrics

### 3. Question Classification

```bash
jupyter notebook notebooks/03-question-classification.ipynb

```

- Text preprocessing pipeline
- Manual categorization integration
- Machine learning model training
- Performance evaluation

## 📈 Key Findings

### Community Engagement Patterns

- **Peak Activity**: Weekdays 14:00-18:00, especially Thursday-Friday
- **Response Time**: 75% of questions receive replies within 2 hours
- **Thread Depth**: Most threads resolved with 0-3 answers

### Content Analysis

- **Dominant Topics**: JavaScript leads with 391 threads, followed by HTML (293) and CSS (246)
- **Question Types**: 37% Bug Help, 33% General Discussion, 18% Learning Questions
- **User Behavior**: Power-law distribution with most users posting 1-5 times

### Classification Results

- **Best Model**: Random Forest (41% accuracy)
- **Challenge**: Class imbalance affecting rare categories
- **Insight**: Need for balanced training data or weighted models

## 📊 Visualizations

The project generates 19 comprehensive visualizations including:

- Activity heatmaps by day/hour
- Response time distributions
- Message volume trends
- Word clouds for questions/answers
- User activity patterns
- Engagement metrics by category

## 🤖 Machine Learning Pipeline

### Text Preprocessing

1. **Cleaning**: Lowercase, URL/HTML removal, special character handling
2. **Tokenization**: Stop word removal, lemmatization
3. **Vectorization**: TF-IDF with unigrams and bigrams (3000 features)

### Classification Models

- **Naive Bayes**: 40% accuracy, biased toward majority class
- **Linear SVM**: 34% accuracy, better class distribution
- **Random Forest**: 41% accuracy, best overall performance

### Categories

- Bug Help
- General Discussion
- Learning Question
- Resource Request
- Career Advice
- Code Review

## 🔍 Data Quality

- **Completeness**: 100% - No missing values in critical fields
- **Cleanliness**: All text sanitized, timestamps standardized
- **Bot Detection**: ~6% of responses flagged as bot-generated
- **Validation**: Manual verification of 280 question labels

## 📋 Future Work

### Model Improvements

- Address class imbalance with oversampling/class weights
- Implement deep learning approaches (BERT, transformers)
- Cross-validation with different train/test splits

### Analysis Extensions

- Sentiment analysis of questions and answers
- Topic modeling with LDA/BERT-topic
- User journey analysis and retention patterns
- Automated response quality assessment

### Feature Engineering

- Include user history features
- Thread timing and seasonal patterns
- Cross-category interaction analysis

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://claude.ai/chat/LICENSE) file for details.

## 🙏 Acknowledgments

- FreeCodeCamp Discord community for providing the data source
- Contributors to the manual question labeling process
- Open source libraries that made this analysis possible

## 📞 Contact

For questions or collaboration opportunities, please open an issue or contact the project maintainers.
