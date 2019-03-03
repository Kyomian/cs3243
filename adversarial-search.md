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
