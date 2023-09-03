# TetrisChallenge

naive solution
imagine a piece is put onto the board what would be the metric for a given rotation and offset?

thus everything is about how to calculate the metric
 1. min weight of the system (pieces should be as low as possible)
 2. add penalty for covered holes
 3. add penalty for non-adjacent piece locations

 penalties are taken into the consideration for 4 rows in depth at most
 not to prevent new pieces being stacked upon each other

 holes penalty is multiplied by a magic number 2.1
 adjacent penalty is divided by a magic number - the width of the board
 (to show it's much less important than the holes penalty)

 current solution is not ideal, is quite volatile 
 (the best result so far is 615 score; average ~394 per run)
 
