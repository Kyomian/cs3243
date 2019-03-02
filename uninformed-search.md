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
