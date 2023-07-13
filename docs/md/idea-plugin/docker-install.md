## docker install

```shell
 curl -fsSL https://get.docker.com -o get-docker.sh
 sudo sh get-docker.sh
```

## docker-compose install
### 最新发行版本地址
https://github.com/docker/compose/releases

### 安装
```shell
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

### 验证
```bash
docker-compose version
```