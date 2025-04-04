# Meme Caption Generator  

## 📌 Overview  
This project is a **Meme Caption Generator** that extracts text from meme images and generates humorous captions using AI. The pipeline:  
1. **Downloads a dataset** of memes from Kaggle.  
2. **Extracts text from images** using Tesseract OCR.  
3. **Generates descriptions** of the images using BLIP (Salesforce's Image Captioning model).  
4. **Creates meme captions** using the Mistral model from Ollama.  

## 🛠️ Technologies Used  
- **Python** (Core language)  
- **Pandas** (For dataset handling)  
- **KaggleHub** (For dataset retrieval)  
- **Pytesseract** (OCR for text extraction)  
- **PIL (Pillow)** (For image processing)  
- **Transformers (Hugging Face)** (For image captioning)  
- **Ollama (Mistral Model)** (For generating humorous captions)  

## ⚙️ Installation & Setup  

### 1️⃣ Install Dependencies  
Make sure you have Python installed, then install all required dependencies using:  
```bash
pip install -r requirements.txt
```  

### 2️⃣ Install & Configure Tesseract OCR  
- Download & install **Tesseract OCR** from [here](https://github.com/UB-Mannheim/tesseract/wiki).  
- Update the **Tesseract path** in the script:  
  ```python
  pytesseract.pytesseract.tesseract_cmd = r'C:\Path\To\Tesseract-OCR\tesseract.exe'
  ```  

### 3️⃣ Download the Meme Dataset  
- Ensure you have Kaggle API credentials set up.  
- Run the following command to download the dataset:  
  ```python
  import kagglehub
  path = kagglehub.dataset_download("akuppps/dankmemes-reddit-top-comments")
  ```  

### 4️⃣ Run the Pipeline  
Run the script to generate meme captions:  
```python
for i in range(7):
    print(urls[i])
    captions = pipeline(urls[i])
    print(captions)
```  

## 🎯 Output Example  
```
https://example-meme.com/meme1.jpg
"When you realize it's Monday again... 😭"
```  
