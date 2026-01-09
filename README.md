# AI Resume Search System

An intelligent system designed for HR departments to transform a passive PDF resume database into an active, strategic tool for talent discovery. It empowers recruiters to find the best-fit candidates in seconds using natural language queries, replacing tedious manual screening and keyword-based searches.

---

## 💬 Core Idea

The goal is to enable HR professionals to instantly source relevant candidates based on complex, nuanced requirements. Instead of spending hours manually reviewing hundreds of resumes, a recruiter can simply ask the Telegram bot:

> "Find a DevOps engineer who has reduced AWS costs."

Within seconds, the system returns a ranked list of candidates, complete with direct quotes from their resumes that prove their relevant experience.

The system analyzes not just keywords, but the **meaning and context** of each resume, uncovering qualified specialists who are easily missed by traditional search methods.

---

## ⚙️ Key Features

#### 📄 1. Automated Resume Ingestion & Indexing
✔️ The system automatically ingests and processes all PDF resumes from a designated cloud storage location (e.g., OneDrive).
✔️ Each resume is parsed to extract text, skills, experience, and key achievements.
✔️ The extracted data is then converted into semantic vectors and stored in a specialized vector database (Pinecone), creating an intelligent, searchable digital archive.

#### 🔍 2. Intelligent Natural Language Search
✔️ The entire search process is conducted through a user-friendly Telegram bot, requiring no special training or complex interfaces.
✔️ The system understands complex, contextual queries involving multiple conditions, specific metrics, or notable achievements.
✔️ Search results are automatically ranked by relevance, prioritizing candidates with exact matches before presenting those with semantically similar experience.

#### 🎯 3. Contextual and Evidence-Based Results
✔️ Recruiters receive clean, concise candidate cards with essential information, not just a list of files.
✔️ For each candidate, the system provides a **direct quote** from their resume, offering clear evidence of why they match the query.
✔️ A direct link to view the full PDF resume is included for in-depth review.

---

## 🧩 Tech Architecture

The system is available in two configurations, featuring different data indexing engines to meet specific business needs.

### **Comfort Engine** (based on Google Cloud Vision)
Utilizes Google's robust OCR service for text recognition and a secondary AI model for basic metadata extraction. This architecture is characterized by high stability and cost-effectiveness.

### **Business Engine** (based on Anthropic Claude)
Employs a cutting-edge multimodal model (Claude) that processes the entire PDF and returns perfectly structured data in a single step. This architecture ensures maximum indexing speed and superior data extraction quality.

### 🔧 Overall Tech Stack:
-   **Orchestration & Logic:** `n8n`
-   **User Interface:** `Telegram Bot API`
-   **Vector Database:** `Pinecone`
-   **LLM & AI Services:** `OpenAI (GPT-4o)`, `Anthropic Claude`, `Google Cloud Vision`
-   **Cloud Storage:** `OneDrive`
-   **Deployment & Testing:** `Docker`, `Docker Compose`, `ngrok`

---

## 💼 Business Impact

-  ✅ **Saves up to 40 hours of recruiter time per month** by eliminating manual screening.
-  ⚡️ **Accelerates time-to-hire** by providing instant access to a shortlist of relevant candidates.
-  🧠 **Improves quality-of-hire** by uncovering "hidden gems" within the company's existing talent pool.
-  💰 **Reduces Cost-per-Hire** through more efficient utilization of the internal candidate database.
-  🎯 **Increases the ROI of the HR team**, allowing specialists to focus on engaging top candidates rather than searching for them.
