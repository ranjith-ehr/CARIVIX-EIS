21. ml-models-reference.md

- Model inventory table: name, type, purpose, input features, output, framework
- XGBoost Regressor: feature list, target variable, evaluation metric (RMSE/R²)
- Logistic Regression Classifier: classes, decision boundary, confidence threshold
- Isolation Forest: contamination parameter, anomaly score interpretation
- Time-Series Forecasting: model type (ARIMA/Prophet), horizon, seasonality settings
- Model artifact storage location and versioning

---

22. model-optimization.md

- Feature selection method and selected features per model
- Hyperparameter tuning: method (GridSearch/Bayesian), parameter grid per model
- Imbalanced dataset handling: technique used (SMOTE, class weighting)
- Cross-validation: fold count, stratification strategy
- SHAP values: how to generate, interpret force plots and summary plots
- Retraining schedule: trigger conditions, data window, deployment steps

---

23. nlp-chatbot-architecture.md

- Component diagram: User input → Intent Detection → NER → RAG → LLM → Response
- Intent Detection: DistilBERT/RoBERTa model, intent taxonomy, confidence threshold
- NER: spaCy pipeline, entity types extracted (DATE, EMPLOYEE_NAME, TASK_ID)
- RAG pipeline: LangChain orchestration, FAISS/Pinecone vector store, retrieval top-k config
- LLM: LLaMA 3 / Mistral, inference endpoint, context window, prompt template
- Response formatting: plain text vs. structured data response types
- Fallback and low-confidence handling