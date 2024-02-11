<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Search Algorithms README</title>
</head>
<body>

<h1>search.py</h1>

<p>This module implements generic search algorithms that are utilized by Pacman agents in searchAgents.py.</p>

<h4>Class: SearchProblem</h4>

<p>This class outlines the structure of a search problem. It serves as an abstract class and does not implement any methods.</p>

<ul>
  <li><code>getStartState(self)</code>: Returns the start state for the search problem.</li>
  <li><code>isGoalState(self, state)</code>: Returns True if and only if the state is a valid goal state.</li>
  <li><code>getSuccessors(self, state)</code>: Returns a list of triples, where each triple represents a successor state, an action required to reach it, and the incremental cost of expanding to that successor.</li>
  <li><code>getCostOfActions(self, actions)</code>: Returns the total cost of a particular sequence of actions.</li>
</ul>

<h4>Function: tinyMazeSearch(problem)</h4>

<p>Returns a sequence of moves that solves a specific maze (tinyMaze). Note that this function is specific to a particular maze and should not be used for other mazes.</p>

<h4>Function: depthFirstSearch(problem)</h4>

<p>Searches the deepest nodes in the search tree first. This algorithm returns a list of actions that reaches the goal. It uses a graph search algorithm and implements depth-first search.</p>

<h4>Function: breadthFirstSearch(problem)</h4>

<p>Searches the shallowest nodes in the search tree first. It returns a list of actions that reaches the goal and utilizes a graph search algorithm with breadth-first search.</p>

<h4>Function: uniformCostSearch(problem)</h4>

<p>Searches the node of least total cost first. It returns a list of actions that reaches the goal and utilizes a graph search algorithm with uniform cost search.</p>

<h4>Function: nullHeuristic(state, problem=None)</h4>

<p>This is a trivial heuristic function that estimates the cost from the current state to the nearest goal in the provided SearchProblem. It always returns 0.</p>

<h4>Function: aStarSearch(problem, heuristic=nullHeuristic)</h4>

<p>Searches the node that has the lowest combined cost and heuristic first. It returns a list of actions that reaches the goal and utilizes the A* search algorithm, where the heuristic parameter is used to calculate the heuristic cost.</p>

<h1>searchAgents.py</h1>

<p>This file contains agents that control Pacman. The agents use various search algorithms to find paths through the maze.</p>

<h4>Class: GoWestAgent</h4>

<p>An agent that moves west until it cannot move further west. It's a simple demonstration agent.</p>

<h4>Class: SearchAgent</h4>

<p>A general search agent that finds a path using a supplied search algorithm for a supplied search problem. It supports different search algorithms like depth-first search (dfs) and breadth-first search (bfs).</p>

<h4>Class: StayEastSearchAgent</h4>

<p>An agent for position search with a cost function that penalizes being on the west side of the board.</p>

<h4>Class: StayWestSearchAgent</h4>

<p>An agent for position search with a cost function that penalizes being on the east side of the board.</p>

<h4>Function: manhattanHeuristic(position, problem)</h4>

<p>A heuristic function that calculates the Manhattan distance between the current position and the goal in a PositionSearchProblem.</p>

<h4>Class: CornersProblem</h4>

<p>A search problem that finds paths through all four corners of a layout. It defines the state space, start state, goal test, successor function, and cost function.</p>

<h4>Function: cornersHeuristic(state, problem)</h4>

<p>A heuristic for the CornersProblem that estimates the shortest path from the state to a goal. It's admissible and consistent.</p>

<h4>Class: AStarCornersAgent</h4>

<p>A search agent for the CornersProblem that uses the A* algorithm with the corners heuristic.</p>

<h4>Class: FoodSearchProblem</h4>

<p>A search problem associated with finding a path that collects all the food (dots) in a Pacman game. It defines the start state, goal test, successor function, and cost function.</p>

<h4>Function: foodHeuristic(state, problem)</h4>

<p>A heuristic for the FoodSearchProblem that estimates the distance to the closest food and the sum of distances to all remaining food.</p>

<h4>Class: AStarFoodSearchAgent</h4>

<p>A search agent for the FoodSearchProblem that uses the A* algorithm with the food heuristic.</p>

<h4>Class: ClosestDotSearchAgent</h4>

<p>Searches for all food using a sequence of searches. It implements the findPathToClosestDot method to find a path to the closest dot.</p>

<h4>Class: AnyFoodSearchProblem</h4>

<p>A search problem for finding a path to any food. It inherits from the PositionSearchProblem and has a different goal test.</p>

<h4>Function: mazeDistance(point1, point2, gameState)</h4>

<p>Returns the maze distance between any two points using the search functions. It's a helper function for approximate search agents.</p>

</body>
</html>
