# ChatGPT Discord Bot

> ### Build your own Discord bot using ChatGPT
---
> **Warning**
>
> #### 2023-02-10 Update: ChatGPT model but requires payment
> #### 2023-02-08 Update: ChatGPT API is highly unstable now
> #### 2023-02-03 Update: ChatGPT API working again
> #### 2023-02-02 Update: OpenAI has closed ChatGPT API, temporarily switching to using GPT-3 model
> #### 2023-02-01 Update: Now using the official ChatGPT API

## Features

* `/chat [message]` Chat with ChatGPT!
* `/private` ChatGPT switch to private mode
* `/public`  ChatGPT switch to public  mode
* `/replyall`  ChatGPT switch between replyall mode and default mode
* `/reset` Clear ChatGPT conversation history

### Chat

![image](https://user-images.githubusercontent.com/89479282/206497774-47d960cd-1aeb-4fba-9af5-1f9d6ff41f00.gif)

### Mode

* `public mode (default)`  the bot directly reply on the channel

  ![image](https://user-images.githubusercontent.com/89479282/206565977-d7c5d405-fdb4-4202-bbdd-715b7c8e8415.gif)

* `private mode` the bot's reply can only be seen by the person who used the command

  ![image](https://user-images.githubusercontent.com/89479282/206565873-b181e600-e793-4a94-a978-47f806b986da.gif)

* `replyall mode` the bot will reply to all messages in the server without using slash commands

   > **Warning**
   > The bot will easily be triggered in `replyall` mode, which could cause program failures

# Setup

## Install

1. `pip install -r requirements.txt`
2. **Rename the file `.env.dev` to `.env`**

## Step 1: Create a Discord bot

1. Go to https://discord.com/developers/applications create an application
2. Build a Discord bot under the application
3. Get the token from bot setting

   ![image](https://user-images.githubusercontent.com/89479282/205949161-4b508c6d-19a7-49b6-b8ed-7525ddbef430.png)
4. Store the token to `.env` under the `DISCORD_BOT_TOKEN`

   ![image](https://user-images.githubusercontent.com/89479282/217743218-26e3d999-44d5-4a0b-88e1-ee23f3ffd5d8.png)
   
5. Turn MESSAGE CONTENT INTENT `ON`

   ![image](https://user-images.githubusercontent.com/89479282/205949323-4354bd7d-9bb9-4f4b-a87e-deb9933a89b5.png)
   
6. Invite your bot to your server via OAuth2 URL Generator

   ![image](https://user-images.githubusercontent.com/89479282/205949600-0c7ddb40-7e82-47a0-b59a-b089f929d177.png)

## Step 2: Generate a OpenAI API key

1. Go to https://beta.openai.com/account/api-keys

2. Click Create new secret key

   ![image](https://user-images.githubusercontent.com/89479282/207970699-2e0cb671-8636-4e27-b1f3-b75d6db9b57e.PNG)

2. Store the SECRET KEY to `.env` under the `OPENAI_KEY`

## Step 3: Run the bot on the desktop
1. Open a terminal or command prompt
2. Navigate to the directory where you installed the ChatGPT Discord bot
3. Run `python3 main.py` to start the bot

## Step 3: Run the bot with Docker

1. Build the Docker image & Run the Docker container `docker compose up -d`
2. Inspect whether the bot works well `docker logs -t chatgpt-discord-bot`

   ### Stop the bot:

   * `docker ps` to see the list of running services
   * `docker stop <BOT CONTAINER ID>` to stop the running bot

### Have a good chat!

## Optional: Setup starting prompt

* A starting prompt would be invoked when the bot is first started or reset
* You can set it up by modifying the content in `starting-prompt.txt`
* All the text in the file will be fired as a prompt to the bot  
* Get the first message from ChatGPT in your discord channel!

   1. Right-click the channel you want to recieve the message, `Copy  ID`
   
        ![channel-id](https://user-images.githubusercontent.com/89479282/207697217-e03357b3-3b3d-44d0-b880-163217ed4a49.PNG)
    
   2. paste it into `.env` under `DISCORD_CHANNEL_ID`
