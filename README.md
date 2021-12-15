# biliroaming-go-server-docker
[biliroaming-go-server](https://www.github.com/JasonKhew96/biliroaming-go-server) 的 [docker](https://hub.docker.com/r/jasonkhew96/biliroaming-go-server) 镜像

## 文件夹说明
```
config/ - 设置文件
db/ - PostGreSQL 数据库密码
html/ - 自定义首页
proxy/ - nginx 证书配置
```

## 使用方式
### 使用 nginx
1. 复制 `config/config.example.yml` --> `config/config.yml`，修改 设置
2. 修改 PostgreSQL 数据库密码 `db/password.txt`
3. 复制证书到 `proxy/certs/` 里，分别为 `site.crt` 和 `site.key`
4. 当前文件夹执行 `docker-compose -f docker-compose.yml up -d --build`
### 裸连
1. 复制 `config/config.example.yml` --> `config/config.yml`，修改 设置
2. 修改 PostgreSQL 数据库密码 `db/password.txt`
3. 当前文件夹执行 `docker-compose -f docker-compose-http.yml up -d --build`
