# NYSE News Center

A real-time stock market news dashboard built with Streamlit. Fetches latest financial news, analyzes sentiment, calculates hype scores, and displays live market data.

## Features

- **Live Market Ticker** - Real-time prices for Gold, USD, EUR, GBP, BIST 100, Bitcoin, and Silver
- **News Aggregation** - Fetches news from multiple sources (GoogleNews, RSS feeds)
- **Sentiment Analysis** - Automatic positive/negative/neutral classification using TextBlob
- **Hype Score** - Algorithm that prioritizes sensational and breaking news
- **Time Filtering** - Filter news by 1, 4, 6, 12, or 24 hours
- **Monthly Insight** - Shows the biggest market movement in the last 30 days with related headlines

## Screenshot

NYSE News Center <img width="1883" height="847" alt="image" src="https://github.com/user-attachments/assets/049d3979-60d7-43cf-b50c-057e1c03f792" />



## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/nyse-news-center.git
cd nyse-news-center

# Install dependencies
pip install -r requirements.txt

# Run the application
streamlit run main.py
```

## Requirements

- Python 3.8+
- streamlit
- GoogleNews
- textblob
- pandas
- yfinance
- feedparser

## Usage

1. Run `streamlit run main.py`
2. Open `http://localhost:8501` in your browser
3. Select time range from the sidebar
4. Click "Refresh" to update news

## Project Structure

```
nyse-news-center/
├── main.py           # Main application
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

## How It Works

### Hype Score Algorithm
The hype score is calculated based on:
- Presence of sensational keywords (surge, crash, record, etc.)
- Number of exclamation marks
- Uppercase words in the title

### Sentiment Analysis
Uses TextBlob library to analyze the polarity of news headlines:
- **Positive** (+): Polarity > 0.1
- **Negative** (-): Polarity < -0.1
- **Neutral** (~): Otherwise

### Market Data
Real-time data fetched via yfinance API with 60-second cache.

## License

MIT License

## Contributing

Pull requests are welcome. For major changes, please open an issue first.
