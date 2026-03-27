# Trading Bot - Binance Futures Testnet

## Overview
This is a simple Python-based trading bot that places MARKET and LIMIT orders on Binance Futures Testnet.

## Features
- Place MARKET and LIMIT orders
- Supports BUY and SELL
- CLI-based input using argparse
- Input validation
- Logging of requests and responses
- Error handling for API and user input

## Project Structure
trading_bot/
  bot/
    client.py
    orders.py
    validators.py
    logging_config.py
  cli.py
  .env
  requirements.txt
  bot.log

## Setup Instructions

1. Clone the repository
2. Create virtual environment:
   python -m venv .venv
   .venv\Scripts\activate

3. Install dependencies:
   pip install -r requirements.txt

4. Create .env file:
   API_KEY=your_testnet_key
   API_SECRET=your_testnet_secret

## How to Run

### Market Order
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.002

### Limit Order
python cli.py --symbol BTCUSDT --side BUY --type LIMIT --quantity 0.004 --price 30000

## Notes
- Minimum notional value must be ≥ 100 USDT
- Testnet may not instantly fill orders

## Logs
All API requests and responses are logged in bot.log