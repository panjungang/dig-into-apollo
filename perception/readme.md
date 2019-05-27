# Dig into Apollo - Perception ![GitHub](https://img.shields.io/github/license/daohu527/Dig-into-Apollo.svg?style=popout)

> 温故而知新，可以为师矣


## Table of Contents
- [CNN](#cnn.md)
    - [什么是CNN？](#what_is_cnn)
    - [CNN的原理](#cnn_principle)
        - [卷积层(Convolutional Layer)](#convolutional)
        - [池化层(Max Pooling Layer)](#max_pool)
        - [全连接层(Fully Connected Layer)](#fully_connect)
    - [如何构建CNN](#how_to)
    - [基本概念](#base_concept)
    - [引用](#reference)


<a name="introduction" />

## Perception模块简介

我们先看下perception的目录结构：  
```
.
├── base         // 基础类
├── BUILD        // 编译testdata，用于测试
├── camera       // 摄像头
├── common       // 公共目录
├── data
├── fusion       // 融合
├── inference    // 推理
├── lib          // lib库
├── lidar        // 雷达
├── map          // 地图
├── onboard      // 消息处理
├── production   // 加载模块
├── proto        // 数据格式，protobuf
├── radar        // 毫米波
├── README.md
└── testdata    // 上述几个模块的测试数据，包括训练好的模型
```
apollo的感知模块没有开放训练模型，只是开放了testdata，下载训练好的模型之后来跑一个简单的Demo。  




## radar
我们先从一个简单的模块开始看起，首先看下radar目录：  
```
.
├── app          // 每个模块都有一个app目录
├── common       // 公共目录
└── lib          // 库
```




radar模块被"RadarDetectionComponent"引用，perception的入口在onboard中。我们最后分析下"RadarDetectionComponent"模块。  


## tools
obstacle_detection 根据kitti的例子，对camera做完整流程的识别，如果需要入门，可以把这个例子先跑通，同时也可以拿这个例子进行性能调优。  

lane_detection 车道线识别的例子


## Reference
[A Beginner's Guide to Convolutional Neural Networks](https://skymind.ai/wiki/convolutional-network)  
[cnn](https://cs231n.github.io/convolutional-networks/)  
[traffic light dataset](https://hci.iwr.uni-heidelberg.de/node/6132/download/3d66608cfb112934ef40175e9a20c81f)  
[pytorch-tutorial](https://github.com/yunjey/pytorch-tutorial)  
[全连接层的作用是什么？](https://www.zhihu.com/question/41037974)  
[索伯算子](https://zh.wikipedia.org/wiki/%E7%B4%A2%E8%B2%9D%E7%88%BE%E7%AE%97%E5%AD%90)  
[卷积](https://zh.wikipedia.org/wiki/%E5%8D%B7%E7%A7%AF)  
