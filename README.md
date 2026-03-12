# MentorMatch
### AI-Powered Mentorship Recommendation Platform

MentorMatch is an AI-driven recommendation system designed to connect aspiring professionals with suitable mentors based on **skills, experience, and career interests**.

The system analyzes mentor and mentee profiles using **Natural Language Processing (NLP)** techniques and semantic similarity to recommend the most compatible mentors.

This project demonstrates techniques from:

- Natural Language Processing (NLP)
- Recommendation Systems
- Web Data Collection
- Semantic Similarity Matching

---

# System Architecture

<p align="center">
  <img src="images/pipeline.png" width="900">
</p>

The system integrates multiple data sources and NLP techniques to identify the best mentor matches.

### 1. Data Collection

Two datasets are used:

- **LinkedIn profiles dataset** provided in the course
- **Web-scraped mentor data from MentorCruise**

MentorCruise data was collected using **Python Selenium** to gather information about mentors, including:

- Skills
- Professional fields
- Experience
- Technical expertise

---

### 2. Preprocessing

The scraped mentor profiles are processed to extract **clean skill representations**.

This stage includes:

- Removing irrelevant text
- Standardizing skill names
- Extracting relevant expertise areas

---

### 3. Filtering High-Tech Profiles

The extracted skills are used to filter the LinkedIn dataset and identify **high-tech professionals**.

These professionals are then categorized into:

- **Mentors**
- **Mentees**

---

### 4. Matching Process

When a user submits a query describing what they need help with, the system:

1. Converts the query into a text representation
2. Compares it with mentor profiles
3. Computes similarity scores
4. Ranks mentors based on relevance

Mentors with the highest similarity scores are returned to the user.

---

# Example Interface and Results

<p align="center">
  <img src="images/interface_example.png" width="900">
</p>

The interface allows users to describe the type of help they need (for example, *Python mentorship*).  
The system retrieves and ranks mentors based on their similarity to the query.

Each recommended mentor includes:

- Profile description
- Relevant experience
- Similarity score indicating compatibility

---

# Technologies Used

### Programming

- Python

### Libraries

- Pandas  
- NumPy  
- Selenium  
- BeautifulSoup  
- scikit-learn

### NLP Methods

- Word2Vec embeddings
- BERT embeddings
- Cosine similarity matching

---

# Project Pipeline


MentorCruise Scraping
+
LinkedIn Profiles
↓
Preprocessing & Skill Extraction
↓
Filtering High-Tech Professionals
↓
Mentor / Mentee Categorization
↓
User Query
↓
Similarity Matching
↓
Ranked Mentor Recommendations


---

# Evaluation

The system was evaluated on **1,000 mentor–mentee pairs**.

The matching system achieved approximately **60% average match accuracy**, demonstrating that semantic similarity methods can effectively identify relevant mentors.

---

# Future Improvements

Potential extensions include:

- Hybrid recommendation systems (content + collaborative filtering)
- Graph-based mentorship networks
- Fine-tuning domain-specific language models
- Integration with mentorship platforms via APIs
- Deploying the system as a web application

---

# Repository Structure


MentorMatch
│
├── data
├── scraping
├── preprocessing
├── matching
├── interface
│
├── images
│ ├── pipeline.png
│ └── interface_example.png
│
└── README.md


---

# Author

**Soaad Hamood**  
B.Sc. Data and Information Engineering  
Technion – Israel Institute of Technology  

GitHub:  
https://github.com/SoaadHamood
