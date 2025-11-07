# Restaurants-WHATSAPP-BOT
📱 Restaurant WhatsApp Chatbot (RAG + n8n + OpenAI + Supabase)
🔹 Overview

This project demonstrates a WhatsApp-integrated AI chatbot built using n8n, OpenAI, and Supabase Vector Store, designed for a restaurant recommendation and customer support system.

Customers can message the restaurant’s WhatsApp number to:

Ask about available meals and timings (breakfast, lunch, dinner)

Get prices, delivery options, and FAQs

Find restaurant locations or book events and parties

The chatbot uses Retrieval-Augmented Generation (RAG) to fetch relevant information from a structured database and provide concise, polite answers in real time.

⚙️ Tech Stack
Component	Description
n8n	Workflow automation platform used to orchestrate WhatsApp trigger, AI responses, and Supabase vector queries.
OpenAI GPT Model	Generates concise and polite replies to customer queries.
Supabase Vector Store	Stores embedded restaurant data (menu, timing, FAQs, events) for semantic search.
Google Drive	Source for uploading meal data files (CSV or PDF).
WhatsApp Cloud API	Used for receiving and sending customer messages.
PostgreSQL Chat Memory	Maintains conversational context with customers.
🧠 Workflow Overview


Video description of workflow:


https://youtu.be/YiP8R5js9RY

The automation consists of two main pipelines:

1️⃣ WhatsApp Chatbot Workflow

Trigger: Incoming WhatsApp message

Action: Message is passed to AI Agent

Agent retrieves related info from Supabase Vector Store using OpenAI embeddings

Response: AI summarizes and sends polite message back via WhatsApp API

2️⃣ RAG (Retrieval-Augmented Generation) Pipeline

Triggered manually for updating data

Loads a new dataset (e.g., CSV or PDF) from Google Drive

Generates vector embeddings using OpenAI

Stores embedded data in Supabase Vector Store for retrieval

💬 Example Queries

Users can ask questions like:

“Which meals are available in the morning?”

“What is today’s lunch special?”

“Where is your restaurant located?”

“Do you offer catering for events or parties?”

“Can I see the dinner menu with prices?”

🧩 System Prompt Used

“You are a polite and concise restaurant assistant.
When a message is received via WhatsApp, retrieve the most relevant data from the Supabase Vector Store and summarize it clearly and helpfully.
Always respond naturally and avoid listing unnecessary items.”

🚀 How to Use

Clone this repository

git clone https://github.com/Tanzeela00Sharif/restaurant-whatsapp-bot.git


Import the .json n8n workflow into your n8n instance.

Connect the following credentials:

WhatsApp Cloud API

Supabase

OpenAI API key

Upload your restaurant data (CSV/PDF) to Google Drive or Supabase.

Run the RAG pipeline to index the data.

Start the WhatsApp Chatbot Workflow and message your WhatsApp number to chat with the bot.



<img width="1220" height="555" alt="Screenshot 2025-10-18 233027" src="https://github.com/user-attachments/assets/cf25ad95-5e7b-4070-ad91-9ae683144412" />




📍 Future Improvements

Add multi-language support (e.g., Urdu + English)

Integrate payment or table reservation systems

Enable voice message understanding using Whisper API

👩‍💻 Author

Tanzeela Sharif
Data Science & AI Automation Enthusiast
📧 Email: tanzeelasharif1@gmail.com

🌐 GitHub: https://github.com/Tanzeela00Sharif
