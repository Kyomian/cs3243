Resource: <a href="http://aima.cs.berkeley.edu/">Textbook</a>

For AI to think rationally.

<ul>
  <li>Turing Test</li>
  <li>Winograd Scheme</li>
  <li>How To Test AI? Subjective. What do you mean by "rational"?</li>
</ul>

<h2>Agent</h2>

An agent is a <b>function</b> from <b>percept histories</b> (what I have seen until now) to <b>actions</b>. To design the best program given the limited resources.

An agent has <b>sensors</b> to perceive and <b>actuators</b> to act. Agent = Program + Architecture

<h2>Rational agent</h2>

<s>An agent needs to have a goal to complete?</s> To measure the success of an agent's behaviour, we use <b>performance measure</b> (objective criterio, eg. resources used)

Thus we define <b>rational agent</b> as:

- For each possible percept sequence, select an
action that is expected to maximize its
performance measure…

- given the evidence provided by the percept
sequence and whatever built-in knowledge the
agent has.

Rationality ≠ omniscience (all-knowing with
infinite knowledge)

• Agents can perform actions that help them
gather useful information (exploration)

• An agent is <b>autonomous</b> if its behavior is
determined by its own experience (with
ability to learn and adapt)

<h2>Task Environment</h2>

Set a task environment for the rational agent to act in. This is known as <b>PEAS</b>:

- Performance measure

- Environment

- Actuators

- Sensors

Task Environment Properties:

<ol>
  <li> Fully observable vs partially observable: <b>sensors</b> can see complete state of environment or not</li>
  <li> Deterministic vs Stochastic: By deterministic, the next state of the environment is completely determined
by the current state and the action executed by the agent.</li>
  <li> Episodic vs Sequential: By episodic: the choice of current action does not depend on actions in past episodes. Alternatively: current action does not affect future
decisions</li>
  <li> Static vs Dynamic environment? </li>
  <li> Discrete vs Continuous: By discrete: finite number of distinct <b>states, precepts or actions</b> </li>
  <li> Single agent vs multi-agent: only one agent in environment or many? </li>
</ol>

<h2>Designing the agent function and program</h2>

An agent is completely specified by the
agent function mapping percept sequences
to actions.

• One agent function (or a small equivalence
class) is rational

• Aim: Find a way to implement the rational
agent function concisely

The native way is to implement a look-up table for the agent function! 

Drawbacks of naive approach: 

- Huge table to store
- Take a long time to build the table
- No autonomy: impossible to learn all correct table entries
from experience
- No guidance on filling in the correct table entries

<h2>Agent Types</h2>

- Simple Reflex agent (least general): <b>Passive</b> (only acts when observed a percept) and updates state based on <b>percept only</b>

- Model Reflex agent: <b>Passive</b>, and updates state according to percept, current state, most recent action and model of the world (which is inferred?)

- Goal Based agent: <b>Not passive, has goals</b>, updates state according to percept, current state, most recent action and model of the world

- Utility Based agent (most general): <b>Has utility function, seeks to maximise said function</b>, updates state according to percept, current state, most recent action and model of the world

- Learning agent? Will adjust the utility function according to users' input (machine learning?)

<h2>Exploitation vs Exploration</h2>

An agent operating in the real world must
often choose between:

• maximizing its expected utility according to its
current knowledge about the world; and

• trying to learn more about the world since this
may improve its future gains.

<h2>Miscellaneous</h2>

<b>Q: What is the difference between the static/dynamic dichotomy vs the discrete/continuous dichotomy?</b>

A: if your agent operates in a static environment then it can be safe to assume that the environment does not change while the agent is thinking about what to do. If the enviroment changes as the agent thinks then it's dynamic. In particular, dynmaic environments don't "wait" for the agent to make an action before changing. For example, if you play chess with a clock running then a good computer agent should consider that the clock is ticking while it's thinking and not take forever to make a move. 

Discrete/continuous handles how one models time in the environment; if the environment operates in discrete turns (like in solving puzzles) then time is discrete. If it is continuously offering feedback to the agent then it's continuous. 

<b>Q: What are stochastic environments? </b>

A: in stochastic environments, some parameters in the environment are unknown. For example, in poker games, the deck is shuffled which causes uncertainty about what cards I'll be getting. However, poker is still a static game (the environment doesn't change while you think about your next move) and still operates in discrete "turns" (rather than continuously requesting the agent for feedback).  
