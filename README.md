# EECS 183 Homework 4: Speech Processing

This assignment consists of three parts: probing experiments, Automatic Speech Recognition (ASR), and Text-to-Speech (TTS).

## Overview

- **Part A**: Probing experiments with Hubert model (35 points)
- **Part B**: ASR by fine-tuning Hubert (25 points)
- **Part C**: TTS with Language Models (40 points)

---

## Part A: Probing Experiments (35 points)

Understand what information is captured at different layers of the Hubert SSL model.

- **Task 1** (10 pts): Phoneme recognition - train classifier to predict phone labels
- **Task 2** (10 pts): MFCC regression - train regressor to predict acoustic features
- **Task 3** (10 pts): Speaker embedding analysis - visualize speaker separation with t-SNE
- **Task 4** (5 pts): Personal speaker embedding - record your voice and create embeddings

**Deliverables**: Plots and answers to questions in PDF report.

---

## Part B: Automatic Speech Recognition (25 points)

Fine-tune Hubert model for ASR using CTC loss.

**Tasks**:
- Implement ASR model with Hubert upstream + LSTM layers
- Train on LibriSpeech subset
- Generate test transcriptions

**Grading** (based on WER):
- < 70%: 10 points
- < 50%: 15 points
- < 40%: 20 points
- < 30%: 25 points

**Submission**: Notebook, `best_model.pt`, `asr_submission.txt`

**Note**: Requires GPU, training takes several hours. Save checkpoints regularly.

---

## Part C: Text-to-Speech with Language Models (40 points)

Implement and train a transformer-based language model for TTS following CosyVoice2 architecture.

**Tasks**:
- Implement dataset loader and collate function
- Implement `TextToSpeechLM` transformer model
- Implement training and validation loops
- Implement autoregressive generation
- Voice cloning and evaluation

**System**: Text → Text Tokens → [Your LM] → Speech Tokens → Mel → Audio

**Grading** (based on WER):
- < 70%: 15 points
- < 50%: 20 points
- < 45%: 25 points
- < 40%: 30 points
- < 35%: 35 points
- < 30%: 40 points (full points)

**Hardware**: GPU required (16GB+ VRAM). Training takes 8-12 hours.

**Submission**: 
- `submission_[YOUR_ID].txt` (auto-generated)
- `hw4-c.pdf` with all code and outputs

---

## Submission

- **Part A**: Notebook + PDF report (only PDF graded)
- **Part B**: Notebook + `best_model.pt` + `asr_submission.txt`
- **Part C**: `submission_[YOUR_ID].txt` + `hw4-c.pdf`

---

## Contact

For questions or issues, feel free to contact GSIs.
