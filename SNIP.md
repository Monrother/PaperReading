### SNIP -- An Analysis of Scale Invariance in Object Detection
本文研究尺度变化对目标检测任务带来的挑战及应对方案。

一般我们都是用目标分类的模型的 pre-trained model，在其基础上进行检测任务的 fine-tune。由于目标分类和检测的训练集的尺度差异，造成 domain shift。

- 解决 scale variation 和 small objects 检测的问题
    - 使用与输入很近的层的 feature 与深层的 feature 相融合，用于检测 small objects（FPN、Mask R-CNN、SSD）
    - dilated / deformable conv 以增大感受野，用于检测大的物体 
    - 在不同分辨率的层上做独立检测，用来捕获不同大小的物体
    - 增加 context 防止 ambiguation （红绿灯、Raw Roi padding）
    - 在多个 scale 上进行训练
    - 在多个尺度上进行 infer，并与 NMS 结合

