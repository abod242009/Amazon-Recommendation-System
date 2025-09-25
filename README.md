# 📦 Amazon Product Recommendation System

This project implements a **Recommendation System** on the **Amazon Electronics dataset**.  
It compares **Popularity-based**, **User–User Collaborative Filtering**, **Item–Item Collaborative Filtering**, and **Matrix Factorization (SVD)** models.  
Performance is evaluated using **Precision@10** and **Recall@10**, with a final **hybrid recommendation strategy** proposed for business deployment.  

---
## 📂 Dataset  
You can download the dataset from here:  
[🔗 Amazon Electronics Ratings Dataset (Google Drive)](https://drive.google.com/file/d/1XahZcR287ke7j48I7-oj0KzmmwSSvA3Y/view?usp=sharing)

---
## 📊 Project Overview
- **Dataset**: Amazon Electronics ratings (~7.8M ratings, ~420k users, ~475k products).  
- **Filtering**: Users with ≥50 ratings, Products with ≥5 ratings.  
- **Goal**: Evaluate different recommendation strategies and suggest a scalable hybrid system.  

---

## 🧰 Methods Implemented
1. **Popularity-based Recommender**  
   - Fast and scalable, but lacks personalization.  

2. **User–User Collaborative Filtering**  
   - Captures user similarities but struggles with sparsity.  

3. **Item–Item Collaborative Filtering**  
   - More stable than User–User, used historically by Amazon.  

4. **Matrix Factorization (SVD)**  
   - Best performance overall, captures hidden latent structures.  

---

## 📈 Model Performance
| Model                  | Precision@10 | Recall@10 |
|-------------------------|--------------|-----------|
| Popularity              | 0.23         | 0.11      |
| User–User (Base)        | 0.28         | 0.15      |
| User–User (Tuned)       | 0.32         | 0.19      |
| Item–Item (Base)        | 0.30         | 0.17      |
| Item–Item (Tuned)       | 0.36         | 0.22      |
| SVD (Base)              | 0.34         | 0.20      |
| **SVD (Tuned)**         | **0.40**     | **0.25**  |

---

## 🚀 Business Recommendations
- Deploy a **hybrid recommender**:
  - **SVD (Tuned)** as the core recommender.  
  - **Item–Item CF** for real-time serving.  
  - **Popularity model** as a fallback for cold-start users.  
- Expected impact: **+8–12% CTR uplift, +5–7% conversion boost**.  

---

## 📂 Project Structure

Amazon-Recommendation-System/
│── Amazon_Recommendation.ipynb   # Jupyter Notebook (code + results)
│── report/
│   └── Abdalbari_Amazon_Recommendation_Project.pdf   # Full project report
│── requirements.txt               # Python libraries
│── README.md                      # Project overview

## 📌 Future Work
Explore Deep Learning recommenders (Neural CF, Transformers).

Use Contextual Bandits for real-time personalization.

Apply Reinforcement Learning for long-term engagement optimization.

Add Fairness and Diversity metrics to reduce bias.
## 👨‍💻 Author:Abdalbari R. Abuwarda
## 🛠️ Installation
Clone the repository and install required dependencies:
```bash
git clone https://github.com/your-username/Amazon-Recommendation-System.git
cd Amazon-Recommendation-System
pip install -r requirements.txt
```
## 👨‍💻 Author:Abdalbari R. Abuwarda
