# python-qa-chatbot
Problem Statement  Develop a simple personal chatbot that can answer questions related to Python programming.
# 🐍 Python QA Assistant Chatbot

> A lightweight, client-side Question-Answering Chatbot built with **100% Python** and hosted directly on **GitHub Pages** via **PyScript**.

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyScript](https://img.shields.io/badge/PyScript-2024.1.1-3776AB?style=for-the-badge)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-222222?style=for-the-badge&logo=github)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📌 Project Overview

This project is a personal **Python Question-Answering Chatbot** created as an internship project. It is designed to run entirely in the web browser using Python. 

Unlike traditional web applications that require external servers (Flask, Django, or Node.js) or local developer tools (VS Code), this app uses **PyScript (WebAssembly)** to execute Python logic directly in the browser and host the application for free via **GitHub Pages**.

---

## ✨ Key Features

* **100% Python Backend Logic:** All core operations—including natural language query tokenization, vector math, dictionary lookups, and response rendering—are written in pure Python.
* **TF-IDF & Cosine Similarity Engine:** Uses custom vector mathematical processing written from scratch in Python (without heavy external libraries like `scikit-learn` or `numpy`) to compute relevance scores for user queries.
* **Interactive Explanations & Code Examples:** Answers standard Python programming questions (variables, data structures, OOP) and advanced topics (decorators, generators, walrus operator) complete with executable code snippets.
* **Zero Installation Required:** Developed, updated, and hosted entirely on GitHub without needing VS Code, Python installations, or local terminal commands.

---

## 🛠️ Architecture & Tech Stack

┌──────────────────────────────────────────────────────────────┐
│                      GitHub Pages                            │
│                                                              │
│  ┌────────────────────────────────────────────────────────┐  │
│  │                HTML/CSS Display Interface              │  │
│  └───────────────────────────┬────────────────────────────┘  │
│                              │                               │
│  ┌───────────────────────────▼────────────────────────────┐  │
│  │        PyScript / Pyodide (Python WebAssembly)         │  │
│  └───────────────────────────┬────────────────────────────┘  │
│                              │                               │
│  ┌───────────────────────────▼────────────────────────────┐  │
│  │             Python Matching & Calculation Engine       │  │
│  │                                                        │  │
│  │  • RegEx Tokenization & Cleaning                       │  │
│  │  • Term Frequency (TF) Calculation                     │  │
│  │  • Inverse Document Frequency (IDF) Matrix             │  │
│  │  • Cosine Similarity Scoring Engine                    │  │
│  │  • Knowledge Base (20+ Concepts & Examples)            │  │
│  └────────────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────────┘
| Layer | Technology | Function |
| :--- | :--- | :--- |
| **Execution Engine** | [PyScript](https://pyscript.net/) | Compiles Python code to WebAssembly to execute in-browser |
| **Match Engine** | Pure Python (`math`, `re`) | Preprocesses input text, computes TF-IDF vectors, and ranks responses |
| **Knowledge Base** | Python Dictionaries | Stores structured topics, text explanations, and code blocks |
| **Hosting** | [GitHub Pages](https://pages.github.com/) | Static web publishing directly from the main repository branch |

---

## 🧠 Matching Logic (TF-IDF & Cosine Similarity)

The chatbot uses natural language processing (NLP) primitives built in Python:

1. **Tokenization:** Converts input text into lowercase alphanumeric word arrays using `re.findall()`.
2. **Term Frequency (TF):** Calculates word density across individual documents and queries:
   $$\text{TF}(t) = \frac{\text{Count of } t \text{ in text}}{\text{Total words in text}}$$
3. **Inverse Document Frequency (IDF):** Penalizes common words while heavily weighting unique Python terms:
   $$\text{IDF}(t) = \ln\left(\frac{N + 1}{\text{DF}(t) + 1}\right) + 1$$
4. **Cosine Similarity:** Computes vector angles between the user query and knowledge base entries:
   $$\cos(\theta) = \frac{\mathbf{A} \cdot \mathbf{B}}{\Vert{}\mathbf{A}\Vert{} \Vert{}\mathbf{B}\Vert{}}$$

---

## 📚 Covered Python Topics

The knowledge base covers 20+ core and advanced Python concepts:

| Basic Concepts | Advanced Concepts |
| :--- | :--- |
| Variables & Data Types | List Comprehensions |
| Lists, Tuples & Dictionaries | Decorators (`@decorator`) |
| For & While Loops | Generators (`yield`) |
| Functions & `*args`/`**kwargs` | Context Managers (`with`) |
| Object-Oriented Programming (Classes) | `@dataclass` Modules |
| Exception Handling (`try/except`) | Functional Programming (`map`/`filter`/`reduce`) |
| Anonymous Functions (`lambda`) | Type Hinting & Walrus Operator (`:=`) |

---

## 🚀 Deployment Instructions

To deploy this project to your own GitHub repository:

1. **Create Repository:** Create a public GitHub repository named `python-qa-chatbot`.
2. **Add Code:** Create an `index.html` file in the root directory and paste your PyScript + HTML code.
3. **Enable GitHub Pages:**
   * Go to **Settings > Pages** in your repository.
   * Under **Build and deployment**, set **Source** to `Deploy from a branch`.
   * Set Branch to `main` (or `master`) and folder to `/ (root)`.
   * Click **Save**.
4. **Access Live Site:** Your site will be live at `https://<your-username>.github.io/python-qa-chatbot/`.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
