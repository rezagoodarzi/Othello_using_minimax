# Othello Game
## Table of Contents
- `1` Player and Game Classes
- `2`Player Implementations
- `3` HumanPlayer
- `4` RandomAgent
- `5` MinimaxAgent
- `6` AlphaBeta
- `7` State Class
- `8` OthelloMove Class
- `9` Creating Players
- `10`  Running the Game

1. Player and Game Classes <a name="player-and-game-classes"></a>
- Player Class
The Player class serves as an abstract base class for different player implementations. It declares an abstract method choose_move, which should be implemented by its subclasses.


- Game Class
The Game class represents the Othello game. It takes an initial game state, player1, and player2 as input. The play method runs the game loop, allowing players to take turns until the game is over. The current state is displayed in the console after each move.

2. Player Implementations <a name="player-implementations"></a>
- HumanPlayer
The HumanPlayer class is a subclass of Player. It allows a human player to input moves through the console. The choose_move method generates a list of legal moves and prompts the user to choose one.

- RandomAgent
The RandomAgent class is a subclass of Player. It makes random moves by selecting a move from the list of legal moves.

- MinimaxAgent
The MinimaxAgent class is a subclass of Player that implements the minimax algorithm. It evaluates possible moves up to a specified depth using a recursive approach and selects the move with the highest evaluated score.

- AlphaBeta
The AlphaBeta class is a subclass of Player that implements the alpha-beta pruning algorithm. It improves upon the minimax algorithm by reducing the number of nodes evaluated. This leads to more efficient decision-making, especially in deeper search spaces.
3. State Class <a name="state-class"></a>
- The State class represents the game state, including the game board, its size, and the player to move. It provides methods for generating legal moves, applying moves, and checking the game's completion.
4. OthelloMove Class <a name="othellomove-class"></a>
The OthelloMove class encapsulates a move in the Othello game. It includes information about the player making the move and the move's coordinates on the game board.

5. Creating Players <a name="creating-players"></a>
The create_player function creates player instances based on the input arguments. It supports creating human players, random agents, minimax agents, and alpha-beta agents.

6. Running the Game <a name="running-the-game"></a>
The main section of the script initializes the Othello game with an initial state and two agents (minimax and alpha-beta). The game is then played, and the final winner is displayed in the console.

To run the game with different player configurations, command-line arguments can be provided. The get_arg function retrieves command-line arguments, allowing users to specify player types and depths or times for the search algorithms.