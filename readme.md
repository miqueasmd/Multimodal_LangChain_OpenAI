# LangChain OpenAI Multimodal Application Project

## Overview
This project implements a Multimodal AI application using LangChain and OpenAI's APIs. It processes YouTube videos by downloading the audio, transcribing it using OpenAI's Whisper model, and creating a knowledge base for answering questions about the content.

## Features
- Downloads audio from YouTube videos using yt-dlp
- Transcribes audio to text using OpenAI's Whisper API
- Creates vector embeddings of the transcribed content
- Implements a retrieval-based QA system using LangChain's RetrievalQA
- Provides an interactive chat interface

## Technologies Used
- Python 3.12
- LangChain (including langchain-openai, langchain-community)
- OpenAI API (GPT models and Whisper)
- yt-dlp for YouTube downloads
- FFmpeg for audio processing
- DocArray for vector storage
- dotenv for environment management

## Setup

### Prerequisites
- Python 3.x
- FFmpeg installed on your system
- OpenAI API key

### Installation
1. Clone this repository
2. Install the required packages:
   ```bash
   pip install langchain langchain-openai yt_dlp tiktoken docarray python-dotenv
   ```
3. Install FFmpeg (if not already installed)
4. Create a `.env` file in the project root with your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

### Usage
1. Run the notebook cells in sequence
2. Input a YouTube URL to download and process
3. Ask questions about the video content through the application interface

## Project Structure
- `notebook-solution.ipynb`: Main Jupyter notebook with the implementation
- `downloads/`: Directory for storing downloaded audio files
- `files/transcripts/`: Directory for storing transcribed text
- `.env`: Configuration file for API keys (not included in repo)
- `.gitignore`: Specifies files to be ignored by Git

## How It Works
1. Downloads the audio track from a YouTube video
2. Transcribes the audio using OpenAI's Whisper model
3. Splits the transcription into manageable chunks
4. Creates vector embeddings of these chunks
5. Uses these embeddings to retrieve relevant information when answering questions
6. Generates responses using OpenAI's language models

## Acknowledgments
This project is based on a tutorial from [DataCamp](https://www.datacamp.com/datalab/w/1e5655d4-40a9-4244-85a8-c7f96fb52f6f/edit).

## Disclaimer
This project is for educational purposes only. Be aware of YouTube's terms of service when downloading content.
