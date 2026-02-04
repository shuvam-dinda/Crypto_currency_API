# Crypto_currency_API
Cryptocurrency API Project
A Python application that fetches real-time cryptocurrency market data, analyzes price performance, and generates reports on top-performing and worst-performing cryptocurrencies.

Features
✅ Fetches real-time cryptocurrency data from the CoinGecko API
✅ Retrieves data for top 250 cryptocurrencies by market cap
✅ Analyzes 24-hour price changes
✅ Identifies top 10 best-performing cryptocurrencies (highest positive change)
✅ Identifies top 10 worst-performing cryptocurrencies (highest negative change)
✅ Exports data to CSV files with timestamps
✅ Collects comprehensive market data (current price, market cap, ATH, ATL)
Requirements
Python 3.x
requests
pandas
datetime (built-in)
Installation
Clone this repository:
git clone https://github.com/shuvam-dinda/Crypto_currency_API.git
cd Crypto_currency_API
Install required packages:
pip install requests pandas
Usage
Run the script:

python app.py
The script will:

Connect to the CoinGecko API
Fetch current market data for top 250 cryptocurrencies
Generate three CSV files with timestamps:
crypto_data_[timestamp].csv - Full dataset
top_positive_10_of_[timestamp].csv - Top 10 gainers (24h)
top_negative_10_of_[timestamp].csv - Top 10 losers (24h)
API Information
Endpoint: https://api.coingecko.com/api/v3/coins/markets

Parameters:

vs_currency: USD
order: market_cap_desc (sorted by market cap)
per_page: 250 (maximum cryptocurrencies per request)
page: 1
Output Files
CSV Columns
id: Cryptocurrency identifier
current_price: Current price in USD
market_cap: Market capitalization
price_change_percentage_24h: 24-hour price change percentage
ath: All-time high price
atl: All-time low price
time_stamp: Data collection timestamp
Example Output
Files are generated with the format: filename_DD-MM-YYYY_HH-MM-SS.csv

Example:

crypto_data_03-02-2026_21-37-36.csv
top_positive_10_of_03-02-2026_21-37-36.csv
top_negative_10_of_03-02-2026_21-37-36.csv
Project Structure
Crypto_currency_API/
├── app.py                           # Main application script
├── app.txt                          # API configuration reference
├── README.md                        # Project documentation
└── crypto_data_*.csv               # Generated data files
Future Enhancements
Add scheduled execution (daily at 8 AM)
Implement email notifications for top gainers/losers
Add database storage for historical tracking
Create visualization dashboards
Add more analysis metrics
License
This project uses the free CoinGecko API for cryptocurrency data.

Author
Shuvam Dinda - GitHub Profile
