# Telegram speedtest bot - speeedy

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/kraloveckey)

[![Telegram Channel](https://img.shields.io/badge/Telegram%20Channel-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/cyber_notes)

Python bot reports speedtests to a Telegram channel or bot.

## Install dependencies

```bash
sudo apt install python3 python3-pip
sudo pip3 install python-telegram-bot speedtest-cli
```

## Create config file

Create the file `config.json` in the root directory of this project,
which has the following format:

```json
{
    "telegram": {
        "token": "abc...",
        "channel": "@channel_xy or Telegram ID"
    }
}

``` 

## Create a Telegram bot

Write to the account `@BotFather` the message `/newbot` and follow the
instructions. Enter the retreived token to the `token` property in `config.json`,
next get your Telegram ID and enter the retreived id to the `channel` property in `config.json`.

## Create a Telegram channel

Create a Telegram channel and add your created bot as an admin with the
privileges to post messages. Then add the name of the created channel
(with a leading `@`) to the `channel` property in `config.json`. Make
shure your channel is public, otherwise it will not work.

## Run the script

```bash
cd /opt/speeedy/
python3 . 
``` 

If you want to run the script repeatedly, you can create a cronjob for
that:

`5,15,25,35,45,55 * * * *    cd /opt/speeedy/ && /usr/bin/python3 . >/dev/null 2>&1`