# WTT-Bridge
A Bot that forwards conversations and media from Whatsapp to Telegram

## Installation

#### 1. Telegram: 

1.1 Talk to the Bot Father to create a bot. https://telegram.me/botfather 

1.2 Enter the bot API key in the config.json

#### 2. Whatsapp:

2.1 Run ```yowsup-cli registration --requestcode sms --config-phone 49XXXXXXXXXXX --config-cc 49 --config-mcc 228 --config-mnc 02``` to start the registration. 
You can find your MMC and MNC codes here:
https://en.wikipedia.org/wiki/Mobile_country_code


2.2 When you receive the verification sms, run ```yowsup-cli registration --register 123456 --config-phone 49XXXXXXXX``` to verify your number


### Notes
 