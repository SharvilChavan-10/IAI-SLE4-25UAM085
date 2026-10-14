# IAI-SLE4-25UAM085
SLE-4: Architecture Decision Record (ADR)

Course: 02AML204 — Introduction to Artificial Intelligence
Student: Sharvil S. Chavan
PRN: 25UAM085
Division: B
Date: 08 October 2026

📌 Project Overview

This project documents an important architectural decision for a Maze Solver System: selecting Breadth-First Search (BFS) as the primary search algorithm.

The decision is based on the experimental comparison of BFS and Depth-First Search (DFS) performed in SLE-2 and the system architecture documented in SLE-3.

The main objective is to find the shortest path from a starting cell to a goal cell in an unweighted grid maze.

🎯 Objectives

- Document the selection of BFS as the primary maze-solving algorithm.
- Compare BFS and DFS using execution time, nodes expanded, and path length.
- Explain the advantages, disadvantages, and trade-offs of the selected approach.
- Record alternative algorithms considered for future development.
- Maintain transparency regarding AI-assisted report preparation.

🧠 Algorithms Compared

1. Breadth-First Search (BFS)

- Uses a FIFO (First In, First Out) queue.
- Explores cells level by level.
- Guarantees the shortest path in an unweighted grid.
- Can require more time and memory than DFS in the tested cases.

2. Depth-First Search (DFS)

- Uses a LIFO (Last In, First Out) stack.
- Explores one path deeply before backtracking.
- Was faster in the experiments conducted.
- Does not guarantee the shortest path.

📊 Experimental Results

The algorithms were tested on three maze sizes, with five runs per algorithm and maze size.

Maze Size| BFS Time (ms)| DFS Time (ms)| BFS Path (cells)| DFS Path (cells)
20×20| 0.277| 0.088| 39| 79
40×40| 1.037| 0.380| 79| 193
70×70| 3.084| 0.664| 141| 379

Observation: DFS was faster in all three tested cases, but BFS produced shorter paths.

✅ Final Architecture Decision

BFS was selected as the primary search algorithm because shortest-path quality is the main requirement of the maze solver.

DFS is retained as a baseline for performance comparison.

A* Search with a Manhattan-distance heuristic is considered a potential future improvement for larger mazes.

🏗️ System Architecture

The maze-solving system contains the following major components:

- Maze Generator: Creates the maze, including walls, start, and goal cells.
- Experiment Driver: Runs the algorithms repeatedly for comparison.
- Search Engine: Executes BFS or DFS.
- Neighbour Generator: Identifies valid neighbouring cells.
- Frontier: Stores discovered cells waiting to be explored.
- Visited Set: Prevents repeated exploration.
- Parent Map: Supports path reconstruction.
- Result Reporter: Records timings and organizes results.
- Output Module: Presents the path and performance measurements.

BFS and DFS share the same supporting components; their primary difference is the Frontier data structure.

⚖️ Advantages and Trade-offs

Advantages of BFS

- Guarantees a shortest path in an unweighted grid.
- Uses a straightforward and testable design.
- Supports consistent comparisons with DFS.

Limitations of BFS

- Was slower than DFS in the tested cases.
- May require substantial memory for larger mazes.
- Does not guarantee minimum total cost when moves have different costs.

🤖 AI Contribution

Claude was used to assist with ADR organization, drafting explanations, calculating comparison ratios, and preparing viva questions.

The student reviewed the reported values against the earlier SLE-2 results and verified the architecture terminology against the SLE-3 documentation.

For more information, see ""Contribution_Log.md"" (Contribution_Log.md).

📚 SLE Learning Journey

- SLE-1: Developed a basic rule-based AI Study Assistant and maintained an AI Contribution Log.
- SLE-2: Implemented and profiled BFS and DFS on different maze sizes.
- SLE-3: Documented the maze solver architecture using the C4 model.
- SLE-4: Recorded and justified the decision to use BFS as the primary search strategy.

🔮 Future Improvements

- Implement A* Search using a Manhattan-distance heuristic.
- Compare BFS, DFS, and A* using the same maze layouts.
- Measure memory consumption in addition to execution time.
- Test more maze layouts and larger grid sizes.

📁 Repository Contents

- "README.md" — Project overview and decision summary.
- "Contribution_Log.md" — Documentation of AI assistance and human verification.
- ADR report — The SLE-4 architecture decision document, if included in the repository.

👨‍🎓 Student Information

Name: Sharvil S. Chavan
PRN: 25UAM085
Department: CSE (AI & ML)
Course: 02AML204 — Introduction to Artificial Intelligence

Conclusion: BFS was selected because the shortest path is more important than execution speed alone for this maze-solving project.
