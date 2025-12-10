<div align="center">

# 🎨 AI-Powered Design Studio
### 

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=500&size=22&pause=1000&color=3498DB&center=true&vCenter=true&width=600&lines=The+Sales+Automation+Platform+for+Designers;Developer%3A+Ahmed+Hashim;Date%3A+December+10%2C+2025" alt="Project Info Typing SVG" />

<p align="center">
  <img src="https://img.shields.io/badge/Status-In%20Development-yellow?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Focus-AI%20%26%20Behavioral%20Psychology-blueviolet?style=for-the-badge" alt="Focus">
  <img src="https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge" alt="License">
</p>

</div>

---

## 📋 Executive Summary

**This is not just a portfolio.**

This project is a comprehensive **Sales Automation Platform** tailored for graphic designers. It leverages advanced **Artificial Intelligence** and principles of **Behavioral Psychology** to actively convert passive visitors into high-value, paying clients.

The core philosophy is to remove friction and demonstrate immediate value ("Show, Don't Tell") before any financial commitment is requested.

---

## 🛠️ High-Performance Tech Stack

This project is built on a modern, scalable, and robust architecture designed for speed and complex background processing.

| Domain | Technologies |
| :--- | :--- |
| **Frontend (SPA)** | ![React](https://img.shields.io/badge/-React.js-61DAFB?logo=react&logoColor=white) ![Vite](https://img.shields.io/badge/-Vite-646CFF?logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/-Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white) ![Framer Motion](https://img.shields.io/badge/-Framer_Motion-0055FF?logo=framer&logoColor=white) ![Redux Toolkit](https://img.shields.io/badge/-Redux_Toolkit-764ABC?logo=redux&logoColor=white) |
| **Backend (API)** | ![Django](https://img.shields.io/badge/-Django-092E20?logo=django&logoColor=white) ![DRF](https://img.shields.io/badge/-Django_REST_Framework-A30000?logo=django&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-336791?logo=postgresql&logoColor=white) |
| **AI Engine** | ![OpenAI](https://img.shields.io/badge/-OpenAI_GPT--4o-412991?logo=openai&logoColor=white) ![Whisper](https://img.shields.io/badge/-Whisper_API-svg?logo=openai&logoColor=white) ![DALL-E 3](https://img.shields.io/badge/-DALL--E_3-svg?logo=openai&logoColor=white) ![Gemini](https://img.shields.io/badge/-Google_Gemini-8E75B2?logo=google&logoColor=white) |
| **Automation & DevOps** | ![Celery](https://img.shields.io/badge/-Celery-37814A?logo=celery&logoColor=white) ![Redis](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white) ![AWS S3](https://img.shields.io/badge/-AWS_S3-232F3E?logo=amazon-aws&logoColor=white) |

---

## 🧠 Features & The Psychology Behind Them

We map technical features to specific psychological triggers to maximize conversion rates.

### 1. The Hook: AI Style Matcher
* **🎯 Feature:** The user enters their industry (e.g., "Coffee Shop," "Real Estate"). The entire website theme (colors, fonts, background) instantly adapts to reflect that industry.
* **💡 Psychology:** **Cocktail Party Effect & Implicit Egotism**. The brain subconsciously focuses immediately on information relevant to itself.
* **⚙️ Tech Flow:** React Input ➔ Django API ➔ GPT (Generate Hex Codes) ➔ React Context Update.

### 2. The Lead Magnet: AI Logo Audit
* **🎯 Feature:** Users upload their current logo and receive an instant, AI-generated PDF report analyzing its strengths and weaknesses.
* **💡 Psychology:** **Reciprocity**. By providing significant upfront value for free, we create a psychological urge in the client to return the favor (i.e., hire us).
* **⚙️ Tech Flow:** Image Upload ➔ Celery Worker ➔ GPT-4o Vision Analysis ➔ PDF Generation ➔ Email Dispatch.

### 3. Reducing Cognitive Load: Voice Brief Generator
* **🎯 Feature:** Clients can speak their project requirements instead of typing. The system converts audio to text and generates a visual "Moodboard."
* **💡 Psychology:** **Law of Least Effort**. Reducing the energy required to start the process significantly increases the likelihood of follow-through.
* **⚙️ Tech Flow:** Audio Blob Recording ➔ Whisper API (STT) ➔ GPT (Keyword Extraction) ➔ DALL-E 3 (Concept Generation).

### 4. The Close: Smart Pricing & Auto-Contract
* **🎯 Feature:** An interactive pricing calculator. Once approved, the system automatically generates a binding contract, creates a user account, and issues the first invoice.
* **💡 Psychology:** **Commitment & Consistency**. Once a client has customized their order and clicked "approve," they feel internally committed to finalizing the deal.

### 5. Retention: Client Dashboard
* **🎯 Feature:** Clients view their project progress on a real-time timeline.
* **💡 Psychology:** **Operational Transparency**. Seeing the work happen increases perceived value and trust.

---

## 🗄️ Database Schema Overview (Modular Design)

Designed for flexibility using PostgreSQL and JSONB.

* `Users`: Registered Clients & Admins. Contains **`brand_archetype`**.
* `Leads`: Visitors who used free tools. Tracked via **`interaction_score`**.
* `AI_Interactions`: Central log for all AI requests, storing results in **`ai_response_json`**.
* `Projects`: Contracted work where **`status`** triggers automation hooks.
* `Project_Timeline`: Milestones visible to the client.
* `Quotations` & `Invoices`: Automated financial records.

---

## 🔄 Automation Workflows (Celery Workers)

Background tasks ensure the UI remains responsive while complex operations occur.

### Workflow 1: New Lead Audit
> **Trigger:** New entry in `AI_Interactions` (Type: LOGO_AUDIT).
1.  Analyze Image via GPT-4o Vision.
2.  Generate PDF Report.
3.  **Immediate Action:** Email "Your Report is Ready".
4.  **Delayed Action (24h):** Email "Did you like the report? Book a consultation."

### Workflow 2: Deal Signed
> **Trigger:** `Quotation.is_accepted` turns `True`.
1.  Convert `Lead` data to `User`.
2.  Initialize new `Project`.
3.  Generate Deposit `Invoice`.
4.  Notify the Designer (Admin).

### Workflow 3: Project Updates
> **Trigger:** Designer updates the `Project_Timeline`.
1.  **Action:** Send WhatsApp/Email notification to the Client: "Phase X Complete. See Details."

---

## 🚀 Getting Started (Development)

*Prerequisites: Docker & Docker Compose installed.*

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/ai-design-studio.git](https://github.com/yourusername/ai-design-studio.git)
    ```

2.  **Set up Environment Variables:**
    Rename `.env.example` to `.env` and add your API keys (OpenAI, AWS, DB credentials).

3.  **Build and Run with Docker:**
    ```bash
    docker-compose up --build
    ```
    The backend API will be at `http://localhost:8000` and frontend at `http://localhost:3000`.

---

<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&pause=1000&color=2ECC71&center=true&vCenter=true&width=500&lines=Developed+By%3A+Ahmed+Hashim;Full+Stack+Python+%26+AI+Developer" alt="Developer Animated Text" />

<p align="center">
  <a href="https://linkedin.com/in/yourprofile">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:your.email@example.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://github.com/yourusername">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>

<p align="center">
  <sub>© 2025 AI-Powered Design Studio. All Rights Reserved.</sub>
</p>

</div>
