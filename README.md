DEEPSEEK-R1 via OLLAMA :: README

Customer-Support AI Simulator (DeepSeek + Ollama)
This project demonstrates how to deploy a local Large Language Model (LLM) using Ollama on Google Colab to simulate an interactive customer support conversation. It uses the DeepSeek-R1 model to generate empathetic, context-aware responses in a support-ticket scenario

Features:: 

•	Local LLM Execution: Runs DeepSeek-R1 (1.5b) using Ollama's backend.
•	Interactive CLI: A real-time chat interface within a Python environment.
•	Role-Specific Prompting: Uses System Prompts to define the Agent's personality and the Customer's issue.
•	Streaming Responses: Real-time text generation for a natural chat experience.

Tech Stack:: 
•	Model: DeepSeek-R1
•	Runtime: Google Colab (T4 GPU recommended)
•	Engine: Ollama
•	Language: Python 3.x

Setup & Usage:: 
1.	Open the Notebook: Import the provided .ipynb file into Google Colab.
2.	Enable GPU: Go to Runtime > Change runtime type > T4 GPU.
3.	Install Dependencies:
   
Ensure decompression tools are present-- 

!apt-get update && apt-get install -y zstd

Then run the official installer-- 

!curl -fsSL https://ollama.com/install.sh | sh

5.	Run the Server: Execute the cell containing the background thread to start ollama serve.
6.	Start Chatting: Run the interactive loop cell. Type your messages as the customer, and the AI agent will respond.

Example Conversation
Customer: Hi, I was charged twice for my January premium subscription. Can you help?
Agent: Hello! I'm so sorry to hear about the double charge. I completely understand how frustrating that is. Let me look into your account right away..

Project Structure:: 
•	DeepSeek-R1_via_Ollama_Support_Chat.ipynb: The main notebook containing the environment setup and chat logic. 
•	README.md: Project documentation. 
•	requirements.txt: List of necessary Python libraries.

**Post-Conversation Analytics:**
The system doesn't just simulate a chat; it performs a Post-Interaction Analysis. Once the session ends, the model switches from "Support Agent" mode to "Data Analyst" mode to process the transcript.

Extracted Data Points:
Contextual Summary: A high-level overview of the customer's journey.

Sentiment Analysis: Detection of emotional shifts (e.g., Frustrated → Satisfied).

Resolution Tracking: A boolean check to see if the ticket can be closed.

Actionable Insights: Specific feedback for the product or billing team based on the customer's complaint.

