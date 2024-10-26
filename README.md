
```markdown
# HybridRecommendationEngine

A hybrid recommendation system combining multiple Content-Based Filtering and Collaborative Filtering techniques to provide personalized movie recommendations. Built with Python and leveraging the MovieLens dataset.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Methodology](#methodology)
  - [Content-Based Filtering](#content-based-filtering)
  - [Collaborative Filtering](#collaborative-filtering)
  - [Hybrid Approach](#hybrid-approach)
- [Results](#results)
- [Notes](#notes)
- [License](#license)
- [Authors](#authors)

## Introduction

This project implements a hybrid recommendation system that combines multiple content-based and collaborative filtering methods to enhance the accuracy and personalization of movie recommendations.

## Features

- **Hybrid Recommendation Engine**: Integrates various Content-Based and Collaborative Filtering techniques.
- **Advanced Text Processing**: Implements methods like TF-IDF, Bag-of-Words, BM25, and BERT for feature extraction.
- **Multiple Collaborative Algorithms**: Includes both Singular Value Decomposition (SVD) and Neural Collaborative Filtering (NCF).
- **Modular Structure**: Each method is implemented in separate Jupyter notebooks for clarity and ease of use.
- **Scalable Architecture**: Designed to handle large datasets efficiently.
- **Customizable**: Easy to extend or modify methods and parameters.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/HybridRecommendationEngine.git
   ```
2. **Navigate to the project directory:**
   ```bash
   cd HybridRecommendationEngine
   ```
3. **Create and activate a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
4. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

The project is organized into two main directories:

- **`Collaborative_Filtering`**
- **`Content_Based_Filtering`**

Each directory contains multiple Jupyter notebooks implementing different methods.

### Collaborative Filtering

- **Notebooks:**
  - `SVD.ipynb`: Implements Singular Value Decomposition.
  - `NCF.ipynb`: Implements Neural Collaborative Filtering.

### Content-Based Filtering

- **Notebooks:**
  - `TF-IDF.ipynb`: Uses Term Frequency-Inverse Document Frequency.
  - `BoW.ipynb`: Uses Bag-of-Words representation.
  - `BM25.ipynb`: Implements Okapi BM25 algorithm.
  - `BERT.ipynb`: Uses BERT embeddings for text data.

### Running the Notebooks

1. **Navigate to the desired directory:**

   - For Collaborative Filtering:
     ```bash
     cd Collaborative_Filtering
     ```
   - For Content-Based Filtering:
     ```bash
     cd Content_Based_Filtering
     ```

2. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

3. **Open and Run the Notebooks:**

   - In the Jupyter interface, you will see a list of notebooks (*.ipynb files).
   - Select the notebook you want to explore (e.g., `SVD.ipynb`, `BM25.ipynb`, `NCF.ipynb`, `BERT.ipynb`).
   - Run the notebook cells sequentially to execute the code and see the results.





## Dataset

- **MovieLens 25M Dataset**: Contains 25 million ratings and one million tag applications applied to 62,000 movies by 162,000 users.
  - **Ratings**: User ratings from **0** to **5**.
  - **Tags**: User-generated tags for movies.
  - **Movies Metadata**: Includes titles, genres, and other metadata.

Download the dataset from [MovieLens](https://grouplens.org/datasets/movielens/25m/).

## Methodology

### Content-Based Filtering

Implemented multiple text processing techniques to capture the features of movies based on their descriptions and metadata.

- **Bag-of-Words (BoW)**: Converts movie descriptions into numerical feature vectors based on word counts.
- **TF-IDF**: Weighs the importance of words in the descriptions relative to their frequency across all movies.
- **BM25**: An improved version of TF-IDF that considers term frequency saturation and document length normalization.
- **BERT Embeddings**: Uses transformer-based models to capture contextual relationships in text, providing deep semantic understanding.

### Collaborative Filtering

Implemented algorithms that leverage user-item interactions to predict user preferences.

- **Singular Value Decomposition (SVD)**: Decomposes the user-item interaction matrix to identify latent factors influencing user preferences.
- **Neural Collaborative Filtering (NCF)**: Utilizes deep neural networks to model complex user-item interaction patterns.

Each method is explored and implemented in separate Jupyter notebooks within the `Collaborative_Filtering` directory.

### Hybrid Approach

- **Integration of Methods**: Combines the strengths of both content-based and collaborative filtering methods.
- **Aggregation of Scores**: Final recommendation scores are computed by appropriately weighting the outputs from different models.
- **Flexibility**: The hybrid model can be adjusted to emphasize either content-based or collaborative aspects based on the application needs.

## Results

- **Performance Metrics**: Evaluated using metrics such as RMSE.
- **Findings**:
  - **Content-Based Filtering**:
    - **BM25** and **BERT embeddings** provided superior results in capturing the semantic meaning of movie descriptions.
  - **Collaborative Filtering**:
    - **SVD** effectively handled sparse data and captured latent user preferences.
    - **NCF** provided improved performance by modeling non-linear interactions.
  - **Hybrid Model**:
    - The combination of **BM25/BERT** with **SVD/NCF** yielded the best overall performance.
    - The hybrid approach provided more personalized and diverse recommendations.
- **Dataset Dependency**:
  - Results were optimized for the MovieLens 25M dataset.
  - Performance may vary with different datasets due to variations in data sparsity, user behavior, and content richness.

## Notes

- **Dataset Specificity**: The effectiveness of the implemented methods is tied to the characteristics of the MovieLens dataset used.
- **Generalization**: While the models performed well on this dataset, their performance may differ on other datasets. Users are encouraged to retrain and adjust the models when applying them to new data.
- **Customization**: Parameters and model configurations can be tuned within the notebooks to explore different scenarios.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Authors

- **Alluri Lakshman Narendra** - [GitHub](https://github.com/lakshmannarendra)
  - Department of Computer Science, Indian Institute of Technology Dharwad




