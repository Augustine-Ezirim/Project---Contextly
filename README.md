# Project---Contextly
# CONTEXTLY
### Real-Time Emotional Intelligence for Text-Based Team Communication

CONTEXTLY is an applied machine learning project that detects emotional tone in text messages and visualizes it using a color-based interface. The goal is to reduce miscommunication in remote and hybrid teams where emotional cues are often lost in text-only conversations.

This project was developed as the final project for **MA 707 – Machine Learning** at **Bentley University**, combining natural language processing, system design, and product thinking.

---

## Problem Motivation

Modern teams rely heavily on tools like Slack and Microsoft Teams. While efficient, text-based communication removes emotional context, often causing messages to be interpreted as harsh, dismissive, or emotionally ambiguous. These misunderstandings lead to friction, slower collaboration, and unnecessary conflict.

---

## Solution Overview

CONTEXTLY introduces a real-time emotional intelligence layer for text communication by:
- Analyzing message tone using a trained NLP model
- Classifying messages into eight emotional categories
- Mapping predicted emotions to distinct colors for fast visual interpretation

The system is designed to be non-intrusive, lightweight, and extensible for future chat integrations.

---

## Machine Learning Approach

### Emotion Classification
- Model: Fine-tuned DistilRoBERTa
- Task: Multi-class emotion classification
- Emotion classes:
  - Joy
  - Love
  - Surprise
  - Anger
  - Sadness
  - Fear
  - Disgust
  - Neutral

### Text Preprocessing
- Emoji conversion to text
- Slang expansion
- Reduction of exaggerated spelling (e.g., “soooo” → “soo”)
- Whitespace normalization

### Evaluation
- Test split: 10% held-out data
- Metrics: Accuracy and F1-score
- Performance: Approximately 84% balanced performance across emotion classes

---

## Emotion-to-Color Mapping

| Emotion   | Color |
|----------|-------|
| Joy      | Green |
| Love     | Pink  |
| Surprise | Yellow|
| Anger    | Red   |
| Sadness  | Blue  |
| Fear     | Purple|
| Disgust  | Brown |
| Neutral  | Gray  |

---

## Tools and Technologies

- Python
- Hugging Face Transformers
- PyTorch
- scikit-learn
- Jupyter Notebook
- Google Colab

---

## Limitations and Future Work

- This implementation is a prototype and not a live chat integration
- Future improvements include:
  - Emotion smoothing across conversational context
  - Domain-specific fine-tuning
  - Integration with Slack or Microsoft Teams
  - Team-level sentiment analytics dashboards

---

## Contributors

- Augustine Ezirim
- Kingsolomon Ehinola
- Mitchel Igolimah
- Nyasha Sibanda


