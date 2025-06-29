+++
date = '2025-06-28T22:07:04+02:00'
draft = false
title = 'RandomForest vs KNN'

tags = ["Machine Lrearning"]
categories = ["skills"]
ShowToc = true

[cover]
image = "imgs/test.png"
alt = "A comparison between Random Forest and KNN"
caption = "RandomForest vs KNN"


+++

## Relationship to Nearest Neighbours

## 与最近邻算法的关系

### Original Text & Translation

### 原文与翻译对照：

1. **A relationship between random forests and the k-nearest neighbours algorithm was pointed out by Lin and Jeon in 2002.**
    Lin 和 Jeon 在 2002 年指出了随机森林与 k-近邻算法（k-NN）之间的关系。

2. **It turns out that both can be viewed as so-called weighted neighbourhoods schemes.**
    研究发现，这两种算法都可以被视为一种“加权邻域策略”（weighted neighbourhood scheme）。

3. **These are models built from a training set that make predictions for new points by looking at the neighbourhood of the point, formalized by a weight function.**
    它们的模型都是基于训练集建立的，通过观察新样本点的“邻域”来进行预测，并使用某种权重函数对邻域内的样本加权。

---

### Explanation and Comparison

### 解释与对比说明：

| 特征维度     | 随机森林（Random Forest）                                                    | k-近邻算法（k-NN）                     |
| ------------ | ---------------------------------------------------------------------------- | -------------------------------------- |
| **预测方式** | 基于多棵树中落叶节点样本的“邻域投票”                                         | 基于欧氏距离或其他距离的最近邻样本投票 |
| **邻域定义** | 每棵树划分特征空间 → 决定落在哪个叶子节点 → 邻域样本由落在相同节点的样本组成 | 距离样本点最近的 k 个样本              |
| **权重机制** | 可通过树结构间接引入权重（如树的深度、样本分布）                             | 可使用距离加权（如 1/distance）        |
| **本质**     | 集成学习（Ensemble Learning）方法                                            | 懒惰学习（Lazy Learning）方法          |
| **训练成本** | 高（训练时构建多棵树）                                                       | 低（几乎无训练过程）                   |
| **预测成本** | 中等偏高                                                                     | 高（需要计算与所有训练样本的距离）     |

---

### Daily Life Analogy 日常生活类比：

- **k-NN 就像问离你最近的几个人意见**：你想知道去哪里吃饭，你就问最近的几个朋友，然后根据他们的建议来决定。

- **随机森林像在多个不同场合问一群人**：你在多个不同社交场景（不同树）中问“身边的人”意见，这些人是按你所在场合随机分配的，他们的集体意见形成预测。

---

### Summary 总结：

虽然随机森林和 k-最近邻算法在实现机制和使用场景上差异很大，但它们都依赖于“邻域”的概念：即一个样本的预测与其周围的训练样本密切相关。它们都可以形式化为 **加权邻域模型（weighted neighbourhood models）**，其中预测是通过参考一组具有某种权重的邻近点来完成的。

这个观点有助于我们从统一视角理解不同的机器学习方法之间的联系。

# See also

