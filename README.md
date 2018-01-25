# Binance-Telegram-Bot
A basic Telegram bot that sends updates if a transaction has gone through on Binance. 
Written for Python 3.6.4.

# Usage

- Copy `config.ini.sample` to `config.ini` and fill all of the data
- `pip install -r requirements`
- `python start.py`

For a deeper installation guide (including creating a Telegram bot): 

# Config

- GENERAL
	- `refresh-rate`: (int) The number of minutes to wait before refreshing orders from Binance (Default: 1)
	- `update-open`: (yes/no) A boolean on if to send Telegram messages for new open buy/sell orders (Default: yes)
	- `update-closed`: (yes/no) A boolean on if to send Telegram messages for closed buy/sell orders (Default: yes) 
- BINANCE
	- `key`: (string) API key fetched from Binance's website
	- `secret`: (string) API secret fetched from Binance's website
- TELEGRAM
	- `token` (string) Bot token fetched from @Botfather on Telegram
	- `chat_id` (string) Your chat ID on the chat to send these messages
		- *Get your personal/group chat ID easily from this bot: https://telegram.me/myidbot*

# Notes

- If enabled, a message will be sent even if you closed the buy/sell order yourself
- A notification will not be sent if a buy/sell order goes through before the script has refreshed
- Currently it is purely server-sided with no callback support
	- This *may* get added in the future for additional features
	
# APIs Used

- [Python-Binance](https://github.com/sammchardy/python-binance
- [Python-Telegram-Bot](https://github.com/python-telegram-bot/python-telegram-bot)
