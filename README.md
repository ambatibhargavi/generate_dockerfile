### **🐳 Dockerfile Generator**  
_A GenAI-powered tool that generates optimized Dockerfiles based on programming language input._  
This project utilizes **Ollama** with the **Llama3 model** to create Dockerfiles following **best practices**.  
![Your paragraph text (1)](https://github.com/user-attachments/assets/6222bc2e-b7d0-490e-a0dd-c09a1408fd24)

---

## **📋 Prerequisites**  

### **Install Ollama**  
🔹 **For Linux:**  
```bash
curl -fsSL https://ollama.com/install.sh | sh
```  

🔹 **For macOS:**  
```bash
brew install ollama
```
![Screenshot 2025-03-18 at 22 13 06](https://github.com/user-attachments/assets/a0a3ae24-9f70-4d06-b48d-1cbf34120208)


### **Start Ollama Service**  
```bash
ollama serve
```  

### **Download Llama3 Model**  
```bash
ollama pull llama3.2:1b
```  
![Screenshot 2025-03-18 at 22 05 20](https://github.com/user-attachments/assets/a1cbfd90-5b1d-40f8-9d80-4e54e2c6a502)
![Screenshot 2025-03-18 at 22 03 53](https://github.com/user-attachments/assets/242a97b3-9b3e-4a8b-a3dc-09a663a28b0b)
![Screenshot 2025-03-18 at 22 03 34](https://github.com/user-attachments/assets/37a126e1-593b-4f27-91d7-d93718e19bc3)
![Screenshot 2025-03-18 at 21 59 28](https://github.com/user-attachments/assets/743eb635-a801-47e0-adc8-f4f837bdfa6c)

---

## **🚀 Project Setup**  

### **1️⃣ Create a Virtual Environment**  
```bash
python3 -m venv venv
source venv/bin/activate  # On Linux/macOS
# or
.\venv\Scripts\activate  # On Windows
```  

### **2️⃣ Install Dependencies**  
```bash
pip3 install -r requirements.txt
```  

### **3️⃣ Run the Application**  
```bash
python3 generate_dockerfile.py
```  

---

## **💡 How It Works**  
✅ The script **takes a programming language as input** (e.g., Python, Node.js, Java).  
✅ Connects to the **Ollama API** running locally.  
✅ Generates an **optimized Dockerfile** with best practices for the specified language.  
✅ Returns the **Dockerfile content** with explanatory comments.  

---

## **📝 Example Usage**  
```bash
python3 generate_dockerfile.py
```
📌 **Input:**  
```
Enter programming language: python
```
📌 **Output:** _(Generated Dockerfile)_  
```Dockerfile
FROM python:3.10-slim
WORKDIR /app
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "app.py"]
```

---

## **🏆 Troubleshooting**  
🛠 **Ensure Ollama is running before executing the script.**  
```bash
ollama serve
```  

🛠 **Verify that the correct model is installed:**  
```bash
ollama list
```  
Expected output:  
```
NAME                ID              SIZE      MODIFIED           
llama3.2:1b         baf6a787fdff    1.3 GB    About a minute ago    
```

🛠 **If the script throws a model error, use an available model:**  
Replace this in `generate_dockerfile.py`:  
```python
response = ollama.chat(model='llama3.2:1b', messages=[{'role': 'user', 'content': PROMPT.format(language=language)}])
```

---

## **📜 License**  
This project is licensed under the **MIT License**.  

---

## **📬 Contact & Contributions**  
💡 **Got ideas or improvements?** Feel free to **fork & contribute**!  
📩 Reach out on **[LinkedIn](https://www.linkedin.com/in/ambatibhargavi/)** or **[GitHub](https://github.com/ambatibhargavi)**.  

