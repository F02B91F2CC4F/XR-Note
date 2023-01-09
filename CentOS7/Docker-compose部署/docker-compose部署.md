## 概述

docker-compose.yml 已经集成了下列组件

| 组件:版本                                                    | 中文名称                                     |
| ------------------------------------------------------------ | -------------------------------------------- |
| nginx:1.23.3                                                 | nginx前端代理服务                            |
| bladex/sentinel-dashboard:1.8.0                              | 流量防卫兵                                   |
| seataio/seata-server:1.4.2                                   | 分布式事务                                   |
| mysql:8.0.31                                                 | mysql数据库                                  |
| redis:alpine3.17                                             | redis                                        |
| nacos/nacos-server:v2.1.2                                    | nacos注册与配置中心                          |
| apache/rocketmq:4.9.4<br />apache/rocketmq:4.9.4<br />apacherocketmq/rocketmq-dashboard:1.0.0 | rocketMQ消息队列、rmq-broker、rocketMQ控制台 |
| lmenezes/cerebro:0.9.2<br />kibana:7.8.0<br />elasticsearch:7.8.0 | ES                                           |

## 1.将 docker-compose 文件夹复制到服务器

```shell
# 进入 docker-compuse 目录，运行下列指令
docker-compose up -d
```

