# ML-based QoE Inference of Encrypted Traffic in Low-Bandwidth Environments
---
## Overview

QoE inference in resource-constrained environments (e.g. rural / developing areas with limited bandwidth). The solution should be able to predict QoE with a high rate of accuracy when network conditions are sub-optimal.

---
## Considerations

- #### Data Collection
	- Will data come pre-encrypted or will I have to encrypt it?
	- Where to collect data from? What kind of data?
- #### Feature Selection
	- Determine what features are relevant to QoE inference in low-bandwidth environments (LBEs).
- #### Model Architecture
	- What model to use?
		- Deep learning (e.g. CNNs, ANNs, RL).
		- Classic ML models (e.g. SVMs, Decision Trees, KNNs, Naïve-Bayes).
		- Has to work within my computation constraints (Google Colab / AWS SageMaker).
- #### Quality Metrics / Ground Truth
	- Determine which metrics can be obtained for / generated from the data.
		- Common metrics include video bitrate, frame rate, video quality scores (e.g., SSIM, PSNR), and buffering duration.
		- Could infer Startup delay, re-buffering, selected quality.
- #### Privacy Concerns
    - Given the sensitivity of encrypted traffic, consider privacy-preserving ML techniques that allow for QoE inference without revealing the content of the traffic or compromising user privacy. Techniques like federated learning or secure multi-party computation may be relevant.
- #### Model Optimization for LBEs
	- It is likely that in practice, such a model would be required to run on resource-constrained hardware and/or network conditions. The model will need to be optimized to ensure that it can be run in such environments.
- #### Evaluation / Benchmarking
	- Design evaluation metrics, train it on one dataset and evaluate it on another to see how it performs.
	- Compare its performance to other SotA models as a benchmark.

## Tools & Frameworks
[MahiMahi](http://mahimahi.mit.edu): A set of lightweight tools for browser developers, website authors, and network protocol designers that provides accurate measurements when recording and replaying HTTP content over emulated network conditions.