### Mask R-CNN
#### 特点
- 灵活，可以增加不同的分支完成不同的任务，包括分类、检测、语义分割、实例分割、人体关键点识别
- 目标
    - 高速、高准确率：采用 Faster R-CNN 解决检测问题和 FCN 解决分割问题，5fps 的速度，提出 RoI Align 的策略，解决 RoI pooling 中的像素偏差的问题。
#### Contrib
- RoI Align
    - 发现 RoI Pooling 中由于引入了两次量化存在像素偏差的问题。
    - 在 RoI Align 中，对 RoI pooling 不进行量化，得到的结果用双线性保留，最后采取双线性插值的办法。
    