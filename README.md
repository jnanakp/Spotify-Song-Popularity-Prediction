# 🎧 Spotify Song Popularity Prediction

This project focuses on predicting the future popularity of songs on Spotify using historical song-level audio and metadata. Built as part of the Blended Analytics (DSO 528) course at the University of Southern California, the goal was to support Universal Music Group in maximizing the return on their music promotion efforts through predictive modeling.

By combining domain-specific knowledge with machine learning, the team developed an interpretable and highly accurate classification model to estimate the likelihood of a song becoming a hit.

---

## 📊 Project Overview

Universal Music Group provided access to a dataset containing thousands of songs released in the past decade, along with their associated acoustic features and popularity scores (on a scale of 0 to 100). The team was tasked with:

- Analyzing the relationships between song characteristics and popularity
- Framing the problem as a binary classification task (popular vs. not popular)
- Training and comparing multiple machine learning models
- Selecting and optimizing the final model based on business performance metrics

The final deliverables included a predictive model, detailed business case analysis, and recommendations for integrating the solution into Universal’s promotional planning.

---

## 🎯 Objectives

- Build a model to **predict whether a song will be above or below the median popularity** score
- Identify **key acoustic and metadata features** that drive popularity
- Support **$139M in annual marketing spend** through better forecasting of hits
- Provide a framework that is **interpretable, repeatable, and scalable**

---

## 🧠 Machine Learning Models Explored

Several classification algorithms were tested and tuned to find the optimal balance between accuracy, interpretability, and robustness:

| Model                 | Description                                     |
|----------------------|-------------------------------------------------|
| Logistic Regression  | Interpretable baseline model                    |
| Random Forest        | High-performing ensemble, handled feature noise |
| Gradient Boosted Trees (GBT) | Better handling of non-linear interactions |
| K-Nearest Neighbors  | Used for comparison, less scalable              |

### ✅ Final Model: Random Forest Classifier
- **Accuracy:** 87.6%
- **Precision:** 88%
- **Recall:** 87%
- Chosen for its **strong out-of-sample generalization**, ease of interpretation via feature importance, and business relevance.

---

## 🔍 Key Features Used

The following Spotify audio features and metadata were most predictive of popularity:

- **Acousticness** – likelihood the track is acoustic
- **Danceability** – suitability for dancing
- **Energy** – intensity and activity level of the track
- **Valence** – positivity of the mood
- **Liveness** – presence of audience
- **Tempo** – beats per minute
- **Duration** – track length
- **Release year**
- **Artist metadata** – proxies for brand influence

The `is_popular` binary label was derived by splitting the dataset at the median popularity score, making the problem a balanced classification task.

---

## 📈 Business Impact

- Enables **early-stage prediction** of which songs are likely to succeed
- Informs **playlist placements**, marketing strategies, and A&R decisions
- Estimated to generate **$139M in annual ROI** improvement through better resource allocation
- Reduces over-reliance on subjective or manual methods of hit prediction

This model could be integrated into Universal Music's internal A&R dashboard to flag high-potential tracks shortly after production or release.

---

## 💡 Technologies & Tools

- **Python**: Core language for data analysis and modeling
- **Pandas, NumPy**: Data manipulation
- **Scikit-learn**: Model building and evaluation
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebooks**: Experiment tracking and reproducibility

---

## 🚀 Potential Extensions

- Incorporate real-time streaming metrics (e.g., skips, saves, playlist adds)
- Use NLP on lyrics to enhance prediction
- Add external data such as TikTok virality or artist social metrics
- Implement a regression model to directly predict Spotify popularity score (0–100)



