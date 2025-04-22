# Crypto Sentiment Analyzer

A real-time cryptocurrency sentiment analysis dashboard that aggregates and analyzes social media data to provide market insights.

## Features

- Real-time sentiment analysis of cryptocurrency mentions on social media
- Interactive dashboard with dynamic charts and visualizations
- AI-powered insights using Gemini and Claude
- Support for multiple cryptocurrencies
- Customizable time ranges and data filters
- Topic distribution analysis
- Message volume tracking
- Risk level assessment

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd crypto-sentiment-analyzer
```

2. Create a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root with your API keys:

```
GEMINI_API_KEY=your_gemini_api_key
CLAUDE_API_KEY=your_claude_api_key
```

## Running the Application

1. Start the Flask backend:

```bash
python app.py
```

The backend will run on http://localhost:5000

2. Serve the frontend:

```bash
python -m http.server 8000
```

Access the application at http://localhost:8000

## Project Structure

- `app.py`: Main Flask application with API endpoints
- `scrapper.py`: Data collection and processing logic
- `index.html`: Main frontend interface
- `data/`: Directory containing historical data files
  - `twitter_*.json`: Twitter data for different cryptocurrencies
  - `telegram_*.json`: Telegram data for different cryptocurrencies

## API Endpoints

- `/api/data`: Get dashboard data with optional coin filter
- `/api/coins`: Get list of supported cryptocurrencies
- `/api/analyze`: Get detailed analysis for a specific coin
- `/api/sentiment`: Get sentiment analysis with AI insights
- `/api/refresh_data`: Force refresh of cached data
- `/api/trending`: Get trending cryptocurrencies
- `/api/urgent`: Get urgent alerts and notifications

## Technologies Used

- Backend:
  - Flask
  - pandas
  - NLTK
  - VADER Sentiment Analysis
  - Google Gemini AI
  - Anthropic Claude
- Frontend:
  - HTML5/CSS3
  - Bootstrap 5
  - Plotly.js
  - JavaScript

## Contributing

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Acknowledgments

- VADER Sentiment Analysis
- TextBlob
- Google Gemini AI
- Anthropic Claude
