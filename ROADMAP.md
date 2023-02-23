# HyperDL Roadmap

本文介绍了轻量化训练平台HyperDL各特性版本的功能发布和对应的文档动态，欢迎了解试用。

## HyperDL4.3 Release ，发布日期：2023-02

本次发版内容主要包括涉及数据中心，开发中心，算法中心，训练中心，模型中心、服务中心以及运维管理七大模块的功能升级。

### 数据中心

- 标注类型新增视频标注，斜框标注能力。其中视频标注场景，支持对视频文件预处理，包括视频切帧、视频分割等；支持目标追踪场景，视频帧继承标注。
- 标注格式新增目标追踪[MOT17](https://motchallenge.net/data/MOT17/)，斜框标注[DOTA](https://captain-whu.github.io/DOTA/index.html)，[roLabelImg](https://github.com/cgvict/roLabelImg)格式
- 标注任务支持直接发布样本集，支持目标检测场景样本集合并功能。

### 开发中心

- 集成GitLab代码管理功能
- 升级交互式开发环境为[JupyterLab](https://jupyterlab.readthedocs.io/en/stable/)，并支持开发环境端口暴露与远程SSH连接
- 预置主流AI引擎框架镜像，包括[TensorFlow](https://www.tensorflow.org/ )，[Pytorch](https://pytorch.org/ )以及[MindSpore]( https://www.mindspore.cn/ )

### 算法中心

- 新增[MindSpore]( https://www.mindspore.cn/ )框架下的深度学习算法，包括[ 目标追踪fairmot](https://gitee.com/mindspore/models/tree/master/research/cv/fairmot)，[Bert命名实体识别](https://gitee.com/mindspore/models/tree/master/official/nlp/Bert)，[Bert文本分类](https://gitee.com/mindspore/models/tree/master/official/nlp/Bert)，[文本检测CTPN](https://gitee.com/mindspore/models/tree/master/official/cv/CTPN)，[文本识别CRNN](https://gitee.com/mindspore/models/tree/master/official/cv/CRNN)在GPU和NPU下的训练任务
- 新增[Pytorch](https://pytorch.org/ )框架下的深度学习算法，包括[MMtracking](https://github.com/open-mmlab/mmrotate),[MMRotate](https://github.com/open-mmlab/mmrotate)，在GPU下的训练任务
- 新增[Pytorch](https://pytorch.org/ )框架下的强化学习算法，包括[A2C](https://openai.com/blog/baselines-acktr-a2c/)、PPO、APPO和IMPALA单智能体算法，在GPU下的训练任务

### 训练中心

- 优化超参搜索任务的可视化展示，并支持模型发布与在线评估
- 新增训练任务优先级调度策略，支持设置组织的优先级，包括高，中，低三个档次
- 支持[MindSpore]( https://www.mindspore.cn/ )框架在NPU上提交多机多卡训练任务

### 模型中心

- 预置目标追踪、文本检测、文字识别、命名实体识别、文本分类、斜矩形框检测场景的评估引擎

### 服务中心

- 预置[TFServing](https://www.tensorflow.org/tfx/guide/serving)、[MindSpore Serving](https://www.mindspore.cn/tutorial/lite/zh-CN/master/serving/index.html)和[Triton Inference Server](https://github.com/triton-inference-server/server )模型推理引擎，并支持用户自定义推理引擎

### 其他

- 新增管理员单独界面
- 支持[Kubernetes 1.21.14](https://kubernetes.io/docs/home/)，[Cuda 11.4](https://www.nvidia.cn/geforce/technologies/cuda/technology/)，华为版本[CANN ](https://www.hiascend.com/zh/software/cann),[MindX DL](https://www.hiascend.com/zh/software/mindx-dl)



