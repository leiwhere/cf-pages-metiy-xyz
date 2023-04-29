### 在 3090 上使用测试 MOSS

* 建议所有的工作，在docker上完成，尽量不要污染 host 系统。
* host 的 home 目录下 有一个 脚本 run_cuda_docker.sh  。 这个脚本启动一个 docker ， 并将所有 GPU 映射进 docker 。
* run_cuda_docker.sh 会 将 ~/workplace/exp 映射进 docker ，名字叫 /home/dev ， 所有的代码 都 建议 保存在 workplace 里面 。
* 因为 docker 是独占使用 GPU ，所以使用的时候 请 大家 做好协同工作 。

### 训练工具(背诵阶段) train_moss.py

```
train_moss.py  input_model  out_model  data.txt
```

### 训练工具(finetune) finetune_moss.py

```
finetune_moss.py
```

### 训练工具(LORA) LORA_moss.py


```
```

### 测试工具 moss_cli_chat.py 

```
```

### 训练数据 

```
```

