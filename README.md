Project Overview

NeuroTouch is a cognitive state prediction system that estimates a user's mood and fatigue levels based on a combination of behavioral and biosignal inputs. It takes in brainwave features from EEG (such as alpha, beta, theta wave power), heart rate and heart rate variability (HRV) readings, and smartphone interaction metrics (like tap speed, swipe velocity, typing patterns, screen time, etc.). A trained deep learning model (built with PyTorch) fuses these multimodal signals to predict how you’re feeling. The system also applies some heuristic rules to fine-tune the model’s predictions, ensuring they align with real-life context (for example, adjusting for time of day or inconsistent readings). The goal is to provide an accurate, real-time insight into your emotional mood and mental fatigue through everyday devices.

Features

Multimodal Input Support: Integrates data from multiple sources – EEG brainwave features, HRV and heart rate, and smartphone usage metrics – for a comprehensive view of the user’s state.
Mood & Fatigue Prediction: Uses a deep neural network to predict the user’s current mood (e.g. happiness/calmness level) and fatigue (mental tiredness or alertness). Results are presented on a convenient scale (for example, mood and fatigue scores from 1 to 10, or categorized as low/medium/high).
Daily GPT-Based Summary: Generates a natural language summary of your daily state using OpenAI’s GPT API. This feature produces a short “journal entry” style report each day, summarizing your overall mood and energy levels, and offering gentle feedback or insights (e.g. noting trends like improvement or suggesting if you had mixed signals).
Trend Visualization: Displays interactive charts of mood and fatigue over time. The dashboard plots your historical data (hourly, daily, weekly) so you can easily visualize trends, patterns, and progress. For example, you might see a line chart of your mood score across the week to identify highs and lows.
Sleek Gradio UI Dashboard: Provides an intuitive web-based interface (built with Gradio) to input data and view results. The dashboard is user-friendly, featuring clean visuals for the predictions and charts. You can enter sensor readings or connect devices, then watch as NeuroTouch updates your mood/fatigue indicators and summary in real time.

Tech Stack

PyTorch: Used to build and train the deep learning model that underpins the mood and fatigue predictions.
Gradio: Powers the interactive dashboard, allowing users to enter inputs and see outputs through a web app with no coding required.
OpenAI GPT-3.5/4 API: Utilized for generating the daily natural-language summaries of the user’s cognitive state (mood and fatigue). This adds an easy-to-understand narrative explanation of the raw predictions.
Pandas & NumPy: Employed for data wrangling, feature extraction, and preprocessing of the input signals (e.g., computing average band power from EEG, deriving HRV metrics, aggregating phone usage stats).
Matplotlib & Seaborn: Used for plotting the mood and fatigue trend charts on the dashboard, providing visual insights into how the user’s state changes over time.
Scikit-learn: Used for data preprocessing tasks such as normalization/scaling of features and possibly classical machine learning utilities. It may also be used for any baseline models or to apply heuristic rules (e.g., outlier detection).
