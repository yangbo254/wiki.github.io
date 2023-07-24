# docker about
## docker install
### 通用方法
```shell
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

### Amazon Linux
```shell
yun install docker
```

## docker-compose install
### 最新发行版本地址
https://github.com/docker/compose/releases

### 安装
```shell
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

### 验证
```bash
docker-compose version
```

## Github加速
https://ghproxy.com/

## docker pull加速
https://dockerproxy.com/

https://gist.github.com/y0ngb1n/7e8f16af3242c7815e7ca2f0833d3ea6

## 泛域名证书
https://ssl.ioiox.com/

## GEOIP
https://github.com/Loyalsoldier/geoip