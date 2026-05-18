# Small-walk-in-metro-and-tramway



**Problem to solve:**
As part of the Eco'Prepa plan, we neeed to develop an offline public transport route planner for Paris, Bordeaux, Lille, and Lyon that calculates the optimal path between any two stations based on travel time, including transfer penalties (120 seconds per transfer). The system must be generic: adding a new city requires only a new JSON data file, with no external APIs or automatic code generation tools.

**Team roles:**

Alexandre : Team leader
Mathis : Scribe
Anne : Timekeeper
Raphaël : Activator
Axel : Secretary


**Core Functionality:**

Network data loading(read JSON files containing):
- Lines (name, color, ordered stations)
- Connections (departure, arrival, time, line)
- Transfers (station, lines, transfer time)
- a weighted graph from this data.
Current status: Not started


**Graph Traversal:**

we implemented BFS (fewest stops) and DFS (exploration) in order to verify if all stations are reachable by taking into account transfer stations


**Pathfinding:**

A Dijkstra’s algorithm is also used to: 

- calculate shortest path by travel time
-  Integrate 120-second transfer penalty
- Reconstruct and display the full route:

The pathfiding has to include severall informations : 

- Boarding station and line
- Intermediate stations
- Transfer points
- Alighting station and line
- Total travel time


**The interface:**

The interface works as a multi-city mapper where the user can choose different parameters to help him travelling through a city, it includes: 
- A city picker
- Departure and arrival station input (with error handling) 
- Clear, formatted route display with the pathfinding informations




**No optional features added to the code**

