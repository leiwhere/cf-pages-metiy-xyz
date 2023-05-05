### 参考资料

* [github  ssbuild  moss finetune](https://github.com/ssbuild/moss_finetuning)
* [ssbuild deep training](https://github.com/ssbuild/deep_training)
* [在 docker 中使用 moss](https://github.com/linonetwo/MOSS-DockerFile)
* 依据 [弥补斯坦福70亿参数“羊驼”短板，精通中文的大模型来了，已开源](https://www.thepaper.cn/newsDetail_forward_22396024) ， batchsize 64 ， lr 3e-6 ，epochs 3 ，weight_decay 0.001 ， warmup_rate 0.1 ， lr_scheduler linear

### 3090 notebook

[notebook ， 可以用来处理 数据 ， LMFlow 的数据 在 LMFlow/data 下 ](http://10.254.28.4:8888/)

### 在 3090 上使用测试 MOSS

* 建议所有的工作，在docker上完成，尽量不要污染 host 系统。
* host 的 home 目录下 有一个 脚本 run_cuda_docker.sh  。 这个脚本启动一个 docker ， 并将所有 GPU 映射进 docker 。
* run_cuda_docker.sh 会 将 ~/workplace/exp 映射进 docker ，名字叫 /home/dev ， 所有的代码 都 建议 保存在 workplace 里面 。
* 因为 docker 是独占使用 GPU ，所以使用的时候 请 大家 做好协同工作 。
* 建议所有工作 ， 尽量在 notebook 中 完成 。

### 训练工具(背诵阶段) train_moss.py

```
train_moss.py  input_model  out_model  data.txt
```


### 训练工具(finetune) finetune_moss.py

```
usage: finetune_moss.py [-h] [--model_path MODEL_PATH] [--data_dir DATA_DIR] [--output_dir OUTPUT_DIR]
                        [--log_dir LOG_DIR] [--max_seq_len MAX_SEQ_LEN] [--train_bsz_per_gpu TRAIN_BSZ_PER_GPU]
                        [--eval_bsz_per_gpu EVAL_BSZ_PER_GPU] [--weight_decay WEIGHT_DECAY]
                        [--learning_rate LEARNING_RATE] [--warmup_rates WARMUP_RATES] [--n_epochs N_EPOCHS]
                        [--save_step SAVE_STEP] [--eval_step EVAL_STEP] [--seed SEED]
optional arguments:
  -h, --help            show this help message and exit
  --model_path MODEL_PATH
  --data_dir DATA_DIR
  --output_dir OUTPUT_DIR
  --log_dir LOG_DIR
  --max_seq_len MAX_SEQ_LEN
  --train_bsz_per_gpu TRAIN_BSZ_PER_GPU
  --eval_bsz_per_gpu EVAL_BSZ_PER_GPU
  --weight_decay WEIGHT_DECAY
  --learning_rate LEARNING_RATE
  --warmup_rates WARMUP_RATES
  --n_epochs N_EPOCHS
  --save_step SAVE_STEP
  --eval_step EVAL_STEP
  --seed SEED


examples:

```

### 训练数据 finetune

```
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

