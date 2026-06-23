# AI Video Moderation System

## Overview

AI Video Moderation System is an intelligent content filtering application designed to automatically detect and moderate inappropriate video content.

The system combines Computer Vision and Speech Processing techniques to analyze both visual and audio components of a video. It can blur potentially inappropriate visual content, detect offensive language from speech, and generate a moderation report through an interactive Gradio interface.

---

## Features

### Visual Content Moderation

* Person detection using YOLOv8.
* Skin region detection using computer vision techniques.
* Automatic blurring of potentially explicit visual content.

### Audio Content Analysis

* Speech-to-text transcription using Faster-Whisper.
* Offensive language detection using profanity filtering.
* Audio moderation reporting.

### Interactive Web Interface

* Upload videos directly from the browser.
* Select moderation mode:

  * NSFW Filtering
  * Profanity Detection
  * Both
* Preview processed videos.
* Download moderated output.
* View moderation reports.

---

## System Architecture

1. User uploads a video.
2. Video frames are analyzed using YOLOv8.
3. Skin detection is applied within detected person regions.
4. Potentially inappropriate regions are blurred.
5. Audio is extracted from the video.
6. Faster-Whisper transcribes speech content.
7. Profanity filtering identifies offensive language.
8. A moderation report is generated.
9. Processed video is returned to the user.

---

## Technologies Used

* Python
* YOLOv8
* OpenCV
* Faster-Whisper
* Gradio
* MoviePy
* NumPy
* Better-Profanity
* PyTorch

---

## Project Structure

```text
AI-Video-Moderation-System/
│
├── notebook.ipynb
├── sample_videos/
├── output/
├── README.md
└── requirements.txt
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/AI-Video-Moderation-System.git
cd AI-Video-Moderation-System
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Open the notebook and execute all cells.

Or launch the Gradio interface:

```python
app.launch()
```

The application will generate a public/local URL where users can upload videos and receive moderated outputs.

---

## Example Workflow

1. Upload a video.
2. Choose:

   * NSFW
   * Profanity
   * Both
3. Click Process.
4. Wait for analysis.
5. Download the processed video.
6. Review the moderation report.

---

## Future Improvements

* Real NSFW classification models.
* Multi-language profanity detection.
* Timestamp-based moderation reports.
* Face anonymization.
* Real-time video moderation.
* Cloud deployment.
* User authentication and moderation dashboard.

---

## Educational Purpose

This project was developed as an educational AI application demonstrating the integration of:

* Computer Vision
* Natural Language Processing
* Speech Recognition
* Content Moderation Systems
* Interactive AI Interfaces

---

## Author

Fatma Abdullah

