# All Paths From Source to Target - W13D1

## Problem Statement

Given a directed acyclic graph (DAG), find all possible paths from node `0` to node `n - 1` and return them in any order. Each node is labeled from `0` to `n - 1` and graph is represented as a neighboring list.

## Approach

1. Depth-First Search (DFS) - DFS used to explore all possible paths from source node `0` to target node `n-1`.
2. Recursion - Recursive function `dfs(node, path)` checks all neighbors of current node and appends current path to result when target is reached.
3. Base Case - If current node is target, we add current path to result list.
4. Recursive Case - For each neighbor of current node, recursively call `dfs` function with neighbor and updated path.

## Solution

Initialize empty list `result` to store all paths and starting DFS from source node `0` with the initial path `[0]`.

## Optimization

- Time Complexity - O(2^n) in worst case, where n is number of nodes, because each node can have multiple paths leading to exponential growth in number of paths.
- Space Complexity - O(n) for recursion stack and path storage.
