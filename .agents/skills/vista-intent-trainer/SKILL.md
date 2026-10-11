---
name: vista-intent-trainer
description: Step-by-step workflow for updating Citizen Charter intents and retraining the VISTA scikit-learn NLP model.
---

# VISTA Intent Trainer Skill

## Purpose
Use this skill when adding new inquiry intents, modifying chatbot response templates, or retraining the NLP model.

## Dataset Location
- Primary dataset: `backend/data/answers.json`
- Model output: `backend/models/intent_model.joblib` and `backend/models/tfidf_vectorizer.joblib`

## Workflow Steps
1. **Add or Modify Intents**:
   - Open `backend/data/answers.json`.
   - Add new patterns (queries that citizens might ask) and responses under the appropriate tag.
2. **Run the Training Script**:
   ```bash
   cd backend
   python train.py
