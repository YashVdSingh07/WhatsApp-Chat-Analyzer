# WhatsApp Chat Analyzer 📊

A Streamlit web app that analyzes your exported WhatsApp chat history and surfaces insights through interactive statistics, charts, and visualizations.

---

## Features

- **Top Statistics** — total messages, word count, media shared, and links shared
- **Monthly & Daily Timelines** — see messaging trends over time
- **Activity Maps** — identify the busiest days of the week and months of the year
- **Weekly Heatmap** — visualize activity patterns across days and time slots
- **Most Busy Users** — find the most active participants (group chats)
- **Word Cloud** — visualize the most frequently used words
- **Most Common Words** — horizontal bar chart of top words
- **Emoji Analysis** — breakdown of emoji usage with a pie chart

All analyses can be viewed for the **overall group** or filtered by an **individual user**.

---

## Project Structure

```
├── app.py               # Main Streamlit application
├── preprocessor.py      # Parses raw WhatsApp chat export into a DataFrame
├── helper.py            # Functions for stats, charts, and NLP analysis
├── requirements.txt     # Python dependencies
└── README.md
```

---

## Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

```bash
git clone https://github.com/your-username/whatsapp-chat-analyzer.git
cd whatsapp-chat-analyzer
pip install -r requirements.txt
```

### Run the App

```bash
streamlit run app.py
```

---

## Usage

1. Export a WhatsApp chat: **Chat > More > Export Chat > Without Media**
2. Open the app in your browser (usually `http://localhost:8501`)
3. Upload the exported `.txt` file via the sidebar
4. Select a user or choose **Overall** for group-wide analysis
5. Click **Show Analysis**

---

## Dependencies

| Package | Purpose |
|---|---|
| `streamlit` | Web UI framework |
| `matplotlib` | Charts and plots |
| `seaborn` | Heatmap visualization |
| `pandas` | Data manipulation |
| `wordcloud` | Word cloud generation |
| `emoji` | Emoji extraction and counting |

Install all at once:

```bash
pip install streamlit matplotlib seaborn pandas wordcloud emoji
```

---

## Notes

- The app expects the standard WhatsApp export format (12-hour or 24-hour timestamps)
- System messages like `group_notification` are automatically filtered out
- Stop words are excluded from word frequency and word cloud analysis
