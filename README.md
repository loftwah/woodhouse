# Woodhouse Discord Bot

Get things done with Woodhouse

![Woodhouse](https://user-images.githubusercontent.com/19922556/219645171-6fba43a6-f339-44ee-ae63-6f2f13aa0af3.jpg)

Welcome to Woodhouse, your personal assistant for all things Discord. With Woodhouse, you can chat with a state-of-the-art AI, powered by OpenAI's GPT-3 technology, and perform various commands to customize your chat experience. Whether you're looking to switch between public and private chat, reply to all messages in a channel, or clear your conversation history, Woodhouse has got you covered.

## Features

* `/chat [message]` - Chat with Woodhouse!
* `/private` - Switch to private mode
* `/public` - Switch to public mode
* `/replyall` - Switch between replyall mode and default mode
* `/reset` - Clear your conversation history

## Chatting with Woodhouse

Once you've invited Woodhouse to your Discord server, you can start chatting with the bot by using the `/chat` command followed by your message. Woodhouse will then respond to your message with a generated response from its GPT-3 model. You can also switch to private or public chat modes, or even reply to all messages in a channel with the `/replyall` command.

## Getting Started

To get started with Woodhouse, you'll need to do the following:

### Step 1: Create a Discord bot

1. Go to [https://discord.com/developers/applications](https://discord.com/developers/applications) and create an application
2. Build a Discord bot under the application
3. Get the token from bot settings
4. Store the token in a `.env` file under `DISCORD_BOT_TOKEN`
5. Turn MESSAGE CONTENT INTENT `ON`
6. Invite your bot to your server via OAuth2 URL Generator

### Step 2: Generate an OpenAI API key

1. Go to [https://beta.openai.com/account/api-keys](https://beta.openai.com/account/api-keys)
2. Click Create new secret key
3. Store the secret key in a `.env` file under `OPENAI_KEY`

### Step 3: Run the bot

1. Open a terminal or command prompt
2. Navigate to the directory where you installed the Woodhouse Discord bot
3. Run `python3 main.py` to start the bot

Alternatively, you can use Docker to run the bot. To do so:

1. Build the Docker image and run the Docker container with `docker compose up -d`
2. Inspect whether the bot is working properly with `docker logs -t woodhouse-discord-bot`

### Optional: Setup a starting prompt

A starting prompt will be invoked when the bot is first started or reset. To set it up:

1. Modify the content in `starting-prompt.txt`
2. All the text in the file will be fired as a prompt to the bot
3. Get the first message from Woodhouse in your Discord channel by right-clicking on the channel you want to receive the message from, copying the ID, and pasting it into `.env` under `DISCORD_CHANNEL_ID`

## Important Updates

As of the last update, ChatGPT is no longer available, so Woodhouse has been switched to using OpenAI's GPT-3 model instead. Also, please note that the ChatGPT API has been highly unstable, so please proceed with caution when using it. Lastly, the ChatGPT model now requires payment to use.

## Contributing

If you'd like to contribute to Woodhouse, feel free to fork the repository and submit a pull request. We'd be happy to consider your contributions.

## License

This project is licensed under the GPL License.
