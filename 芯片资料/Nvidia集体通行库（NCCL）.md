# 文档说明
NVIDIA 集体通信库[NCCL](https://developer.nvidia.com/nccl)NVIDIA GPU 和网络进行优化的多 GPU 和多节点通信原语。NCCL 提供全收集、全归约、广播、归约、归约分散以及点对点发送和接收等例程，这些例程经过优化，可在 PCIe 和 NVLink 高速互连上实现高带宽和低延迟。一个节点以及跨节点的 NVIDIA Mellanox 网络。

[Caffe2](https://www.caffe2.ai/)、[Chainer](https://chainer.org/)、[MxNet](https://mxnet.incubator.apache.org/)、[PyTorch](http://pytorch.org/)和[TensorFlow](https://www.tensorflow.org/) 等领先的深度学习框架都集成了 NCCL，以加速多 GPU 多节点系统上的深度学习训练。

![img](https://d29g4g2dyqv443.cloudfront.net/sites/default/files/akamai/NCCL_1GPU_multiGPU.png)

