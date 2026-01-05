# 🎬 Movie Recommendation System (Content-Based)

## 📌 Project Overview

This project is a **Content-Based Movie Recommendation System** built using **Python, Pandas, and Scikit-learn**.
The system recommends movies similar to a given movie based on **metadata such as overview, genres, keywords, cast, and director**.

This project is ideal for:

* Machine Learning beginners
* Internship / placement interviews
* Portfolio & GitHub projects

---

## 🎯 Objective

To build a system that:

* Analyzes movie metadata
* Converts text data into numerical form
* Computes similarity between movies
* Recommends the **top 5 similar movies** for a given input

---

## 🧠 Recommendation Approach

**Content-Based Filtering**

* Uses movie **content/features**, not user ratings
* Works well even for new users (no cold start)
* Based on **Cosine Similarity**

---

## 📂 Dataset

A **TMDB-style dataset** is used (locally created for learning purposes):

### Files:

* `tmdb_5000_movies.csv`
* `tmdb_5000_credits.csv`

### Features Used:

* `title`
* `overview`
* `genres`
* `keywords`
* `cast`
* `crew (director)`

> Note: JSON-like fields are stored as strings and parsed during preprocessing.

---

## 🛠️ Technologies Used

* Python 3
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

---

## 🔄 Project Workflow

### 1️⃣ Data Loading

* Load movies and credits datasets
* Merge them using the movie title

### 2️⃣ Exploratory Data Analysis (EDA)

* Check shape, null values, and data types
* Select relevant columns only

### 3️⃣ Data Preprocessing

* Handle missing values
* Convert stringified JSON to Python lists
* Extract:

  * Top 3 actors
  * Director name

### 4️⃣ Feature Engineering

* Combine overview, genres, keywords, cast, and director into a single column called **tags**
* Convert text to lowercase

### 5️⃣ Text Vectorization

* Use **Bag of Words (CountVectorizer)**
* Remove stopwords
* Limit features to improve performance

### 6️⃣ Similarity Calculation

* Use **Cosine Similarity** to measure closeness between movies

### 7️⃣ Recommendation Function

* Accepts a movie name as input
* Returns top 5 similar movies

---

## 🧪 Sample Output

**Input:**

```
Avatar
```

**Recommended Movies:**

* The Avengers
* Interstellar
* Inception
* The Dark Knight
* Titanic

*(Results may vary depending on dataset size)*

---

## 📈 Evaluation Method

* **Qualitative Evaluation**
* Manual inspection of recommendations
* Semantic similarity check

> Traditional metrics like accuracy or RMSE are not suitable for content-based recommenders.

---

## ▶️ How to Run the Project

1. Clone or download the repository
2. Open CMD in project folder
3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
4. Open the notebook and run cells sequentially
5. Use the `recommend("movie_name")` function

---

## 🌐 (Optional) Flask Integration

The recommendation logic can be deployed as a **Flask API** to serve recommendations via a browser or frontend application.

---

## 🎤 Interview Explanation (Short)

> "I built a content-based movie recommendation system using TMDB metadata. I combined textual features, vectorized them using Bag of Words, and calculated cosine similarity to recommend similar movies."

---

## 🚀 Future Improvements

* Use TF-IDF instead of Bag of Words
* Add collaborative filtering
* Integrate user ratings
* Build a frontend using Flask or Streamlit

---

## 👩‍💻 Author

**Sujith**
Movie Recommendation System – Machine Learning Project

---

⭐ If you like this project, don’t forget to star the repository!
