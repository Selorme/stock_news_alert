# Stock Price Notification Application

This application sends a text message notification to a user whenever a significant change in the stock price of Tesla Inc (TSLA) is detected. The notification includes the stock price change percentage along with the latest news articles related to the company.

## Features

- Fetches the daily closing prices of Tesla Inc (TSLA) stock.
- Calculates the percentage change in stock price from the previous day.
- Retrieves the latest news articles about Tesla Inc if the stock price change exceeds 1%.
- Sends a text message with the stock price information and news articles via Twilio.

## Technologies Used

- Python
- Requests library for API calls
- Twilio API for sending SMS
- dotenv for managing environment variables

## Prerequisites

- Python 3.x
- `requests`, `twilio`, and `python-dotenv` libraries
- A Twilio account for SMS notifications
- API keys for stock and news data

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/Selorme/stock_news_alert.git
   cd stock-price-notification
   ```

2. Install the required packages:

   ```bash
   pip install requests twilio python-dotenv
   ```

3. Create a `.env` file in the root directory and add your environment variables:

   ```plaintext
   STOCK_ENDPOINT=your_stock_api_endpoint
   NEWS_ENDPOINT=your_news_api_endpoint
   STOCK_API_KEY=your_stock_api_key
   NEWS_API_KEY=your_news_api_key
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_NUMBER=your_twilio_phone_number
   MY_NUMBER=your_phone_number
   ```

   Replace the placeholder values with your actual API keys and phone numbers.

## How It Works

1. The application fetches the daily stock prices of Tesla Inc (TSLA) using the specified stock API.
2. It calculates the difference between the closing prices of the last two days and determines the percentage change.
3. If the percentage change exceeds 1%, the application fetches the latest news articles related to Tesla Inc from the news API.
4. The formatted stock change and news articles are sent to the user via SMS using the Twilio API.

## Example Message Format

```
TSLA: 🔺2%
Headline: Were Hedge Funds Right About Piling Into Tesla Inc. (TSLA)?
Brief: We at Insider Monkey have gone over 821 13F filings that hedge funds and prominent investors are required to file by the SEC. The 13F filings show the funds' and investors' portfolio positions as of March 31st, near the height of the coronavirus market crash.
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
