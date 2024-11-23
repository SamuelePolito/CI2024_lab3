# N-Puzzle Solver

This repository contains an implementation of an N-Puzzle solver using various search algorithms, including Breadth-First Search (BFS), Depth-First Search (DFS), and A* search with Manhattan Distance as the heuristic.

### Search Algorithms
The implementation includes the following search algorithms:
- **Breadth-First Search (BFS)**: Guarantees finding the shortest solution but may take a lot of time and memory for larger puzzles.
- **Depth-First Search (DFS)**: Explores deeply first but may not find the optimal solution. A depth limit can be provided.
- **A* Search**: Uses the Manhattan Distance heuristic to find an optimal solution efficiently.

## Code Overview
### Constants
- `PUZZLE_DIM`: The dimension of the puzzle (e.g., 3 for an 8-puzzle).
- `GOAL_STATE`: The target configuration of the puzzle.

### Helper Functions
- `get_neighbors(state)`: Returns the possible moves from a given puzzle state.
- `shuffle_puzzle(goal_state, randomize_steps)`: Generates a random initial state by shuffling the goal state.
- `print_puzzle(state)`: Prints the current state of the puzzle in a grid format.

### Algorithms
- **BFS (`bfs_solve_puzzle`)**: Uses a queue to explore all possible states layer by layer.
- **A* (`a_star_solve_puzzle`)**: Uses a priority queue and the Manhattan Distance heuristic to find the shortest solution path.
- **DFS (`dfs_solve_puzzle`)**: Uses a stack to explore paths deeply. A depth limit can be set to restrict the search.

## Example Output
After running the script, the following output is generated:
- Initial state and goal state of the puzzle.
- Solution paths for BFS, A*, and DFS (if found).
- Length of the solution paths.
- Additional analysis on the nodes explored by each algorithm.

Example:
```
Initial state:
(0, 1, 4)
(5, 8, 3)
(2, 7, 6)

Goal state:
(1, 2, 3)
(4, 5, 6)
(7, 8, 0)

BFS Solution Length: 18
A* Solution Length: 18
DFS Solution Length: No solution found
```

## License
This project is licensed under the MIT License.

