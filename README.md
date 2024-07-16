# PrimeMusic-Lavalink

## Introduction
Welcome to **PrimeMusic-Lavalink**! This guide will help you set up your own music bot, capable of streaming music from YouTube, SoundCloud, and Spotify. This bot, made by Shiva, uses Lavalink for high-quality audio streaming. Let's get started!

## Features
- **Supported Platforms**: YouTube, SoundCloud, Spotify
- **Customization**: Configurable musicard themes, buttons, and more

## Requirements
- **Node.js** version 18 or higher
- **discord.js** version 14

## Setup Guide

### 1. Fork the Repository
1. **Fork the repository** on GitHub to get your own copy.
2. **Clone your fork** to your local machine:
    ```bash
    git clone https://github.com/GlaceYT/PrimeMusic-Lavalink.git
    cd PrimeMusic-Lavalink
    ```

### 2. Configuration
#### Bot Token and Intents
1. **Create a new bot** on the [Discord Developer Portal](https://discord.com/developers/applications).
2. **Copy your bot token** and create a `.env` file in the root directory of your project:
    ```env
    TOKEN=YOUR_BOT_TOKEN_HERE
    ```
3. **Enable the required intents** in the Developer Portal:
    - Navigate to `Bot` > `Privileged Gateway Intents`
    - Turn on `PRESENCE INTENT`, `SERVER MEMBERS INTENT`, and `MESSAGE CONTENT INTENT`.

### 3. Lavalink Setup
1. **Lavalink Server Details** are already configured in `config.js`. If you want to use your own server, modify the `nodes` section:
    ```javascript
    nodes: [
      {
        name: "Node #1",
        host: "your-lavalink-host",
        port: 2333,
        password: "your-lavalink-password",
        secure: false
      },
    ]
    ```
2. Alternatively, you can use pre-hosted Lavalink servers. For example, you can use servers from [lavalink.darrennathanael.com](https://lavalink.darrennathanael.com/).
   *Just make sure you are using the v3 version.*

### 4. Running the Bot
1. **Install the dependencies**:
    ```bash
    npm install
    ```
2. **Run the bot**:
    ```bash
    node index.js
    ```
    The bot should now be online and ready to use!

## Commands
```css
[ /play    ] - Start playing the songs.
[ /pause   ] - Pause the current song.
[ /resume  ] - Resume the current song.
[ /lyrics  ] - Displays the lyrics of a song.
[ /skip    ] - Skip the current song.
[ /stop    ] - Destroys the music player.
[ /np      ] - Shows now playing song.
[ /volume  ] - Sets the volume of the player.
[ /ping    ] - Check bot latency.
[ /support ] - Shows support server info.
[ /help    ] - Display the help menu.
```

## Configuration Options
### config.js
```javascript

module.exports = {
  TOKEN: "", // Your bot token you can either put here or .env to be safe
  ownerID: ["1004206704994566164", ""], // Bot owner IDs
  setupFilePath: './commands/setup.json', // Setup file path
  commandsDir: './commands', // Commands directory
  embedColor: "#1db954", // Embed color
  musicardTheme: "themes16", // Theme for music card (1-19)
  activityName: "You", // Bot status activity name
  activityType: "WATCHING", // Bot status activity type (LISTENING, PLAYING, WATCHING)
  SupportServer: "https://discord.gg/xQF9f9yUEM", // Support server link
  CheckmarkIcon: "https://cdn.discordapp.com/attachments/1230824451990622299/1230836684774576168/7762-verified-blue.gif", // Checkmark icon URL
  MusicIcon: "https://media.discordapp.net/attachments/1230824451990622299/1236664581364125787/music-play.gif", // Music icon URL
  embedTimeout: 5, // Embed timeout in seconds
  errorLog: "", // Error log file path

  // Lavalink Server Details
  nodes: [
    {
      name: "Node #1",
      host: "lava-v3.ajieblogs.eu.org",
      port: 80,
      password: "https://dsc.gg/ajidevserver",
      reconnectTimeout: 5000,
      reconnectTries: Infinity,
      secure: false
    },
  ]
}
```
## Configuration Themes
These are images for some of the themes we have for the music card:

![Theme 1](https://private-user-images.githubusercontent.com/82333197/348460473-a4338251-00cf-47e2-b90d-f568f023eb7e.png)
![Theme 2](https://private-user-images.githubusercontent.com/82333197/348439269-d83bd2ab-e328-41a0-97ab-d122f41b914a.png)
![Theme 3](https://private-user-images.githubusercontent.com/82333197/348439267-699f6e68-a8b6-4a5c-be5f-f42077d94e98.png)

## Troubleshooting
- **Bot not responding?** Check if the token is correct and the intents are enabled.
- **Music not playing?** Ensure the Lavalink server details are correct and change the lavalink some public ones may not work.

## Additional Resources
- **Discord.js Documentation**: [discord.js.org](https://discord.js.org/)
- **Lavalink Documentation**: [freya.io/Lavalink](https://freya.io/Lavalink/)

## Support
Join our [Support Server](https://discord.gg/mH5djUtBCX) for any help or questions.

## Contributors
- **Shiva** - Original creator
- **Dante** - Random guy

## YouTube Tutorial
For a step-by-step video guide on setting up the PrimeMusic, check out our [YouTube tutorial](https://youtu.be/M_7TAJ9oqcs?si=p8-vc4T6KrxkoZlM).
