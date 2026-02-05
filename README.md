# SIC Capstone: Unified AI Dashboard (Team 013)

> **Phase 1 Delivery:** A unified web interface aggregating our Dual-AI Microservices.
> **Live Demo:** [**https://sic-team013-frontend.vercel.app/**](https://sic-team013-frontend.vercel.app/)

## ⚡ Overview
This repository hosts the **Frontend Presentation Layer** for Team 013's Capstone Project. 

Instead of a monolithic application, we adopted a **Micro-Frontend Architecture**. This lightweight dashboard acts as a shell, consuming our two headless AI "Brain" servers (hosted on Hugging Face) using **embedded integration**. This ensures zero-latency updates: if we improve the model backend, this dashboard updates instantly without redeployment.

## 🚀 Live Modules
This dashboard unifies two distinct AI pipelines into a single "Vertical Stack" experience:

| Module | Tech Stack | Function |
| :--- | :--- | :--- |
| **📄 Intelligent Resume Screener** | **Llama 3.3 (70B)** via Groq | Semantic analysis of candidates against Job Descriptions. |
| **🤖 AI Research Agent** | **LangChain + FAISS** | Agentic RAG workflow for querying private technical papers. |

---

## 🛠️ Architecture
The application is built using a **Serverless/Aggregator** approach:

* **Frontend (This Repo):** Pure HTML5/CSS3 dashboard hosted on **Vercel**. It aggregates the microservices into a seamless vertical layout.
* **Backend 1 (Resume):** Python/Gradio microservice hosting the Llama 3 inference logic.
* **Backend 2 (RAG):** Python/LangChain microservice hosting the Vector Database and Retrieval logic.

### Why this approach?
1.  **Decoupling:** The UI is completely separate from the heavy ML logic.
2.  **Scalability:** The frontend loads instantly (served by Vercel CDN) while the AI models spin up on demand.
3.  **Stability:** By using direct embedding, we bypass complex CORS/API restrictions, ensuring a reliable demo environment.

---

## 💻 Local Development

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/CodeByDiablo/sic-team013-frontend.git](https://github.com/CodeByDiablo/sic-team013-frontend.git)
    ```
2.  **Open in VS Code.**
3.  **Run with Live Server:**
    Right-click `index.html` and select **"Open with Live Server"**.

## 🌐 Deployment
This project is configured for **Zero-Config Deployment** on Vercel.

1.  Install Vercel CLI: `npm i -g vercel`
2.  Run command: `vercel --prod`

---

## 👥 Team 013
* **Vasamsetti Naga Bala (Swamy)** - Team Lead
* **Devesh Panwar** - Architecture & Frontend
* **Dhadi Eswar** - Data Pipelines
* **Kovvuri PC Durga Reddy** - Model Optimization
* **Sakshi** - Research & Validation

*Samsung Innovation Campus • Capstone Batch 25-26*
