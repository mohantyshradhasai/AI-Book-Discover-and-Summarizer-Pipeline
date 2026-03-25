# 📚 AI Book Discovery & Summarizer Pipeline

An automated intelligence system that leverages **Large Language Models (LLMs)** to discover high-value literature and generate structured, multi-section summaries. This project demonstrates the use of **LangChain Sequential Chains** to link multiple AI reasoning steps into a single workflow.

## 🌟 Key Features
- **Theme-Based Discovery:** Dynamically generates lists of the top 10 most influential books for any user-provided theme (e.g., "Finance," "Personality Development").
- **Sequential Intelligence:** Implements a `SequentialChain` where the output of the "Book Finder" agent serves as the context for the "Expert Summarizer" agent.
- **3x3 Structured Summaries:** Enforces strict output formatting—summaries are divided into **3 distinct sections** with **3 bullet points each** for high readability.
- **Real-Time Data Integration:** Includes a utility module using `yfinance` to bridge the gap between static LLM training data and real-time market information.
- **OCR Support:** Integrated with **Tesseract OCR** and **Pillow** for processing text from book covers or scanned images.

## 🛠️ Technical Stack
- **Orchestration:** LangChain (Chains, PromptTemplates, SequentialChain)
- **LLM Provider:** Cohere (Command-R Series)
- **Computer Vision:** Tesseract OCR, PIL (Pillow)
- **Data APIs:** Yahoo Finance (`yfinance`)
- **Environment:** Python 3.11+, Google Colab / Linux

## 📂 Project Architecture
1. **Book List Chain:** A `PromptTemplate` configured with a temperature of `0.5` to ensure a balanced mix of classic and trending book recommendations.
2. **Summary Generation Chain:** A high-temperature (`0.9`) chain that handles abstractive summarization, providing nuanced insights rather than simple text extraction.
3. **Execution Loop:** A Python driver that iterates through the generated list, providing a complete "reading guide" in
