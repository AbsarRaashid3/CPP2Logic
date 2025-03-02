# **CPP2Logic: AI-Powered C++ to Pseudocode Converter** 🚀  

**CPP2Logic** is a Transformer-based AI model that converts **C++ code into human-readable pseudocode**. It utilizes a **seq2seq deep learning architecture** to understand code structure and generate clear, logical explanations.  

## **🔍 Overview**  
CPP2Logic aims to bridge the gap between **complex C++ syntax and human understanding**, making code **more accessible** for students, educators, and developers.  

## **✨ Features**  
- 🚀 **AI-Powered Translation** - Converts C++ code into pseudocode with high accuracy  
- 🧠 **Transformer-based Model** - Utilizes a seq2seq architecture for code understanding  
- 📊 **Custom Training** - Trained on a structured dataset of C++-pseudocode pairs  
- 🎯 **Interactive Streamlit UI** - Allows real-time code conversion  
- 🔥 **Supports Large Code Blocks** - Handles complex logic structures  
- 🏆 **Improves Code Comprehension** - Helps programmers and learners grasp algorithms  

## **🛠 Tech Stack**  
- **Python** (Core Language)  
- **PyTorch** (Deep Learning Framework)  
- **NLP & Transformers** (Seq2Seq Model)  
- **Streamlit** (Web UI for live testing)  
- **C++** (Source Code Language)  



## **🚀 Installation & Setup**  
### **1️⃣ Clone the Repository**  
git clone https://github.com/AbsarRaashid3/CPP2Logic.git  
cd CPP2Logic

### **2️⃣ Install Dependencies**
Ensure you have Python 3.8+ and install the required libraries:
pip install -r requirements.txt

### **3️⃣ Preprocess Data**
Convert raw training data into paired C++-pseudocode samples:
python src/preprocess_code_to_pseudocode.py --input_tsv "data/spoc-train-train.tsv" --output_txt "data/train_pairs_code_to_pseudocode.txt"

### **4️⃣ Build Vocabulary**
python src/vocab.py --pairs_file "data/train_pairs_code_to_pseudocode.txt" --src_vocab_file "src/src_vocab_code2pseudo.pkl" --tgt_vocab_file "src/tgt_vocab_code2pseudo.pkl"

### **5️⃣ Train the Model**
python src/train_code_to_pseudocode.py --pairs_file "data/train_pairs_code_to_pseudocode.txt" --src_vocab_file "src/src_vocab_code2pseudo.pkl" --tgt_vocab_file "src/tgt_vocab_code2pseudo.pkl" --epochs 30 --batch_size 8

### **6️⃣ Run Inference (Convert C++ to Pseudocode)**
python src/infer_code_to_pseudocode.py --model_checkpoint transformer_code_to_pseudocode.pt --src_vocab_file "src/src_vocab_code2pseudo.pkl" --tgt_vocab_file "src/tgt_vocab_code2pseudo.pkl" --code "int main() { cout << 'Hello World'; }"

### **7️⃣ Run the Web App**
streamlit run src/app_code_to_pseudocode.py


## 📌 Future Improvements
### 🔄 Beam Search Decoding for better accuracy
### 🌎 Multi-Language Support (Python, Java)
### 🏆 Better Dataset Expansion for higher quality outputs
### ⚡ Model Optimization for faster inference

## 📩 Connect With Me
#### 💼 GitHub: AbsarRaashid3
### 📧 Email: absarrashid3@gmail.com
### 🔗 LinkedIn: www.linkedin.com/in/absarraashid

# 🚀 CPP2Logic is here to revolutionize code understanding and translation!

