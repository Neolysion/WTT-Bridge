# WTT-Bridge (WIP)

A Bot that forwards conversations and media from Whatsapp to Telegram. 
To make it as seamless as possible, the bot will simulate conversations on Telegram by creating a separate group chat for each Whatsapp conversation and forward the messages accordingly.

>TODO screenshot

## Installation

1. Download WTT-Bridge:

    ```bash
    sudo apt-get install git
    git clone https://github.com/Neolysion/WTT-Bridge.git WTT-Bridge
    cd WTT-Bridge
 
    ```

2. Make sure you have at least Python 3.6 with python-dev and pip installed.
    Example for Ubuntu 16.04:
    
    ```bash
    sudo add-apt-repository ppa:jonathonf/python-3.6
    sudo apt-get update
    sudo apt-get install python3.6
    sudo apt-get install python3.6-dev
    wget https://bootstrap.pypa.io/get-pip.py
    sudo python3.6 get-pip.py
 
    ```

3. Install the libraries:
    
    ```bash
    sudo pip3.6 install -r requirements.txt
 
    ```
    
4. Check the next section on how to setup your config file. When you're done you can start the bot with:
 
     ```bash
    python3.6 run.py
 
    ```

## Configuration

You have to fill out all values in the config.json to run the bot. Here is as some info how you can find each value:

#### Telegram: 

- "bot_token": Talk to https://telegram.me/botfather and create a bot to get a token

- "bot_username": The username you gave your bot (with the @ in front)

- "api_id" and "api_hash": Visit https://my.telegram.org/

#### Whatsapp:

- "phone": your phone number with country code but without + or 0 at the beginning

- "client_static_keypar": to get your keypair do the following: 

1. Run ```yowsup-cli registration --requestcode sms --config-phone 49XXXXXXXXXXX --config-cc 49 --config-mcc 228 --config-mnc 02``` to start the registration. 
You can find your MMC and MNC codes here:
https://en.wikipedia.org/wiki/Mobile_country_code

2. When you receive the verification sms, run ```yowsup-cli registration --register 123456 --config-phone 49XXXXXXXX``` to verify your number.

3. If the verification was successfull you should now be able to see your client_static_keypair in the console. Copy it into the config.json 



## Notes
 