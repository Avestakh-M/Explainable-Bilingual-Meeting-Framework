# An Explainable Framework for Streaming and Offline Bilingual Meeting Processing

This repository contains the official implementation of the paper: **"An Explainable Framework for Streaming and Offline Bilingual Meeting Processing with Quality and Scalability Evaluation"**.

## 🚀 Quick Start (Google Colab)
You can run the entire pipeline directly in Google Colab without any installation. Click the button below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Avestakh-M/Explainable-Bilingual-Meeting-Framework/blob/main/Avestakh_Framework.ipynb)

## 📌 Overview
The framework consists of 6 layers:
1. Preprocessing (VAD)
2. ASR (Whisper)
3. Speaker Diarization (Pyannote)
4. Summarization (mT5)
5. Explainability (Confidence Score)
6. Deployment (Ray Serve)

## ⚙️ Requirements & Setup
If you run the notebook locally or manually in Colab:
1. Open `Avestakh_Framework.ipynb`.
2. Run **Cell 0** to set up the virtual environment and install dependencies (`numpy<2`, `faster-whisper`, `pyannote.audio`, etc.).
3. ⚠️ **Important:** You need a **Hugging Face Token** for the Pyannote diarization pipeline. Replace `"YOUR_HF_TOKEN_HERE"` in Cell 4 with your own token.

## 📊 Datasets Used
- **LibriSpeech (test-clean)**: Used for ASR evaluation (WER).
- The pipeline automatically downloads a subset of LibriSpeech for testing.

## 📈 Results
The real experimental results obtained from this implementation are:
- **ASR (Whisper Small) WER:** 5.56% (LibriSpeech, 5 samples)
- **Diarization Latency:** ~0.15s (Pyannote 3.1)
- **Summarization Confidence:** 59.08% (Below the 75% threshold, correctly flagged for human review)

## 📝 Citation
If you use this code in your research, please cite our paper:
*(در اینجا رفرنس مقاله خودتان را بعد از چاپ قرار دهید)*
