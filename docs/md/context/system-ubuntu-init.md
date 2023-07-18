## Ubuntu 20.04 开启Google BBR的方法

### 设置
```shell
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
```
```shell
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
```
```shell
sysctl -p
```


### 查询
```shell
sysctl net.ipv4.tcp_available_congestion_control
```
```
# sysctl net.ipv4.tcp_available_congestion_control
net.ipv4.tcp_congestion_control = bbr
```
```shell
lsmod | grep bbr
```
```
# lsmod | grep bbr
tcp_bbr                20480  14
```

## Ubuntu 软件仓库镜像(清华源)

https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/