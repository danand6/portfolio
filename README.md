# Projects Portfolio

Hi, I'm Dhruv. Here's a curated set of projects from research, coursework, and fun late-night builds.

## Coursework & Research Projects

### Job Recommender Service
**Repo:** [GitHub – job-recommender](https://github.com/danand6/job-recommender)  
**Stack:** Python (FastAPI, Pandas, NumPy), Sentence Transformers, FAISS, Docker, AWS App Runner, S3  
**What I built:** A semantic job recommendation engine that lets users submit free-form queries and receive relevant postings powered by embeddings and vector search.

**Highlights:**
- Semantic search with [Sentence Transformers](https://www.sbert.net/) embeddings instead of brittle keyword matching.  
- FAISS-backed vector index for sub-second similarity lookups across thousands of jobs.  
- FastAPI REST endpoints packaged as a Docker image and deployed on AWS App Runner.  
- Sample catalog (`catalog_sample.parquet`) included so anyone can experiment locally.

**Example query:**
```bash
curl -X POST https://<your-app-url>/recommend \
  -H "Content-Type: application/json" \
  -d '{"query":"machine learning engineer fintech","k":5}'

# Sample Response
# {
#   "items": [
#     {
#       "id": 3904724926,
#       "title": "Software Development Engineer, Fintech",
#       "score": 0.664,
#       "url": "https://www.linkedin.com/jobs/view/3904724926/"
#     },
#     ...
#   ]
# }
```

### F1 Visualization (D3.js)
**Stack:** JavaScript, D3.js, HTML/CSS  
**Repo:** [GitHub – d3-test-proj](https://github.com/blacklamma/d3-test-proj)  
**What I built:** Interactive scrollytelling visualizations of Formula 1, including driver performance, constructors, and track evolution using D3.js.  
**Highlights:** Custom hex map layout, animated line charts, and dynamic lasso selection for stateful interactivity.  
**Impact:** Designed for storytelling with clear, data-driven visuals tailored to motorsports analytics.

## Fun Projects

### Football Trip Planner – Agentic AI Travel Planning
**Repo:** [GitHub – football-trip-planner](https://github.com/danand6/football-trip-planner)  
**Stack:** Python (FastAPI, LangGraph), Next.js, Ollama (Llama 3), Server-Sent Events  
**What I built:** A full-stack trip planner that answers a question no travel tool handles well: *"I want to watch my team play somewhere in the world next month — plan the whole trip around the fixture."* The app finds real matches across competitions, picks the best destination given budget and flight cost, and generates a complete 7-day itinerary.

**Highlights:**
- 10-agent pipeline (LangGraph `StateGraph`) with a shared `PlannerState` — each agent has a single responsibility and a mock fallback, so the full pipeline works offline.
- Real fixture data from football-data.org and API-Football, with a `ChainedFixtureProvider` that falls back to mock data gracefully.
- Flight cost feeds into *destination selection*, not just the budget output — a budget traveller gets Manchester, a premium traveller might get Milan for the same fixture window.
- Live SSE streaming via `asyncio.Queue` + `ThreadPoolExecutor`: each agent fires `running` and `completed` events that animate a real-time pipeline UI in the browser.
- Weather for the travel window via Open-Meteo (historical climate data, no API key needed).
- Official match ticket links resolved for 30+ clubs with competition-level and StubHub fallbacks.
- 50 tests across unit, integration, and SSE stream layers.

**Example use case:**  
*"Man United, October, flying from San Francisco, mid-range budget"* → pipeline finds fixtures across EPL and Champions League, scores each by flight cost and budget level, selects the best destination, and returns a full itinerary with matchday on day 4, hotel areas, attractions, and a ticket link.

---

### FPL Toolkit – Vibe Coding with Codex
**Stack:** Python, Flask, React (Vite), Retrieval-Augmented Generation, OpenAI API  
**Repo:** [GitHub – fpl-toolkit-gui](https://github.com/danand6/fpl-toolkit-gui)  
**What I built:** A browser-based FPL assistant co-built with Codex that blends deterministic stats with an AI chat workflow, featuring chip strategy guidance, fixture-aware projections, and a Vite-powered UI.  
**Highlights:** Flask API with caching, intent classification, RAG pipeline, and reusable React components for charts, chat, and squad visualizations.

---

## Contact
- GitHub: [github.com/dhruv-anand6](https://github.com/dhruv-anand6)  
- LinkedIn: [linkedin.com/in/dhruv-anand6](https://linkedin.com/in/dhruv-anand6)  
- Email: danand6@asu.edu
