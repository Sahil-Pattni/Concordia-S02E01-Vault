---
center: "false"
theme: consult
height: "540"
width: "943"
slideNumbers: "false"
fragments: "false"
bg: "#ffffff"
pdfSeparateFragments: "false"
transition: convex
transitionSpeed: normal
css: /Users/sahilpattni/Library/Mobile Documents/iCloud~md~obsidian/Documents/Concordia/(COMP 691) Presentation/css/slide-template.css
---


# Learned Video Compression
### An ML-based video encoding algorithm
#### Sahil Pattni (40216177)

---
## Frame types
1) Intra-coded frames (**I-frames**)
	+ compressed using an image codec.
	+ Does not depend on any other frames.
2) Predicted frames (**P-frames**)
	+ Extrapolated from past frames.
3) Bi-directional frames (**B-frames**)
	+ Interpolated from previously transmitted frames in both the past and future.
	+ Increases latency.

note: put speaker notes here.

---

## Prediction frames
Motion compensation <!-- element class="fragment" data-fragment-index="1" -->

Residual compression <!-- element class="fragment" data-fragment-index="2" -->

---
## Motion Compensation
<div element class="fragment" data-fragment-index="0">
<h4> Block Matching </h2>

Sending frame $x_t$ at time $t$... 

</div>

+ Compare parts of $x_t$ to similar parts in past reference frames.
+ Optical flow map $f_t$.
+ Group similar areas together into *blocks*.
+ Motion-compensated approximation $m_t$.

note:
- Imagine video where not much changes from one frame to the next.
- No need to send entire frame.

---
## Residual Compression
$\Delta_t = x_t - m_t$

---
## Prediction Frames
#### Traditional Approach
![[Motion Compensation.png|600]]

---
## Prediction Frames
#### Idea: Compress jointly via the same bottleneck?

![[Joint Compression.png]]

---
## Contributions
+ Compensation beyond translation
+ Propagation of a learned state.
+ Joint compression of motion and residual.
+ Flexible motion field representation.
+ Multi-flow representation.
+ Spatial rate control.
+ ML-based video compression.
+ Enhancement of traditional coding using ML.
+ Optical flow estimation.
---
