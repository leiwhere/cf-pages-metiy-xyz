### 训练过程

* [预训练](train/pretrain.md) 通常采用 **自监督学习**，背诵 **领域** 相关知识，通常用 PPL 即困惑度来评价
* [Finetune](train/ft.md) 通常也采用 自监督学习 ， ~~学习~~ 背诵 领域 相关 知识，通常用 PPL 即困惑度来评价
    * 然后 通过 prompt 工程 ， 学习 具体 知识，此阶段 PPL 并不具备实质性的评价意义
* 然后 通过 打分 系统 或者 奖赏模型 ， 进行 价值观 学习 

### 参考库
* PEFT 用于 LoRA 训练
* TRL 用于 奖赏模型和PPO训练

### 训练框架

* [DeepSpeed](https://www.deepspeed.ai/)
* [Lightting](https://www.lightning.ai/)
* [Accelerate](https://huggingface.co/docs/accelerate/index)

### 标注工具

#### Label Studio 社区版
不推荐原因：
- 界面无中文支持
- 访问 sentry.io 回传运营数据
- 导入 CSV 有时会出错，原因不明

#### Prodi.gy 
待评估