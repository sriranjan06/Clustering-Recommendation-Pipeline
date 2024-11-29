# **Clustering and Recommendation Pipeline**

This project is part of a Data Mining homework assignment aimed at implementing and analyzing clustering and recommender system techniques using real-world datasets. The project is divided into two main tasks: K-Means Clustering and Recommender Systems.

### Table of Contents

1.	Introduction
2.	Task 1: K-Means Clustering
    - Objective
    - Implementation Details
    - Results
3.	Task 2: Recommender Systems
    - Objective
    - Implementation Details
    - Results
4.	Key Takeaways
5.	Repository Structure
6.	How to Run

## **Introduction**

This project explores:
- **Task 1:** The implementation and evaluation of K-Means clustering with different distance metrics (Euclidean, Cosine, and Jaccard).
- **Task 2:** The development of a recommender system using collaborative filtering and matrix factorization techniques, evaluated using MAE and RMSE.

The project provides insights into clustering performance, recommender system evaluation metrics, and the impact of parameters such as similarity metrics and neighborhood sizes.

### **Task 1: K-Means Clustering**

#### **Objective**

To implement K-Means clustering from scratch and evaluate its performance under three distance metrics:
1.	Euclidean Distance
2.	1 - Cosine Similarity
3.	1 - Generalized Jaccard Similarity

#### **Implementation Details**
- Dataset: A simulated dataset containing 10,000 samples and 784 features.
- Metrics: SSE (Sum of Squared Errors) and predictive accuracy using majority voting.
- Stopping Criteria: Convergence when centroids do not change, SSE increases, or a maximum number of iterations is reached.
- Evaluation:
    - SSE comparison across distance metrics.
	- Predictive accuracy using ground-truth labels.
	- Analysis of convergence time and iterations.

#### **Results**

- SSE Comparison:
    - Euclidean: 25323652080.95
	- Cosine: 25580504792.08
	- Jaccard: 25453946708.70

- Predictive Accuracy:
	- Euclidean: 60.07%
	- Cosine: 58.85%
	- Jaccard: 59.79%

- Convergence Analysis:
    - Euclidean converged faster with fewer iterations compared to Cosine and Jaccard.
    - Key Takeaway: Euclidean Distance outperformed other metrics in terms of SSE, accuracy, and convergence efficiency.

### **Task 2: Recommender Systems**

#### **Objective**

To build a movie recommender system and evaluate collaborative filtering methods:
1.	User-based Collaborative Filtering
2.	Item-based Collaborative Filtering
3.	Probabilistic Matrix Factorization (PMF)

#### **Implementation Details**
- Dataset: ratings_small.csv containing user-item ratings.
- Metrics: MAE (Mean Absolute Error) and RMSE (Root Mean Squared Error) evaluated under 5-fold cross-validation.
- Analysis:
    - Comparison of MAE and RMSE across models.
	- Impact of similarity metrics (Cosine, MSD, Pearson) on User-based and Item-based CF.
	- Effect of the number of neighbors on model performance.

#### **Results**

	•	Model Comparison:
	•	PMF: RMSE = 0.8973, MAE = 0.6913 (Best overall performance)
	•	User-based CF: RMSE = 0.9679, MAE = 0.7439
	•	Item-based CF: RMSE = 0.9345, MAE = 0.7207
	•	Impact of Similarity Metrics:
	•	MSD provided the best RMSE for both User-based and Item-based CF.
	•	Cosine performed the worst.
	•	Effect of Neighbors:
	•	User-based CF performed best at K=20.
	•	Item-based CF performed best at K=50.
	•	Key Takeaway: PMF is the best overall method, while similarity metrics and neighborhood sizes significantly impact CF performance.

Key Takeaways

	1.	K-Means Clustering:
	•	Euclidean Distance is the most effective metric, achieving the best SSE and predictive accuracy.
	•	Convergence efficiency varies across metrics, with Euclidean being the fastest.
	2.	Recommender Systems:
	•	PMF is the most accurate model in terms of MAE and RMSE.
	•	MSD is the best similarity metric for collaborative filtering.
	•	The optimal number of neighbors varies between User-based (K=20) and Item-based CF (K=50).

Repository Structure

Clustering-Recommendation-Pipeline/
├── data/                    # Contains the dataset files
├── Task1_KMeans.ipynb       # Jupyter notebook for Task 1
├── Task2_Recommender.ipynb  # Jupyter notebook for Task 2
├── Homework3.pdf            # Final project deliverable
├── README.md                # This file

How to Run

	1.	Clone the repository:

git clone https://github.com/sriranjan06/Clustering-Recommendation-Pipeline.git


	2.	Install required libraries:

pip install -r requirements.txt


	3.	Open the Jupyter notebooks:

jupyter notebook


	4.	Run Task1_KMeans.ipynb and Task2_Recommender.ipynb to reproduce the results.

Contributors

	•	Sriranjan Srikanth
MS Computer Science, Arizona State University
GitHub Profile

For any queries or feedback, feel free to reach out through the repository’s issues section.

This README provides a detailed overview of the project and ensures clarity for both graders and collaborators. Let me know if you need further refinements! 😊