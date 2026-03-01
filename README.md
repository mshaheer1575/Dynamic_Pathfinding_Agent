# Dynamic_Pathfinding_Agent

1Introduction
This project is a Python GUI-based Pathfinding Simulator developed using Tkinter. It visualizes how artificial intelligence search algorithms find a path from a Start node to a Goal node in a grid environment that may contain obstacles.
Supported features:
•A* Search
•Greedy Best-First Search
•Manhattan & Euclidean heuristics
•Dynamic obstacle mode (real-time replanning)

2Algorithms Implemented
2.1A* Search
A* is an informed search algorithm that uses the evaluation function:

f (n) = g(n) + h(n)	(1)
where
•g(n) = cost from start node to current node n
•h(n) = heuristic estimate of cost from node n to goal
Properties:
✓Finds the optimal path (if heuristic is admissible)
✓More accurate and reliable

2.2Greedy Best-First Search
Greedy Best-First Search only uses the heuristic:

f (n) = h(n)	(2)
Properties:
✓Usually faster than A*
C Not guaranteed to find the optimal path

3Heuristics
Two common admissible heuristics are implemented:
•Manhattan Distance (L1 norm)
Best suited for 4-direction grid movement (up, down, left, right)
•Euclidean Distance (L2 norm)
Straight-line distance – suitable when diagonal movement is allowed

4Working of the System
1.User selects grid size and obstacle density
2.User places Start and Goal positions
3.Selected algorithm is executed and nodes are explored
4.Real-time visualization shows:
•Visited nodes
•Frontier / open-set nodes
•Final path (when found)
5.Performance metrics displayed:
•Number of nodes visited / expanded
•Total path cost
•Execution time (milliseconds)

5Dynamic Obstacle Mode
This mode simulates real-world robot navigation with unexpected changes:
•Agent begins moving along the calculated path
•Random obstacles may suddenly appear on the path
•If the current path becomes blocked → automatic replanning

•If no valid path exists after replanning → agent stops

This feature demonstrates real-time path adaptation — a key requirement in practical robotics and autonomous systems.

6Conclusion
The project successfully demonstrates core AI search algorithms through interactive visual- ization.
•A* provides optimal solutions (when using admissible heuristic)
•Greedy Best-First Search is faster but suboptimal
•Dynamic mode illustrates practical replanning under changing conditions

This simulator is well-suited for:
•AI / Algorithms laboratory assignments
•Teaching and demonstrating heuristic search concepts
•Understanding differences between optimal and non-optimal search strategies
