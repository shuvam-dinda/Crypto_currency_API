# Cryptocurrency API Analyzer

A Python-based application that fetches real-time cryptocurrency market data from the CoinGecko API, analyzes price movements, and generates reports for the top performing and underperforming cryptocurrencies.

## Overview

This project fetches cryptocurrency market data daily, identifies the top 10 cryptocurrencies with the highest and lowest 24-hour price changes, and saves the results to CSV files. It's designed to help users track market trends and identify significant market movements.

## Features

- 🔄 **Real-time Data Fetching**: Retrieves current cryptocurrency prices and market data from CoinGecko API
- 📊 **Top Performers**: Identifies the top 10 cryptocurrencies with highest 24-hour price increase
- 📉 **Top Decliners**: Identifies the top 10 cryptocurrencies with highest 24-hour price decrease
- 💾 **CSV Export**: Saves all data and analysis results to CSV files with timestamp
- 📈 **Market Analysis**: Includes market cap, all-time high, and all-time low data

## Requirements

- Python 3.x
- requests
- pandas
- datetime (built-in)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/shuvam-dinda/Crypto_currency_API.git
cd Crypto_currency_API
```

2. Install required dependencies:
```bash
pip install requests pandas
```

## Usage

Run the application:
```bash
python app.py
```

The script will:
1. Connect to CoinGecko API and fetch market data for top 250 cryptocurrencies
2. Process and analyze the data
3. Display top 10 gainers and losers in the console
4. Generate three CSV files with timestamps

## Output Files

The application generates three CSV files with the current date and time:

1. **crypto_data_[DATE_TIME].csv** - Complete data for all 250 cryptocurrencies
2. **top_positive_10_of_[DATE_TIME].csv** - Top 10 cryptocurrencies with highest 24h price increase
3. **top_negative_10_of_[DATE_TIME].csv** - Top 10 cryptocurrencies with highest 24h price decrease

### CSV Columns

- `id` - Cryptocurrency name/identifier
- `current_price` - Current price in USD
- `market_cap` - Market capitalization in USD
- `price_change_percentage_24h` - 24-hour price change percentage
- `ath` - All-Time High price
- `atl` - All-Time Low price
- `time_stamp` - Data collection timestamp

## API Used

**CoinGecko API** (Free, no authentication required)
- Endpoint: `https://api.coingecko.com/api/v3/coins/markets`
- Provides market data for top cryptocurrencies by market cap
- Documentation: https://www.coingecko.com/api/documentations/v3

## Use Cases

- Monitor cryptocurrency market trends
- Track significant price movements automatically
- Analyze market volatility
- Create historical records of price changes
- Generate reports for investment decisions

## Future Enhancements

- Email notifications for significant price changes
- Scheduled execution (cron job)
- Database storage instead of CSV
- Web dashboard for visualization
- API endpoint for accessing historical data

## License

This project is open source and available under the MIT License.

## Author

**Shuvam Dinda**

## Disclaimer

This tool is for informational purposes only. Cryptocurrency markets are highly volatile. Always conduct your own research before making investment decisions.

