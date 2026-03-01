Dynamic Pathfinding Agent (AI Assignment – Q6)
Project Overview

This project implements a **Dynamic Pathfinding Agent** in a grid-based environment using:
* Greedy Best-First Search (GBFS)
* A* Search Algorithm
* Dynamic obstacle spawning with real-time re-planning
* Graphical visualization using **Pygame**

The agent navigates from a fixed Start node to a Goal node while obstacles may appear randomly during motion.
Features Implemented

* Dynamic grid environment (custom rows × columns)
* Random obstacle generation with adjustable density
* Interactive algorithm selection (A* / GBFS)
* Two heuristic options:

  * Manhattan Distance
  * Euclidean Distance
* Dynamic obstacle spawning during execution
* Automatic re-planning when path gets blocked
* GUI visualization:

  * Start node (Blue)
  * Goal node (Red)
  * Obstacles (Black)
  * Final Path (Green)
* Real-time metrics:

  * Nodes Visited
  * Path Cost
  * Execution Time (ms)

Algorithms Used

1. Greedy Best-First Search (GBFS)

Uses only heuristic:
f(n) = h(n)

Fast but not guaranteed optimal.

2. A* Search

Uses combined cost:
f(n) = g(n) + h(n)

Guaranteed optimal if heuristic is admissible and consistent.
Heuristic Functions

 Manhattan Distance

h(n) = |x1 - x2| + |y1 - y2|

Euclidean Distance

h(n) = √((x1 - x2)^2 + (y1 - y2)^2)
 Dynamic Re-Planning Logic

1. Agent computes path using selected algorithm.
2. During movement, new obstacles may spawn randomly.
3. If an obstacle blocks the current path:

   * Agent detects collision
   * Re-runs search from current position
4. This simulates real-world navigation in changing environments.

Installation & Setup

Step 1: Install Dependencies

pip install pygame
 Step 2: Run the Program

python dynamic_pathfinding.py

Controls

| Key | Function                     |
| --- | ---------------------------- |
| A   | Run A* Search                |
| G   | Run Greedy Best-First Search |
| M   | Use Manhattan Heuristic      |
| E   | Use Euclidean Heuristic      |
| R   | Reset and generate new map   |

Output Metrics

The GUI displays:

* Total Nodes Visited
* Path Cost
* Execution Time (milliseconds)

Test Cases (For Report)

Include screenshots for:

1. Best Case Scenario – minimal obstacles, fast path
2. Worst Case Scenario – dense obstacles, more expansions

Pros & Cons

A* Search

✔ Optimal solution
✔ Handles dynamic replanning effectively
❌ Higher memory usage

Greedy Best-First Search

✔ Faster execution
✔ Simpler implementation
❌ Not optimal, may take wrong path

Repository Structure

dynamic_pathfinding.py   # Main GUI + algorithms
README.md                # Project documentation

Author

Muhammad Usman
BS Computer Science
AI 2002 – Assignment 2


* Start and Goal nodes remain fixed during execution.
* Re-planning occurs only when obstacle blocks the current path.
* Designed for educational demonstration of informed search in dynamic environments.
