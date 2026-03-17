# 🧾 Tax Document Intelligence System

> AI-Powered Receipt & Invoice Data Extraction — NLP & MLOps Final Year Project

---

## 🚀 Live Demo

👉 **HuggingFace Space:** [tax-document-intelligence](https://huggingface.co/spaces/Attiqfr/tax-document-intelligence)

---

## 🎯 Project Overview

**Tax Document Intelligence** is an end-to-end NLP system that automatically extracts financial data from invoices, receipts, and tax documents using Computer Vision, Transformers, and a clean Gradio interface.

---

## ✨ Key Features

- 📸 **OCR Engine** — Extract text from any receipt or invoice image using EasyOCR
- 🤖 **Document Classifier** — Auto-detect document type (Invoice / Receipt / Tax Form) using DistilBERT
- 🔍 **Smart Entity Extraction** — Pull out vendor, amount, date, invoice number, and line items
- 🗄️ **SQLite Database** — Every extraction saved and browsable
- 🎨 **Gradio Interface** — Clean, professional interactive UI

---

## 🛠️ Tech Stack

| Component        | Technology                  |
|------------------|-----------------------------|
| OCR Engine       | EasyOCR                     |
| Classifier       | DistilBERT (Zero-Shot)      |
| Entity Extraction| Smart Regex Patterns        |
| Database         | SQLite + SQLAlchemy         |
| Interface        | Gradio                      |
| Image Processing | OpenCV + PIL                |
| Runtime          | Google Colab (GPU: T4)      |

---

## 📊 What Gets Extracted

- ✅ Vendor / Company Name
- ✅ Invoice / Receipt Number
- ✅ Date
- ✅ Subtotal, Tax Amount, Total
- ✅ Line Items (product names + prices)
- ✅ Document Type Classification

---

## ▶️ How to Run

### Option 1 — Google Colab (Recommended)
1. Open `Tax_Document_Intelligence_Demo.ipynb` in Google Colab
2. Run all cells top to bottom
3. Click the Gradio public URL that appears

### Option 2 — Local
```bash
git clone https://github.com/CoderAttiq/tax-document-intelligent-System.git
cd tax-document-intelligent-System
pip install easyocr opencv-python-headless pillow transformers torch gradio sqlalchemy pymupdf
jupyter notebook Tax_Document_Intelligence_Demo.ipynb
```

---

## 🔄 Pipeline Architecture
```
Image Upload
     │
     ▼
Image Preprocessing  ← Grayscale + Denoise + CLAHE
     │
     ▼
EasyOCR Engine       ← Extract raw text
     │
     ▼
DistilBERT Classifier ← Invoice / Receipt / Tax Form
     │
     ▼
Regex Entity Extractor ← Vendor, Total, Date, Items
     │
     ▼
SQLite Database       ← Persistent storage
     │
     ▼
Gradio UI Display     ← Show results
```

---

## 👨‍💻 Author

**Muhammad Attiq**
- HuggingFace: [Attiqfr](https://huggingface.co/Attiqfr)
- GitHub: [CoderAttiq](https://github.com/CoderAttiq)

---

## 🏆 Built For

**NLP & MLOps Final Year Project — Bootcamp Cohort 14**

---

*Made with ❤️ using Python, Transformers & Gradio*
