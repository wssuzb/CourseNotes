首先是数值流体动力学，通常需要给暗物质、气体以及恒星分配粒子网格，然后计算他们之间的引力、流体动力学以及热力学方程。用这种方法，可以很好的给出不同成分之间密度、速度温度随时间的演化，以及可以很好描述星系的结构、运动学性质，空间分布等。比如左边这幅Illustris项目模拟的可视化图，从左到右从上到下分别对应不同成分，不同红移从1-4的演化。

右边这幅图是EAGLE项目模拟的切片，表明了数值流体动力学模拟可以获得的动态范围为图中放大的区域，大致为3*10^10太阳质量星系的光学波段图像。

但是这种方法受限于计算机的算力，没办法对参数空间进行更近一步的探索优化，并且我们对小尺度物理过程的性质不够了解，只能用相对不确定的subgrid子网格来处理。

数值流体动力学的热力学演化早期模拟仅通过原始气体 (H + He) 进行的辐射冷却，如今还包括了来自金属线发射的冷却，这篇综述中关注的是后再电离时期的模拟，通常假设所有气体在光学上都很薄并且与空间均匀的总星系（megagalactic）辐射场处于电离平衡状态来解释光电离加热。

跟踪气体中重元素的富集对于冷却计算和银河化学演化的预测很重要。化学演化中包含了化学富集模型，并且早期模型仅跟踪与氧丰度密切相关的 II 型 SN 富集。为了追踪其他关键元素，如碳和铁，有必要模拟渐近巨星分支 (AGB) 星。

第二种方法是半解析模型，这种方法采用了简化的flow equation，因此需要的计算力相对较小。通常考虑有多少气体吸积成晕，有多少热气体冷却并变成恒星，反馈过程如何从星系中去除冷气体或加热晕气体，以及并合是如何将盘转化为球体等，例如这幅图，显示了一些可以在 SAM 中跟踪的晕合并树。

在半解析的热力学演化中，早期用自相似冷却流模型来跟踪气体的热演化。比如说当气体进入晕时，假设它被激波加热到维里温度，然后可以计算气体辐射掉其所有能量所需的冷却时间。

SAM中的化学演化考虑单区瞬时循环模型。老师上课讲过这里就不多介绍。近年来，一些 SAM 也用了流体数值模拟中的方法，包含了更详细的化学富集处理、跟踪多个单个元素以及 AGB 恒星、Ia 型和 II 型超新星的富集和气体循环的有限时间尺度。