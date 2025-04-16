-X-VOID-BLACKICE-X

---

## 📌 USIC Bot – Discord Music & Utility Bot

**USIC Bot** is a powerful, multipurpose bot made with Discord.js v14. It includes music capabilities, event handlers, and utility features. Designed to run on the latest Node.js versions.

---

### 🚀 Features

- 🎵 Play music in voice channels
- 💬 Generates transcripts using `discord-html-transcripts`
- 🧰 Utility functions loaded dynamically
- 🖥️ Built-in web interface using Express (if configured)
- 📅 Timestamping and time-related functions via `moment`
- 🧼 Cleaner code with auto-loading utils from `src/utils`

---

### 📂 Project Structure

```
root
│
├── index.js                 # Entry point
├── package.json             # Project metadata and dependencies
├── package-lock.json        # Exact dependency tree
└── src/
    ├── config.js            # Bot token and configurations
    └── utils/               # Auto-loaded utility functions (e.g., music, commands)
```

---

### 📥 Installation

> **Requirements**:  
> - Node.js `v20+`  
> - A Discord bot token  
> - Basic knowledge of running JavaScript/Node projects

#### 1. Clone the repo

```bash
git clone https://github.com/yourusername/usic-bot.git
cd usic-bot
```

#### 2. Install dependencies

```bash
npm install
```

#### 3. Setup your bot token

Create a file at `src/config.js` and add:

```js
module.exports = {
  token: "YOUR_BOT_TOKEN_HERE"
};
```

---

### ▶️ Running the Bot

Start the bot with:

```bash
npm start
```

You should see your bot come online if everything is set up correctly.

---

### 🧠 How It Works

#### `index.js`
- Loads all utilities from `src/utils/`
- Initializes `discord.js` client with all intents and partials
- Starts listening with `client.login(token)`

#### `src/utils/`
Each file inside this folder should export an `execute(client)` function. This allows you to modularize logic, such as:
- `music.js`
- `commands.js`
- `events.js`

Example `utils/music.js`:
```js
module.exports.execute = (client) => {
  // register music commands or events
};
```

---

### 🧰 Available Dependencies

- `discord.js` – Bot framework
- `express` – Optional web interface
- `moment` – Time formatting
- `discord-html-transcripts` – For generating transcripts
- `lodash.uniqwith`, `fs`, `greetify` – Utility libraries

---

### 🔐 Notes

- Keep your token secure! Never share it.
- Deploy to platforms like Heroku, Replit, or use PM2 for self-hosting.

---

### 💡 Future Ideas

- Add Slash commands support
- Voice channel auto-disconnect
- Express-based dashboard
- Playlist system

---
