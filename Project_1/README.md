Search.py:
• Proposal one of the nodes at the deepest level of the search tree.
• BFS Search: The search starts from the root of the tree and explores neighboring nodes
before moving on to the neighbors of the next level.
• Uniform Cost Search (UCS): Expands the frontier node with the lowest cost. UCS expands
nodes in order of increasing path cost, ensuring that the first goal node selected for
expansion is the optimal solution.
• A*: A best-first search algorithm using an evaluation function that combines heuristic and
actual costs. In this case, it is the estimated cost of the cheapest solution through node n.
searchAgents.py:
• getSuccessors:
• Returns a list of triples (successor, action, stepCost) for a given state.
• CornersHeuristic:
• Always returns a number, a lower bound of the shortest path from the state to the
goal node.
• nonvisited: Coordinates of unvisited food.
• currentpos: Current position of Pac-Man.
• distances: Stores Euclidean distances.
• If there is no food, it returns 0.
• Then, a loop calculates the distance from the current position to the food.
• Distances are sorted in ascending order.
• The Euclidean distance between the current position and the closest food is added to
the heuristic.
• The current position changes to the position of the closest food.
• If there is no more food, the heuristic is returned.
• Loop to calculate the Euclidean distance and position of the closest food.
• Distances are distributed in descending order.
• The Euclidean distance between the closest food and the farther food is added to the
heuristic.
• foodHeuristic:
• When reaching a goal state with no more food, the heuristic is 0.
• If all food in the current state is eaten, the heuristic is 0.
• If a food is eaten, return the distance to the last food.
• Find the Euclidean distance from the current state to the next nearest corner.
• Find the Euclidean distance between unexplored foods.
• If you find a minimum Euclidean distance between the next and current closest
foods, the next one becomes the current one in the next iteration, and the next one is
removed. Repeat until all food is eaten.
• The heuristic is the sum of distances between the current state and the closest food
and between the closest food and the remaining foods.
