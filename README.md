# 无人机视角下的目标检测
主要收录自己整理的一些相关文章和数据集
## 1.Mr.DETR:Instructive Multi-Route Training for Detection Transformers(2025 CVPR)
### ①contributions
1、首先，在多任务框架中，文章通过实验证明，即使在共享其他组件的情况下，解码器中的任何独立组件都可以有效地同时学习一对一和一对多目标；
2、其次，在上述见解的基础上，文章提出了一种多路径训练机制，并通过所提出的指导性自注意力机制增强它，动态灵活地指导object queries进行一对多预测；
3、第三，在COCO 2017数据上进行了广泛的实验。
### ②method
<img width="1041" height="480" alt="image" src="https://github.com/user-attachments/assets/7dc661d8-2b49-42c3-8f10-2904e17fe18b" />

### ③https://github.com/Visual-AI/Mr.DETR
## 2.VMamba: Visual State Space Model（2024 NeurIPS）
### ①contributions
1、文章提出了一种基于SSM的视觉骨干VMamba，用于具有线性时间复杂性的视觉表征学习；2、引入了二维选择性扫描（SS2D），在一维阵列扫描和二维平面遍历之间架起了桥梁，使选择性SSM能够扩展到处理视觉数据；3、Vmamba在图像分类、物体检测和语义分割等各种视觉任务中都取得了令人满意的性能。并且对输入序列长度的显著适应性，显示出计算复杂度的线性增长。
### ②method
SS2D
<img width="1017" height="315" alt="image" src="https://github.com/user-attachments/assets/7d163d78-72a1-4247-b7ce-e5482b909978" />
Vmamba

<img width="554" height="577" alt="image" src="https://github.com/user-attachments/assets/b65ec3f5-ffcc-426a-a3a7-a64ba0366c68" />

### ③https://github.com/MzeroMiko/VMamba
## 3.MambaVision: A Hybrid Mamba-Transformer Vision Backbone（2025 CVPR）
### ①contributions
1、文章引入了重新设计的视觉友好型Mamba块，与原始架构相比，提高了准确性和图像吞吐量；2、文章对Mamba和Transformer块的集成模式进行了系统研究，并证明在最后阶段加入自注意力块可显著提高模型捕捉全局上下文和长距离空间依赖性的能力；3、提出一种新颖的混合 Mamba Transformer 模型。在 ImageNet-1K数据集上的 Top-1 准确率和推理吞吐量方面均达到了新的最先进水平（SOTA）。
### ②method
<img width="913" height="292" alt="image" src="https://github.com/user-attachments/assets/4a4da39c-1663-453f-8323-4f80e1a6f4ff" />

### ③https://github.com/NVlabs/MambaVision
## 4.MambaOut: Do We Really Need Mamba for Vision?（2025 CVPR）
### ①contributions
1、文章分析了SSM类RNN的机制，从概念上得出Mamba适合具有长序列和自回归特性任务的结论；
2、文章研究了视觉任务的特性，并假设由于ImageNet图像分类任务不满足上述两个特性，因此SSM对于该任务并非必要；而对于检测和分割任务，尽管它们不具有自回归特性，但由于符合长序列特性，探索 SSM 在这些任务中的潜力仍然具有价值；
3、文章开发了一系列基于Gated CNN块但不含SSM的MambaOut模型，实则是去掉SSM模块的Mamba block。
### ②method
<img width="800" height="240" alt="image" src="https://github.com/user-attachments/assets/da3c0d16-33e7-45ae-b693-5b51bc380412" />

### ③https://github.com/yuweihao/MambaOut
## 5.Mamba-Adaptor: State Space Model Adaptor for Visual Recognition（2025 CVPR）
### ①contributions
1、引入了即插即用的Adaptor，Adaptor-T和Adaptor-S，有效解决时间衰减和空间定位问题。在可接受的计算开销下提升模型在各种视觉任务中的表现；
2、Mamba-Adaptor不仅可以作为图像分类和预测任务的通用视觉骨干，还能在迁移学习任务中发挥作用；
3、以大量实验结果证明MambaAdaptor在多种视觉下游任务中优于Mamba基线表现优异，并有显著提升。
### ②method
<img width="938" height="355" alt="image" src="https://github.com/user-attachments/assets/3319f97f-5249-4f05-8ce7-63750cc48f61" />

### ③https://arxiv.org/pdf/2505.12685
## 6.Uncertainty-Aware Gradient Stabilization for Small Object Detection（2025 ICCV）
### ①contributions
1、进行了梯度分析以探讨小物体探测（SOD）挑战，表明传统物体定位在小物体上存在不稳定梯度，导致收敛性挑战。文章提出了一种新型的不确定性感知梯度稳定（UGS）方法，以提升梯度稳定性并促进更好的收敛；2、UGS集成了三个关键组件：基于分类的定位目标，用于生成有界和置信度驱动梯度;一个显式建模并最小化小物体预测不确定性的不确定性最小化损失;以及一个利用对抗扰动识别和细化高不确定性区域的不确定性引导细化模块；3、UGS在基线探测器和最先进的小物体探测器上表现出持续的提升，展现出在一般物体检测和高分辨率检测方面的有效性。
### ②method
<img width="919" height="272" alt="image" src="https://github.com/user-attachments/assets/2e7106b7-30a4-46e7-9c32-c38273a116da" />

### ③https://arxiv.org/pdf/2303.01803

