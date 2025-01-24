# User Feedback and Station Management with AI: Sentiment Analysis and Topic Modeling for the Munich Stammstrecke Network

## About the Project
This repository contains the resources, datasets, and scripts used in the thesis titled **"User Feedback and Station Management with AI: Sentiment Analysis and Topic Modeling for the Munich Stammstrecke Network"**. The study explores the integration of AI tools into public transportation infrastructure management, focusing on Munich's Stammstrecke train stations.

## Table of Contents
- [Overview](#overview)
- [Datasets](#datasets)
- [Methodology](#methodology)
- [Tools and Techniques](#tools-and-techniques)
- [Results](#results)
- [How to Use](#how-to-use)
- [License](#license)

## Overview
Efficient station management is critical for improving user satisfaction and meeting urban mobility goals. This project applies sentiment analysis and topic modeling on user-generated feedback collected from Google Maps reviews to:
- Quantify user sentiment
- Identify key themes
- Propose actionable recommendations

## Datasets

### Data Sources
- **Primary Source**: User reviews from Google Maps for 10 Munich Stammstrecke stations (2019–2024).
  - [Review dataset](data/processed.xlsx)
  - [Sentiment dataset](data/sentimet.xlsx)
  - [Topic modelling dataset](data/topic/.xlsx)
  - [Interview questionare](data/interview.pdf)
- **Ethics**: Data is publicly available; no personally identifiable information was collected.

### Data Details
- **Total Reviews**: 7,043 collected, 3,592 validated.
- **Features**: Review text, star rating, date, station name, etc.

## Methodology
1. **Data Preprocessing**: Cleaning, tokenization, stopword removal, stemming, and lemmatization.
2. **Sentiment Analysis**: Using RoBERTa and IBM Watson Natural Language Understanding to classify sentiment and detect emotions.
3. **Topic Modeling**: Using BERTopic and Llama 2 to identify themes in feedback.
4. **Urgency Classification**: Categorizing feedback into immediate, short-term, and long-term priorities.

## Tools and Techniques
- **Sentiment Analysis**: RoBERTa (Hugging Face) and IBM Watson NLU.
- **Topic Modeling**: BERTopic and Llama 2.
- **Data Preprocessing**: Python libraries (NLTK, SpaCy, Pandas).
- **Visualization**: Tableau

## Results
- **Sentiment Distribution**:
  - Positive: 25.8%
  - Neutral: 51.9%
  - Negative: 22.3%
- **Key Topics**: Cleanliness, infrastructure, crowding, customer service, accessibility.
- **Recommendations**:
  - Implement dynamic resource allocation.
  - Scale feedback systems for multimodal networks.

## How to Use

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/station-feedback-ai.git
   cd station-feedback-ai

### Running the Analysis

#### 1.	Preprocess Data
Clean and prepare the raw dataset for analysis:
   ```bash
python src/preprocessing/clean_data.py
```
#### 2.	Run Sentiment Analysis
Perform sentiment analysis on user reviews:	
   ```bash
python src/sentiment_analysis/analyze_sentiment.py
```
#### 3.	Generate Topics
Use topic modeling to identify themes in user feedback:
   ```bash
python src/topic_modeling/model_topics.py
```
#### 4.	Classify Urgency
Categorize feedback into urgency levels (immediate, short-term, long-term):
   ```bash
python src/classification/urgency_classification.py
```

## License
This project is licensed under the MIT License.
