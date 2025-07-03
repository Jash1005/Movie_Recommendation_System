---

# 🎬 Movie Recommender System

A **Content-Based Movie Recommender System** that suggests similar movies based on metadata like cast, genres, keywords, overview, and director. This system uses **Natural Language Processing (NLP)** techniques to build meaningful movie similarities.

---

## 🚀 Project Overview

This project demonstrates how to build a movie recommendation engine using **content-based filtering**. Given a movie title, it suggests other movies with similar content by analyzing text-based features.

---

## 🧠 Types of Recommendation Systems

* 📄 **Content-Based Filtering** (used in this project): Recommends similar items based on features of the item itself.
* 👥 **Collaborative Filtering**: Recommends based on user preferences and similarities.
* ⚡ **Hybrid Systems**: Combines both approaches for better accuracy.

---

## 🛠️ Tech Stack & Tools

* **Python**
* **Pandas, NumPy** – Data handling
* **Scikit-learn** – CountVectorizer, Cosine Similarity
* **NLTK/AST** – Text preprocessing and parsing

---

## 📂 Data Used

* [`tmdb_5000_movies.csv`](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
* [`tmdb_5000_credits.csv`](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## 🔧 Workflow & Implementation

### 1. Data Preparation

* Merged the movies and credits datasets on the `title` column.
* Selected relevant columns: `genres`, `keywords`, `cast`, `crew`, `overview`, and `title`.
* Handled missing data and removed duplicates.

### 2. Feature Engineering

* Extracted:

  * Top 3 cast members.
  * Director from crew.
  * Cleaned genres and keywords.
* Combined all features into a single text field called `tags`.

### 3. Text Vectorization

* Converted the `tags` text into vectors using **Bag of Words (CountVectorizer)**.
* Computed **cosine similarity** between movie vectors.

### 4. Recommendation Function

* Built a function `recommend(movie_name)` that returns the top 5 similar movies based on cosine similarity.

---

## 📌 Example

```python
recommend("Avatar")
```

**Output:**

```
1. John Carter
2. Guardians of the Galaxy
3. Prince of Persia: The Sands of Time
4. Star Trek Into Darkness
5. Pirates of the Caribbean: At World's End
```

---

## 📎 Project Structure

```
├── Movie_Recommender_System_Content.ipynb
├── tmdb_5000_movies.csv
├── tmdb_5000_credits.csv
└── README.md
```

---

Based on the content of your notebook `Collaborative_Movie_Recommendation.ipynb`, here is a structured `README.md` section for your GitHub repository:

---

# 🎥 Collaborative Movie Recommender System

This project implements a **Collaborative Filtering-based Movie Recommendation System**, where suggestions are made by analyzing **user preferences** and **rating patterns**. If two users have rated movies similarly in the past, they will likely enjoy similar future recommendations.

---

## 📌 Project Overview

Unlike content-based filtering, which uses item features, **collaborative filtering** focuses on user behavior. The system finds relationships between users and items using a **user-item interaction matrix**, making it especially useful when item metadata is limited or unavailable.

---

## 🛠️ Tech Stack & Tools

* **Python**
* **Pandas, NumPy** – Data preprocessing and matrix construction
* **Scikit-learn** – Cosine similarity
* **Random** – Simulated data mapping
* **Jupyter Notebook** – Experimentation and visualization

---

## 📂 Data Used

* `tmdb_5000_movies.csv`: Movie metadata
* `Users.csv`: Simulated user data
* `Ratings.csv`: Simulated user ratings (e.g., book ratings repurposed for movies)

---

## 🔧 Workflow & Implementation

### 1. Dataset Preparation

* Loaded three datasets: `movies`, `users`, and `ratings`.
* Merged datasets on `User-ID`.
* Simulated movie IDs by replacing unrelated IDs (like ISBNs) with random movie IDs from the movie dataset.

### 2. Preprocessing

* Cleaned nulls and checked for duplicates.
* Renamed movie ID columns for consistency.
* Filtered:

  * Movies with at least **200 total ratings**.
  * Users who have rated **more than 50 movies**.

### 3. Popularity-Based Filtering

* Computed average ratings and total rating count.
* Recommended the **top 20 most popular movies** as a baseline.

### 4. Collaborative Filtering

* Created a **user-movie matrix** (pivot table).
* Calculated **cosine similarity** between movies.
* Built a recommendation function to suggest similar movies based on user preferences.

---

## 🔁 Recommendation Example

```python
recommend(movie_title="Inception")
```

Returns top N movies rated similarly by users with overlapping preferences.

---

## 📎 Project Structure

```
├── Collaborative_Movie_Recommendation.ipynb
├── tmdb_5000_movies.csv
├── Users.csv
├── Ratings.csv
└── README.md
```

---


## 🧑‍💻 Author

**Jash Sheth** – [LinkedIn](https://linkedin.com) | [GitHub](https://github.com)



