# 🎬 Movie Recommendation System Using Collaborative Filtering

This project implements a movie recommendation engine that leverages collaborative filtering to suggest personalized movie recommendations based on historical user ratings. By identifying user or item similarities using cosine similarity, the system intelligently recommends movies aligned with a user's preferences — without requiring metadata such as genre, cast, or reviews.

---

## 📌 Objective

To build a personalized movie recommendation system using collaborative filtering techniques on the MovieLens dataset. The project compares user-based and item-based filtering approaches to suggest relevant movies to users.

---

## 🗂️ Dataset

- **Source**: [MovieLens Dataset](https://grouplens.org/datasets/movielens/)
- **Structure**: Contains ratings of movies by users with features such as `userId`, `movieId`, `rating`, and `timestamp`
- **Preprocessing**:
  - Merged movie metadata and rating data
  - Constructed a user-item interaction matrix
  - Handled missing values due to sparse rating matrix

---

## 🧠 Methodology

The project uses **collaborative filtering**, a memory-based approach that relies on past user behavior rather than content.

### ✅ User-Based Collaborative Filtering
- Recommends movies liked by users who have similar rating behavior.
- Finds similar users using cosine similarity between rating vectors.

### ✅ Item-Based Collaborative Filtering
- Recommends movies that are similar to those a user already rated highly.
- Computes similarity between items (movies) based on user ratings.

### 💡 Cosine Similarity
Used to compute similarity between users or items by measuring the angle between their rating vectors.

---

## 🛠️ Implementation

- **Libraries Used**: `Pandas`, `NumPy`, `Scikit-learn`
- Steps:
  1. Load and preprocess MovieLens dataset
  2. Create a pivot table to form the user-item rating matrix
  3. Compute similarity matrix using cosine similarity
  4. Build logic to retrieve top-N recommended movies
  5. Handle sparse data and unseen users/items gracefully

---

## 📈 Results

- **User-Based Example**: For a given user, the system suggests top movies rated highly by similar users.
- **Item-Based Example**: For a selected movie, the system recommends similar movies based on collective user feedback.
- Evaluated recommendations qualitatively through sample user scenarios, showing relevant and meaningful suggestions.

---

## 🚀 Future Enhancements

- Incorporate **matrix factorization techniques** (SVD, ALS)
- Add **content-based filtering** using genres, tags, and keywords
- Build a **hybrid recommender system**
- Deploy with **Streamlit** or **Flask** for an interactive web app

---


