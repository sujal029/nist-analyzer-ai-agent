# 🔐 NIST 800-171 v3 Gap Analysis AI Agent

This AI Agent analyzes uploaded policy documents (PDF, DOCX) to find **gaps** compared to the NIST 800-171 Rev 3 Account Management controls.  
It uses semantic similarity to detect coverage gaps, suggests improvements, and supports question answering with fallback to Google Search results using SerpAPI.

---

## 🚀 Features

- Upload **PDF** or **DOCX** policy files (TXT support removed for stability)
- Automatically detects **gaps** in policy coverage vs NIST 800-171 controls
- Exports results as **Excel**, **JSON**, and **Text** summary reports
- Ask questions about your policy; if the answer isn't clear, fallback to live Google Search via SerpAPI
- Built with **Gradio** UI for easy drag-and-drop and chat interaction

---

## 🧰 Installation

Make sure you have Python 3.7+ installed. Then run:

```bash
pip install -q gradio sentence-transformers transformers docx2txt PyMuPDF openpyxl
pip install -q git+https://github.com/serpapi/google-search-results-python.git

