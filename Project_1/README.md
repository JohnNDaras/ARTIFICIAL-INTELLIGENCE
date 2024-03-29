<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<p>The computational intelligence component of the entire codebase is outlined below:</p>

<h2>search.py</h2>

<p>This module implements generic search algorithms that are utilized by Pacman agents in searchAgents.py.</p>

<h3>Class: SearchProblem</h3>

<p>This class outlines the structure of a search problem. It serves as an abstract class and does not implement any methods.</p>

<ul>
  <li><code>getStartState(self)</code>: Returns the start state for the search problem.</li>
  <li><code>isGoalState(self, state)</code>: Returns True if and only if the state is a valid goal state.</li>
  <li><code>getSuccessors(self, state)</code>: Returns a list of triples, where each triple represents a successor state, an action required to reach it, and the incremental cost of expanding to that successor.</li>
  <li><code>getCostOfActions(self, actions)</code>: Returns the total cost of a particular sequence of actions.</li>
</ul>

<h3>Function: tinyMazeSearch(problem)</h3>

<p>Returns a sequence of moves that solves a specific maze (tinyMaze). Note that this function is specific to a particular maze and should not be used for other mazes.</p>

<h3>Function: depthFirstSearch(problem)</h3>

<p>Searches the deepest nodes in the search tree first. This algorithm returns a list of actions that reaches the goal. It uses a graph search algorithm and implements depth-first search.</p>

<h3>Function: breadthFirstSearch(problem)</h3>

<p>Searches the shallowest nodes in the search tree first. It returns a list of actions that reaches the goal and utilizes a graph search algorithm with breadth-first search.</p>

<h3>Function: uniformCostSearch(problem)</h3>

<p>Searches the node of least total cost first. It returns a list of actions that reaches the goal and utilizes a graph search algorithm with uniform cost search.</p>

<h3>Function: nullHeuristic(state, problem=None)</h3>

<p>This is a trivial heuristic function that estimates the cost from the current state to the nearest goal in the provided SearchProblem. It always returns 0.</p>

<h3>Function: aStarSearch(problem, heuristic=nullHeuristic)</h3>

<p>Searches the node that has the lowest combined cost and heuristic first. It returns a list of actions that reaches the goal and utilizes the A* search algorithm, where the heuristic parameter is used to calculate the heuristic cost.</p>

<h2>searchAgents.py</h2>

<p>This file contains agents that control Pacman. The agents use various search algorithms to find paths through the maze.</p>

<h3>Class: GoWestAgent</h3>

<p>An agent that moves west until it cannot move further west. It's a simple demonstration agent.</p>

<h3>Class: SearchAgent</h3>

<p>A general search agent that finds a path using a supplied search algorithm for a supplied search problem. It supports different search algorithms like depth-first search (dfs) and breadth-first search (bfs).</p>

<h3>Class: StayEastSearchAgent</h3>

<p>An agent for position search with a cost function that penalizes being on the west side of the board.</p>

<h3>Class: StayWestSearchAgent</h3>

<p>An agent for position search with a cost function that penalizes being on the east side of the board.</p>

<h3>Function: manhattanHeuristic(position, problem)</h3>

<p>A heuristic function that calculates the Manhattan distance between the current position and the goal in a PositionSearchProblem.</p>

<h3>Class: CornersProblem</h3>

<p>A search problem that finds paths through all four corners of a layout. It defines the state space, start state, goal test, successor function, and cost function.</p>

<h3>Function: cornersHeuristic(state, problem)</h3>

<p>A heuristic for the CornersProblem that estimates the shortest path from the state to a goal. It's admissible and consistent.</p>

<h3>Class: AStarCornersAgent</h3>

<p>A search agent for the CornersProblem that uses the A* algorithm with the corners heuristic.</p>

<h3>Class: FoodSearchProblem</h3>

<p>A search problem associated with finding a path that collects all the food (dots) in a Pacman game. It defines the start state, goal test, successor function, and cost function.</p>

<h3>Function: foodHeuristic(state, problem)</h3>

<p>A heuristic for the FoodSearchProblem that estimates the distance to the closest food and the sum of distances to all remaining food.</p>

<h3>Class: AStarFoodSearchAgent</h3>

<p>A search agent for the FoodSearchProblem that uses the A* algorithm with the food heuristic.</p>

<h3>Class: ClosestDotSearchAgent</h3>

<p>Searches for all food using a sequence of searches. It implements the findPathToClosestDot method to find a path to the closest dot.</p>

<h3>Class: AnyFoodSearchProblem</h3>

<p>A search problem for finding a path to any food. It inherits from the PositionSearchProblem and has a different goal test.</p>

<h3>Function: mazeDistance(point1, point2, gameState)</h3>

<p>Returns the maze distance between any two points using the search functions. It's a helper function for approximate search agents.</p>

</body>
</html>
