# SIATD 复杂背景下红外弱小运动目标检测数据集

## 数据/data:

[https://www.scidb.cn/en/detail?dataSetId=808025946870251520](https://www.scidb.cn/en/detail?dataSetId=808025946870251520)

## 数据集描述/paper:

 [http://www.csdata.org/p/553/](http://www.csdata.org/p/553/)

Small infrared moving target detection is one of the key technologies of infrared detection. And it has always been a hot issue in photoelectric detection, especially for small infrared moving target under clutter background. The problem has not yet been solved. In view of the lack of high quality data in current research, we adopt infrared imaging equipment installed on a small UAV platform to capture image sequences as backgrounds. The synthetic targets are embedded in backgrounds properly. We build a semi-synthetic dataset for small infrared moving target detection under clutter background. Various conditions are set in image capturing, including relative height (up looking, head up looking and down looking), scenes (vegetation, water and building), platform motion, weather, time, etc. The imaging platform motion and the synthetic target motion are considered simultaneously to guarantee that the semi-synthetic image sequences as close as possible to the real application scenario. In addition, we vary the target characteristics in synthetizing, including shape, intensity, and motion. Our dataset contains 350 image sequences, 150185 images. The annotation file provided the targets positions in images. The dataset can be used in small infrared moving target detection and tracking researches.The target label of the test set in this data set and the evaluation program for the detection results are stored in Baidu online disk, link: [https://pan.baidu.com/s/1yraqQOE43HizL6syeRT9pw](https://pan.baidu.com/s/1yraqQOE43HizL6syeRT9pw) Extraction code: GLCC.

# 我们做了什么

为了在训练数据中获得更丰富的多样性和更高的信息密度，我们在实验过程中对 SIATD 数据集进行了进一步的采样、分割和标记。

- 第一，重新采样。我们的研究重点是小型空中目标，因此我们从 175 个序列中选取了 40 个空中场景的序列（106-140）。考虑到每个序列包含大量背景相似的帧，我们从每个序列中随机抽取了 50 幅图像，以达到更高的信息密度。
- 第二，重新划分。我们选择了奇偶数方式，以 1:1 的比例将序列分为训练集和测试集。一方面，以 1:1 的比例划分数据集具有重要的好处，包括在训练集和测试集之间实现数据的均衡分布，防止模型过拟合，增强泛化能力验证的真实性，以及提供更稳健的模型性能评估。另一方面，在 40 个序列中，前 20 个序列有一个目标，接下来的 10 个序列有两个目标，最后的 10 个序列有三个目标。而背景分布相对随机。为了平衡训练数据集和测试数据集中目标数的分布，我们根据帧数是奇数还是偶数来划分这些数据集。
- 第三，重新标记。我们根据局部对比度将点注释转化为二进制掩码，使 SIATD 能够用于基于分割的小目标检测方法。

最终我们处理过的数据集中训练集包含900张图像，测试集包含850张图像。处理后的数据集已公开。

链接：[https://pan.baidu.com/s/1DW7v1YulG5f0M8ayH64KVQ?pwd=ywdo](https://pan.baidu.com/s/1DW7v1YulG5f0M8ayH64KVQ?pwd=ywdo)
提取码：ywdo
