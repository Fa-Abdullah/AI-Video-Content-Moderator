# AI Video Content Moderator – Intelligent Video Moderation System

An AI-powered video moderation system that automatically analyzes both visual and audio content to identify potentially inappropriate material and apply the appropriate level of censorship.

## Overview

This project combines Computer Vision and Audio Processing to create a smarter content moderation pipeline. Instead of blindly censoring entire videos, the system first analyzes spoken content and visual elements to determine the most suitable action.

If offensive language is detected in the audio, the entire video is blurred. Otherwise, the system performs visual analysis and selectively blurs only sensitive skin-exposed regions while preserving the rest of the scene.

This approach helps maintain content visibility while still protecting users from inappropriate material.

## How It Works

### Audio Analysis

The system begins by extracting audio from the video and converting speech into text using Faster-Whisper. The generated transcript is then analyzed for profanity and offensive language.

* Audio extraction and transcription
* Profanity detection
* Full-video blur when inappropriate language is detected

### Visual Analysis

If the audio passes moderation checks, the system proceeds to analyze the video frames.

* Detects people using YOLOv8
* Identifies exposed skin regions through HSV-based skin detection
* Applies blur only to detected sensitive areas
* Preserves faces, clothing, and background details whenever possible

## Key Features

* Automated video moderation pipeline
* Multi-modal analysis using audio and visual data
* Selective blurring instead of unnecessary full censorship
* Fast and scalable processing
* Privacy-friendly solution that can run locally using open-source tools
* Designed for integration into content moderation and safety workflows

## Technologies Used

* Python
* YOLOv8
* OpenCV
* Faster-Whisper
* Better-Profanity
* MoviePy
* FFmpeg
* Hugging Face Transformers

## Potential Applications

* Social media content moderation
* Educational platform safety systems
* Video sharing platforms
* Automated compliance and content review pipelines
* AI-powered media monitoring solutions
