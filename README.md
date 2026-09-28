<div align="center">
  <img src="banner.png" alt="Certificate Verifier Banner" width="100%"/>
  <h1>🔐 CertiFier — Smart Certificate Verification System</h1>
  <p><strong>A robust, AI-powered backend for authenticating and verifying digital certificates using Optical Character Recognition (OCR).</strong></p>

  [![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
  [![FastAPI](https://img.shields.io/badge/FastAPI-0.100%2B-009688?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
  [![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv)](https://opencv.org/)
  [![License](https://img.shields.io/badge/License-PolyForm%20Noncommercial-purple?style=for-the-badge)](LICENSE)
</div>

---

## 📌 Overview

**CertiFier** is an advanced certificate validation API designed to prevent fraud and ensure the authenticity of academic and professional certificates. 

By leveraging **Tesseract OCR (Optical Character Recognition)** and **OpenCV**, this system can scan uploaded certificate images, extract the text, and cross-reference the data against a secure **SQLite** database. It includes an admin panel and supports packaging as a standalone executable via PyInstaller.

---

## ⚡ Core Features

*   **🔍 AI-Powered OCR Extraction:** Uses `pytesseract` and `cv2` to read text directly from certificate images.
*   **🚀 High-Performance API:** Built with **FastAPI** for lightning-fast, asynchronous request handling.
*   **🗄️ Secure Database:** Uses SQLite to store valid certificate records, admin credentials, and logs.
*   **🛡️ Fraud Prevention:** Cross-checks extracted names, dates, and IDs against the database to instantly flag forged documents.
*   **📦 Standalone Executable:** Fully configured to be bundled into a `.exe` using PyInstaller (with bundled Tesseract support).
*   **🔗 CORS Enabled:** Ready to be connected to any modern frontend framework (React, Next.js, Vue).

---

## 🛠️ Installation & Setup

### 1. Prerequisites
You must have Python and Tesseract-OCR installed on your machine.
*   **Windows:** Install Tesseract from [UB-Mannheim](https://github.com/UB-Mannheim/tesseract/wiki)
*   **Mac/Linux:** `brew install tesseract` or `sudo apt install tesseract-ocr`

### 2. Clone the Repository
```bash
git clone https://github.com/BhavyaKansal20/Certificate-Verifier.git
cd Certificate-Verifier
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Server
```bash
uvicorn main:app --reload
```
The API will be live at `http://127.0.0.1:8000`. 
You can view the interactive API documentation (Swagger UI) at `http://127.0.0.1:8000/docs`.

---

## 🏗️ Project Architecture

```
Certificate-Verifier/
├── main.py               ← FastAPI server & OCR processing logic
├── database.py           ← SQLite database initialization & queries
├── database.db           ← The active SQLite database file
├── Main.html             ← Frontend dashboard for the verifier
├── requirements.txt      ← Python dependencies
└── uploads/              ← Directory for uploaded certificates and logos
```

---

## 🤝 Contributing

We welcome contributions to improve the OCR accuracy, enhance the API, or build out the frontend!
Please read our [Contributing Guidelines](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before submitting a pull request.

---

## 🔐 Security

This system handles sensitive verification data. If you discover any security vulnerabilities or bypass methods in the OCR validation, please refer to our [Security Policy](SECURITY.md) for reporting instructions.

---

## 📄 License

This project is licensed under the **PolyForm Noncommercial License 1.0.0** — see the [LICENSE](LICENSE) file for details. This means you are free to study, modify, and use this code for personal or educational purposes, but **commercial use (making money from this software) is strictly prohibited.**

---

<div align="center">
  Maintained with ❤️ by <strong>Bhavya Kansal</strong>
</div>
