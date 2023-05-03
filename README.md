# Mapper

Built a Geographic Information System (GIS) software program that visualizes fastest-path and travelling courier (variant on travelling salesman) problems.

## Notable Contributions

### Bucketing
Designed a recursive bucketing scheme that creates grids at power-of-two layers, efficiently building up from lower-to-higher grid buckets and removing unneccesssary information at each layer. Only features contained in sections of a grid in the current bounds of the screen are computed, decreasing the overall draw time of the map by an order of magnitude.

![](https://github.com/Evelyn-he/Mapper/blob/main/grid_lines.gif)

### Fastest-path computations
For paths between intersections, made use of an A* algorithm in conjunction with a min heap

### Travelling Courier

* Multi-destination Dijkstra to pre-compute fastest paths between all nodes.
* Used Greedy algorithm and multistart to produce a number of preliminary solutions.
* Pertubated all preliminary solutions (using 2-opt, 3-opt, and smaller local swapping pertubations) in parallel with multithreading to produce faster path times.
* Used simulated annealing with hill climbing to find deeper local minima. 

## Key Words
* A *, Multi-Destination Dijkstra 
* Multi-start, Greedy, 2-opt, 3-opt, simulated annealing
* gtk, ezgl, glade
