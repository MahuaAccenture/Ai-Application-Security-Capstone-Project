# Lab Setup Guide – AI Application Security Capstone

## 1. Environment
- OS: Kali Linux 2026.3
- Virtualization: VirtualBox
- AI Runtime: Ollama
- Model: Llama 3
- Framework: Flask
- Language: Python

## 2. Install Ollama
curl -fsSL https://ollama.com/install.sh | sh


Verify installation:
ollama --version


Download Llama 3:
ollama pull llama3


Verify the model:
ollama list


## 3. Create Python Virtual Environment
python3 -m venv ai-lab
source ai-lab/bin/activate


## 4. Install Dependencies
pip install flask requests


Verify installation:
pip show flask requests


## 5. Start Ollama Service
sudo systemctl start ollama


Verify service status:
sudo systemctl status ollama


## 6. Run the Flask Application

Navigate to the project directory:
cd ~/ai-application-security-capstone


Activate the virtual environment:
source ai-lab/bin/activate


Start the chatbot:
python app.py


## 7. Access the Application

Open Firefox and visit:
http://localhost:5000


Send a test message and verify that the chatbot returns an AI-generated response.

## 8. Verify Model Execution
ollama ps


This command displays the models currently loaded in Ollama.

## 9. Expected Result

The Flask-based AI chatbot runs locally and communicates with the Llama 3 model through Ollama, providing an environment for OWASP LLM Top 10 (2025) security testing.
