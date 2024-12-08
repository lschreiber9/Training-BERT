# Climate Sentiment Analysis with BERT

This project leverages a fine-tuned BERT model to analyze text in ESG reports from industrial companies listed in the S&P 500. It classifies sentiment into **Risk**, **Opportunity**, or **Neutral**, helping to interpret how companies communicate about climate-related topics.

---

##  Classification Criteria

### 1. Risk  
A paragraph is classified as **"risk"** if it primarily discusses:  
- Business downside risks, potential losses, or adverse developments detrimental to the entity.  
- Negative impacts of the entity’s activities on society or the environment.  
- Specific negative adjectives describing anticipated, past, or present developments.

### 2. Opportunity  
A paragraph is classified as **"opportunity"** if it primarily discusses:  
- Business opportunities arising from mitigating or adapting to climate change that may benefit the entity.  
- Positive impacts of the entity’s activities on society or the environment.  
- Specific positive adjectives describing anticipated, past, or present developments.

### 3. Neutral  
A paragraph is classified as **"neutral"** if it primarily:  
- States facts and developments without framing them in a positive or negative perspective for the entity, society, or the environment.  
- Does not associate specific positive or negative adjectives with the facts or topics discussed.

---

##  Steps to Run

### 1. Prepare Data  
   - Download datasets (e.g., climate sentiment, specificity).  
   - Use the provided code to tokenize and preprocess the data.  

### 2. Train the Model  
   - Fine-tune a BERT model using the training script.  
   - Models are saved in `/content/drive/MyDrive/Big Data Project/NLP analysis/`.

### 3. Prepare Dataset of ESG-Reports
   - Extract text from PDFs
   - Keep only segments related to climate change

### 4. Analyze Text  
   - Use the trained model to predict sentiment for new climate-related text files.  
   - Results include sentiment labels:  
     - **`0` (Neutral):** Facts and developments without a positive or negative perspective.  
     - **`-1` (Risk):** Business risks, negative impacts, or adverse developments.  
     - **`1` (Opportunity):** Business opportunities or positive impacts.  

### 5. Save Results  
   - Export analysis results as **JSON** and **CSV** files for easy review.  

---

##  Requirements

- **Python**: 3.10+  
- **Libraries**: `transformers`, `torch`, `pandas`, `numpy`, 

