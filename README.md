# Algorithm_Design
Building shortest path algrorithm

# 🔍 Shortest Path Finder (Dijkstra's Algorithm)

This Python script finds the shortest path between nodes in a weighted graph using **Dijkstra's algorithm**.

---

## 📌 Features

- Works on any connected, weighted graph (with positive weights)
- Prints shortest distance and path from a start node
- Optional: specify a target node to focus the output

---

## 🧠 How It Works

The graph is stored as a dictionary of nodes. Each node maps to a list of `(neighbor, weight)` tuples.

The `shortest_path()` function:
1. Initializes all distances to infinity, except the start node (0).
2. Repeatedly visits the closest unvisited node.
3. Updates the shortest paths and distances.
4. Stops when all nodes are visited.

---

## 📄 Example Graph

```python
my_graph = {
    'A': [('B', 5), ('C', 3), ('E', 11)],
    'B': [('A', 5), ('C', 1), ('F', 2)],
    'C': [('A', 3), ('B', 1), ('D', 1), ('E', 5)],
    'D': [('C', 1), ('E', 9), ('F', 3)],
    'E': [('A', 11), ('C', 5), ('D', 9)],
    'F': [('B', 2), ('D', 3)]
}
```
---

## 🧪 Usage
```python
shortest_path(my_graph, 'A', 'F')
```
This will output:
```less
A-F distance: 8
Path: A -> C -> B -> F
```
You can also call it without a target to show all shortest paths:

```python
shortest_path(my_graph, 'A')
```

---


## 🛠️ Requirements
Python 3.x

No external libraries required.

---


## ✅ Example Output
```less
A-F distance: 8
Path: A -> C -> B -> F
```

---

## 🚀 Future Improvements
As you gain more experience, consider adding:

- ✅ Use a priority queue (e.g. heapq) to optimize selection of the next node

- ✅ Add input validation (check if start/target nodes exist in the graph)

- ✅ Allow directed graphs or graphs with negative weights (using Bellman-Ford)

- ✅ Visualize the graph using networkx and matplotlib

- ✅ Turn the code into a class-based structure

- ✅ Create a web interface using Flask or Streamlit

- ✅ Handle disconnected graphs and unreachable nodes

- ✅ Add unit tests to make the function more robust

---


