#  Hybrid Movie Recommender System

This project implements a hybrid movie recommendation system using the MovieLens dataset. It combines **Content-Based Filtering (CBF)** and **Collaborative Filtering (CF)** to improve accuracy and solve cold-start issues.

##  Dataset

- **MovieLens 10M** dataset
- Includes user ratings, movie metadata (title, genres), and user-generated tags.

##  Models Implemented

1. **Content-Based Filtering**
   - Uses TF-IDF to vectorize movie content (title, genres, tags)
   - Builds user profiles based on positively rated movies
   - Predicts ratings using cosine similarity

2. **Collaborative Filtering (Unconstrained Matrix Factorization)**
   - Learns latent features of users and items
   - Optimized using Stochastic Gradient Descent with bias terms

3. **Hybrid Model**
   - Linearly combines predictions from CBF and CF
   - Best performance achieved with α = 0.95

##  Evaluation

- Metric: Root Mean Square Error (RMSE)
- Hybrid model achieved **Test RMSE = 0.8021**
- Outperforms both standalone models

| Model               | Test RMSE |
|---------------------|-----------|
| Content-Based       | 0.8824    |
| Collaborative       | 0.8098    |
| **Hybrid (α=0.95)** | **0.8021**|

