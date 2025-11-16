**Role Context:** ML Engineer  
**Primary Focus:** Model development, training pipelines, evaluation, deployment  
**Daily Tasks:** Model training, feature engineering, dataset prep, MLOps integration  
**Output:** Production ML models (classification, regression, embeddings, pipelines)

---

# MUST-HAVE (Primary): 80/20 Core

## 1. Python for ML Development  
**System Alignment:** Programming Languages → ML Ecosystem  
**Task Frequency:** Daily  

### Your 20%  
- **NumPy**: https://numpy.org/doc  
- **Pandas**: https://pandas.pydata.org/docs  
- **Scikit-Learn**: https://scikit-learn.org/stable  
- **Matplotlib / Seaborn**: https://matplotlib.org • https://seaborn.pydata.org  
- **Jupyter Notebooks**: https://jupyter.org  
- **Joblib / Pickling**: https://joblib.readthedocs.io  

### What You *Don't* Need  
- Deep Python internals  
- Async programming  
- Web dev frameworks (FastAPI, Django)  

### Pattern Alignment  
- Fit → Predict loops  
- Cross-validation cycles  
- DataFrame transformation pipelines  

---

## 2. Model Training & Evaluation  
**System Alignment:** ML Ecosystem → Model Development  
**Task Frequency:** Daily  

### Your 20%  
- **Train/validation/test splits**:  
  https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html  
- **Cross-validation**:  
  https://scikit-learn.org/stable/modules/cross_validation.html  
- **Model metrics (F1, ROC, MSE)**:  
  https://scikit-learn.org/stable/modules/model_evaluation.html  
- **GridSearchCV / RandomizedSearchCV**:  
  https://scikit-learn.org/stable/modules/grid_search.html  
- **Overfitting/underfitting detection**  

### What You *Don't* Need  
- Bayesian hyperparameter tuning  
- SOTA research papers  

### Pattern Alignment  
- Evaluate → Compare → Select  
- Bias/variance trade-off evaluation  

---

## 3. Feature Engineering  
**System Alignment:** Data Ecosystem → Preprocessing Layer  
**Task Frequency:** Daily  

### Your 20%  
- **StandardScaler / MinMaxScaler**: https://scikit-learn.org/stable/modules/preprocessing.html  
- **OneHotEncoder / OrdinalEncoder**  
- **Feature selection (SelectKBest)**:  
  https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html  
- **SMOTE / imbalance handling**: https://imbalanced-learn.org  
- **Text vectorization (TF-IDF, bag-of-words)**:  
  https://scikit-learn.org/stable/modules/feature_extraction.html  

### What You *Don't* Need  
- Large-scale feature stores  
- Custom-written C++ preprocessing  

### Pattern Alignment  
- Transform → Normalize → Encode  
- Leakage prevention patterns  

---

## 4. Deep Learning Foundations  
**System Alignment:** AI/ML Ecosystem → Neural Architectures  
**Task Frequency:** Regular  

### Your 20%  
- **PyTorch**: https://pytorch.org/docs  
- **TensorFlow / Keras**: https://keras.io  
- Training loops (forward, backward pass)  
- **Optimizers (Adam, SGD)**: https://pytorch.org/docs/stable/optim.html  
- **Loss functions (cross-entropy, MSE)**  

### What You *Don't* Need  
- Writing custom CUDA kernels  
- Transformer internals  

### Pattern Alignment  
- Forward → Backward → Optimize  
- Batch training patterns  

---

## 5. MLOps Foundations  
**System Alignment:** MLOps → Deployment Pipelines  
**Task Frequency:** Daily to Weekly  

### Your 20%  
- **MLflow**: https://mlflow.org/docs/latest/index.html  
- Model versioning  
- Experiment tracking  
- Model registry usage  
- Serialization (pickle, torch.save)  

### What You *Don't* Need  
- Custom CI/CD frameworks  
- Full infra provisioning  

### Pattern Alignment  
- Train → Track → Register → Serve  

---

## 6. Data Pipelines  
**System Alignment:** Data Engineering → ETL/ELT Prep  
**Task Frequency:** Daily  

### Your 20%  
- ETL fundamentals  
- Batch processing workflows  
- Data validation  
- Data quality checks  
- **Apache Airflow (optional)**: https://airflow.apache.org/docs  

### What You *Don't* Need  
- Advanced distributed compute systems  

### Pattern Alignment  
- Ingest → Clean → Process  

---

# SHOULD-HAVE (Secondary)

## 7. Advanced Model Tuning  
### Your 20%  
- **Optuna**: https://optuna.org  
- Learning rate scheduling  
- Early stopping  
- Ensembling (stacking, boosting)  

---

## 8. Deployment & Serving  
### Your 20%  
- **FastAPI model endpoints**: https://fastapi.tiangolo.com  
- **ONNX Runtime**: https://onnxruntime.ai  
- **TorchScript**: https://pytorch.org/docs/stable/jit.html  

---

## 9. Cloud ML Services  
### Your 20%  
- **AWS Sagemaker**: https://docs.aws.amazon.com/sagemaker  
- **GCP Vertex AI**: https://cloud.google.com/vertex-ai/docs  
- **Azure ML**: https://learn.microsoft.com/azure/machine-learning  

---

# COULD-HAVE (Tertiary)

## 10. Distributed Training  
### Your 20%  
- **PyTorch Distributed**:  
  https://pytorch.org/tutorials/beginner/dist_overview.html  
- **Horovod**: https://horovod.ai  
- **DeepSpeed**: https://github.com/microsoft/deepspeed  

---

## 11. Advanced Architectures  
### Your 20%  
- CNNs  
- RNNs / LSTMs  
- Transformer basics  

---

# WOULD-LIKE (Optional)

## 12. Research-Level Skills  
### Your 20%  
- Reading ML papers  
- Reproducing benchmarks  
- Kaggle competitions  
