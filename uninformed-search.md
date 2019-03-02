<h2>Uninformed-search</h2>

Fully Observable, Deterministic, Discrete Environments

Solution: sequence of actions
leading from initial to goal state

<h2>Definitions</h2>

<b>Frontier</b>: nodes that we have seen but haven’t
explored yet (at initialization: the frontier is just
the source) Alternatively: ```The frontier is the leaf nodes in the current search tree```

<b>Tree Search</b>: might revisit nodes again

<b>Graph Search</b>: Do not revisit nodes again

A <b>state</b> represents a physical configuration while a <b>node</b> is a data structure constituting part of
search tree. It includes state, parent node, action (i.e. the action applied to the parent to generate the node),
and path cost g(n) (i.e. the cost of the path from the <i>initial</i> state to the node).

<h2>Search strategies</h2>

Any deterministic search algorithm is determined by the
order of node expansion.

• completeness: always find a solution if exists<br>
• optimality: find a least-cost solution<br>
• time complexity: number of nodes generated<br>
• space complexity: max. number of nodes in memory

• b: maximum # of successors of any node (may be ∞)<br>
• d: depth of shallowest goal node<br>
• m: maximum depth of search tree (may be ∞)

<b>BFS</b>

Idea: Expand shallowest unexpanded node <br>
Implementation: Frontier is a FIFO queue,
i.e., insert new successors at the end

<b>UCS</b>

Dijskstra is a variant of UCS. 
Dijkstra's algorithm searches for shortest paths from root to every other node in a graph, whereas uniform-cost searches for shortest paths in terms of cost to a goal node.

Idea: expand least-path-cost unexpanded node <br>
Frontier: priority queue ordered by path cost g(n) <br>
Equivalent to BFS if all step costs are equal

<b>DFS</b>

Idea: Expand deepest unexpanded node<br>
Implementation: Frontier = LIFO stack, i.e.,
insert successors at the front

When checking a node v, we push at most
b descendants to stack. We do so at most m times ⇒ O(bm) space.

Do we really need to push all b
descendants to the stack? No need. You need an extra data structure:
You can consider one neighbour first, instead all the b neighbours. The extra data structure is used to save the ANCESTOR, so you can re-trace the steps.

<b>DLS</b>

If infinite depth, cannot use DFS... Use DLS. DFS with depth limit l.

<b>IDS</b>

Perform DLSs with increasing depth limit until goal node is reached.

Iterative deepening search may seem wasteful because states are generated multiple
times. It turns out this is <b>not too costly</b>. The reason is that in a search tree with the same (or
nearly the same) branching factor at each level, most of the nodes are in the bottom level,
so it does not matter much that the upper levels are generated multiple times.

![](/summary-uninformed-search.PNG)
