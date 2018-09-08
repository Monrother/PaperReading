### Retina Net
1. 作者在论文中提出之所以 one-stage 的检测方法不如 two-stage 的最关键的原因就是正负样本的比例不均衡
2. 作者在原来的交叉熵 CE 的基础上，提出了一个新的 loss Focal loss，在原来交叉熵的基础上增加一个系数。

- Cross Entropy (CE) Loss
    