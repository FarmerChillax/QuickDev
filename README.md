# QuickDev
快速启动后端开发环境

后端开发通常需要使用到 MySQL 与 redis，每次开发都要安装、配置无疑十分麻烦。本项目通过 docker-compose 将 MySQL 与 redis 打包集成，一键启动开发所需环境。
## 环境要求
- docker: `Docker Compose version v2.10.2`

## Index
- 基础开发环境: `main` 分支
- 微服务开发环境: `micro` 分支

## 快速开始

1. 克隆本项目
```shell
$ git clone git@github.com:FarmerChillax/QuickDev.git
```
2. 进入到项目根目录

```shell
$ cd QuickDev
```

3. 执行以下命令
```shell
$ docker-compose up -d
```

### 打开管理页面
1. MySQL 管理页面
   1. 访问地址: `http://localhost:1000/`
   2. 数据库账号: `admin`
   3. 密码: `123456`
   4. 管理员账号: root
   5. 密码: `123456`
2. redis 管理页面
   1. 访问地址: `http://localhost:2000/`
   2. 账号: `admin`
   3. 密码: `123456`


## 环境变量描述
如需更改自行修改 `.env` 文件对应配置
| 变量名              | Description                 |
| :------------------ | :-------------------------- |
| TZ                  | 时区设置                    |
| NETWORKS_DRIVER     | docker 网络模式             |
| LIMIT_MEMORY_MYSQL  | MySQL 资源限制              |
| LIMIT_MEMORY_REDIS  | redis 资源限制              |
| MYSQL_PORT          | MySQL 访问端口              |
| MYSQL_DATABASE      | MySQL database 名           |
| MYSQL_USERNAME      | MySQL 账号                  |
| MYSQL_PASSWORD      | MySQL 密码                  |
| MYSQL_ROOT_PASSWORD | MySQL 管理员密码            |
| REDIS_PORT          | Redis 端口                  |
| MySQL_PATH          | 宿主机上 MySQL 数据存放路径 |
| REDIS_PATH          | 宿主机上 redis 数据存放路径 |