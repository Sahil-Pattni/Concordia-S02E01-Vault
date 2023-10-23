# The Pumping Lemma

### Basic Idea: The Pigeonhole Principle
If there are $(n+1)$ objects put into $n$ boxes, then at least one box must contain $2$ or more objects.

### Definition
Given an ***infinite*** regular language $L$, there exists an integer $m$, for any string $w \in L$ with length $|w| \geq m$. So we can say:

$\forall w \in L: \exists xyz$

$w=xyz,\ |xy| \leq m,\ |y| \geq 1$.  

$\therefore w_i = xy^iz \in L$.

If $w_i \notin L$, this is a **contradiction** and the language $L$ is not regular.