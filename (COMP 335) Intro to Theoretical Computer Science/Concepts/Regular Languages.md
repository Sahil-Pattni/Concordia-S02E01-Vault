# Regular Expressions (RegEx) 

### Operations
- $r_1 + r_2$
- $r_1r_2$
- $r_1^*$
- $(r_1)$


### Generalized Transition Graphs (GTGs)
To convert a finite automata to a regular expression, we can use GTGs.

Example:
M = 
```mermaid
	stateDiagram-v2
	direction LR
	[*] --> q0
	q0 --> q1: b
	q1 --> q0: a
	q1 --> q1: b
	q1 --> q2: a,b
	q2 --> q2: b
	q2 --> [*]
```

M = 
```mermaid
	stateDiagram-v2
	direction LR
	[*] --> q0
	q0 --> q0: bb*a
	q0 --> q1: bb*(a+b)
	q1 --> q1: b
	q1 --> [*]
```
