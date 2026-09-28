# Final Project: Emotion Detector

An AI-based Natural Language Processing (NLP) web application that detects emotions in user-provided text using Watson NLP services and Flask.

## Project Overview
This is the **Final Project** for developing an AI-based web application with Python and Flask. The application analyzes user input text and detects five emotional categories:
- **Anger**
- **Disgust**
- **Fear**
- **Joy**
- **Sadness**

It also computes the **Dominant Emotion** (the emotion with the highest confidence score).

## Architecture & Project Structure
```text
oaqjp-final-project-emb-ai/
├── EmotionDetection/
│   ├── __init__.py                # Package initialization exposing emotion_detector
│   └── emotion_detection.py       # Core emotion detector logic using Watson NLP
├── screenshots/
│   ├── 6b_deployment_test.png     # Screenshot of application deployment & output
│   └── 7c_error_handling_interface.png # Screenshot of error handling on invalid/blank input
├── static/
│   └── mywebscript.js             # Client-side JavaScript handling async API calls
├── templates/
│   └── index.html                 # Bootstrap web user interface
├── test_emotion_detection.py      # Unit tests for emotion detection statements
├── server.py                      # Flask web application server (Pylint 10/10)
├── README.md                      # Project documentation
└── submission_guide.md            # Coursera submission deliverables guide
```

## Features
- **Watson NLP Integration**: Connects to the Watson NLP `EmotionPredict` service.
- **Structured Output**: Formats response with all individual emotion scores and dominant emotion.
- **Python Package Architecture**: Fully modularized as the `EmotionDetection` package.
- **Error Handling**: Gracefully handles status code 400 and empty text inputs with `"Invalid text! Please try again!"`.
- **Unit Testing**: Verified via Python's `unittest` module across five core emotion statements.
- **Static Code Analysis**: Clean, PEP 8-compliant code achieving a perfect **10.00/10** score on `pylint`.

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/alihashmi2288/oaqjp-final-project-emb-ai.git
   cd oaqjp-final-project-emb-ai
   ```
2. Install dependencies:
   ```bash
   pip install flask requests pylint
   ```

## Running Unit Tests
Execute the unit tests:
```bash
python -m unittest test_emotion_detection.py
```

## Running the Web Application
Start the Flask development server:
```bash
python server.py
```
Open your browser and visit: `http://localhost:5000`

## Static Code Analysis
Run Pylint to check code quality:
```bash
pylint server.py
```
Score: **10.00/10**