

# Meme Caption Generator  

## 📌 Overview  
This project is a **Meme Caption Generator** that extracts text from meme images and generates humorous captions using AI.  

### 💡 Pipeline Overview:  
1. **Downloads a dataset** of memes from Kaggle  
2. **Extracts text from images** using Tesseract OCR  
3. **Generates image descriptions** using BLIP (Salesforce's Image Captioning model)  
4. **Generates meme captions** using the Mistral model via Ollama  

---

## 🛠️ Technologies Used  
- **Python**  
- **Pandas**  
- **KaggleHub**  
- **Pytesseract**  
- **Pillow (PIL)**  
- **Transformers (Hugging Face)**  
- **Ollama (Mistral)**  

---

## ⚙️ Installation & Setup  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/your-username/meme-caption-generator.git  
cd meme-caption-generator  
```


## 🐳 Run with Docker Compose  

This project uses Docker Compose to run the **Mistral model (via Ollama)**.

### ▶️ Start the Ollama Server  
Ensure Docker is installed, then run:
```bash
docker-compose up
```

### ⏳ Wait for this message to appear in the terminal:
```
✅ Mistral model pulled and ready.
```

Once you see that, you can run the meme caption pipeline in your Python script.

---

## 🧠 Run the Meme Captioning Pipeline  
Once everything is set up, generate meme captions like so:
```python
for i in range(7):
    captions = pipeline(urls[i])
    print("Caption:", captions)
```

---

## 🎯 Sample Output  

![image](https://github.com/user-attachments/assets/a509d554-2657-4083-8bad-be62499fe155)


---
