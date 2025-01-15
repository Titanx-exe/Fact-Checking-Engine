# Fact-Checking-Engine

## Project Overview
A Knowledge Graph Fact Verification System - This system determines the truthfulness of RDF statements using path-based features and ensemble machine learning. Here's how it works:

<u>**Core Components**</u>

**Knowledge Graph Processing**

* Takes a reference knowledge graph containing 675,859 triples
* Removes literal values to keep only URI relationships, resulting in 660,000 triples
* Uses these relationships to find paths between entities
  
**Path Discovery**

* For each subject-object pair, finds connecting paths up to length 3
* Generates SPARQL query templates dynamically
* Excludes basic RDF predicates (subClassOf, range, domain, type)
* Counts frequency of unique paths between entities

<u>**Machine Learning Approach**</u>

**Ensemble Architecture**
Combines three powerful classifiers:
* XGBoost with hyperparameter tuning and Cross Validation
* Support Vector Machine (SVM)
* Random Forest
  
**Feature Engineering**
Uses three different feature extraction methods:

* DictVectorizer for XGBoost
* MultiLabelBinarizer for SVM
* CountVectorizer for Random Forest
  
**Prediction Process**
* Each classifier makes independent predictions
* Final truth value determined by majority voting
* Outputs a binary score (0 or 1) indicating statement veracity

## Installation

- pip install -r requirements.txt
- You will need Jupyter Notebook
- Just Run the file main.ipynb

## Contribution:

| Name              | Matriculation Number |
| ----------------- | -------------------- |
| Harshit Purohit   |    4012382    |

