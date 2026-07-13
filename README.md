# Repository for final project
# Emotion Detection Web Application

Final project for the IBM course Developing AI Applications with Python and Flask.

A web application that detects emotions in text using the Watson NLP library (Emotion Predict function). Given a text input, it returns scores for five emotions — anger, disgust, fear, joy, and sadness — and identifies the dominant emotion.

## Features

- Emotion detection powered by Watson NLP embedded AI libraries
- Formatted output with all five emotion scores and the dominant emotion
- Packaged as a reusable Python package (EmotionDetection)
- Unit tested with unittest (5 test cases, one per emotion)
- Web interface deployed with Flask
- Error handling for blank input (HTTP 400)
- Static code analysis: PyLint score 10/10

### As a package

```python
from EmotionDetection.emotion_detection import emotion_detector

result = emotion_detector("I am so happy I am doing this.")
print(result)
# {'anger': 0.004, 'disgust': 0.0003, 'fear': 0.003, 'joy': 0.994, 'sadness': 0.012, 'dominant_emotion': 'joy'}
```

### As a web application
bash
python3 server.py


Then open `localhost:5000` in your browser, enter a text, and click the analyze button.

Example response:

> For the given statement, the system response is 'anger': 0.006, 'disgust': 0.002, 'fear': 0.009, 'joy': 0.968 and 'sadness': 0.049. The dominant emotion is joy.

For blank input, the application responds with: *Invalid text! Please try again!*

## Running Tests

bash
pytho3 test_emotion_detection.py
