# Patel-Kashyap-Kalpeshkumar_21BCE0216
A turn-based chess-like game developed with server-client architecture utilizing websockets for real-time communication. Created as a submission for Hitwicket's recruitment challenge.
# Chess-like Game Project

I apologize for the late changes into the README.md. By mistake i need to make one change that's why i have to Re-commit it for the proper working. As i haven't made any changes into codes please do consider.Here's a comprehensive README file for the Chess-like Game project, including detailed step-by-step instructions on how to install all dependencies and set up the project properly.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Project Structure](#project-structure)
5. [Running the Application](#running-the-application)
6. [Game Rules](#game-rules)
7. [Troubleshooting](#troubleshooting)

## Project Overview

This project is a web-based implementation of a chess-like game played on a 5x5 grid. It features real-time multiplayer gameplay using WebSocket communication.

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- Node.js (version 12.0 or higher)
- npm (usually comes with Node.js)

You can check your Node.js and npm versions by running:
```
node --version
npm --version
```

## Installation

Follow these steps to set up the project:

1. Create a new directory for your project and navigate into it:
   ```
   mkdir chess-like-game
   cd chess-like-game
   ```

2. Initialize a new Node.js project:
   ```
   npm init -y
   ```

3. Install the required dependencies:
   ```
   npm install express socket.io
   ```

4. Create the necessary files for the project:
   ```
   mkdir public
   touch server.js
   touch public/index.html
   touch public/styles.css
   touch public/game.js
   ```

5. Open `package.json` and modify it to include the start script:
   ```json
   {
     "name": "chess-like-game",
     "version": "1.0.0",
     "description": "A web-based chess-like game",
     "main": "server.js",
     "scripts": {
       "start": "node server.js"
     },
     "dependencies": {
       "express": "^4.17.1",
       "socket.io": "^4.0.0"
     }
   }
   ```

6. Copy the provided server code into `server.js`.

7. Copy the provided HTML code into `public/index.html`.

8. Copy the provided CSS code into `public/styles.css`.

9. Copy the provided client-side JavaScript code into `public/game.js`.

## Project Structure

After following the installation steps, your project structure should look like this:

```
chess-like-game/
│
├── public/
│   ├── index.html
│   ├── styles.css
│   └── game.js
│
├── server.js
├── package.json
└── package-lock.json
```

## Running the Application

1. Start the server by running:
   ```
   npm start
   ```
   or
   ```
   node server.js
   ```

2. Open a web browser and navigate to `http://localhost:3000` (or the port specified in your server configuration).

3. You should see the game interface. Open the game in two different browser windows to play as both players.

## Game Rules

- The game is played on a 5x5 grid.
- Each player controls a team of 5 characters: Pawns, Hero1, Hero2, and Hero3.
- Players take turns moving their pieces.
- Pieces have different movement patterns:
  - Pawn (P): Moves 1 step in any direction
  - Hero1 (H1): Moves up to 2 steps in any direction (↑ ↓ ← →)
  - Hero2 (H2): Moves up to 2 steps diagonally (↖ ↗ ↙ ↘)
  - Hero3 (H3): Moves up to 3 steps in any direction
- Capturing occurs when a piece moves to a square occupied by an opponent's piece.
- The game ends when one player eliminates all of their opponent's heroes or after 100 moves.

## Troubleshooting

- If you encounter any issues with WebSocket connections, ensure that your firewall is not blocking the connection.
- For any "module not found" errors, make sure you've run `npm install` and that all dependencies are correctly listed in your `package.json` file.
- If the server fails to start, check if the specified port (default 3000) is already in use by another application.
- If styles are not applying, make sure the path to your CSS file in the HTML is correct and that the server is correctly serving static files.
- If client-side JavaScript is not working, check the browser's console for any error messages and ensure the path to your JS file in the HTML is correct.
