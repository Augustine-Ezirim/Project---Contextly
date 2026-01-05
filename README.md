# Project---Contextly
# CONTEXTLY  
### Real-Time Emotional Intelligence for Remote Team Communication

CONTEXTLY is a machine learning–powered prototype that detects emotional tone in text messages and visualizes it in real time.  
The project addresses a core problem in remote work: **loss of emotional context in text-based communication**, which often leads to misinterpretation, friction, and reduced team effectiveness.

Built as part of **MA 707 – Machine Learning (Bentley University)**, this project combines **NLP modeling, product design, and business strategy** into a single end-to-end solution.

---

## Problem Statement

Remote and hybrid teams rely heavily on tools like Slack and Microsoft Teams.  
While efficient, text-based communication strips away emotional cues, often causing messages to be perceived as:

- Harsh or dismissive  
- Passive-aggressive  
- Emotionally ambiguous  

These misinterpretations lead to unnecessary conflict, slower collaboration, and increased stress across teams.

---

## Solution Overview

CONTEXTLY restores emotional clarity to workplace messaging by:

- Analyzing message tone **in real time**
- Classifying messages into **8 emotional states**
- Displaying subtle emotional cues directly within the chat interface

The solution is designed to be **non-intrusive**, requiring no workflow changes or message rewriting.

**Target users:**  
Remote teams, managers, HR & People Operations teams.

---

## Machine Learning Approach

### Emotion Classification
- **Model:** Fine-tuned **DistilRoBERTa**
- **Task:** Multi-class emotion classification
- **Emotion classes (8):**
  - Joy
  - Love
  - Surprise
  - Anger
  - Sadness
  - Fear
  - Disgust
  - Neutral

### Model Performance
- **Evaluation:** 10% held-out test set
- **Metric:** Accuracy & F1-score
- **Result:** ~84% balanced performance across classes

---

## Text Preprocessing

To improve robustness on real-world chat messages, preprocessing included:

- Emoji conversion to textual meaning
- Slang expansion
- Reduction of exaggerated spelling (e.g., “soooo” → “soo”)
- Whitespace normalization

This ensured consistent inputs for model inference while preserving emotional signal.

---

## Emotion-to-Color Mapping

Each predicted emotion is mapped to a consistent color, allowing users to **visually interpret tone instantly** without disrupting conversation flow.

| Emotion   | Color |
|---------|-------|
| Joy     | Green |
| Love    | Pink |
| Surprise| Yellow |
| Anger   | Red |
| Sadness | Blue |
| Fear    | Purple |
| Disgust | Brown |
| Neutral | Gray |

---

## System Design (Prototype)

The conceptual architecture separates concerns for scalability:

1. **Message ingestion**
2. **Text preprocessing**
3. **ML inference**
4. **Emotion + confidence output**
5. **UI visualization (Slack-style interface)**

While this repository focuses on the **ML and prototype layer**, the system is designed to integrate seamlessly with collaboration platforms.

---

## Business & Product Perspective

- **Business Model:** B2B SaaS (per-seat or per-team pricing)
- **Value Proposition:**  
  Reduced miscommunication → faster alignment → lower conflict & turnover
- **Differentiation:**  
  Real-time, message-level emotional insight (not retrospective surveys)

---

## Future Enhancements

**Machine Learning**
- Larger, domain-specific datasets
- Emotion smoothing across conversations
- Context-aware emotion transitions

**Product**
- Slack API integration
- Expansion to Microsoft Teams
- Team-level sentiment analytics dashboards

---

## Team

- Augustine Ezirim  
- Kingsolomon Ehinola  
- Mitchel Igolimah  
- Nyasha Sibanda  

