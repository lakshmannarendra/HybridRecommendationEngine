

---

# 🎬 **Movie Recommendation Using Content-Based Filtering**

A **Content-Based Movie Recommendation System** that leverages multiple Natural Language Processing (NLP) techniques — **TF-IDF**, **Bag-of-Words**, and **BM25** — to generate personalized movie recommendations using the **MovieLens 25M** dataset.
Developed with Python, this project demonstrates how textual features and metadata can be used to build efficient, scalable, and relevant movie recommendation systems.

---

## 📚 **Table of Contents**

* [Introduction](#introduction)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Dataset](#dataset)
* [Methodology](#methodology)

  * [Data Preprocessing](#data-preprocessing)
  * [Text Representation Techniques](#text-representation-techniques)

    * [Bag-of-Words (BoW)](#bag-of-words-bow)
    * [TF-IDF](#term-frequency-inverse-document-frequency-tf-idf)
    * [BM25](#bm25)
  * [Similarity Computation](#similarity-computation)
* [Results](#results)
* [Conclusion](#conclusion)
* [Notes](#notes)
* [License](#license)
* [Author](#author)

---

## 🧠 **Introduction**

With the exponential growth of streaming platforms, users face difficulty in discovering movies aligned with their interests.
This project implements a **Content-Based Movie Recommendation Engine** that suggests movies similar to a given one using descriptive and metadata features such as **overview**, **genres**, **cast**, **crew**, and **keywords**.

By employing advanced text representation techniques and similarity computations, the system provides **personalized and semantically relevant** movie recommendations — **without relying on explicit user ratings**.

---

## ⚙️ **Features**

* 🎯 **Content-Based Filtering** using BoW, TF-IDF, and BM25
* 🧹 **Text Preprocessing Pipeline** – tokenization, lemmatization, stopword removal, noise cleaning
* 🎬 **Comprehensive Metadata Integration** – combines genres, overview, cast, crew, and production info
* 🔍 **Cosine Similarity + KNN** – to retrieve top related movies
* 🚀 **Scalable & Modular Design** – handles large datasets effectively
* 📊 **Exploratory Visualizations** – genre distribution, release patterns, and ratings overview

---

## 💻 **Installation**

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/MovieRecommendationSystem.git
   cd MovieRecommendationSystem
   ```

2. **(Optional) Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 **Usage**

1. **Navigate to the project directory:**

   ```bash
   cd Content_Based_Filtering
   ```

2. **Start Jupyter Notebook:**

   ```bash
   jupyter notebook
   ```

3. **Open and run the notebooks:**

   * `BoW.ipynb`
   * `TF-IDF.ipynb`
   * `BM25.ipynb`

Each notebook covers preprocessing, feature extraction, similarity computation, and generation of top movie recommendations.

---

## 🎞️ **Dataset**

**Source:** [MovieLens 25M Dataset](https://grouplens.org/datasets/movielens/25m/)

* 🎥 **Movies:** 62,000+
* ⭐ **Ratings:** 25 million
* 🏷️ **Tags:** 1 million user-generated
* 🧩 **Metadata:** Titles, genres, cast, crew, keywords, and overviews
* 📅 **Time Span:** 1995–2019

This dataset offers a rich combination of structured metadata and textual data, ideal for content-based analysis and NLP-based feature modeling.

---

## 🧩 **Methodology**

### 🧼 **Data Preprocessing**

Steps involved:

1. **Data Loading & Cleaning:** Handling missing, duplicate, or inconsistent entries.
2. **Integration:** Merged movie metadata, tags, and credits.
3. **Feature Extraction:**

   * Top 3 **cast members**
   * Top 3 **crew members** (Director, Producer, Screenwriter)
   * **Production companies**
4. **Feature Engineering:**

   * Combined extracted data into a unified **`movie_tags`** column (overview + metadata).
5. **Text Preprocessing:**

   * Tokenization
   * Lowercasing
   * Lemmatization
   * Stopword and noise removal
   * Handling negations for better context preservation

---

### 🧮 **Text Representation Techniques**

#### 🧱 **Bag-of-Words (BoW)**

* Represents movie descriptions as vectors of word frequencies.
* **Pros:** Simple, explainable, and scalable.
* **Cons:** Ignores word order and deeper context.

#### 📊 **Term Frequency–Inverse Document Frequency (TF-IDF)**

* Enhances BoW by considering word importance across the corpus.
* Highlights rare but meaningful terms that define a movie’s uniqueness.
* Provides improved discrimination between movies compared to plain word counts.

#### ⚖️ **BM25**

* A more advanced ranking algorithm building upon TF-IDF.
* **Features:**

  * Term frequency saturation
  * Document length normalization
  * Tunable parameters *(k1, b)*
* **Advantages:**

  * Produces robust and contextually relevant results
  * Handles varying document lengths efficiently
  * Offers better ranking and relevance compared to BoW/TF-IDF

---

### 🔎 **Similarity Computation**

After converting movie data into feature vectors:

* **Cosine Similarity** measures the degree of closeness between movie vectors.
* **K-Nearest Neighbors (KNN)** identifies the *top K most similar* movies to a given input.

---

## 🧾 **Results**

Quantitative evaluation metrics (like accuracy or recall) are less meaningful for recommendations due to subjective user preferences.
Instead, we performed **qualitative analysis** based on the **relevance and contextual similarity** of the generated results.

**Key Observations:**

* **BoW:** Provided quick, interpretable results but missed deeper semantic context.
* **TF-IDF:** Improved distinctiveness of relevant matches.
* **BM25:** Produced the most *semantically coherent* and *contextually accurate* recommendations.
* **Example Output:** When querying *“The Dark Knight”*, the top recommendations included *“Batman Begins”*, *“Man of Steel”*, and *“The Dark Knight Rises”* — demonstrating strong thematic and cast relevance.

---

## 🧩 **Conclusion**

This project showcases the effectiveness of **content-based recommendation systems** built on textual and metadata analysis.
Among all tested methods, **BM25** consistently yielded the most **relevant and context-aware** results, proving ideal for real-world recommendation tasks.

Future improvements may include:

* Incorporating **semantic embeddings** (e.g., Word2Vec, Sentence Transformers)
* Introducing **genre-weighted scoring** for personalization
* Integrating a simple **web interface** for live recommendations

---

## 🧾 **Notes**

* The quality of recommendations depends heavily on data preprocessing and metadata completeness.
* **BM25** parameter tuning (`k1`, `b`) can further enhance retrieval performance.
* The system architecture is **scalable and easily extensible** to other domains (books, music, etc.).

---

## ⚖️ **License**

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 **Author**

**Alluri Lakshman Narendra**
Department of Computer Science,
Indian Institute of Technology Dharwad

📧 [220010002@iitdh.ac.in](mailto:220010002@iitdh.ac.in)
🔗 [GitHub Profile](https://github.com/lakshmannarendra)

---
