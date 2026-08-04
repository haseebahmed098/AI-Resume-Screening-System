# ⚡ AI Resume Screening System

An AI-powered resume screening assistant that goes beyond a simple chatbot — it **computes** semantic match scores, skill-gap analysis, and ATS compatibility using real NLP/ML models, and layers an optional LLM-generated career report on top.

Built and run entirely on **Google Colab** — no local setup required.

---

## 🚀 Live Demo

Run the notebook in Colab and launch the Gradio app to get a shareable public link with a full interactive UI.

## 📸 Preview

> _Add a screenshot or GIF of the app here (e.g. `assets/demo.png`) once you have one — it makes the repo much more compelling._

---

## 🧩 What's Inside

This repo contains **two notebooks**, from beginner to advanced:

### 1️⃣ `AI_Resume_Screening_System.ipynb` — Core Version
- TF-IDF + Cosine Similarity resume-to-job matching
- Keyword-based skill extraction
- Naive Bayes ML classifier for resume categorization
- PDF/TXT upload support
- Bonus: AI Career Assistant powered by the **Groq API** (free) — CV vs Job Description eligibility analysis

### 2️⃣ `AI_Resume_Screening_Advanced.ipynb` — Advanced Version
Everything above, upgraded with:

| Feature | Technology |
|---|---|
| 🧠 Semantic (meaning-based) matching | Sentence-Transformers (`all-MiniLM-L6-v2`) |
| 🏷️ Automatic candidate info extraction | spaCy NER + Regex (Name, Email, Phone, Experience) |
| 📊 Real-world classifier | Logistic Regression trained on a 2,484-resume, 24-category dataset |
| 🏆 **Resume Score (0–100)** | Custom weighted formula (semantic match + skill coverage + ATS score) |
| 🎯 **Skill Gap Analysis** | Visual chart of matched vs. missing skills against the job description |
| ✅ **ATS Compatibility Check** | Structure/formatting heuristic score (algorithmic, no LLM) |
| 🤖 AI Career Report | Optional Groq LLM layer that explains the computed results in plain English |
| 🌐 Web Interface | Gradio, with a custom futuristic neon UI |

> **Why this isn't "just a chatbot":** the Resume Score, Skill Gap chart, and ATS check are all computed independently through embeddings, regex, and a trained classifier — the LLM step is an optional final layer that explains those numbers, not the source of them.

---

## 🛠️ Tech Stack

- **NLP/ML:** Sentence-Transformers, spaCy, scikit-learn, TF-IDF
- **Data:** Hugging Face `datasets` (real-world Resume Dataset, 24 job categories)
- **LLM (optional):** [Groq API](https://console.groq.com/keys) — free tier, `openai/gpt-oss-120b`
- **Interface:** Gradio (custom-themed, responsive)
- **File handling:** PyPDF2 for PDF/TXT parsing
- **Environment:** Google Colab (Python 3)

---

## ▶️ How to Run

1. Open either notebook in **[Google Colab](https://colab.research.google.com/)**
   (`File → Upload notebook`, or open directly from this repo)
2. `Runtime → Run all`
3. For the AI Career Report step, get a **free Groq API key** at [console.groq.com/keys](https://console.groq.com/keys) (no card required)
4. In the Advanced notebook's last cell, a **public Gradio link** will be generated — open it to use the full web app
5. Upload a CV and Job Description (PDF, TXT, or pasted text — all supported) and click **Analyze**

---

## 📁 Repository Structure

```
AI-Resume-Screening-System/
├── AI_Resume_Screening_System.ipynb       # Core version (TF-IDF + Groq)
├── AI_Resume_Screening_Advanced.ipynb     # Advanced version (embeddings + NER + Gradio app)
└── README.md
```

---

## 🗺️ Roadmap

- [ ] Replace TF-IDF classifier with a fine-tuned DistilBERT model
- [ ] Add custom-trained NER for Education, Skills, and Company extraction
- [ ] Deploy the Gradio app permanently on Hugging Face Spaces
- [ ] Batch screening — rank multiple CVs against one job description

---

## 🤝 Contributing

Issues and pull requests are welcome. If you spot a bug or have an idea for a new feature, feel free to open an issue.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Haseeb Ahmed**
- GitHub: [@haseebahmed098](https://github.com/haseebahmed098)

---

⭐ If you find this project useful, consider giving it a star!
