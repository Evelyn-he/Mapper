# Mapper

## Notable Contributions

### Bucketing
Designed a recursive bucketing scheme that creates grids at power-of-two layers, efficiently building up from lower-to-higher grid buckets and removing unneccesssary information at each layer. Only features contained in sections of a grid in the current bounds of the screen are computed, decreasing the overall draw time of the map by an order of magnitude.

### Fastest-path computations
For paths between intersections, made use of an A* algorithm in conjunction with a min heap

## Key Words
* A *, Multi-Destination Dijkstra 
* Multi-start, Greedy, 2-opt, 3-opt, simulated annealing
* gtk, ezgl, glade
