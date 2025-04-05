# 📄 RFP Task Analyzer for Engineering Proposals

Extracting actionable tasks from RFP (Request for Proposal) documents is often one of the most challenging and time-consuming steps in writing technical proposals. This tool automates and streamlines that process using LLMs (Large Language Models) and RAG (Retrieval-Augmented Generation) techniques — saving engineers hours of manual work.

---

## 🔍 What This Tool Does

This project provides a **three-stage pipeline** to turn PDF RFP documents into a structured list of **proposal-ready engineering tasks**, complete with effort estimation, required expertise, and delivery guidance.

---

## 📊 Process Flow

<img src="images/workflow.png" width="400"/>

> ✅ **Tip**: Save the image in your repo as `images/workflow.png` (rename your uploaded image).

---

## 🧠 How It Works

### 🗂️ **Stage 1: Task Extraction**
- Upload one or more PDF RFP documents.
- The system reads the content paragraph by paragraph.
- Tasks are extracted using a large language model (LLM), chunked into 500-character blocks.

### 🧹 **Stage 2: Task Filtering**
- The LLM assumes the role of a **proposal engineer**.
- It filters out vague or non-actionable items.
- Only relevant, proposal-worthy tasks are kept.

### 🧠 **Stage 3: Detailed Task Analysis (RAG)**
- Uses **semantic search (RAG)** to retrieve the most relevant sections of the RFP for each task.
- For each task, the system estimates:
  - ✅ Whether it's a deliverable or activity
  - 👤 Who should do it (expertise, domain)
  - 🧑‍💻 Required experience level (junior, mid, senior)
  - ⏱️ Estimated effort/time
  - 📌 Why the task is important and how it fits in the project

---

## 🚀 Run in Google Colab

This project is optimized for Google Colab. Simply open the provided notebook and follow the steps:

1. Install dependencies
2. Upload PDF(s)
3. Add your OpenAI API key
4. Run through stages 1 to 3
5. Optionally export the results (CSV, TXT)

---

## 🧰 Requirements

- Python 3.8+
- [OpenAI API Key](https://platform.openai.com/)
- Dependencies (automatically installed in Colab):
  - `openai`
  - `PyMuPDF`
  - `sentence-transformers`
  - `google.colab`

---


## 📦 Output

The output consists of:
- A filtered list of proposal-ready tasks
- A detailed breakdown per task including resource estimates
- Printable or downloadable format (optional: CSV/TXT)

---

## 💡 Why Use This?

✅ Save engineering and proposal teams hours of manual work  
✅ Improve proposal quality and consistency  
✅ Focus your proposal only on high-impact, clearly defined tasks  
✅ Automate repetitive, error-prone analysis with LLM intelligence

---

## 🤝 Contributions

Pull requests and suggestions are welcome. If you're improving prompt tuning, task detection logic, or adding local LLM support — feel free to open an issue or submit a PR.

---

## 📄 License

MIT License — use freely, modify, and share. Just don't forget to give credit!

---
