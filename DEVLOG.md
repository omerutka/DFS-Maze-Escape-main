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