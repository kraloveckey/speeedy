# Telegram speedtest bot - speeedy

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

---

<a href="https://www.paypal.com/donate/?hosted_button_id=GWWLEXEF3XL92">
  <img src="https://raw.githubusercontent.com/kraloveckey/kraloveckey/refs/heads/main/.assets/paypal-donate-button.png" alt="Donate with PayPal" width="225" height="100"/>
</a>
