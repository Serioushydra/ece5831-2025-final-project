# Intelligent Triage for Customer Support Tickets

## Project Overview
This project implements an intelligent customer support ticket triage system using Natural Language Processing (NLP) and Large Language Models (LLMs). The goal is to automatically classify real-world customer complaint narratives into the correct financial product category, reducing manual routing effort and improving efficiency.

The project compares a traditional machine learning baseline (TF-IDF + Logistic Regression) with a modern LLM-based approach using a QLoRA fine-tuned Llama-3 (8B) model. The system is evaluated using weighted F1-score due to strong class imbalance and is deployed as a web application for real-time prediction.

---

## Dataset
We use the **Consumer Financial Protection Bureau (CFPB) Consumer Complaint Dataset**, which contains real customer complaints submitted to financial institutions in the United States.

- Input (X): Customer complaint narrative (unstructured text)
- Target (Y): Financial product category (20 classes)
- Dataset link:  
  https://www.consumerfinance.gov/data-research/consumer-complaints/

Due to the large size of the original dataset (over 2 million records), a stratified sample of 100,000 complaints is used to ensure representation of minority classes while enabling efficient experimentation.

---

## Repository Contents

### 📁 Files in This Repository
- `EDA_and_Baseline.ipynb`  
  Exploratory Data Analysis and baseline TF-IDF + Logistic Regression model.

- `Finetuning.ipynb`  
  Fine-tuning Llama-3 (8B) using Quantized Low-Rank Adaptation (QLoRA).

- `app.py`  
  Streamlit web application for real-time complaint classification.

- `Final_Report.pdf`  
  Final project report written in IEEE format.

- `Customer_Support_Triage_Presentation.pptx`  
  Presentation slides used for the project walkthrough.

- `Youtube-Demo-Video.mp4`  
  Short demo video showing the deployed application.

- `ece5831-Final-Presentation-Recording.mp4`  
  Full pre-recorded project presentation.

- `Output_screenshots/`  
  Screenshots showing classification results and confidence scores.

---

## Results Summary
- Baseline Model (TF-IDF + Logistic Regression):  
  Weighted F1-score ≈ 0.73

- LLM Model (Llama-3 + QLoRA):  
  **Weighted F1-score = 0.7333**

The LLM-based model demonstrates strong contextual understanding and produces interpretable confidence scores, especially for well-defined categories such as Debt Collection and Mortgage.

---

## Demo and Presentation Links
- A.**Final Report (PDF):**  
  `ECE-5831-Final-Report-Intelligent-Traige-For-Customer-Support-Tickets.pdf` 

- B.**Presentation Slides:**  
  `Customer_Support_Triage_Presentation.pptx`

- C.**Pre-recorded Presentation Video:**  
  `ECE-5831-Final-Presentation-Recording.mp4`

- D.**Demo Video:**  
  `ECE-5831-Final-Presentation-Recording.mp4`

- E.**Google Drive Folder:**
https://drive.google.com/your-folder-link-here: https://drive.google.com/drive/folders/1C1vrYdnh6pHIPNi1xA8-uc1ZJr5hzxA9?usp=drive_link

- F.**Dataset Source:**  
  [https://www.consumerfinance.gov/data-research/consumer-complaints/](https://drive.google.com/drive/folders/1C1vrYdnh6pHIPNi1xA8-uc1ZJr5hzxA9?usp=drive_link)

---

## How to Run the Project

### 1. Install Dependencies
```bash
pip install -r requirements.txt
