<div align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:5e60ce,100:7400b8&height=300&section=header&text=Chess-like%20Game&fontSize=90&fontColor=fff&animation=fadeIn&fontAlignY=38&desc=Turn-based%20Tactical%20Strategy%20with%20WebSockets&descAlignY=60&descSize=20" width="100%"/> </div> <div align="center"> <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=30&duration=3000&pause=1000&color=6930C3&center=true&vCenter=true&random=false&width=600&lines=Real-time+Multiplayer+Gameplay;Strategic+Chess-like+Battles;WebSocket+Communication;5x5+Grid+Tactical+Combat" alt="Typing SVG" /> </div> <p align="center">  </p> <div align="center"> <a href="#%EF%B8%8F-project-overview"> <img src="https://img.shields.io/badge/Overview-5E60CE?style=for-the-badge&logo=opsgenie&logoColor=white" alt="Overview"/> </a> <a href="#-features"> <img src="https://img.shields.io/badge/Features-7400B8?style=for-the-badge&logo=feathub&logoColor=white" alt="Features"/> </a> <a href="#-prerequisites"> <img src="https://img.shields.io/badge/Prerequisites-6930C3?style=for-the-badge&logo=pnpm&logoColor=white" alt="Prerequisites"/> </a> <a href="#-installation"> <img src="https://img.shields.io/badge/Installation-5390D9?style=for-the-badge&logo=instructure&logoColor=white" alt="Installation"/> </a> <a href="#-game-rules"> <img src="https://img.shields.io/badge/Game_Rules-4EA8DE?style=for-the-badge&logo=bookstack&logoColor=white" alt="Game Rules"/> </a> <a href="#-troubleshooting"> <img src="https://img.shields.io/badge/Troubleshooting-48BFE3?style=for-the-badge&logo=sentry&logoColor=white" alt="Troubleshooting"/> </a> </div> <div align="center"> <img src="https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js"/> <img src="https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB" alt="Express.js"/> <img src="https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101" alt="Socket.io"/> <img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E" alt="JavaScript"/> <img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/> <img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/> </div>

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
