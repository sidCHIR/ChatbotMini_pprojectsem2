# ChatbotMini_pprojectsem2

🧠 Bedrock Chatbot with LangChain & Streamlit
This project is a multilingual chatbot interface powered by Amazon Bedrock (Anthropic Claude v2) and built using LangChain and Streamlit. It allows users to interact with the Claude v2 LLM using a clean sidebar UI and receive dynamic, natural language responses in multiple languages.

🚀 Features
🔁 Real-time Chat Interface with Streamlit

🧩 LangChain Integration for prompt chaining

☁️ Amazon Bedrock Support with Anthropic Claude v2

🌐 Multilingual Support (e.g., English, Spanish – easily extendable)

🎛️ Adjustable prompt templates for dynamic control

🔐 Secured via AWS SDK and local profile-based authentication


🛠️ Setup Instructions
1. Clone the Repository

git clone https://github.com/your-username/bedrock-langchain-chatbot.git
cd bedrock-langchain-chatbot
2. Set Up Python Environment

python -m venv venv
source venv/bin/activate    # For Windows: venv\Scripts\activate
pip install -r requirements.txt
3. Set AWS Profile
Ensure your AWS CLI is configured with a profile named SID:

aws configure --profile SID
You must have access to Bedrock Runtime and the Anthropic Claude v2 model.

📦 Requirements
Your requirements.txt should include:


boto3
streamlit
langchain>=0.1.0
🔧 Configuration
Modify AWS Profile
In the script (main.py):


os.environ["AWS_PROFILE"] = "SID"
Replace "SID" with your own AWS CLI profile name if needed.

▶️ Run the Chatbot
bash
Copy
Edit
streamlit run main.py
This launches the chatbot in your browser at http://localhost:8501.

🧠 How It Works
PromptTemplate: Takes user’s language and input question to build a structured prompt.

LLMChain: Wraps the Claude v2 model via LangChain and generates a response.

Streamlit Sidebar UI: Captures inputs and displays real-time model replies.

✍️ Example Prompt
For input:

Language: English

Question: Who is Buddha?

The model receives:

sql
Copy
Edit
You are a chatbot. You are in english.

Who is Buddha?
📌 Notes
Bedrock access is not open by default. Ensure your AWS account has explicit access to use anthropic.claude-v2.

max_tokens_to_sample and temperature are configurable in model_kwargs.

🛡️ Disclaimer
This project is a prototype. For production use, implement:

Rate limiting

Error handling for AWS access or response failures

Enhanced prompt sanitization

Logging and monitoring

