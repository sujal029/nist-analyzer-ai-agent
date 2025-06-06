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

## 📂 Usage

Run the AI agent script:

python app.py
In the browser UI:

Upload a policy file (PDF or DOCX)

Click Analyze Policy to see gaps and download reports

Ask questions about your policy in the text box

Click Ask to get answers from your policy or Google Search fallback

📝 What It Does
Extracts text from your uploaded file

Compares each NIST control to your policy text using semantic similarity

Marks controls as Covered or Gap Found

Suggests improvements for gaps

Supports advanced Q&A powered by transformers and SerpAPI web search

📄 NIST 800-171 Controls Covered
AC.L1-3.1.1 to AC.L2-3.1.22 (Account Management domain subset)

🚫 Limitations
Supports only PDF and DOCX uploads

Quality depends on your policy document text content

Requires internet for SerpAPI-powered web search fallback

👨‍💻 Developed By
Sujal Singh Bais

🔗 Links
SerpAPI

Gradio

Sentence Transformers

Hugging Face Transformers

🧪 Example
Gap Output:

❌ AC.L2-3.1.8: Limit unsuccessful login attempts.  
Improvement: Implement account lockout or delay after multiple failed login attempts.
Q&A Output:

📄 Answer from policy (confidence: 0.85):  
The policy requires automatic lockout after 5 failed login attempts.
Enjoy automating your NIST 800-171 gap analysis!



