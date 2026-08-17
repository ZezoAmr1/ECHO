# 🧠 ECHO — Early Cognitive Health Observatory

An AI-powered speech analysis tool for early detection of cognitive decline. ECHO analyzes speech recordings using acoustic and linguistic features to screen for Alzheimer's Disease (AD) and Mild Cognitive Impairment (MCI).

## 🔬 How It Works

ECHO processes a short speech sample (20–60 seconds) through a multi-stage pipeline:

1. **Speech-to-Text** — Transcription via OpenAI Whisper
2. **Acoustic Analysis** — 88 features extracted using OpenSMILE (eGeMAPS v02)
3. **Linguistic Analysis** — Vocabulary diversity, speech rate, sentence complexity, content density, and more via spaCy/jieba
4. **ML Classification** — Trained binary classifiers predict cognitive status

## 📊 Models

| Model | Task | Accuracy | Language | Features |
|-------|------|----------|----------|----------|
| AD-CN | Alzheimer's vs Healthy | **85.9%** | English | Acoustic + Linguistic |
| MCI-CN | MCI vs Healthy | **76.6%** | English | Acoustic + Linguistic |
| MCI-CN | MCI vs Healthy | **60.0%** | Chinese | Linguistic only |

## 🚀 Try It

The app is deployed on Streamlit Community Cloud:

👉 **[Launch ECHO](https://your-app.streamlit.app)** *(link updated after deployment)*

## 🏃 Run Locally

```bash
# Clone the repository
git clone https://github.com/ZezoAmr1/ECHO.git
cd ECHO

# Install dependencies
pip install -r requirements.txt

# Install system dependency
# On Ubuntu/Debian: sudo apt install ffmpeg
# On macOS: brew install ffmpeg
# On Windows: choco install ffmpeg

# Run the app
streamlit run echo-app-final.py
```

## 🛠 Tech Stack

- **Frontend**: Streamlit
- **Speech Recognition**: OpenAI Whisper
- **Acoustic Features**: OpenSMILE (eGeMAPS v02)
- **NLP (English)**: spaCy, LexicalRichness
- **NLP (Chinese)**: jieba, spaCy
- **ML**: scikit-learn (trained offline)

## ⚠️ Disclaimer

ECHO is a **research tool** developed for educational and scientific purposes. It is **not** a medical diagnostic device. Results should not be used as a substitute for professional medical evaluation. Always consult qualified healthcare professionals for cognitive health assessment.

## 📄 License

This project is for research and educational purposes.
