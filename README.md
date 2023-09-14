# 如何在vps上安装python 3.11.5
如何在vps服务器上安装python3.11.5



## 服务器系统
- debain


## 安装依赖
```bash
sudo apt update && sudo apt upgrade
sudo apt install wget build-essential libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
```

## 获取python相应版本源码

```bash
cd ~
wget https://www.python.org/ftp/python/3.11.5/Python-3.11.5.tgz
```

## 解压python源码

```bash
tar xzf Python-3.10.0.tgz
```

## 编译源码
```bash
cd Python-3.10.0
./configure --enable-optimizations

#--enable-optimizations为优化性能选项，其余类似的还有 --prefix=PATH 指定安装目录……，可根据需要进行选择。
#默认安装路径为 /usr/local/bin
```

## 安装python
```bash
make altinstall

#altinstall用于防止编译器覆盖默认Python版本
```


end

