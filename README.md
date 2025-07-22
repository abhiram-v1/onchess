# Chess Web App

A modern chess web app with:
- **Single-player vs Bot** (Stockfish, in-browser)
- **Real-time Multiplayer** (WebSocket server backend)
- **Beautiful, authentic UI**
- **Mobile and desktop support**

## Features
- Play against a strong chess bot (Stockfish) in your browser
- Play real-time multiplayer games with others online
- Choose from multiple board and piece styles
- Responsive, elegant UI for all devices
- Online player count and rapid time controls in multiplayer

## Project Structure

- `simple-chess.html` — Single-player chess vs bot (works on GitHub Pages or any static host)
- `Multi-chess.html` — Multiplayer chess UI (connects to backend WebSocket server)
- `server.js` — Node.js WebSocket server for multiplayer (deploy to Render, Railway, etc.)
- `stockfish.js` — Stockfish chess engine for browser bot
- `Boards/`, `Glothic style/`, etc. — Board and piece assets

## How to Run (Local Development)

1. **Install Node.js** (https://nodejs.org/)
2. **Install dependencies for multiplayer server:**
   ```bash
   npm install
   ```
3. **Start the WebSocket server:**
   ```bash
   node server.js
   ```
4. **Serve the frontend (for bot and multiplayer):**
   ```bash
   python -m http.server 8000
   ```
5. **Open in your browser:**
   - Single player: [http://localhost:8000/simple-chess.html](http://localhost:8000/simple-chess.html)
   - Multiplayer: [http://localhost:8000/Multi-chess.html](http://localhost:8000/Multi-chess.html)

## How to Deploy

### Single Player (Bot)
- Upload all frontend files (including `stockfish.js`) to GitHub Pages or any static host.
- Users can play against the bot directly from your site.

### Multiplayer
- Deploy `server.js` and `package.json` to a Node.js host (e.g., Render, Railway).
- Update the WebSocket URL in `Multi-chess.html` to your deployed backend (e.g., `wss://your-app.onrender.com`).
- Upload your frontend to GitHub Pages or any static host.
- Multiplayer users will connect to your backend for real-time play and online player count.

## Main Menu Flow
- **Single Player:** Choose bot difficulty, board/piece style, and play instantly.
- **Multiplayer:**
  1. Choose a time control (10, 15, 30 min)
  2. See the number of players online
  3. Click Play to join/create a game (enter your name and optional room code)
  4. Play real-time chess with others

## Notes
- Do **not** commit `node_modules` to your repo. Use `npm install` to install dependencies.
- The multiplayer server must be running for online play to work.
- For production, use a secure WebSocket URL (`wss://`).

## License
MIT 
