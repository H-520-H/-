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
## 7.UniRepLKNet: A Universal Perception Large-Kernel ConvNet for Audio, Video, Point Cloud, Time-Series and Image Recognition（2024 CVPR）
### ①contributions
用于大核CNN架构设计的四条guideline，一种名为UniRepLKNet的强力backbone（只用ImageNet-22K预训练，精度和速度SOTA，ImageNet达到88%, COCO达到56.4 box AP，ADE20K达到55.6 mIoU，实际测速优势很大），在时序预测的超大数据上用这一为图像设计的backbone达到SOTA水平（全球气温和风速预测，前SOTA是发在Nature子刊上专门为此设计的Transformer），在点云、音频、视频上凭着极为简单的预处理方式和毫无改变的模型结构均超过或接近SOTA水平。
### ②method
<img width="499" height="533" alt="image" src="https://github.com/user-attachments/assets/e6e5f45b-4114-41ae-920b-c59f9cdb6510" />
<img width="1054" height="269" alt="image" src="https://github.com/user-attachments/assets/944cebe6-ae21-4bea-b1d0-568299654d59" />

### ③https://github.com/AILab-CVC/UniRepLKNet
### ④https://zhuanlan.zhihu.com/p/669527907（作者解读）
## 8.LEGNet: A Lightweight Edge-Gaussian Network for Low-Quality Remote  Sensing Image Object Detection（2025 ICCV）
### ①contributions
1、作者介绍了新颖的EGA模块，该模块将传统的图像处理算子（方向感知夏尔边缘增强和基于高斯先验的特征建模）与可学习的深度特征相结合，专门解决低质量RS图像中的特征退化问题；2、提出轻量级网络 LEGNet，旨在高效地改进对具有挑战性的对象（如低质量、模糊或遮挡）的检测，同时保持适合边缘部署的计算效率；3、在五个具有挑战性的RSOD基准上进行的广泛实验表明，LEGNet 建立了新的SOTA性能。
### ②method
<img width="1150" height="596" alt="image" src="https://github.com/user-attachments/assets/877b6d1c-6751-44ea-b317-a1344154d8c7" />

### ③https://github.com/AeroVILab-AHU/LEGNet
## 9.Self-Prompting Analogical Reasoning for UAV Object Detection(2025 AAAI)
### ①contributions
1、提出了一种基于视觉-语言模型的类比推理框架：该框架包含三个步骤：演绎、映射和推理，分别对应基于语言特征的图构建、图边构建和图推理。通过这种方式，更容易检测到的对象可以支持小而难以检测对象的检测；2、提出了一种自提示方法：为每张图像生成上下文感知提示和目标性提示分数图，隐式提取上下文信息并增强特征表示；3、通过类别级和像素级图节点实现类比推理：增强了直接通过视觉特征难以检测到的对象的特征，使其能够通过关系推理成功检测。
### ②method
<img width="1184" height="628" alt="image" src="https://github.com/user-attachments/assets/ded2e048-f46c-4a01-b7a5-80a526aacc36" />

### ③https://github.com/lnxwow/Analogical-Reasoning
## 10.RemDet: Rethinking Efficient Model Design for UAV Object Detection（2025 AAAI）
### ①contributions
1、作者重新思考了无人机检测器的设计，摒弃了复杂的手工设计。通过探索信息损失，使用最简单的结构有效地增强了小物体检测；
2、遵循减少信息损失的原则，研究发现，仅高维表示就可以减少信息损失并提高小物体的性能。并通过实证结果、理论探索和可视化表示验证了分析；
3、为解决复杂的实时要求，其中复杂设计和多特征融合在提高准确性方面不切实际，研究表明，乘法而非前馈网络是一种成本效益高且更简单的高维表示方法。基于这一见解的设计减少了信息损失，同时保持了低延迟。
### ②method
<img width="1161" height="565" alt="image" src="https://github.com/user-attachments/assets/359a5ec1-7bc6-4abd-9c35-42a85ae24c49" />

### ③https://github.com/HZAI-ZJNU/RemDet

#
# Dataset
### Stanford Drone dataset 行人、自行车、滑板、汽车等多目标行为理解与轨迹预测——多目标跟踪 + 轨迹预测
### UAV123 dataset 移动物体跟踪（车辆、人、动物）——视觉跟踪
### Car Parking Lot dataset (CARPK) dataset 停车场汽车计数与检测——目标检测 + 计数
### UAV-ROD dataset 城市场景多类物体检测（人、车、建筑等）——目标检测
### Okutama-Action dataset 行为识别（跑步、携物、打电话等）——行为检测 + 动作识别
### UAV Detection and Tracking (UAVDT) dataset 车辆检测与跟踪、天气与光照变化鲁棒性——检测 + 跟踪
### DAC-SDC dataset 智慧城市中的自动驾驶检测竞赛数据——检测 + 交通目标识别
### Moving Object Recognition (MOR-UAV) dataset 移动物体识别（人、车、船等）——检测 + 分类
### DroneVehicle dataset 高密度交通目标检测与再识别——检测 + Re-ID + 跟踪
### AU-AIR dataset 多模态无人机检测（RGB+IMU+GPS）——检测 + 多模态感知
### UVSD dataset 视频监控检测与目标分割——检测 + 视频分割
### AerialMind 首次构建无人机指代多目标跟踪大规模基准——多目标跟踪（AAAI 2026 Oral）
### HazyDet 带有场景深度的雾天无人机目标检测开源基准——检测（2024）
### AirSim360  无人机视角下的全景数据集及仿真平台（还未开源）
### UTUAV: A Drone Dataset for Urban Traffic Analysis 汽车、摩托车和大型车辆——检测（2025）
