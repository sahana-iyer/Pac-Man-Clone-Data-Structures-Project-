# Pac-Man Clone (Data Structures Project)
Project Overview
This project is a simplified Pac-Man clone built in C. The game features a 10x10 grid maze with walls, pellets, Pac-Man, and ghosts. The player controls Pac-Man to collect pellets and avoid ghosts, earning points while navigating the maze. The game is over when all pellets are collected or if Pac-Man loses all lives.

FEATURES
Maze Display: A 10x10 grid representing the game maze with walls, pellets, Pac-Man, and ghosts.
Dynamic Pellet Management: Pellets are tracked and removed from the maze upon collection, using a linked list.
Pac-Man and Ghost Movement: Pac-Man moves in response to player inputs, while ghosts move randomly within the maze.
Score and Life Tracking: Pac-Man’s score increases as pellets are consumed, and lives decrease if caught by a ghost.

DATA STRUCUTES USED
2D Array (maze[ROWS][COLS]): Used to represent the maze layout, with each cell storing a character (wall, pellet, Pac-Man, ghost, or empty space).
Struct (Position): Holds x and y coordinates for Pac-Man and ghosts.
Linked List (PelletNode): Stores the positions of all pellets in the maze. When Pac-Man collects a pellet, the node for that position is removed from the list, enabling dynamic pellet management.
Queue (Queue): Tracks each ghost's recent positions to avoid excessive backtracking, providing a more realistic movement pattern for ghosts.
Array of Structs (Position ghosts[2]): Holds the positions of two ghosts within the maze.

CODE STRUCTURE
initializeMaze: Sets up the initial layout of the maze, placing walls, pellets, Pac-Man, and ghosts.
displayMaze: Outputs the maze to the console, showing Pac-Man's current position, remaining pellets, and ghost locations.
movePacman: Updates Pac-Man's position based on player input, checks for collisions with walls, pellets, and ghosts, and adjusts the score and life count.
moveGhosts: Moves ghosts randomly, using a queue to keep track of recent positions and prevent backtracking.
Pellet Management Functions: Manages the addition and removal of pellets in the maze through a linked list, updating the score upon pellet collection.

FUTURE ENHANCEMENTS
Advanced Ghost AI: Implement pathfinding algorithms (like A*) for more challenging ghost movement.
Power-Ups: Add power-ups that allow Pac-Man to temporarily eat ghosts.
