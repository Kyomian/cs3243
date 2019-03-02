<h2>Informed Search</h2>

Exploit problem-specific knowledge; obtain heuristics to guide search

<b>Best-first Search</b>: Use function f(n) for each node n. Expand node with lowest f(n) first.

There are 2 types of best-first search: <b>greedy best-first search</b> and <b>A* Search</b>

<b>Greedy BFS</b>

f(n) = h(n) = Estimated cost of cheapest path from n to goal.

Complete? Yes, if b is finite. Optimal? No. Time complexity? O(b^m) Space complexity? O(b^m)

<b>QNS</b>: Why is greedy best-first search not optimal? What info does it ignore?<br>
<b>ANS</b>: how far it is from the start; it only takes into account of how far it is from the goal...

<b>A* Search</b>

f(n) = g(n) + h(n). g(n) = <i>true</i> cost of reaching n from start node. h(n) = cost estimate from n to goal.

IMPT: A* Search will stop only when (a)goal is reached <b>AND</b> (b) f(goal) is lowest among the frontier

<h2>Theorems</h2>

h(n) is admissible if for every n, h(n) <= h*(n) where h* is the true cost to goal.

h(n) is consistent if for every node n and every successor n' of n: h(n) <= d(n, n') + h(n')

If h(n) is admissible, then A* Search using tree-search is optimal.<br>
If h(n) is consistent, then A* Search using graph-search is optimal.

A* with all-zero heuristic = UCS

A* Search evaluation: Complete? Yes (if there is finite number of nodes with f(n) <= f(G)) Optimal? Yes. Time? O(b^(h*(root)-h(root))) Space? O(b^m)

<b>Dominance</b>

If ℎ2(𝑛) ≥ ℎ1(𝑛) for all 𝑛(both admissible), then ℎ2 dominates ℎ1. It follows that ℎ2 incurs lower search cost than ℎ1.

<b>Deriving admissible heuristic</b>: The cost of an optimal solution to a relaxed problem is an admissible heuristic for the original problem

<h2>Local Search</h2>

The path to goal is irrelevant; the goal state itself is the solution

State space = a set of "complete" configurations

Hill-climbing: Look at neighbours of current state. Go to the neighbour with the better evaluation function... Hill-climbing might result in a local minimum, not a global minimum! So, there are some non-guaranteed fixes like sideway moves and random restarts...
