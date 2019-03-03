<h2>Minimax</h2>

Complete? Yes (if game is finite). Optimal? Yes. Time O(b^m). Space O(bm)<br>
Sub-perfect Nash Equilibrium

<h2>Alpha-Beta Pruning</h2>

Initially, a(n) = −∞, b(n) = +∞ <br>
• a(n) is max along search path containing n<br>
• b(n) is min along search path containing n<br>
• If a MIN node has value v ≤ a(n), no need to
explore further.<br>
• If a MAX node has value v ≥ b(n), no need to
explore further.

Order of search in alpha-beta pruning is important too.

<h2>Time Limit</h2>

However, alpha–beta still has to search all the way
to terminal states for at least a portion of the search space. This depth is usually not practical,
because moves must be made in a reasonable amount of time—typically a few minutes at
most.

Solution: run minimax until a <b>cutoff depth</b> d, then use <b>evaluation function</b> (an estimation of utility) to choose nodes.

Modern evaluation functions: weighted sum of
position features
