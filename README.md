# Projects Portfolio

Hi, I’m Dhruv. Here’s a curated set of projects from research and coursework that I’m proud of.

---

## 🔍 Job Recommender Service
[🔗 View Repository](https://github.com/danand6/job-recommender)

A semantic job recommendation engine that helps users discover relevant postings using **natural language queries**. Instead of keyword matching, it leverages **embeddings** and **vector search** to capture semantic meaning.

### ✨ Features
- **Semantic Search** – powered by [Sentence Transformers](https://www.sbert.net/) for embedding generation.  
- **Vector Indexing** – built with **FAISS** for fast similarity lookups across thousands of jobs.  
- **REST API** – clean endpoints built with **FastAPI**.  
- **Dockerized & Deployed** – packaged into a Docker image and deployed on **AWS App Runner**.  
- **Demo Dataset** – includes a sample catalog (`catalog_sample.parquet`) so anyone can test locally.

### 🚀 Example Query
```bash
curl -X POST https://<your-app-url>/recommend \
  -H "Content-Type: application/json" \
  -d '{"query":"machine learning engineer fintech","k":5}'
Sampe Response:
{
  "items": [
    {
      "id": 3904724926,
      "title": "Software Development Engineer, Fintech",
      "score": 0.664,
      "url": "https://www.linkedin.com/jobs/view/3904724926/"
    },
    ...
  ]
}
```

### 🛠 Tech Stack

Python (FastAPI, Pandas, NumPy)

Machine Learning (FAISS, Sentence Transformers)

Infrastructure (Docker, AWS App Runner, S3)

---

## F1 Visualization (D3.js)
**Stack:** JavaScript, D3.js, HTML/CSS  
**Repo:** [GitHub – d3-test-proj](https://github.com/blacklamma/d3-test-proj)  
**What I built:** Interactive scrollytelling visualizations of Formula 1, including driver performance, constructors, and track evolution using D3.js.  
**Highlights:** Custom hex map layout, animated line charts, and dynamic lasso selection for stateful interactivity.  
**Impact:** Designed for storytelling with clear, data-driven visuals tailored to motorsports analytics.

---

## Contact
- GitHub: [github.com/dhruv-anand6](https://github.com/dhruv-anand6)  
- LinkedIn: [linkedin.com/in/dhruv-anand6](https://linkedin.com/in/dhruv-anand6)  
- Email: danand6@asu.edu
