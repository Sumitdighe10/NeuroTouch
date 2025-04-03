# NeuroTouch

## Project Overview
NeuroTouch is a cognitive state prediction system that estimates a user's mood and fatigue levels based on a combination of behavioral and biosignal inputs. It takes in brainwave features from EEG (such as alpha, beta, theta wave power), heart rate and heart rate variability (HRV) readings, and smartphone interaction metrics (like tap speed, swipe velocity, typing patterns, screen time, etc.). A trained deep learning model (built with PyTorch) fuses these multimodal signals to predict how you’re feeling. The system also applies some heuristic rules to fine-tune the model’s predictions, ensuring they align with real-life context (for example, adjusting for time of day or inconsistent readings). The goal is to provide an accurate, real-time insight into your emotional mood and mental fatigue through everyday devices.

---

## Features

- **Multimodal Input Support:** Integrates data from multiple sources – EEG brainwave features, HRV and heart rate, and smartphone usage metrics – for a comprehensive view of the user’s state.
- **Mood & Fatigue Prediction:** Uses a deep neural network to predict the user’s current mood and fatigue. Results are presented on a scale (e.g. mood and fatigue scores from 1 to 10, or categorized as low/medium/high).
- **Daily GPT-Based Summary:** Generates a natural language summary of your daily state using OpenAI’s GPT API. This feature produces a short journal-style report each day.
- **Trend Visualization:** Displays interactive charts of mood and fatigue over time (daily/weekly).
- **Sleek Gradio UI Dashboard:** Offers an intuitive web interface to input sensor data and visualize results and trends in real time.

---

## Tech Stack

- **PyTorch:** Deep learning framework used to develop and train the mood/fatigue prediction model.
- **Gradio:** Web-based interface for interacting with the model.
- **OpenAI API (GPT-3.5/4):** Used for generating daily natural-language summaries.
- **Pandas & NumPy:** For data processing and feature engineering.
- **Matplotlib & Seaborn:** For trend visualization and graphing.
- **Scikit-learn:** For preprocessing and utilities like normalization and feature scaling.

---

## Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/yourusername/NeuroTouch.git
cd NeuroTouch
```

2. **Install Dependencies:**
```bash
pip install -r requirements.txt
# Or install manually:
pip install torch gradio openai pandas numpy matplotlib seaborn scikit-learn
```

3. **Configure OpenAI API:**
```bash
export OPENAI_API_KEY="sk-YourOpenAIKeyHere"
```

---

## Usage

1. **Launch the Dashboard:**
```bash
python app.py
```
Visit `http://127.0.0.1:7860/` in your browser.

2. **Provide Inputs:**
Enter EEG (alpha, beta, theta), HRV, and smartphone metrics manually or through integration.

3. **View Outputs:**
- **Mood Score:** Predicted score (e.g., 6.5/10).
- **Fatigue Level:** Category (e.g., 1 = Moderate Fatigue).
- **Summary:** Natural language daily report generated via GPT.
- **Charts:** Mood/Fatigue trends.

---

## Screenshots

![Dashboard](Screenshot%202025-04-03%20181538.png)

![GPT Summary](Screenshot%202025-03-31%20215212.png

---

## Sample Input & Output

**Input:**
```json
{
  "alpha_power": 0.38,
  "beta_power": 0.68,
  "theta_power": 0.27,
  "hrv": 70,
  "heart_rate": 74,
  "tap_speed": 0.5,
  "tap_pressure": 0.65,
  "swipe_velocity": 1.3,
  "screen_time_min": 180,
  "unlock_freq": 45
}
```

**Output:**
```json
{
  "predicted_mood": 10,
  "predicted_fatigue_level": 1
}
```

---

## Future Improvements

- Real-time wearable integration (EEG headbands, smartwatches).
- Facial emotion tracking (via webcam).
- Mobile app development for passive monitoring.
- Personalization and adaptive model tuning.
- Stress, focus, and anxiety detection.

---

## Acknowledgements

- **OpenAI API**: GPT-powered summaries
- **Gradio**: Interactive UI
- **PyTorch**: Deep learning framework
- **Pandas, NumPy, Matplotlib, Seaborn, Sklearn**: Data science tools

---

---

## 🚀 Like this project?
If you find NeuroTouch insightful or useful:
- Give a ⭐ on GitHub
- Share it with fellow developers, researchers, or friends
- Connect and discuss ideas!

