```markdown
# Bybit Futures Trading Bot

This project is a bot designed for trading futures on the Bybit exchange.

## Configuration Settings

In the `config.py` file, the following parameters are specified:

- `time_frame`: The time frame in minutes for the trading strategy.
- `mode`: Set to `0` for cross margin and `1` for isolated margin.
- `backup_balance`: The amount of funds held outside the futures account that can be used
to replenish the futures account during drawdowns.
- Other essential settings and variables that may be utilized by the decision-making module.

## Decision-Making Modules

The decision-making modules are located in the `brain_modules` subdirectory of the project.
The main file, `main.py`, accesses the chosen decision-making module with the following line:

from brain_modules.change10_BTC_ETH import request_updated_positions_dict_format

The function `request_updated_positions_dict_format` returns a dictionary containing the tickers and the sizes of positions in coins that should be held at the current moment. The format of the dictionary is as follows:

{'BTCUSDT': -0.0, 'ETHUSDT': -0.01}

## Logging

Logs are written to the `bot.log` file located in the root folder of the project.

## API Keys and Secrets

The `keys.py` file should be placed in the main project folder. This file is not uploaded to GitHub; you need to create it manually and add your API keys, Telegram token, and chat ID:

API_KEY = "..."
API_SECRET = "..."

A function to duplicate logs to Telegram will be added in a later version.

## Note

Make sure to keep your API keys and sensitive information secure. Do not share this information in public repositories.
