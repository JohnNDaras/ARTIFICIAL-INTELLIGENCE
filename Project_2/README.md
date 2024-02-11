<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<p>The computational intelligence component of the entire codebase is outlined below:</p>
<h1>multiAgents.py</h1>

<p>This module contains implementations of different types of agents for playing Pacman. Below is an explanation of each function and class within the module:</p>

<h2>ReflexAgent class</h2>

<ul>
  <li><strong>getAction(self, gameState):</strong>
    <ul>
      <li>This method implements a reflex agent, which chooses an action at each choice point based on evaluating its alternatives via a state evaluation function.</li>
      <li>It collects legal moves and successor states, calculates scores for each move based on the evaluation function, and returns the best action to take.</li>
    </ul>
  </li>
  
  <li><strong>evaluationFunction(self, currentGameState, action):</strong>
    <ul>
      <li>This method defines a basic evaluation function for the reflex agent.</li>
      <li>It takes in the current and proposed successor GameStates, extracts useful information, such as remaining food, Pacman position after moving, ghost positions, and calculates a score based on these factors.</li>
    </ul>
  </li>
</ul>

<h2>scoreEvaluationFunction function</h2>

<ul>
  <li><strong>scoreEvaluationFunction(currentGameState):</strong>
    <ul>
      <li>This function serves as a default evaluation function that returns the score of the state.</li>
      <li>It's intended for use with adversarial search agents (not reflex agents).</li>
    </ul>
  </li>
</ul>

<h2>MultiAgentSearchAgent class</h2>

<ul>
  <li><strong>__init__(self, evalFn = 'scoreEvaluationFunction', depth = '2'):</strong>
    <ul>
      <li>Constructor for the MultiAgentSearchAgent class.</li>
      <li>It initializes the evaluation function and depth parameters for the agent.</li>
    </ul>
  </li>
</ul>

<h2>MinimaxAgent class</h2>

<ul>
  <li><strong>getAction(self, gameState):</strong>
    <ul>
      <li>This method implements a Minimax agent, which computes the minimax action from the current gameState using depth and evaluationFunction.</li>
      <li>It utilizes minimax algorithm to find the best action for Pacman to take considering the actions of the ghosts.</li>
    </ul>
  </li>
</ul>

<h2>AlphaBetaAgent class</h2>

<ul>
  <li><strong>getAction(self, gameState):</strong>
    <ul>
      <li>This method implements a Minimax agent with alpha-beta pruning, which is a more efficient variant of the minimax algorithm.</li>
      <li>It uses alpha-beta pruning to search through the game tree and find the best action for Pacman.</li>
    </ul>
  </li>
</ul>

<h2>ExpectimaxAgent class</h2>

<ul>
  <li><strong>getAction(self, gameState):</strong>
    <ul>
      <li>This method implements an Expectimax agent, which computes the expectimax action using depth and evaluationFunction.</li>
      <li>It considers all possible actions for Pacman and the stochastic actions of ghosts, selecting the action with the highest expected value.</li>
    </ul>
  </li>
</ul>

<h2>betterEvaluationFunction function</h2>

<ul>
  <li><strong>betterEvaluationFunction(currentGameState):</strong>
    <ul>
      <li>This function defines an improved evaluation function for Pacman.</li>
      <li>It takes into account various factors such as distance to food, proximity to ghosts, and scared ghosts to calculate a better evaluation score.</li>
    </ul>
  </li>
</ul>

<h2>Abbreviation</h2>

<ul>
  <li><strong>better:</strong>
    <ul>
      <li>Abbreviation for the <code>betterEvaluationFunction</code> function.</li>
    </ul>
  </li>
</ul>

</body>
</html>
