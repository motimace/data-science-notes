## 查看环境信息、包信息
## conda info
```
# 显示所有信息 -a, --all
conda info -a

# 显示所有环境路径 -e, --envs
conda info -e
```
## 创建环境、重命名
### conda create
```
# 创建环境需要指定参数-n 环境名或者-p 完整路径
# 在默认路径创建环境
conda create -n env_name
# 在指定路径创建环境
conda create -p path_to_env/env_name
# 创建环境时可以指定需要安装的包，通常指定某个版本的python
conda create -n env_name python=3.10
```
### conda activate/deactivate
```
# 激活某个环境，即从base环境切换到此环境
conda activate env_name
# 退出某个环境，即从当前活动环境切换至base环境
conda deactivate
```
### conda rename
```
# 环境重命名
# 指定环境名称
conda rename -n env1 env2
# 指定环境路径
conda rename -p path/env1 env2
```
## 安装、更新、卸载包
### conda install
```
# 在当前活动环境中安装scipy
conda install scipy
# 在环境myenv中安装多个包
conda install -n myenv scipy curl wheel
# 在环境中安装指定版本python
conda install -p path/env1 python=3.10
```
### conda update
```
# 在当前活动环境中更新scipy
conda update scipy
# 在环境myenv更新scipy
conda update -n myenv scipy
# 更新环境中所有的包
conda update --all
```
### conda remove
```
# 移除当前活动环境中的包：scipy
conda remove scipy

# 移除环境myenv中的一系列包
conda remove -n myenv scipy curl wheel

# 移除环境中所有包，即移除此环境
conda remove -n myenv --all
```
