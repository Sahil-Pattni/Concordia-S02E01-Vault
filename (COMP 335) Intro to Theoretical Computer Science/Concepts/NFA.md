# Nondeterministic Finite Automata (NFA)

### Overview
NFAs are similar to DFAs, but with a few key differences:
- NFAs allow for $\lambda$-transitions.
- They can have different transitions for the same $w$.
	- (e.g.: $\delta(q_0, a)=q_1,\ \delta(q_0, a)=q_2$)
		```mermaid
			stateDiagram-v2
			direction LR
			[*] --> q0
			q0 --> q1: a
			q0 --> q2: a
		```
	
- Does not need a transition for every letter in alphabet for each state like a DFA does.

**Any language $L$ accepted by an NFA $M$ is also accepted by a DFA $M'$.**