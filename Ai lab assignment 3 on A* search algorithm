[1011.py](https://github.com/user-attachments/files/23253165/1011.py)
import heapq

def a_star_search(graph, start, goal, heuristic):
    # Priority queue stores (f_score, current_node, path, g_cost)
    pq = []
    heapq.heappush(pq, (heuristic[start], start, [start], 0))  # f = g + h, here g=0 for start

    visited = set()  # Track visited nodes

    while pq:  # Continue while queue not empty
        (f, current, path, g) = heapq.heappop(pq)
        print(f"Visiting: {current} (f={f}, g={g}, h={heuristic[current]})")

        if current == goal:  # Goal reached
            return path, g  # Return both path and total cost
            #f(goal)=g(goal)+h(goal)=g(goal)+0=g(goal)

        if current in visited:
            continue
        visited.add(current)

        for neighbor, cost in graph[current].items():  # Each neighbor with travel cost
            if neighbor not in visited:
                g_new = g + cost  # Actual cost so far
                f_new = g_new + heuristic[neighbor]  # Total estimated cost
                heapq.heappush(pq, (f_new, neighbor, path + [neighbor], g_new))

    return None, float('inf')  # No path found


# ---- Example usage ----

# Step 1: Define a weighted graph (edges have costs)
graph = {
    'A': {'B': 6, 'F': 3},
    'B': {'A': 6, 'C': 3, 'D':2},
    'C': {'B': 3, 'D': 1, 'E': 5},
    'D': {'B': 2, 'C': 1},
    'E': {'C': 5, 'I': 5, 'J': 5},
    'F': {'A': 3, 'G': 1, 'H': 7},
    'G': { 'F': 1, 'I': 1},
    'H': {'F': 7, 'I': 2},
    'I': {'G': 3, 'H': 2, 'E': 5, 'J': 3},
    'J': {'E': 5, 'I': 3}
}



# Step 2: Define heuristic values (estimated cost to goal 'F')
# Typically Euclidean or straight-line distance to goal
heuristic = {
    'A': 10, 'B': 8, 'C': 5, 'D': 7, 'E': 3,
    'F': 6, 'G': 5, 'H': 3, 'I': 1, 'J': 0
}

#st=input()
#go=input()

# Step 3: Call the function
path, total_cost = a_star_search(graph, 'A', 'J', heuristic)

# Step 4: Print the result
print("Path found:", path)
print("Total cost:", total_cost)
