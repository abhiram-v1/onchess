# Multiplayer Chess Game

A real-time multiplayer chess game built with HTML5, JavaScript, and WebSocket technology.

## Features

- **Real-time multiplayer gameplay** - Play chess against other players online
- **Room-based matchmaking** - Create or join rooms with unique codes
- **Live chat** - Communicate with your opponent during the game
- **Move validation** - Server-side chess move validation using chess.js
- **Game state synchronization** - Real-time board updates across all players
- **Responsive design** - Works on desktop and mobile devices

## Setup Instructions

### Prerequisites
- Node.js (version 14 or higher)
- npm (comes with Node.js)

### Installation

1. **Install server dependencies:**
   ```bash
   npm install
   ```

2. **Start the WebSocket server:**
   ```bash
   npm start
   ```
   The server will run on `http://localhost:3000`

3. **Open the game:**
   - Open `Multi-chess.html` in your web browser
   - Or serve it using a local web server

### How to Play

1. **Join a Game:**
   - Enter your name
   - Leave the room code empty to create a new game
   - Or enter an existing room code to join a friend's game

2. **Share Room Code:**
   - After creating a room, share the room code with your friend
   - They can join by entering the same room code

3. **Play Chess:**
   - Click on a piece to select it
   - Click on a valid square to move
   - Chat with your opponent using the chat box
   - The game automatically detects checkmate, stalemate, and other end conditions

## Game Rules

- Standard chess rules apply
- White always moves first
- Automatic detection of:
  - Checkmate
  - Stalemate
  - Threefold repetition
  - Insufficient material

## Technical Details

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Backend:** Node.js with WebSocket server
- **Chess Engine:** chess.js library for move validation
- **Real-time Communication:** WebSocket protocol

## Development

To run in development mode with auto-restart:
```bash
npm run dev
```

## File Structure

```
├── Multi-chess.html    # Main game interface
├── server.js           # WebSocket server
├── package.json        # Node.js dependencies
├── simple-chess.html   # Original single-player version
└── README.md          # This file
```

## Troubleshooting

- **Connection issues:** Make sure the server is running on port 3000
- **Room not found:** Check that the room code is correct
- **Game not starting:** Ensure both players have joined the same room

## License

MIT License - feel free to modify and distribute! 