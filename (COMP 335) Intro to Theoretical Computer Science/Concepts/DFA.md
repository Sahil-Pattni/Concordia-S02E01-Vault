# Deterministic Finite Automata (DFA)

### Overview
DFAs can be used to prove regularity: A language $L$ is regular if there is a DFA $M$ that accepts $L$ (i.e. $L(M)=L$).

### Notes
- Every state must have a transition for every possible *letter* in the language it accepts.
	- $\forall q_i \in Q,\ \forall w \in \Sigma:\ \exists \delta (q_i, w)$  