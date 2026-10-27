# oaqjp-final-project-emb-ai

**Project name:** Emotion Detector (final project - AI-based web application)
**Author:** Rutuja Ughade (GitHub: rutujaughade7-ux)

Emotion Detector is a Flask web application that uses the Watson NLP library's
`EmotionPredict` service to detect emotions in text. For any statement it reports the scores
for anger, disgust, fear, joy and sadness and names the dominant emotion.

## Project structure

| File | Purpose |
|---|---|
| `EmotionDetection/emotion_detection.py` | `emotion_detector()` calls Watson NLP and formats the result |
| `EmotionDetection/__init__.py` | Makes `EmotionDetection` a package |
| `server.py` | Flask deployment with the `/emotionDetector` route and blank-input handling |
| `test_emotion_detection.py` | Unit tests for the five emotions |
| `templates/index.html`, `static/mywebscript.js` | Web interface |

## Run

```bash
pip install flask requests pylint
python server.py                     # open http://localhost:5000
python -m unittest test_emotion_detection.py
pylint server.py
```

The Watson service URL can be overridden with the `WATSON_EMOTION_URL` environment variable.
