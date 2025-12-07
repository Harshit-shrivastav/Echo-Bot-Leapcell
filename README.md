# Leapcell deployable telegram bot

A telegram bot that can be deployed on leapcell.io for free.

Deploying Telegram bots has always been a paid service since Heroku.

Leapcell is a hosting platform that offers up to 4gb ram and 100% uptime and much more just check their website.

It is a little bit tricky to deploy a telegram bot on leapcell.io because it doesn't offer long polling and only supports webhook.

Using this template you can write your bot that can be deployed on leapcell.io for free with very good resources.

---

### Structure of Bot

There are three important files in this code structure:

- main.py
- bot.py
- Procfile

`main.py`

Never change anything in the main.py file because it contains all the crucial codes required to work on leapcell.io

Only modify it if you know what you are doing.

`bot.py`

This is the file where you write business logic for your bot.

`Procfile`

I would never recommend you to modify this file except changing the port.
Because this is the file which leapcell.io detects the configuration for deploying the bot.

### Steps to deploy this bot on leapcell.io

1. Visit Leapcell website and login or signup whatever you want to do.
2. If GitHub is not connected then do it.
3. On the dashboard, click create service, then choose the repository you want to connect.
4. Leapcell.io will automatically detect all the Start Command, Build Command, etc. automatically. Just add Environment variables that are required. By default these two variables are required by the template.

```txt
BOT_TOKEN
```

```txt
WEBHOOK_URL
```

> You can get `BOT_TOKEN` from Bot father on telegram.
For `WEBHOOK_URL` just add any random url or text because it can only be added after deploying the bot on leapcell.io

5. Then click the Submit button in the bottom right corner.
   
6. After deployment success, you would see a url with title Domains on leapcell.io of that deployed app.

> You have to copy the very first url and just ignore the async domain url.

7. Click the Env variables button and then replace the value of `WEBHOOK_URL` with the existing value of that variable and then click the save and deploy button.
8. After deployment, you can check that your Telegram bot would be running.
9. The very last and important step is to open uptimerobot and signup there and add the same URL you added in `WEBHOOK_URL`. It would avoid the bot from sleeping automatically after some time. Without doing it your bot will sleep after some minutes.

That's all the steps required to deploy your bot on leapcell.io, if you have any issues or queries just raise an issue on this repo I will help you to solve.

If it helped you in any way please follow me on GitHub for similar tutorials.
[![Follow](https://img.shields.io/github/followers/Harshit-shrivastav?style=social)](https://github.com/Harshit-shrivastav)

If you want more similar ways to host your Telegram bot then check out this [repo](https://github.com/Harshit-shrivastav/Free-Telegram-bot-hosting).
