
Campus Navigation: The "Maze Solver" Agent
The Problem
Imagine you are at the Hostel (S) and need to get to the AI Lab (G) for a morning class. The campus isn't just an empty field—there are buildings, walls, and restricted zones (#) in your path.
I built this Python-based "Problem-Solving Agent" to figure out the best way to navigate a 7x7 grid using two different types of "AI brains": BFS (Uninformed) and A* (Informed).
How the Agent "Thinks"
Algorithm	The Strategy	My Observation
BFS	"The Blind Wanderer"	It checks every single direction equally. It's guaranteed to find the shortest path, but it wastes a lot of energy looking at walls.
A Search*	"The Smart Navigator"	It uses a Heuristic (Manhattan Distance) to "sense" where the Goal is. It's much more efficient because it focuses on moving toward the target.
________________________________________
Real-World Results
When I ran the code on my campus map, here is how the agent performed:
•	Path Found: Yes (19 steps total).
•	Efficiency Win: While BFS had to "look" at 24 different coordinates, A* found the same path by only checking ~21 spots.
•	The Math: A* uses the evaluation function f(n) = g(n) + h(n) to stay on track.
Project Structure
•	src/solver.py: The core logic for the BFS and A* algorithms.
•	.gitignore: Keeps the repository clean by hiding temporary __pycache__ files.
How to Run the Solver
To test the agent on your own machine, follow these steps:
1.	Run the Script: Execute the main solver file from your terminal:
python src/solver.py
2.	Interpret the Map:
o	S = Hostel (Start)
o	G = AI Lab (Goal)
o	# = Buildings (Obstacles)
o	* = The path discovered by the AI!
Created by: Dhairya Jaiswal (25BAI10441)
Course: B.Tech in Artificial Intelligence & Machine Learning

