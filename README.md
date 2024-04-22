# 第五课作业复现及笔记

## 环境部署

### 安装环境

```python
studio-conda -t lmdeploy -o pytorch-2.1.2
```

![image-20240422223620347](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422223620347.png)

![image-20240422224907088](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422224907088.png)

### 安装0.3版本的lmdeploy。

![image-20240422225342721](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422225342721.png)

### 新建pipeline_transformer.py文件

![image-20240422230448224](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422230448224.png)

### 测试模型

![image-20240422230708545](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422230708545.png)

![image-20240422231123652](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422231123652.png)

可以看出，这个推理也是占用了巨大内存

## 使用LMDeploy与模型对话

![image-20240422231859066](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422231859066.png)

### 以命令行方式与InternLM2-Chat-1.8B大模型对话

![image-20240422232857184](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20240422232857184.png)

## 笔记

本文介绍了LMDeploy环境部署的步骤和方法，包括创建开发机、conda环境，安装LMDeploy，以及使用LMDeploy进行模型对话、模型量化和服务部署等。文章还介绍了如何使用LMDeploy运行视觉多模态大模型和第三方大模型，并比较了LMDeploy与Transformer库的推理速度差异。

### 关键要点

1. LMDeploy环境部署包括创建开发机和安装LMDeploy。
2. 使用LMDeploy与模型对话，可以使用Transformer库运行模型并使用LMDeploy与模型对话。
3. LMDeploy模型量化包括设置最大KV Cache缓存大小和使用W4A16量化。
4. LMDeploy服务包括启动API服务器和命令行客户端连接API服务器。
5. Python代码集成包括Python代码集成运行1.8B模型和向TurboMind后端传递参数。