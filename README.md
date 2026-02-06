# 🎮 Retroverse - Multiplayer Board Games

**Play classic board games with friends online!** Built with Phaser 3 + Socket.io.

## 🎯 Games

- **🎲 Ludo** - Roll dice, move pieces, capture opponents
- **🐍 Snakes & Ladders** - Climb ladders, avoid snakes, reach 100
- **❌ Tic-Tac-Toe** - Get 3 in a row

## ✨ Features

✅ Real-time multiplayer
✅ Play with AI bot
✅ Smooth animations & particle effects
✅ Room-based matchmaking
✅ Up to 4 players
✅ Mobile-friendly

## 🚀 Quick Start

### Play Now

Visit: **[Your Vercel URL]**

1. Enter your name
2. Click "Host Game" or enter room code to join
3. Share room code with friends
4. Select a game and play!

### Run Locally

```bash
# Install dependencies
npm install

# Start game server (Terminal 1)
npm run server

# Start frontend (Terminal 2)
npm run dev

# Open http://localhost:3000
```

## 📦 Deploy

### Frontend (Vercel)

1. Push to GitHub
2. Import on Vercel
3. Deploy automatically ✅

### Backend (Railway/Render)

**Option A: Railway** (Recommended)

1. Go to [railway.app](https://railway.app)
2. New Project → Deploy from GitHub
3. Select this repo
4. Set start command: `node server/index.js`
5. Copy your Railway URL
6. Update `src/main.js` line 8:
   ```js
   const socket = io('https://your-railway-url.railway.app');
   ```

**Option B: Render**

1. Go to [render.com](https://render.com)
2. New Web Service
3. Connect GitHub repo
4. Build: `npm install`
5. Start: `node server/index.js`
6. Update socket URL in `src/main.js`

## 🎮 How to Play

### Ludo

- Roll 6 to exit yard
- Land on opponent = capture (they go back)
- Roll 6 or capture = bonus turn
- Get all 4 pieces home to win

### Snakes & Ladders

- Roll dice to move forward
- Land on ladder = climb up 🎉
- Land on snake = slide down 😢
- Exact roll to reach 100

### Tic-Tac-Toe

- X goes first
- Click empty cell to place mark
- Get 3 in a row to win

## 🛠️ Tech Stack

- **Frontend**: Phaser 3 (game engine) + Vite
- **Backend**: Node.js + Socket.io
- **Deploy**: Vercel (frontend) + Railway (backend)

## 📁 Project Structure

```
src/
├── main.js           # Entry point + socket setup
├── scenes/
│   ├── MenuScene.js  # (unused, menu is HTML)
│   ├── LobbyScene.js # Game selection
│   ├── LudoScene.js  # Ludo board + UI
│   ├── SnakesScene.js # Snakes board + UI
│   └── TicTacToeScene.js # TTT board + UI

server/
├── index.js          # Socket.io server
├── engines/
│   ├── ludo.js       # Ludo game logic
│   ├── snakes.js     # Snakes game logic
│   └── ttt.js        # TTT game logic
```

## 🎨 Customization

### Change Colors

Edit `index.html` CSS gradients and Phaser scene colors.

### Add Sounds

1. Add `.mp3` files to `public/sounds/`
2. Load in Phaser: `this.load.audio('dice', 'sounds/dice.mp3')`
3. Play: `this.sound.play('dice')`

### Add More Games

1. Create new scene in `src/scenes/`
2. Add to `config.scene` array in `main.js`
3. Add button in `LobbyScene.js`
4. Create engine in `server/engines/`
5. Add socket handlers in `server/index.js`

## 🐛 Troubleshooting

**"Cannot connect to server"**
- Make sure server is running (`npm run server`)
- Check socket URL in `src/main.js`

**"Room not found"**
- Room codes are case-sensitive
- Rooms expire when all players leave

**Game feels laggy**
- Use Railway instead of free Render tier
- Deploy server closer to players geographically

## 📝 License

MIT - Free to use and modify!

## 🤝 Contributing

Pull requests welcome! Ideas:
- Add sound effects
- Improve AI bot
- Add chat feature
- Mobile touch controls
- More games (Chess, Checkers, etc.)

---

Built with ❤️ using Phaser 3
