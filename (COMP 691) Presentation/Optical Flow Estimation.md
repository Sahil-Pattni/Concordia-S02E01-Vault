### Optical Flow Estimation

**INPUT:** Given two similar frames $x_1,x_2 \in \mathbb{R}^{C \times H \times W}$

**OUTPUT**: $f^* \in \mathbb{R}^{2 \times H \times W}$, of horizontal and vertical displacements.

>[!equation] Formally
>
>$f^* = \min_f \mathscr{L}(x_2, F(x_1,f)) + \lambda \mathscr{R}(f)$
>
>Where:
> $\mathscr{L}(\cdot,\cdot)$ is some metric that describes how well the shuffled $x_1$ matches $x_2$.
> $\mathscr{R}(\cdot)$ is smoothness regularization.
> $F(\cdot,\cdot)$ is the inverse optical flow operator $[F(x,f)]_{chw} = x_{c,h}+f_{1hw},w+f_{2hw}$.
> >[!info] 
> > The *inverse optical flow* is simply called *flow* for brevity.

The goal is to create a *map* (*i.e.* an optical flow field) that describes how each pixel in $x_1$ needs to move to best match $x_2$. In other words, how can $x_1$ be shuffled to match $x_2$?