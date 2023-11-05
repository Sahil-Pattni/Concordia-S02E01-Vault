# Chomsky Normal Form (CNF)
### Description
Each production is either of the form $A \rightarrow BC$ or $A \rightarrow a$.
In regex, this can be written as `([A-Z] -> [A-Z]{1,2}) | ([A-Z] -> [a-z])`

---
### Conversion to CNF
**STEP 0**: Remove nullable variables and unit productions

**STEP 1**: For each terminal (*e.g.* $a,b,c$): introduce variables $T_a,T_b,T_c$.
$S \rightarrow ABa$
$A \rightarrow aab$
$B \rightarrow Ac$

becomes...

$S \rightarrow ABT_a$
$A \rightarrow T_aT_aT_b$
$B \rightarrow AT_c$
$T_a \rightarrow a$
$T_b \rightarrow b$
$T_c \rightarrow c$

**STEP 2**: Introduce intermediate variables
$S \rightarrow AV_1$
$V_1 \rightarrow BT_a$
$\cdots$

---
### Remarks
- CNF is good for parsing and proving theorems.
- It is easy and straightforward to find a CNF for any CFG (which does not generate $\lambda$).
- The time complexity of the CYK conversion algorithm is $\vert w \vert^3$

