---

copyright:
  years: 2016,2017
lastupdated: "2017-04-27"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 可用凭证
{: #available-credentials}

要将应用程序连接到服务，请使用随服务一起创建的凭证。[compose-redis-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-redis-helloworld-nodejs) 样本应用程序会示范如何使用 Node.js 连接到使用凭证的 {{site.data.keyword.composeForRedis}} 服务。

字段名称|描述
----------|-----------
`uri`|连接到服务时要使用的 URI，包括 (redis:)、管理用户名和密码、服务器的主机名和要连接到的端口号。
`uri_cli`|连接到数据库实例的 `redis-cli` 命令行。
`deployment_id`|在 Compose 内创建的服务的内部标识。
`db_type`|服务所提供的数据库类型；在本例中为 `redis`。
`name`|数据库部署名称。

{: caption="表 1. Compose for Redis 凭证" caption-side="top"}
