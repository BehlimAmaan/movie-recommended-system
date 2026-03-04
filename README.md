# 🎬 MovieMind AI – Movie Recommendation System

A **Content-Based Movie Recommendation System** built using **TF-IDF Vectorization** and **Cosine Similarity**.
The system recommends movies similar to a selected movie based on textual features like genres, overview, cast, and keywords.

The project uses **FastAPI for the backend** and **Streamlit for the frontend**, providing an interactive interface for users to discover similar movies.

---

# 🌐 Live Demo

🚀 Try the application here:
👉 [https://moviemind-ai.streamlit.app/](https://moviemind-ai.streamlit.app/)

Users can search for a movie and instantly receive **top recommended movies** based on similarity.

---

# 🚀 Project Overview

Recommendation systems are widely used in platforms like Netflix, Amazon, and Spotify to personalize user experiences.

This project demonstrates how **Natural Language Processing (NLP)** techniques can be applied to build a **content-based recommendation engine**.

The system analyzes movie metadata and recommends similar movies using **text similarity techniques**.

---

# 🧠 Recommendation Method

This system uses **Content-Based Filtering**.

### 1️⃣ Data Preprocessing

* Handling missing values
* Cleaning text data
* Removing special characters
* Normalizing text

### 2️⃣ Feature Engineering

Important columns are combined into one feature:

```
genres + keywords + overview + cast + crew
```

This creates a **rich textual representation of each movie**.

### 3️⃣ TF-IDF Vectorization

Text data is converted into numerical vectors using:

```
TfidfVectorizer
```

TF-IDF assigns higher importance to rare but meaningful words.

### 4️⃣ Similarity Computation

Movie similarity is calculated using:

```
cosine_similarity
```

Movies with the **highest similarity scores** are recommended.

---

# 🏗️ System Architecture

```
User (Streamlit UI)
        │
        ▼
FastAPI Backend (API)
        │
        ▼
Recommendation Engine
(TF-IDF + Cosine Similarity)
        │
        ▼
Movie Dataset
```

---

# 🛠️ Tech Stack

| Technology   | Purpose                    |
| ------------ | -------------------------- |
| Python       | Core programming language  |
| FastAPI      | Backend API                |
| Streamlit    | Frontend UI                |
| Scikit-learn | TF-IDF & Cosine Similarity |
| Pandas       | Data processing            |
| NumPy        | Numerical operations       |
| Uvicorn      | ASGI server                |

---

# 📂 Project Structure

```
MovieMind-AI
│
├── data
│   ├── raw
│   │   └── movies_metadata.csv
│   │
│   └── processed
│       └── cleane_movie_dataset.csv
│
├── notebook
│   └── movie_recommendation.ipynb
│
├── app.py                 # Streamlit frontend application
├── main.py                # FastAPI backend API
│
├── tfidf.pkl              # Saved TF-IDF vectorizer
├── tfidf_matrix.pkl       # TF-IDF feature matrix
├── indices.pkl            # Movie title index mapping
├── df.pkl                 # Processed movie dataframe
│
├── requirements.txt       # Project dependencies
├── .env                   # Environment variables
├── .gitignore             # Ignored files
│
└── README.md              # Project documentation
```

---

# ⚙️ Installation

### Clone the repository

```bash
git clone https://github.com/yourusername/movie-recommender.git
cd movie-recommender
```

### Create virtual environment

```
python -m venv venv
```

Activate environment:

**Windows**

```
venv\Scripts\activate
```

**Mac/Linux**

```
source venv/bin/activate
```

---

### Install dependencies

```
pip install -r requirements.txt
```

---

# ▶️ Running the Application

### Run FastAPI backend

```
uvicorn app:app --reload
```

Backend runs on:

```
http://127.0.0.1:8000
```

---

### Run Streamlit frontend

```
streamlit run streamlit_app.py
```

Frontend runs on:

```
http://localhost:8501
```

---

# 🎯 Features

✔ Content-based movie recommendation
✔ TF-IDF based similarity engine
✔ FastAPI REST API backend
✔ Interactive Streamlit interface
✔ Deployed web application
✔ Scalable architecture

---

# 🔮 Future Improvements

* Hybrid recommendation system
* Deep learning embeddings
* Personalized recommendations
* Movie posters using TMDB API
* Docker deployment

---

