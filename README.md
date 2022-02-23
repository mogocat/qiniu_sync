首先感谢原作者，我适配了Python3，并且添加了删除云端文件的同步功能。如果不想删除云端文件，请注释掉check_delete函数。
请先下载到本地，在本地删除文件后，再同步，即可自动删除云端多余的文件。请在本地做好备份。


以下为原作者说明文件
--

#qiniu_sync

基于七牛Python SDK写的一个同步脚本。
支持批量比较文件，差异增量更新、批量更新。

## 使用方式

* 安装七牛Python SDK
`pip install qiniu`

* 填写脚本文件(qiniusync.py)的配置信息
```
access_key = ''
secret_key = ''
bucket_name = ''
bucket_domain = ''
```
>注册后可以拿到对应的信息 

* 将脚本文件(qiniusync.py)拷贝到待同步根目录

* 运行脚本
```
python qiniusync.py
python qiniusync.py down
python qiniusync.py down [文件路径前缀]
```
