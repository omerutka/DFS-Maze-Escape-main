# DEVLOG
## DFS Maze Escape

### Entry 1
**Date:** 4/16/2026

This is the base case for DFS since I added the out of bounds check and the
wall check. It's a small implementation but very important in order to
avoid runtime errors and to make sure the recursion happens correctly. I
also added CMakeLists.txt because it wasn't implemented when I forked.

### Entry 2
**Date:** 4/20/2026

When I was implementing the recursive neighbor traversal, I struggled 
understanding how the return value propagates back through the recursive
calls. I realized that returning true immediately when a recursive call 
succeeds allows the algorithm to unwind correctly.

### Entry 3
**Date:** 4/22/2026

When I initially added parent tracking, I put the parent assignment 
outside the checks for validity, which caused incorrect paths to be 
recorded. This led to issues when reconstructing the path, which then 
led to broken sequences. I fixed this by making sure parent coordinates 
are only assigned for valid, unvisited neighboring cells before recursion.

### Entry 4
**Date:** 4/25/2026

I mainly just added comments here since I'm not the best at adding them
in the moment. I also added an explicit bounds check at the top of DFS 
to guard against any out of bounds access before touching the maze array.

### Entry 5
**Date:** 4/27/2026

I was thinking about edge cases and realized a 1x1 input would cause the
entrance/exit selection loop to spin forever since both can't be different
cells. Not sure why anyone would run a 1x1 maze, but added a quick check
to catch it and exit with a message.

## Entry 6
**Date:** 4/29/2026

On my final commit, I focused on testing the program with multiple maze 
sizes to make sure the DFS implementation did fine when there was a path 
and when there was not a path. This helped confirm that the recursion, 
visited tracking, and parent reconstruction were all working together 
as intended. I also cleaned up the edge case validation by combining 
the dimension checks into a single if statement.