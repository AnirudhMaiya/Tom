# Tom: Leveraging trend of the observed gradients for faster convergence

## Introduction
Tom (<b>T</b>rend <b>o</b>ver <b>M</b>omentum), is an adaptive optimizer that takes into account of the trend which is observed for the gradients in the loss landscape traversed by the neural network. Tom has an additional smoothing equation which is introduced to address the trend observed during the process of optimization. The smoothing parameter introduced for the trend requires no tuning and can be used with default values.
