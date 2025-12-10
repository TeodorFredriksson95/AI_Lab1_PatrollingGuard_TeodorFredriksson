# Lab 2 – Checkpoint Questions

## 1.1 Grid Basics

### 1. In your own words, what is a node and what is an edge in this grid?
Describe what a grid tile represents as a node, and what connections between tiles represent as edges.

**Answer:**  
---

### 2. How does the grid coordinate `(x, y)` map to world position `(x * cellSize, z * cellSize)`?
Explain the relationship between the grid indices and Unity world positions.

**Answer:**  
---

### 3. What happens if you try to access `nodes[x, y]` with coordinates outside the array bounds?
How can you prevent errors when accessing nodes?

**Answer:**  
---

## 1.2 Walkability & Toggling Tiles

### 4. What Unity function do you use to convert a screen position to a 3D ray?
Explain how raycasting detects which tile is clicked.

**Answer:**  
---

### 5. Why is it useful to visualize walkable vs non-walkable tiles?
What does this help you understand when debugging the grid or pathfinding?

**Answer:**  
---

### 6. In graph terms, what does toggling a tile to a wall represent?
How does changing a tile’s walkability affect the node and its edges?

**Answer:**  
---

## 1.3 A* Pathfinding

### 7. In your code, where do you compute `g(n)`, `h(n)`, and `f(n)`?
Identify where in the algorithm each of these values is updated.

**Answer:**  
---

### 8. Why do we check `tentativeG < neighbour.gCost`?
Explain why this comparison is necessary when exploring neighbours.

**Answer:**  
---

### 9. What happens if your heuristic overestimates the true distance?
How does it affect the correctness of the path found by A*?

**Answer:**  
---

### 10. If you set `h(n) = 0` for all nodes, what classic algorithm does A* become?

**Answer:**  
---

### 11. If you ignore `g(n)` completely and only sort by `h(n)`, what behavior do you expect to see?

**Answer:**  
---

## 1.4 Agent Movement

### 12. What is the difference between computing a path and moving along a path?

**Answer:**  
---

### 13. What happens in your movement code if there is no valid path (FindPath returns null)?
How should this case be handled?

**Answer:**  
---

## 1.5 Dynamic Targets

### 14. If the goal (player) can move, how often should you recompute the path?
What trade-offs appear?

**Answer:**  
---

### 15. What happens if the player moves into a location that is currently unreachable due to walls?
How could you detect and handle that?

**Answer:**  
---

## 1.6 Reflection & Theory

### 16. How is your grid + A* system conceptually similar to Unity’s NavMesh + NavMeshAgent from Lab 1?
How is it different?

**Answer:**  
---

### 17. In which situations would you prefer:
- A NavMesh with built-in pathfinding?  
- A custom grid-based A* like this?

**Answer:**  
---

### 18. Imagine a large RTS map with hundreds of units:
- What performance issues might appear with naive A* usage?  
- What strategies could reduce pathfinding cost?

**Answer:**  
---

### 19. How does diagonal movement (8-neighbour) change the shape of paths?
How do you ensure the heuristic remains admissible?

**Answer:**  
---

### 20. If you introduce different terrain costs (road, mud, water), how should the algorithm handle this?
How could you encode danger (e.g., enemy vision tiles) as a cost?

**Answer:**  
---

### 21. How does handling multiple agents affect pathfinding and movement?
How could you implement simple avoidance?

**Answer:**  
---
