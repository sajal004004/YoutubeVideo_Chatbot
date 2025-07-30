# YoutubeVideo_Chatbot

YouTube Video RAG Q&A:-
This project implements a Retrieval-Augmented Generation (RAG) pipeline to answer questions about a YouTube video. It uses OpenAI's Whisper for transcription, yt-dlp for downloading audio, and a vector store for efficient retrieval of relevant information.

Features:-
-YouTube Video Processing: Downloads the audio from a YouTube video.
-Transcription: Transcribes the audio using OpenAI's Whisper API. For large audio files, it splits the audio into manageable chunks.
-Caching: Caches transcriptions to avoid re-processing the same video.
-Vector Store: Creates an in-memory vector store of the video's transcript for efficient similarity search.
-Q&A: Answers user queries about the video content by retrieving relevant text chunks and using a large language model to generate an answer.

How it Works:-
-Installation: Installs necessary Python libraries.
-Setup:
  Sets up the OpenAI API key.
  Downloads the audio of a given YouTube video.
  Transcribes the audio to text.
  Splits the transcript into smaller chunks.
  Creates a vector store from the text chunks.
-Querying:
  Takes a user's query.
  Searches the vector store for relevant text chunks.
  Uses the retrieved chunks as context for a large language model to generate an answer.
  Provides the answer along with the timestamps of the source video segments.

How to Use:-
-Set up your OpenAI API Key:
-Get your API key from OpenAI.
-In your Colab notebook, go to the "Secrets" tab (🔑 icon) and add a new secret named OPENAI_API_KEY with your API key as the value.
-Install Dependencies:
  Run the first code cell to install the required libraries.
  Run the Pipeline:
  Set the YOUTUBE_URL variable to the URL of the YouTube video you want to query.
  Run the cell that calls setup_rag_pipeline. This will download, transcribe, and create the vector store.
  Ask Questions:
  Use the answer_query function to ask questions about the video.

