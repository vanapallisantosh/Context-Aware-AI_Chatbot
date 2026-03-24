# Context-Aware Conversational AI Chatbot

## Project Overview

This project implements a Context-Aware Conversational Chatbot designed for customer support scenarios. The chatbot maintains conversation history across multiple user interactions and generates relevant responses based on detected intent and stored context.

Unlike basic chatbots that respond independently to each message, this chatbot remembers previous user inputs and uses them to provide coherent multi-turn dialogue responses.

---

## Objectives

The main objectives of this project are:

* Maintain conversation context across multiple turns
* Identify user intent using simple NLP techniques
* Provide meaningful responses based on previous interactions
* Handle unknown queries gracefully
* Simulate real-world customer support conversations

---

## Features

### Context Memory

Stores previous conversation topics and uses them to respond intelligently to follow-up questions.

### Intent Recognition

Detects user intent using keyword matching such as:

* order status
* refund request
* product inquiry
* greetings

### Multi-Turn Dialogue Handling

Supports follow-up conversations like:

User: Where is my order?
Bot: Please provide your order ID
User: 12345
Bot: Your order is currently being processed

### Graceful Unknown Query Handling

If chatbot cannot understand input:

Bot: I am not sure I understood that. Could you please rephrase?

---

## System Architecture

The chatbot follows a modular architecture:

User Input
↓
Intent Detection Module
↓
Context Manager
↓
Response Generator
↓
Output to User Interface

---

## Technology Stack

Backend:

* Python
* Flask

Frontend:

* HTML
* CSS
* JavaScript

NLP:

* Keyword-based intent detection
* Optional NLTK support

Session Handling:

* Flask session storage

---

## Project Structure

project/
│
├── app.py
├── templates/
│   └── index.html
├── static/
│   ├── css/
│   └── js/
├── chatbot_logic.py
└── README.md

---

## Installation Steps

### Step 1: Clone Repository

git clone <repository-link>

### Step 2: Navigate to Project Folder

cd chatbot-project

### Step 3: Install Dependencies

pip install flask

### Step 4: Run Application

python app.py

### Step 5: Open Browser

http://127.0.0.1:5000

---

## Example Conversations

Example 1:

User: Hello
Bot: Hi! How can I assist you today?

Example 2:

User: I want to check my order
Bot: Please provide your order ID

User: 56789
Bot: Your order is out for delivery

Example 3:

User: I want refund
Bot: Please provide your order ID to process refund request

---

## API Endpoint

POST /chat

Request Format:

{
"user_input": "Where is my order?"
}

Response Format:

{
"response": "Please provide your order ID"
}

---

## Context Handling Strategy

The chatbot stores conversation state using session variables such as:

context["topic"] = "order_status"

When user provides additional input, chatbot checks stored topic and generates relevant response accordingly.

---

## Future Improvements

This chatbot can be enhanced by:

* Integrating machine learning intent classification
* Using transformer-based NLP models
* Adding speech-to-text support
* Supporting multilingual conversations
* Connecting with real customer databases

---

## Use Cases

Customer support automation
Order tracking assistance
Refund processing guidance
Product inquiry handling
Helpdesk chatbot systems

---

## Conclusion

This project demonstrates how a context-aware chatbot improves conversational quality compared to traditional rule-based chatbots. It provides a scalable foundation for building intelligent conversational assistants in real-world applications.
