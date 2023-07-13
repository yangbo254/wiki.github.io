# Ubuntu 20.04 开启Google BBR的方法

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