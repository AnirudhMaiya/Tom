# Tom: Leveraging trend of the observed gradients for faster convergence

## Introduction
Tom (<b>T</b>rend <b>o</b>ver <b>M</b>omentum), is an adaptive optimizer that takes into account of the trend which is observed for the gradients in the loss landscape traversed by the neural network. Tom has an additional smoothing equation which is introduced to address the trend observed during the process of optimization. The smoothing parameter introduced for the trend requires no tuning and can be used with default values.

Please check <a href = 'https://arxiv.org/pdf/2109.03820.pdf'>our paper </a>for more details on Tom.
## Prerequisites
- PyTorch == 1.9.0

## Installation
Please clone this repository to your local machine
```
git clone https://github.com/AnirudhMaiya/Tom.git
```
You can import the optimizer as follows:
```python
from optimizer.tom import Tom

network = YourNetwork()
opt = Tom(network.parameters())
for input, output in loader:
  opt.zero_grad()
  loss = YourLossFunction(output, network(input))
  loss.backward()
  opt.step()

```
