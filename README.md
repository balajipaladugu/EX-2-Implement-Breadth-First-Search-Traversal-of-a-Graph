
# EX-2: Implement-Breadth-First-Search-Traversal-of-a-Graph

**Name:** 
VENKATA BALAJI

**Register Number:**
2305001024

### Aim:
To Implement Breadth First Search Traversal of a Graph using Python 3.

### Theory:
Breadth-First Traversal (or Search) for a graph is like the Breadth-First Traversal of a tree. The only catch here is that, unlike trees, graphs may contain cycles so that we may come to the same node again. To avoid processing a node more than once, we divide the vertices into two categories:

Visited

Not Visited

A Boolean visited array is used to mark the visited vertices. For simplicity, it is assumed that all vertices are reachable from the starting vertex. BFS uses a queue data structure for traversal.

**How does BFS work?**
Starting from the root, all the nodes at a particular level are visited first, and then the next level nodes are traversed until all the nodes are visited. To do this, a queue is used. All the adjacent unvisited nodes of the current level are pushed into the queue, and the current-level nodes are marked visited and popped from the queue. Illustration: Let us understand the working of the algorithm with the help of the following example. 

### Algorithm:

step 1: Construct a Graph with Nodes and Edges

Step 2: Breadth First Uses Queue and iterates through the Queue for Traversal.

Step 3: Insert a Start Node into the Queue.

Step 4: Find its Successors Or neighbors and Check whether the node is visited or not.

Step 5: If Not Visited, add it to the Queue. Else Continue.

Step 6: Iterate steps 4 and 5 until all nodes get visited, and there are no more unvisited nodes.

### Program:
```
def bfs(graph, start):
    visited = []  
    queue = [start]  

    while queue:
        node = queue.pop(0)  
        if node not in visited:
            visited.append(node)  
            queue.extend(graph.get(node, []))  

    return visited

graph = {}
n = int(input("Enter number of nodes: "))  

for _ in range(n):
    node = input("Enter node: ")
    neighbors = input(f"Enter neighbors of {node} (comma separated): ").split(",")
    graph[node] = [neighbor.strip() for neighbor in neighbors]  

start_node = input("Enter the starting node for BFS: ")


print("BFS Traversal Order:", bfs(graph, start_node))
```
### Input:

<img width="451" height="219" alt="Screenshot 2025-09-08 140349" src="https://github.com/user-attachments/assets/237c2348-9a2b-4426-9b77-15558f1e0e96" />

### Output:

<img width="476" height="23" alt="Screenshot 2025-09-08 140357" src="https://github.com/user-attachments/assets/d5a1a609-6330-4f0b-95ad-ba09107123b5" />


### Result:
Thus the program to implement bredth first search of a traversal graph has been executed successfully.
