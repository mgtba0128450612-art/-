# 🤖 𝑵𝑨𝑮𝑰 𝑩𝑶𝑻❄️ - Advanced WhatsApp Multi-Device Bot

<p align="center">
  <img src="https://img.shields.io/badge/Version-7.0.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/WhatsApp-Bot-25D366?style=for-the-badge&logo=whatsapp" alt="WhatsApp">
  <img src="https://img.shields.io/badge/Node.js-20-339933?style=for-the-badge&logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

<p align="center">
  <b>The most powerful and feature-rich WhatsApp bot built with Baileys MD</b>
</p>

---

## 🚀 One-Click Deploy

<p align="center">
  <a href="https://heroku.com/deploy?template=https://github.com/Itxxwasi/WASI-MD-V7">
    <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy to Heroku" height="40">
  </a>
  &nbsp;&nbsp;
  <a href="https://railway.app/new/template?template=https://github.com/Itxxwasi/WASI-MD-V7">
    <img src="https://railway.app/button.svg" alt="Deploy on Railway" height="40">
  </a>
</p>

<p align="center">
  <a href="https://render.com/deploy?repo=https://github.com/Itxxwasi/WASI-MD-V7">
    <img src="https://render.com/images/deploy-to-render-button.svg" alt="Deploy to Render" height="40">
  </a>
  &nbsp;&nbsp;
  <a href="https://app.koyeb.com/deploy?type=git&repository=github.com/Itxxwasi/WASI-MD-V7">
    <img src="https://www.koyeb.com/static/images/deploy/button.svg" alt="Deploy to Koyeb" height="40">
  </a>
</p>

---

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-configuration">Configuration</a> •
  <a href="#-commands">Commands</a> •
  <a href="#-deployment">Deployment</a> •
  <a href="#-support">Support</a>
</p>

---

## ✨ Features

### 🎯 Core Features
- **Multi-Device Support** - Works with WhatsApp's latest multi-device feature
- **250+ Commands** - Extensive command library for all your needs
- **Modular Plugin System** - Easy to add/remove functionality
- **Database Integration** - MongoDB for persistent storage
- **Web Dashboard** - Beautiful web interface for management

### 🛠️ Command Categories
| Category | Commands | Description |
|----------|----------|-------------|
| 📥 **Downloader** | `ytmp3`, `ytmp4`, `tiktok`, `instagram`, `facebook` | Download media from any platform |
| 🎵 **Audio** | `bass`, `nightcore`, `slow`, `speed`, `reverse` | Audio manipulation tools |
| 🖼️ **Images** | `sticker`, `toimg`, `removebg`, `blur`, `enhance` | Image processing & editing |
| 🤖 **AI** | `gpt`, `dalle`, `imagine`, `chat`, `translate` | AI-powered features |
| 👥 **Groups** | `kick`, `add`, `promote`, `demote`, `mute`, `antilink` | Group management |
| 🎮 **Games** | `tictactoe`, `truth`, `dare`, `quiz`, `slots` | Fun games to play |
| 🔧 **Tools** | `ping`, `runtime`, `speed`, `info`, `menu` | Utility commands |
| 👤 **Owner** | `broadcast`, `ban`, `unban`, `block`, `eval` | Owner-only commands |

### 🔥 Special Features
- ✅ **Anti-Delete** - Recover deleted messages
- ✅ **Auto-Read Status** - Automatically view status updates
- ✅ **Auto-React Status** - React to status with emoji
- ✅ **Welcome/Goodbye** - Custom group greetings
- ✅ **Anti-Link** - Protect groups from spam links
- ✅ **Anti-Spam** - Rate limiting protection
- ✅ **Always Online** - Keep bot presence active
- ✅ **Auto-Typing** - Show typing indicator

---

## 📦 Installation

### Prerequisites
- Node.js 18+ (Recommended: Node.js 20)
- MongoDB database
- Git

### Quick Start

```bash
# Clone the repository
git clone https://github.com/Itxxwasi/WASI-MD-V7.git
cd WASI-MD-V7

# Install dependencies
npm install

# Configure environment
cp .env.example .env
# Edit .env with your settings

# Start the bot
npm start
```

### Using Docker

```bash
# Build and run with Docker
docker build -t wasi-md-v7 .
docker run -d --name wasi-bot -p 3000:3000 --env-file .env wasi-md-v7

# Or use Docker Compose
docker-compose up -d
```

---

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Required Settings
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/wasimd
SESSION_ID=your_session_name
OWNER_NUMBER=923001234567

# Bot Settings
PREFIX=.
BOT_NAME=WASI-MD V7
MODE=public

# Features
AUTO_READ=false
AUTO_TYPING=false
ALWAYS_ONLINE=true
AUTO_STATUS_VIEW=true
AUTO_STATUS_REACT=true

# Anti-Features
ANTI_DELETE=true
ANTI_LINK=false
ANTI_SPAM=true
```

### Configuration File

```javascript
// config.js - Main configuration
module.exports = {
    bot: {
        name: process.env.BOT_NAME || 'WASI-MD V7',
        prefix: process.env.PREFIX || '.',
        mode: process.env.MODE || 'public'
    },
    owner: {
        number: process.env.OWNER_NUMBER,
        name: 'MR WASI'
    },
    database: {
        uri: process.env.MONGODB_URI
    }
}
```

---

## 📋 Commands

### Basic Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `.menu` | Show all commands | `.menu` |
| `.help` | Get help for a command | `.help <command>` |
| `.ping` | Check bot latency | `.ping` |
| `.runtime` | Bot uptime | `.runtime` |
| `.owner` | Contact owner | `.owner` |

### Downloader Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `.ytmp3` | Download YouTube audio | `.ytmp3 <url/search>` |
| `.ytmp4` | Download YouTube video | `.ytmp4 <url/search>` |
| `.tiktok` | Download TikTok video | `.tiktok <url>` |
| `.instagram` | Download Instagram media | `.instagram <url>` |
| `.facebook` | Download Facebook video | `.facebook <url>` |
| `.twitter` | Download Twitter media | `.twitter <url>` |
| `.spotify` | Download Spotify track | `.spotify <url/search>` |

### Group Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `.kick` | Remove member | `.kick @user` |
| `.add` | Add member | `.add 923001234567` |
| `.promote` | Make admin | `.promote @user` |
| `.demote` | Remove admin | `.demote @user` |
| `.mute` | Mute group | `.mute` |
| `.unmute` | Unmute group | `.unmute` |
| `.antilink` | Toggle anti-link | `.antilink on/off` |
| `.welcome` | Set welcome message | `.welcome <text>` |
| `.goodbye` | Set goodbye message | `.goodbye <text>` |

### AI Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `.gpt` | Chat with GPT | `.gpt <question>` |
| `.dalle` | Generate AI image | `.dalle <prompt>` |
| `.imagine` | Creative AI art | `.imagine <prompt>` |
| `.translate` | Translate text | `.translate <lang> <text>` |

---

## 🚀 Deployment

### Deploy to Heroku

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

1. Click the deploy button
2. Fill in the environment variables
3. Deploy and wait for build
4. Scale the worker dyno

### Deploy to Railway

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new)

1. Connect your GitHub repository
2. Add environment variables
3. Deploy!

### Deploy to Render

1. Create a new Web Service
2. Connect this repository
3. Add environment variables
4. Deploy!

### VPS Deployment

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install Node.js 20
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs

# Install PM2
npm install -g pm2

# Clone and setup
git clone https://github.com/Itxxwasi/WASI-MD-V7.git
cd WASI-MD-V7
npm install

# Start with PM2
pm2 start npm --name "wasi-md" -- start
pm2 save
pm2 startup
```

---

## 📁 Project Structure

```
WASI-MD-V7/
├── lib/
│   ├── database.js        # MongoDB connection
│   ├── message-handler.js # Message processing
│   └── plugin-loader.js   # Plugin system
├── plugins/
│   ├── menu.js           # Menu command
│   └── ping.js           # Ping command
├── config.js             # Configuration
├── loader.js             # Plugin loader
├── start.js              # Entry point
├── package.json          # Dependencies
├── Dockerfile            # Docker config
├── docker-compose.yml    # Docker compose
├── heroku.yml            # Heroku config
├── app.json              # Heroku app config
└── .env.example          # Environment template
```

---

## 🔧 Development

### Adding New Commands

Create a new file in `plugins/` directory:

```javascript
// plugins/example.js
module.exports = {
    name: 'example',
    description: 'Example command',
    usage: '.example <text>',
    category: 'tools',
    
    async execute(client, message, args) {
        const text = args.join(' ')
        await message.reply(`You said: ${text}`)
    }
}
```

### Plugin Structure

```javascript
module.exports = {
    name: 'commandname',      // Command trigger
    aliases: ['cmd', 'c'],    // Alternative triggers
    description: 'What it does',
    usage: '.cmd <args>',
    category: 'category',
    cooldown: 5,              // Seconds
    ownerOnly: false,
    groupOnly: false,
    adminOnly: false,
    
    async execute(client, message, args, context) {
        // Your code here
    }
}
```

---

## 🔄 Updating

```bash
# Pull latest changes
git pull origin main

# Install new dependencies
npm install

# Restart the bot
pm2 restart wasi-md
```

---

## 🐛 Troubleshooting

### Common Issues

**Bot not connecting:**
```bash
# Check logs
pm2 logs wasi-md

# Restart
pm2 restart wasi-md
```

**MongoDB connection failed:**
- Verify your `MONGODB_URI` is correct
- Check if IP is whitelisted in MongoDB Atlas

**Session expired:**
- Delete the session folder
- Restart and scan new QR code

**Commands not working:**
- Check if prefix is correct
- Verify bot mode (public/private)

---

## 📞 Support

- **Developer**: MR WASI
- **WhatsApp**: [Contact](https://wa.me/263788049675)
- **GitHub**: [@Itxxwasi](https://github.com/Itxxwasi)

### Community
- Report bugs via GitHub Issues
- Feature requests welcome
- Pull requests appreciated

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Disclaimer

This bot is for educational purposes only. The developer is not responsible for any misuse. Use responsibly and follow WhatsApp's Terms of Service.

---

## 🙏 Credits

- [Baileys](https://github.com/WhiskeySockets/Baileys) - WhatsApp Web API
- [Node.js](https://nodejs.org/) - Runtime
- [MongoDB](https://www.mongodb.com/) - Database

---

<p align="center">
  <img src="https://img.shields.io/badge/Made_with-❤️-red?style=for-the-badge" alt="Made with love">
</p>

<p align="center">
  <b>⭐ Star this repo if you like it! ⭐</b>
</p>

<p align="center">
  © 2024-2026 WASI-MD-V7 | All Rights Reserved
</p>
