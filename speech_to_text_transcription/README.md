# Speech-to-Text Transcription Pipeline

## Problem Statement
Build a pipeline to transcribe audio files into text and benchmark custom model performance against AWS Transcribe.

## Approach
- Used HuggingFace Wav2Vec2 model for custom transcription.
- Deployed inference on AWS EC2.
- Stored audio and transcripts on AWS S3.
- Queried transcripts via AWS Athena for downstream analysis.
- Audio preprocessing with Librosa; decoding with Wav2Vec2ForCTC.

## Technologies Used
- Python (PyTorch, HuggingFace Transformers)
- AWS (EC2, S3, Athena)
- Librosa for audio preprocessing

## Key Learnings
- Handling unstructured audio data
- Cloud-based model deployment and data pipelines
- Benchmarking custom vs. managed services

## Next Steps
- Fine-tune on domain-specific audio (e.g., customer support calls).
- Build a simple front-end for real-time transcription.
