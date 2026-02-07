

# 🚀 LLM Applications – Production Ready RAG System

A comprehensive, practical guide to building **Retrieval Augmented Generation (RAG)** based Large Language Model applications designed for real-world production environments.

---

## 📌 Overview

This project demonstrates how to design, develop, evaluate, and deploy scalable LLM-powered applications using modern tools such as **Ray, Anyscale Endpoints, and OpenAI models**.

The guide walks through every stage of a production-grade RAG pipeline—from data ingestion to deployment—while focusing on scalability, evaluation, and cost optimization.

---

## 🔗 Resources

* **Blog Post (Part 1):**
  [https://www.anyscale.com/blog/a-comprehensive-guide-for-building-rag-based-llm-applications-part-1](https://www.anyscale.com/blog/a-comprehensive-guide-for-building-rag-based-llm-applications-part-1)

* **GitHub Repository:**
  [https://github.com/jpb2022/-END-TO-END-LLM-RAG-PRODUCTION-PIPELINE](https://github.com/jpb2022/-END-TO-END-LLM-RAG-PRODUCTION-PIPELINE)

* **Interactive Notebook:**
  [https://github.com/jpb2022/-END-TO-END-LLM-RAG-PRODUCTION-PIPELINE.ipynb](https://github.com/jpb2022/-END-TO-END-LLM-RAG-PRODUCTION-PIPELINE.ipynb)

* **Anyscale Endpoints:**
  [https://endpoints.anyscale.com/](https://endpoints.anyscale.com/)

* **Ray Framework Documentation:**
  [https://docs.ray.io/](https://docs.ray.io/)

---

## 🎯 What You Will Learn

By following this guide, you will learn how to:

* 💻 Build a complete **RAG-based LLM application** from scratch
* 🚀 Scale critical components such as:

  * Data loading
  * Text chunking
  * Embedding generation
  * Indexing
  * Model serving
* ✅ Evaluate system performance at multiple levels:

  * Component-level (e.g., retrieval_score)
  * End-to-end quality (quality_score)
* 🔀 Implement **hybrid LLM routing** to intelligently balance:

  * Open-source models
  * Proprietary models
* 📦 Deploy the application in a scalable, highly available architecture
* 💥 Understand real-world product impact and business value of LLM applications

---

## 🧩 System Architecture

<img width="800" src="https://images.ctfassets.net/xjan103pcp94/7FWrvPPlIdz5fs8wQgxLFz/fdae368044275028f0544a3d252fcfe4/image15.png">

The architecture covers:

* Data preprocessing
* Semantic embeddings
* Vector indexing
* Hybrid retrieval
* Reranking
* LLM generation
* API deployment

---

# ⚙️ Setup Guide

Follow the steps below to set up the project and run the interactive notebook.

---

## 1️⃣ API Keys

This project uses:

* **OpenAI APIs** for models like `gpt-3.5-turbo` and `gpt-4`
* **Anyscale Endpoints** for serving open-source models such as `Llama-2-70b`

Make sure you have credentials from:

* OpenAI: [https://platform.openai.com](https://platform.openai.com)
* Anyscale: [https://endpoints.anyscale.com](https://endpoints.anyscale.com)

---

## 2️⃣ Compute Environment

### Option A – Local Setup

You can run the project locally, but a GPU-enabled environment is strongly recommended for faster performance.

---

### Option B – Recommended: Anyscale Cloud

For optimal performance:

* Launch an **Anyscale workspace** using:

  * Instance type: `g3.8xlarge`
  * 2 GPUs and 32 CPUs
* Use the cluster environment:

  * `default_cluster_env_2.6.2_py39`
* Prefer region: `us-west-2`

  * Provides access to shared artifacts (vector DB dumps, docs, etc.)

If not using Anyscale, configure a similar GPU-enabled environment on your preferred cloud platform.

---

## 3️⃣ Clone the Repository

```bash
git clone https://github.com/ray-project/llm-applications.git .
git config --global user.name <GITHUB-USERNAME>
git config --global user.email <EMAIL-ADDRESS>
```

---

## 4️⃣ Data Setup

Preprocessed documentation data is already available at:

```
/efs/shared_storage/goku/docs.ray.io/en/master/
```

If you want to load the data yourself, clone the repository into a shared directory accessible to workers.

---

## 5️⃣ Install Dependencies

```bash
pip install --user -r requirements.txt
export PYTHONPATH=$PYTHONPATH:$PWD
pre-commit install
pre-commit autoupdate
```

---

## 6️⃣ Configure Credentials

Create a `.env` file:

```bash
touch .env
```

Add the following environment variables:

```bash
OPENAI_API_BASE="https://api.openai.com/v1"
OPENAI_API_KEY="YOUR_OPENAI_API_KEY"

ANYSCALE_API_BASE="https://api.endpoints.anyscale.com/v1"
ANYSCALE_API_KEY="YOUR_ANYSCALE_API_KEY"

DB_CONNECTION_STRING="dbname=postgres user=postgres host=localhost password=postgres"
```

Activate them:

```bash
source .env
```

---

## 🚀 Run the Notebook

You are now ready to explore the full pipeline.

Open and execute the interactive notebook:

```
notebooks/rag.ipynb
```

This notebook walks you through:

* Building embeddings
* Creating vector indexes
* Implementing retrieval
* Evaluating configurations
* Serving the final RAG application

---

# 📦 Deployment

The project supports:

* Distributed execution with Ray
* Scalable API serving using Ray Serve
* Hybrid model routing
* Cost-aware inference

This makes it suitable for enterprise-scale LLM deployments.

---

# 📚 Learn More

* Discover how Ray and Anyscale help scale AI workloads:
  [https://github.com/ray-project/ray](https://github.com/ray-project/ray)
  [https://anyscale.com](https://anyscale.com)

* Serve and fine-tune open-source LLMs:
  [https://endpoints.anyscale.com](https://endpoints.anyscale.com)

* Real-world case studies at Ray Summit:
  [https://raysummit.anyscale.com](https://raysummit.anyscale.com)

---

## 🤝 Support

If your organization is building LLM-powered applications at scale, reach out to the Anyscale team for guidance:

📧 [jitendraguptaaur@gmail.com](mailto:jitendraguptaaur@gmail.com)

---

### ⭐ If you find this project useful, please consider starring the repository!

---

If you want, I can further customize this README for:

* Your personal GitHub portfolio
* Resume showcase
* Teaching material
* Startup product documentation

