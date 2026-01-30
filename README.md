# 无人机视角下的目标检测
主要收录自己整理的一些相关文章和数据集
## 1.Mr.DETR:Instructive Multi-Route Training for Detection Transformers(2025 CVPR)
### ①contribution：
1、首先，在多任务框架中，文章通过实验证明，即使在共享其他组件的情况下，解码器中的任何独立组件都可以有效地同时学习一对一和一对多目标；
2、其次，在上述见解的基础上，文章提出了一种多路径训练机制，并通过所提出的指导性自注意力机制增强它，动态灵活地指导object queries进行一对多预测；
3、第三，在COCO 2017数据上进行了广泛的实验。
### ②method
<img width="1041" height="480" alt="image" src="https://github.com/user-attachments/assets/7dc661d8-2b49-42c3-8f10-2904e17fe18b" />
### ③https://github.com/Visual-AI/Mr.DETR
