# 🎤🖼️ Speech-to-Image Live Conversion using Deep Learning  
*Infosys Internship – Oct 2024*

This project implements a live **Speech-to-Image** conversion system using cutting-edge AI models. It combines a fine-tuned **Whisper ASR** model for transcription, **sentiment-aware NLP** for filtering, and **Stable Diffusion** for generating context-driven images. Built with **Streamlit**, the app ensures real-time interaction and a smooth user experience.

---

## 🎯 Objective

To build a deep learning application that can **convert spoken descriptions into images in real-time** by integrating automatic speech recognition, sentiment analysis, and text-to-image generation.

---

## 🚀 Features

- 🎙️ **Audio Recording** via microphone input.
- 📝 **Speech Transcription** using Whisper ASR.
- 😊 **Sentiment Analysis** for content filtering.
- 🖼️ **Image Generation** with Stable Diffusion.
- 🧠 **Intelligent Decision-Making** — images are only generated for positive or neutral sentiments.

---

## 📲 Application Interface

Below are screenshots of the application interface to illustrate how it works:

### 🎛️ Main Interface
![Main UI](images/ui_main.png)

### 🗣️ Transcription and Sentiment
![Transcription and Sentiment](images/ui_sentiment.png)

### 🖼️ Generated Image Output
![Generated Image](images/ui_output.png)

> Replace the `images/xyz.png` paths with the actual paths to your interface screenshots.

---

## 🔄 Workflow

### System Flow Steps:

1. **Audio Input**
   - Set recording duration
   - Record using the `sounddevice` library
   - Save audio as `.wav`

2. **Speech Transcription**
   - Use Whisper to convert audio to text

3. **Sentiment Analysis**
   - Classify transcription as **Positive**, **Neutral**, or **Negative**

4. **Image Generation**
   - If sentiment is **Positive/Neutral**, generate an image using Stable Diffusion
   - If **Negative**, skip image generation

5. **Result Display**
   - Show transcription, sentiment, and image (if applicable)

---

### 📊 Flowchart

```mermaid
graph TD
    A[Start: Open App] --> B[Set Recording Duration]
    B --> C[Record Audio 🎙️]
    C --> D[Save as WAV File]
    D --> E[Transcribe via Whisper]
    E --> F[Run Sentiment Analysis]
    F -->|Positive/Neutral| G[Generate Image with Stable Diffusion]
    F -->|Negative| H[Skip Image Generation]
    G --> I[Show Transcription + Sentiment + Image]
    H --> J[Show Transcription + Sentiment Only]
    I --> K[End]
    J --> K[End]
