# CineBot — Conversational Movie & Mood-Music Recommender

> A desktop chatbot that recommends movies from a 10,000-title TMDB dataset through natural conversation, plus a mood-aware music engine that reads the user's emotion and suggests matching songs.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Tkinter](https://img.shields.io/badge/GUI-Tkinter-2C3E50)
![TheFuzz](https://img.shields.io/badge/NLP-TheFuzz-8E44AD)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

CineBot started as a rule-based recommender and evolved through three iterations:

| # | Notebook | Approach |
|---|---|---|
| 1 | `01_cinebot_rule_based.ipynb` | **Intent detection** with regex rules → search a title, top-rated lists, by year, by genre, similar movies, compare two movies |
| 2 | `02_cinebot_pro_fuzzy_matching.ipynb` | **Fuzzy title matching** (Levenshtein via TheFuzz), conversational context memory, restyled UI |
| 3 | `03_neural_music_mood_engine.ipynb` | **Emotion-aware music recommender**: classifies the user's message into a mood (Happy / Sad / Motivated / Relaxed) and recommends songs, with an animated mood-themed UI |

## Features

- 💬 Natural chat: *"recommend a sci-fi movie from 2014"*, *"movies like Inception"*, *"compare Titanic and Avatar"*
- 🔎 Typo-tolerant title search with fuzzy matching
- ⭐ Ranking by vote average weighted with vote count and popularity
- 🎭 Mood detection → song suggestions with tempo, energy, and danceability
- 🖥️ Dark, animated Tkinter interface with a typing indicator, quick-search chips, and a status bar
- 🧵 Background threads keep the UI responsive

## Datasets

| File | Rows | Description |
|---|---|---|
| `dataset.csv` | 10,000 | TMDB movies: title, genre, language, overview, popularity, release date, votes |
| `music_sentiment_dataset.csv` | 1,000 | User text → sentiment label → recommended song (artist, genre, BPM, mood, energy) |

## Getting started

```bash
git clone https://github.com/ZakariaHibaoui2/cinebot-movie-recommendation.git
cd cinebot-movie-recommendation
pip install -r requirements.txt
jupyter notebook
```

Open any notebook and **Run All**. A desktop window opens (the datasets load automatically from the repo folder).

## Project structure

```
├── 01_cinebot_rule_based.ipynb
├── 02_cinebot_pro_fuzzy_matching.ipynb
├── 03_neural_music_mood_engine.ipynb
├── dataset.csv                     # TMDB movies (10k)
├── music_sentiment_dataset.csv     # mood → music (1k)
├── bg_music.png, happy.png, sad.png, motivated.png, relaxed.png   # UI assets
└── requirements.txt
```

## Author

**Zakaria Hibaoui** — [GitHub](https://github.com/ZakariaHibaoui2) · [LinkedIn](https://www.linkedin.com/in/zakaria-hibaoui-08b235337/)
AI course project, INTI International University, Malaysia (2025).

## License

[MIT](LICENSE)
