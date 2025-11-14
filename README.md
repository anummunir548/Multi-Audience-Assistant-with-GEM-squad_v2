# Multi-Audience-Assistant-with-GEM-squad_v2
A Gemini-powered intelligent system that adapts tone, detail, and writing style based on the target audience.
- 🔥 Features
- 🧩 Project Architecture
- 🚀 How It Works
- 📥 Dataset Structure
- 🧠 Prompting Strategy
- ⚙️ Installation
- 🔑 API Setup
- 📘 Usage
- 📊 Evaluation Metrics
- 📈 Results Summary
- 🛠️ Project Structure
- 🤝 Contributing
- 📜 License
  # Features
- ### ✔ Audience-aware text generation
Automatically rewrites text for Kids, Developers, Professionals, or General public.

### ✔ Multiple Gemini model support
Compare outputs from:
- gemini-2.0-flash-exp  
- gemini-2.0-pro-exp  
- gemini-2.0-flash-lite-preview  

### ✔ Evaluation Metrics
Includes:
- Semantic Similarity  
- ROUGE-1 Score  
- Processing Speed  

### ✔ Function Calling
Demonstrates Gemini’s structured output & tool-calling system.

### ✔ Full logging system
Logs:
- prompts  
- generated outputs  
- evaluation scores  
- processing time
  #Project Architecture
- Input Text
     ↓
Target Audience
     ↓
Gemini Prompt Builder
     ↓
Gemini Model (Selected)
     ↓
Generated Output
     ↓
Evaluation (Semantic + ROUGE)
     ↓
Logging → CSV Results
#How It Works
1. Load dataset containing "Input_Text", "Target_Audience", and "Output_Text".
2. Build a dynamic audience-specific prompt.
3. Send request to Gemini model.
4. Store generated content.
5. Compute evaluation metrics.
6. Log everything into a CSV file.
7. Compare models based on accuracy & speed.

#Dataset Structure
| Input_Text                         | Target_Audience | Output_Text (Ground Truth) |
|-----------------------------------|-----------------|----------------------------|
| "Explain gravity"                 | kids            | ...                        |
| "Describe Kubernetes"             | developers      | ...                        |
| "What is inflation?"              | professionals   | ...                        |
#Prompting Strategy
### 🎯 Goal
Generate the *same meaning* but adjust:
- tone,
- vocabulary,
- depth,
- complexity,
- emotional friendliness,
- examples.

### 👇 Prompt Template
“You are an expert AI assistant. Rewrite the text for the following audience: {TARGET_AUDIENCE}. Maintain meaning but adjust tone, vocabulary, and explanation depth.”
#Installation
pip install google-genai pandas numpy tqdm nltk scikit-learn rouge-score python-dotenv
#API Setup
Create a `.env` file:

GOOGLE_API_KEY=your_key_here
from dotenv import load_dotenv
load_dotenv()
genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))
#Contributing
📂 Multi-Audience-AI
│
├── 📄 README.md
├── 📄 .env
├── 📄 requirements.txt
├── 📁 notebooks/
│     └── multi_audience_ai.ipynb
├── 📁 data/
│     └── dataset.csv
├── 📁 outputs/
│     └── full_log_multi_audience.csv
│     └── Multi_Audience_Final_Dataset.csv
└── 📁 src/
      ├── prompts.py
      ├── evaluation.py
      ├── model_runner.py
      ├── logger.py




