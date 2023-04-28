### 在 3090 上使用测试 MOSS

* 建议所有的工作，在docker上完成，尽量不要污染 host 系统。
* host 的 home 目录下 有一个 脚本 run_cuda_docker.sh  。 这个脚本启动一个 docker ， 并将所有 GPU 映射进 docker 。
* run_cuda_docker.sh 会 将 ~/workplace 里面的 目录 映射 进 docker ， 所有的代码 都 建议 保存在 workplace 里面 。
* 因为 docker 是独占使用 GPU ，所以使用的时候 请 大家 做好协同工作 。

### 训练工具 train.py 

```
train.py  input_model   output_checkpoint    data_file
```

* ``` input_model          需要训练的模型    ```
* ``` output_checkpoint    训练完后，保存模型 ```
* ``` data_file            训练数据存放的文件 ```

### 数据文件 data_file 为文本文件 ， 每行算一个数据 ， 类似下面 

```
随着互联网的发展，我们的个人信息越来越容易被泄露。因此，我们应该采取一些措施来保护我们的隐私，如使用强 密码、定期更改密码、不轻易透露个人信息等。
在商业领域，保护商业机密同样非常重要。企业应该采取措施来保护其商业机密，如加密文件、限制访问权限、定期 备份数据等。
网络安全不仅涉及到个人隐私和商业机密，还涉及到国家安全。政府和企业应该采取措施来保护国家的网络基础设施和数 据，如加强网络安全培训、建立安全防御系统、制定相关法律法规等。
```

### 测试工具 cli_chat.py 

```
cli_chat.py  input_model
```

* ``` input_model  加载的模型文件 ```


