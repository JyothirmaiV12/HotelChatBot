# 🏨 Hotel Chatbot using OpenAI, LangChain & Flask

This project demonstrates how to build an **interactive chatbot** that can answer questions based on custom data (such as PDFs and website content). It integrates **OpenAI’s GPT-3.5-Turbo model** with **LangChain** to provide context-aware responses and is deployed using **Flask**.

---

## ✅ **Features**

* Extracts data from **PDF documents** (hotel information) using `PyMuPDF (fitz)`
* Scrapes or fetches data from a given **website URL** (HTML page included)
* Uses **LangChain** to build a **custom prompt template** for dynamic question-answering
* Leverages **OpenAI’s GPT-3.5-Turbo** (configurable to other models)
* Supports multi-turn conversations with **system** and **user roles**
* Deployed using **Flask** with JSON-based responses
* Runs locally on `127.0.0.1:5000`

---

## 🛠 **Setup Instructions**

### 1. **Environment Setup**

* Install Python 3.8+
* Install the required libraries:

  ```bash
  pip install openai langchain flask pymupdf
  ```
* Get your **OpenAI API key** from the [OpenAI website](https://platform.openai.com/) and set it as an environment variable:

  ```bash
  export OPENAI_API_KEY="your_api_key_here"
  ```

### 2. **Data Preparation**

* Place your **hotel PDF file** in the project directory.
* The PDF data will be extracted using the `fitz` module from **PyMuPDF**.

---

## 🔗 **How It Works**

1. **Data Extraction**

   * PDF content is extracted using `fitz` (PyMuPDF).
   * Website/HTML page content is also processed to provide additional context.

2. **LangChain & Prompt Engineering**

   * A **custom prompt template** is created, allowing users to ask multiple questions.
   * **System role**: Defines the chatbot’s behavior (e.g., “You are a helpful assistant for hotel-related queries.”)
   * **User role**: Takes input queries from the user.

3. **OpenAI Integration**

   * Uses the `gpt-3.5-turbo` model (you can switch to other models like `gpt-4` if needed).

4. **Flask Deployment**

   * The chatbot is deployed locally via **Flask**.
   * Access it in your browser at:

     ```
     http://127.0.0.1:5000
     ```

5. **JSON Responses**

   * The chatbot returns structured JSON responses, making it easy to integrate into other applications.

---

## ▶️ **Running the Application**

1. Start the Flask server:

   ```bash
   python app.py
   ```
2. Open your browser and visit:

   ```
   http://127.0.0.1:5000
   ```
3. Ask your hotel-related questions — the bot will provide **relevant and contextual answers** based on the extracted data.

---
<img width="1470" height="956" alt="Screenshot 2025-07-22 at 5 21 07 PM" src="https://github.com/user-attachments/assets/e9949da4-b197-47c1-bfb0-3b6bc0bb8b1d" />
