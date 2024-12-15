# Network Congestion Analysis and Visualization

## Overview
This project analyzes the effects of congestion on network paths using **Dijkstra's Algorithm** and **Bellman-Ford Algorithm**. It simulates congestion scenarios and visualizes the network using the `pyvis` library for interactive graph representation.

The program evaluates how congestion on specific nodes impacts shortest path calculations and distances within a network. Three congestion scenarios are applied sequentially to demonstrate network performance degradation.

## Features
1. **Pathfinding Algorithms**:
   - Dijkstra's Algorithm: For shortest path calculations without negative edge weights.
   - Bellman-Ford Algorithm: Handles graphs with negative weights and detects negative-weight cycles.
2. **Congestion Simulation**:
   - Three scenarios of congestion applied to specific nodes, increasing edge weights.
   - Models real-world scenarios like traffic or data congestion.
3. **Interactive Visualization**:
   - Visualize the network and its changes using `pyvis`.
   - Generate interactive HTML files showing the network structure and edge weights before and after congestion.

## Prerequisites
Make sure the following tools and libraries are installed before running the project:

- **Python 3.x**
- **Required Libraries**:
   ```bash
   pip install pyvis numpy
   ```

## Project Structure
```
network_congestion_analysis/
|
|-- main.py                 # Main script with Dijkstra, Bellman-Ford, and congestion functions
|-- README.md               # Project documentation (this file)
|-- node.html               # Network visualization (initial graph)
|-- node1.html              # Visualization after Congestion Scenario 1
|-- node2.html              # Visualization after Congestion Scenario 2
|-- node3.html              # Visualization after Congestion Scenario 3
|-- outputs/                # (Optional) Store generated network HTML files
|
|-- utils/                  # (Optional) Helper modules (if added)
|-- requirements.txt        # List of required libraries
```

## Code Description
### Main Components
1. **Shortest Path Algorithms**:
   - `dijkstra(adjacency_matrix, start, end, num_nodes)`: Implements Dijkstra's algorithm.
   - `bellman_ford(adjacency_matrix, num_nodes, start, end)`: Implements Bellman-Ford algorithm.

2. **Congestion Functions**:
   - `apply_congestion_1()`: Adds weight to edges connected to node `n1`.
   - `apply_congestion_2()`: Adds weight to edges connected to node `n2`.
   - `apply_congestion_3()`: Adds weight to edges connected to node `n3`.

3. **Visualization**:
   - The `pyvis` library generates interactive network graphs for:
     - Initial graph structure.
     - Graphs after applying congestion scenarios 1, 2, and 3.

4. **Helper Functions**:
   - `create_network()`: Generates the network's edges.
   - `create_adjacency_matrix()`: Converts an edge list to an adjacency matrix.
   - `adjacency_matrix_to_edge_list()`: Converts an adjacency matrix back to an edge list.

### Execution Flow
1. **Initial Analysis**: Run Dijkstra and Bellman-Ford algorithms on the original graph.
2. **Congestion Scenarios**:
   - Sequentially apply congestion scenarios to specific nodes.
   - Observe how edge weights and paths are affected.
3. **Visualization**:
   - Generate interactive graphs for each scenario to understand changes visually.

### Visualization Files
After running the program, the following HTML files are generated:
- **node.html**: Initial network without congestion.
- **node1.html**: After Congestion Scenario 1.
- **node2.html**: After Congestion Scenario 2.
- **node3.html**: After Congestion Scenario 3.

Open these files in any web browser to interact with the graphs.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/network-congestion-analysis.git
   cd network-congestion-analysis
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the main script:
   ```bash
   python main.py
   ```

4. Open the generated HTML files (**node.html**, **node1.html**, **node2.html**, **node3.html**) in your browser to visualize the network.

## Results
- **Initial Graph**: Displays the network before any congestion is applied.
- **Scenario 1**: Congestion increases weights on edges connected to node `n1`.
- **Scenario 2**: Congestion increases weights on edges connected to node `n2`.
- **Scenario 3**: Congestion increases weights on edges connected to node `n3`.
- The shortest paths and distances adapt to these changes, demonstrating the network's sensitivity to congestion.

## Conclusion
This project demonstrates how network congestion impacts pathfinding algorithms and shortest paths. By applying congestion scenarios, the program showcases how edge weights influence routing decisions in a dynamic network.

## Future Work
- Introduce real-time dynamic congestion simulation.
- Implement additional pathfinding algorithms like A* or Floyd-Warshall.
- Use real-world datasets (e.g., traffic data) for more realistic simulations.
- Enhance visualizations with user controls to switch between scenarios interactively.

