# 无人机视角下的目标检测
主要收录自己整理的一些相关文章和数据集
## 1.Mr.DETR:Instructive Multi-Route Training for Detection Transformers(2025 CVPR)
### ①contribution
1、首先，在多任务框架中，文章通过实验证明，即使在共享其他组件的情况下，解码器中的任何独立组件都可以有效地同时学习一对一和一对多目标；
2、其次，在上述见解的基础上，文章提出了一种多路径训练机制，并通过所提出的指导性自注意力机制增强它，动态灵活地指导object queries进行一对多预测；
3、第三，在COCO 2017数据上进行了广泛的实验。
### ②method
<img width="1041" height="480" alt="image" src="https://github.com/user-attachments/assets/7dc661d8-2b49-42c3-8f10-2904e17fe18b" />

### ③https://github.com/Visual-AI/Mr.DETR
## 2.VMamba: Visual State Space Model（2024 NeurIPS）
### ①contribution
1、文章提出了一种基于SSM的视觉骨干VMamba，用于具有线性时间复杂性的视觉表征学习；2、引入了二维选择性扫描（SS2D），在一维阵列扫描和二维平面遍历之间架起了桥梁，使选择性SSM能够扩展到处理视觉数据；3、Vmamba在图像分类、物体检测和语义分割等各种视觉任务中都取得了令人满意的性能。并且对输入序列长度的显著适应性，显示出计算复杂度的线性增长。
### ②method
SS2D
<img width="1017" height="315" alt="image" src="https://github.com/user-attachments/assets/7d163d78-72a1-4247-b7ce-e5482b909978" />
Vmamba

<img width="554" height="577" alt="image" src="https://github.com/user-attachments/assets/b65ec3f5-ffcc-426a-a3a7-a64ba0366c68" />

### ③https://github.com/MzeroMiko/VMamba
