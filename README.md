# Telegram Channel-Assigned Chat Kicker

>[!WARNING]
> This repository is archived [due to a better fork](https://github.com/zhegal/comment-watchbot-tg-fork). You can still use this version if you want, but it's better to switch to the new version.
> 

This bot automatically kicks users who join the chat, allowing them to only leave comments in reply to channel posts.

## Requirements

- Node.js
- npm

## Setup
#### Manual way

1. Clone the repository:
    ```sh
    git clone https://github.com/ZAZiOs/comment-watchbot-tg
    cd comment-watchbot-tg
    ```

2. Install dependencies:
    ```sh
    npm install
    ```

3. Create a `.env` file in the root directory and add your bot token:
    ```env
    BOT_TOKEN=your-telegram-bot-token
    ```

#### Docker & Docker-compose

1. Clone the repository:
    ```sh
    git clone https://github.com/ZAZiOs/comment-watchbot-tg
    cd comment-watchbot-tg
    ```

2. Open `docker-compose.yml` and edit `BOT_TOKEN` to include your bot's Telegram token (same way as .env).
>[!NOTE]
> Alternatively you can create `.env` file and follow the Step 2 of the manual method. Be sure to remove or comment out `BOT_TOKEN` from `docker_compose.yml`.

## Running the Bot

>[!TIP]
>As [`nodemon`](https://github.com/remy/nodemon) is included with this project, running this script will automatically be wrapped over nodemon service, to allow the application to auto-restart when it crashes or if any file has been changed. See [the `nodemon`'s GitHub page](https://github.com/remy/nodemon) for more information.

- On Windows:
    ```sh
    npm run win
    ```

- On Unix-based systems:
    ```sh
    npm run unix
    ```

- Over docker-compose:
    ```sh
    docker compose up -d
    ``` 
    or 
    ```sh
    docker-compose up -d # if your docker compose installation is component-based
    ```

- For debugging:
    ```sh
    npm start
    ```

  Docker Compose users will need to change `NODE_ENV` variable to `development`.  

## License

This project is licensed under the MIT License.
