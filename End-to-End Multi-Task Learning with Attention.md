### End-to-End Multi-Task Learning with Attention

- 实现 multi task 不仅是关于 memory 和 inference speed，还有数据的问题，因为相关的任务一般会共享视觉特征。
- MTL 中的两个挑战
    - 网络结构。网络中既要有共享的 feature，又要有针对不同的任务的 feature。
    - 损失函数。multi-task loss 是 single-task loss 的加权和，应该使学习每个任务都同等重要，同时不会使学习被更简单的任务所支配。解决办法是要么可以自动调整权重，要么对 loss 的权重不敏感。
- 提出一个 unified approach (MTAN)，(i) 可以使 task-shared 和 task-specific feature 自动学习 -> (ii) 学习对loss weight 的 inherent robustness
