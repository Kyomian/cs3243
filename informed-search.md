<h2>Informed Search</h2>

Exploit problem-specific knowledge; obtain heuristics to guide search

<b>Best-first Search</b>: Use function f(n) for each node n. Expand node with lowest f(n) first.

There are 2 types of best-first search: <b>greedy best-first search</b> and <b>A* Search</b>

<b>Greedy BFS</b>

f(n) = h(n) = Estimated cost of cheapest path from n to goal.

Complete? Yes, if b is finite. Optimal? No. Time complexity? O(b^m) Space complexity? O(b^m)
