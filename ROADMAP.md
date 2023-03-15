# HyperDL Roadmap

本文介绍了轻量化训练平台HyperDL各特性版本的功能发布和对应的文档动态，欢迎了解试用。

## HyperDL 4.5 Release，发布日期：2023-09

HyperDL预计在2023年09月发布v4.5版本，预计新增或者优化功能项超过**50+**。

### 样本库（对应数据中心，存储管理原始样本及标注数据集）

- 增加原始数据的预处理能力，包括无效数据清洗、无效字符过滤
- 优化标注任务创建流程，支持选择是否开启审核任务
- 样本集支持纳管csv、点云等格式，增加样本集的评估统计

### 算法库

- 新增强化学习算法，支持Minds pore和Pytorch框架
- 优化已有算法的数据读取方式，日志输出格式等

### 训练平台（对应开发中心与训练中心，提供多种模型训练方式）

- 优化四种模型训练创建方式，包括Notebook建模、无代码建模、作业建模（基于自主调试代码提交训练任务）与AutoML（超参数调优）
- 提供工作流绘制模板，实现托拉拽提交模型训练任务
- 优化Notebook建模，提供多种版本的预置AI框架
- 增加无代码建模的算法的场景与数量，支持强化学习算法训练
- 支持无代码建模的训练过程中的评估结果输出与图表展示，支持显示训练进度百分比
- 优化多机多卡训练方式，支持定时提交训练任务

### 运行平台（对应推理平台，通过模型服务的方式支撑业务应用）

- 支持模型文件下发，支持边缘节点的批量部署
- 优化数据传输方式，**增加模型加密与签名认证**

### 其他优化

- 界面风格优化，提升平台易用性与可用性，包括创建标注项目流程，选择预置镜像模板启动开发环境，提交训练任务等

- 区分管理员、运维管理员与普通角色，设计不同用户界面，满足不同角色需求

- 预置大量AI资产，涉及样本集、**标注标签体系**，不同版本AI框架镜像、模型等

- 支持镜像安装新的依赖包保存成新镜像，便于保存开发环境

  

## HyperDL4.3 Release ，发布日期：2023-02

本次发版内容主要包括涉及数据中心，开发中心，算法中心，训练中心，模型中心、服务中心以及运维管理七大模块的功能升级。

### 数据中心

- 标注类型新增视频标注，斜框标注能力。其中视频标注场景，支持对视频文件预处理，包括视频切帧、视频分割等；支持目标追踪场景，视频帧继承标注
- 标注格式新增目标追踪[MOT17](https://motchallenge.net/data/MOT17/)，斜框标注[DOTA](https://captain-whu.github.io/DOTA/index.html)，[roLabelImg](https://github.com/cgvict/roLabelImg)格式
- 标注任务支持直接发布样本集，支持目标检测场景样本集合并功能

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
- 升级版本到[Kubernetes 1.21.14](https://kubernetes.io/docs/home/)，[Cuda 11.4](https://www.nvidia.cn/geforce/technologies/cuda/technology/)，华为版本[CANN ](https://www.hiascend.com/zh/software/cann),[MindX DL](https://www.hiascend.com/zh/software/mindx-dl)
- [软硬件支持情况说明](./支持说明.md)



