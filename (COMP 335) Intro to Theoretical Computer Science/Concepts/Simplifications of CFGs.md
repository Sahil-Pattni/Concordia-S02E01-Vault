# Simplifications of CFGs
### Substitution
**IDEA**: *replace $B$*

| **Before** | **After** |
|---|---|
| $S \rightarrow aB$ <br> $B \rightarrow aA$ <br > $B \rightarrow b$ | $S \rightarrow aaA\ \vert \ ab$ |

---
### Remove Nullable Variables
**IDEA**: *remove $M \rightarrow \lambda$*

| **Before** | **After** |
|---|---|
| $S \rightarrow aMb$ <br> $M \rightarrow aMb$ <br > $M \rightarrow \lambda$ | $S \rightarrow aMb$<br>$S \rightarrow ab$<br>$M \rightarrow aMb$<br>$M \rightarrow ab$  |


---
### Unit Productions
**IDEA**: A unit production has a single variable at each side (*e.g.* $A \rightarrow B$)

| **Before** | **After** |
|---|---|
| $S \rightarrow aA$<br>$A \rightarrow a$<br>$A \rightarrow B$<br>$B \rightarrow A$<br>$B \rightarrow BB$  | $S \rightarrow aA\ \vert aB$<br>$A \rightarrow a$<br>$B \rightarrow bb$|

---
### Useless Productions
**IDEA**: Imagine this language
$S \rightarrow A$
$A \rightarrow aA$

It never ends, and therefore it can be removed.

Imagine:
$S \rightarrow A$
$A \rightarrow aA$
$A \rightarrow \lambda$
$b \rightarrow bA$

The last production is unreachable from $S$, and therefore can be removed.

###### Steps to find useless productions:
1. Find every variable that produces strings with *only* terminals (*e.g.* $B \rightarrow aa$)
2. Find all the variables that are reachable from $S$

---
###### Steps to remove all undesired productions
`Note: The order of execution is important`
1. Remove nullable variables and $\lambda$-productions
2. Remove unit-productions
3. Remove useless productions.