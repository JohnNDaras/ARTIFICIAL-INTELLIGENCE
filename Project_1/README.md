Search.py: <br>
• Proposal one of the nodes at the deepest level of the search tree. <br>
• BFS Search: The search starts from the root of the tree and explores neighboring nodes
before moving on to the neighbors of the next level.  <br>
• Uniform Cost Search (UCS): Expands the frontier node with the lowest cost. UCS expands
nodes in order of increasing path cost, ensuring that the first goal node selected for
expansion is the optimal solution.  <br>
• A*: A best-first search algorithm using an evaluation function that combines heuristic and
actual costs. In this case, it is the estimated cost of the cheapest solution through node n.  <br>  <br>
searchAgents.py:  <br>
• getSuccessors:  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Returns a list of triples (successor, action, stepCost) for a given state.  <br>
• CornersHeuristic:  <br>
• Always returns a number, a lower bound of the shortest path from the state to the
goal node.  <br>
• nonvisited: Coordinates of unvisited food.  <br>
• currentpos: Current position of Pac-Man.  <br>
• distances: Stores Euclidean distances.  <br>
• If there is no food, it returns 0.  <br>
• Then, a loop calculates the distance from the current position to the food.  <br>
• Distances are sorted in ascending order.  <br>
• The Euclidean distance between the current position and the closest food is added to
the heuristic.  <br> 
• The current position changes to the position of the closest food.  <br>
• If there is no more food, the heuristic is returned.  <br>
• Loop to calculate the Euclidean distance and position of the closest food.  <br>
• Distances are distributed in descending order.  <br>
• The Euclidean distance between the closest food and the farther food is added to the  <br>
heuristic.  <br>
• foodHeuristic:  <br>
• When reaching a goal state with no more food, the heuristic is 0.  <br>
• If all food in the current state is eaten, the heuristic is 0.  <br>
• If a food is eaten, return the distance to the last food.  <br> 
• Find the Euclidean distance from the current state to the next nearest corner.  <br>
• Find the Euclidean distance between unexplored foods.  <br>
• If you find a minimum Euclidean distance between the next and current closest  <br>
foods, the next one becomes the current one in the next iteration, and the next one is
removed. Repeat until all food is eaten.  <br>
• The heuristic is the sum of distances between the current state and the closest food
and between the closest food and the remaining foods.  <br>
