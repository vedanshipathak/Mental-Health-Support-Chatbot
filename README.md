# Mental Health Chatbot with Mistral Model and RAG Implementation

## Overview
This repository contains a **mental health chatbot** powered by the **Mistral-7B-Instruct-v0.1** model from Hugging Face. The chatbot is designed to provide **therapeutic support** and **actionable advice** for users based on **Retrieval-Augmented Generation (RAG)**. The chatbot aims to offer a compassionate and understanding experience, tailored to the user's emotional state (e.g., anxiety, depression, relationship issues).

The model uses **RAG**, a method that enhances model generation by retrieving relevant context from a dataset before generating responses, ensuring that responses are both **personalized** and **contextually aware**.

## Key Features
- **Emotion-Aware Responses**: The chatbot adjusts its responses based on the user’s emotional state (e.g., anxious, depressed, etc.).
- **Contextual Responses**: Using **Retrieval-Augmented Generation (RAG)**, the chatbot retrieves relevant information from the dataset before generating responses.
- **Mistral-7B-Instruct Model**: Utilizes the **Mistral-7B-Instruct-v0.1** model, a large language model fine-tuned for instruction-following tasks, to generate empathetic responses.
- **Therapeutic Support**: The chatbot offers advice and coping techniques for users dealing with anxiety, depression, and other mental health concerns.
- **Custom Dataset**: The system is trained and fine-tuned using the **CounselChat dataset**, ensuring the chatbot's responses are specific and helpful.

## How It Works
1. **Retrieval-Augmented Generation (RAG)**: 
   - The RAG approach involves retrieving relevant information from the **CounselChat dataset** based on user input.
   - A prompt is generated and passed to the **Mistral-7B-Instruct model** to produce the final response.

2. **Emotion Detection**:
   - The chatbot uses keywords from the user’s input (e.g., "anxious," "sad," "overwhelmed") to identify their emotional state.
   - Based on this, the appropriate therapeutic response template (e.g., anxiety support or depression advice) is chosen.

3. **Mistral Model**:
   - The chatbot uses the **Mistral-7B-Instruct-v0.1 model** hosted on **Hugging Face** for generating the therapeutic responses.
   - The Hugging Face API is used for running the inference and generating responses based on the context provided.

## Dataset
The chatbot is trained using the **CounselChat dataset**. This dataset contains real-world conversations and advice from mental health professionals, specifically focused on mental well-being and therapy.

- **Dataset**: `counselchat-data.csv`
- **Content**: Contains columns like `questionTitle`, `questionText`, `answerText`, which provide real-life conversation examples for training the chatbot.

## Installation

To run the model, you don’t need to install anything locally. Instead, you can use the provided **Google Colab notebook** to run the entire process in the cloud.

### 1. Open the Colab Notebook
- Open the **[COLAB Notebook](https://colab.research.google.com/github/vedanshipathak/Mental-Health-Support-Chatbot/blob/main/Final_Model_mental_health_support.ipynb)**.
- This notebook contains all the necessary code to run the chatbot backend with **Mistral-7B** and **RAG**.

### 2. Set Up the Dataset
Upload the **CounselChat dataset** directly to the Colab environment when prompted.

### 3. Run the Cells
Simply run the cells in the Colab notebook one by one. The notebook will:
- Install all required dependencies
- Load the **Mistral model** from Hugging Face
- Start the **Flask server** and expose it using **ngrok**

### 4. Access the Chatbot
Once the Colab notebook finishes running, **ngrok** will provide a public URL (e.g., `https://abc123.ngrok-free.app`). You can use this URL to interact with the chatbot:
- **Postman**: Send a **POST** request to `/chat` with the message you want to send.
- **Frontend**: You can integrate this backend with a frontend interface.

Example request:
```json
{
  "message": "I feel anxious and overwhelmed."
}

