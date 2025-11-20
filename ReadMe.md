# Master Thesis Repository — Fengdi Huang (231AHG003)

This repository contains all datasets, configurations, trained models, and evaluation summaries used in my Master’s thesis.  
The thesis investigates how **CNN (spaCy)** and **multilingual Transformer models (XLM-R Base & XLM-R Large)** perform under **low-resource** and **reduced-data** conditions, using **Latvian LVTB v2.17** as the experimental dataset.

---

## Repository Structure

### **Corpus/**
Processed corpus files in **`.spacy` DocBin** format:
- `train/` — multiple training sets with different sampling sizes  
- `dev/` — development/validation set  
- `test/` — fixed test set for all experiments  

All files originate from **UD_Latvian_LVTB v2.17** and include tokenization, POS tags, morphological features, and dependency annotations.

---

### **Experiment/**
Contains all experiment resources:
- Config files for **spaCy CNN**, **XLM-R Base**, and **XLM-R Large**
- Training Jupyter notebooks
- Subfolders by training size:
  - `train_1/` → 1%  
  - `train_5/` → 5%  
  - `train_20/` → 20%  
  - `train_50/` → 50%  
  - `train_100/` → 100%  

Each folder includes reproducible pipelines for training, evaluation, and logging.

---

### **Summary_CSV/** & **Summary_JSON/**
Aggregated evaluation outputs for all **15 models**, including:
- POS, morphological feature, and dependency results  
- UAS / LAS per dependency type  
- OOV vs. IV accuracy  
- Learning-curve summaries across architectures and data sizes  

These files support the quantitative analysis presented in the thesis.

---

### **UD_Latvian_LVTB/**
Original **CONLL-U** files from **UD Latvian LVTB v2.17**, used as the raw dataset source before conversion.

---

## Project Overview (Thesis Context)

This repository supports a Master’s thesis with the following goals:
- Compare **spaCy CNN** vs. **XLM-R Transformers**  
- Evaluate **cross-lingual transfer** behavior under extreme data reduction  
- Analyze model robustness across:
  - POS tagging  
  - Morphological features  
  - Dependency parsing (UAS / LAS / per-type LAS)  
  - OOV vs. IV generalization  
- Examine how performance scales from **1% → 100%** of the training data

The analysis, visualizations, and conclusions are presented in the thesis document.

---

