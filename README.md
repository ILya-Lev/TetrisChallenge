# TetrisChallenge

My solution for this challenge (https://github.com/AndreyM-DXC/TetrisChallenge).
A naive solution.
Imagine a piece is put onto the board what would be the metric for a given rotation and offset?

Thus everything is about how to calculate the metric:
 1. min weight of the system (pieces should be as low as possible)
 2. add penalty for covered holes
 3. add penalty for non-adjacent piece locations

Penalties are taken into the consideration for 4 rows in depth at most.
Not to prevent new pieces being stacked upon each other.

Holes penalty is multiplied by a magic number 2.1
Adjacent penalty is divided by a magic number - the width of the board
 (to show it's much less important than the holes penalty).

Current solution is not ideal, is quite volatile 
 (the best result so far is 615 score; average ~394 per run).

Potentially better solution would include taking a few more imaginary steps with all possible pieces
 and calculating the best possible metric over all these steps (i.e. min for the sum).
 
