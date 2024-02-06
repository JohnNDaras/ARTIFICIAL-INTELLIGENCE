**Search.py:** <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Proposal one of the nodes at the deepest level of the search tree. <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• BFS Search: The search starts from the root of the tree and explores neighboring nodes
before moving on to the neighbors of the next level.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Uniform Cost Search (UCS): Expands the frontier node with the lowest cost. UCS expands
nodes in order of increasing path cost, ensuring that the first goal node selected for
expansion is the optimal solution.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• A*: A best-first search algorithm using an evaluation function that combines heuristic and
actual costs. In this case, it is the estimated cost of the cheapest solution through node n.  <br>  <br>
**searchAgents.py:**  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**• getSuccessors:**  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Returns a list of triples (successor, action, stepCost) for a given state.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**• CornersHeuristic:**  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Always returns a number, a lower bound of the shortest path from the state to the
goal node.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• nonvisited: Coordinates of unvisited food.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• currentpos: Current position of Pac-Man.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• distances: Stores Euclidean distances.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• If there is no food, it returns 0.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Then, a loop calculates the distance from the current position to the food.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Distances are sorted in ascending order.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• The Euclidean distance between the current position and the closest food is added to
the heuristic.  <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• The current position changes to the position of the closest food.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• If there is no more food, the heuristic is returned.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Loop to calculate the Euclidean distance and position of the closest food.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Distances are distributed in descending order.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• The Euclidean distance between the closest food and the farther food is added to the
heuristic.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**• foodHeuristic:**  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• When reaching a goal state with no more food, the heuristic is 0.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• If all food in the current state is eaten, the heuristic is 0.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• If a food is eaten, return the distance to the last food.  <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Find the Euclidean distance from the current state to the next nearest corner.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Find the Euclidean distance between unexplored foods.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• If you find a minimum Euclidean distance between the next and current closest
foods, the next one becomes <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;the current one in the next iteration, and the next one is removed. Repeat until all food is eaten.  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• The heuristic is the sum of distances between the current state and the closest food <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;and between the closest food and the remaining foods.  <br>
