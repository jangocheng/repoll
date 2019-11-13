# repoll
使用django框架编写的redis的管理平台

## 项目简介
### 主要功能（当前功能）
- Redis的申请、审批、配置上线
- Redis的监控、启动以及停止操作平台化管理
- 权限管理依赖django 框架
![image](https://github.com/NaNShaner/repoll/blob/master/images/main.png)

# 环境依赖
- python3
- pip3 install django==2.0
- pip3 install djangorestframework
- pip3 install django-crontab
- pip3 install mysqlclient
- pip3 install redis
- pip3 install paramiko
- pip3 install pyecharts(pyecharts-1.5.1)
- pip install django-simpleui
- apt-get install python-dev default-libmysqlclient-dev
- apt-get install python3-dev

# 部署步骤
* 安装完成环境依依赖
* 执行以下命令完成simpleui的静态资源离线可访问
python3 manage.py  collectstatic
* 开启redis的qps监控执行以下命令
python3 manage.py crontab add

# 标准化申请流程
* 分配普通用户权限（dev或者ops角色）
* 领导层进行审批（boss角色）
* 管理员（dba角色）进行配置上线

# Todo list
- 支持哨兵模式和集群模式
- 监控独立展示，包括qps、内存使用率、客户端链接以及慢查询等
- 支持web console

# 声明
该项目将长期维护，期望有对redis有平台化管理的朋友加入一起维护。