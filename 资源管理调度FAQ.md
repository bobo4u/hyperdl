# FAQ常用问题
## 底层资源管理
> > 这是关于`HyperOP`产品客户常用问题

### 1、我们的系统用户权限是怎么管理的？比如给用户分配权限后，是分配了机器的全部权限，还是分配了单张/多张GPU资源的权限？是否固定好了显存/算力的上限供用户使用？是否可以以训练/推理任务为单位，基于任务由平台自动分配GPU资源？

平台通过给用户绑定组织，给每个组织分配资源配合（可以选择开启或者关闭），来限制当前用户使用平台资源。

提交任务的时候，可以选择CPU，内存和GPU卡的数量。

### 2、平台是否设计GPU虚拟化？是否使用K8S？

平台目前已支持`Nvidia GPU`主流加速卡的虚拟化能力，是通过`K8S`的`Device Plugin`的机制来实现。

` Device Plugin`：K8s制定设备插件接口规范，定义异构资源的上报和分配，设备厂商只需要实现相应的API接口，无需修改kubelet源码即可实现对其他硬件设备的支持。`Extended Resource`：`Scheduler`可以根据Pod的创建删除计算资源可用量，而不再局限于CPU和内存的资源统计，进而将有特殊资源需求的Pod调度到相应的节点上。

  通过Device Plugin 异构资源调度流程如下：

1. Device plugin 向kubelet上报当前节点资源情况
2. 用户通过yaml文件创建负载，定义Resource Request
3. kube-scheduler根据从kubelet同步到的资源信息和Pod的资源请求，为Pod绑定合适的节点
4. kubelet监听到绑定到当前节点的Pod，调用Device plugin的allocate接口为Pod分配设备
5. kubelet启动Pod内的容器，将设备映射给容器

![img](./images/异构资源调度示意图.jpg)

### 3、是否使用docker？如果使用docker分配不同节点的GPU资源时，是否影响通讯速度？比如分配了A机器2张卡和B机器两张卡，是否比相同分配模式下不使用docker速度更慢？



### 4、是否有不适用docker、k8s的gpu资源分配方案，如简单的物理分配？容器分配有什么弊端？



## 部署实施过程
>  这是关于`Docker`、`Kubernetes`及其他云原生组件常见问题归纳

### `kubeEdge`部署成功之后，`edgecore`组件正常，但是`node`节点都是提示`notready`

因为`cloudcore`这个默认资源给的太少，没法承载几百个节点的访问，通过调大`pod`的资源。







## 模型训练问题

>  这是关于深度学习训练及推理知识常见问题归纳



