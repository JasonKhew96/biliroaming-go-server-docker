# biliroaming-go-server-docker
docker-compose 规则

## 使用方式
### 使用 nginx
1. 复制 `production.env.example` --> `production.env`，修改 环境变量
2. 修改 PostgreSQL 数据库密码 `db/password.txt`
3. 复制证书到 `proxy/certs/` 里，分别为 `site.crt` 和 `site.key`
4. 当前文件夹执行 `docker-compose -f docker-compose.yml up -d --build --force-recreate`
### 裸连
1. 复制 `production.env.example` --> `production.env`，修改 环境变量
2. 修改 PostgreSQL 数据库密码 `db/password.txt`
3. 当前文件夹执行 `docker-compose -f docker-compose-http.yml up -d --build --force-recreate`
