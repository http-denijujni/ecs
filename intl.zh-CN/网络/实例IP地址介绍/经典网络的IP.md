---
keyword: [阿里云, ip, ecs, 公网带宽]
---

# 经典网络的IP

IP地址是您访问ECS实例或者您的用户访问部署在ECS实例的服务的主要方式。经典网络IP地址由阿里云统一分配，分为内网IP地址和公网IP地址。

## 内网IP地址

每台经典网络类型ECS实例一定会被分配一个IP地址用于内网通信，这个IP地址被称为内网IP地址。关于内网通信的详细信息，请参见[内网](/intl.zh-CN/网络/实例IP地址介绍/内网.md)。

内网IP地址可以应用于以下场景：

-   负载均衡。
-   同一局域网内ECS实例之间内网互访。
-   同一局域网内ECS实例与其他云服务（如对象存储OSS或者云数据库RDS）之间内网互访。

## 公网IP地址

如果您购买了公网带宽，即公网带宽不为0Mbit/s，阿里云会为您的经典网络类型实例分配一个公网IP地址。

公网IP地址可以应用于以下场景：

-   ECS实例与公网（Internet）之间互访。
-   不在同一局域网内的ECS实例与其他云服务之间互访。

**说明：** 经典网络类型ECS实例一经分配公网IP地址，既不能释放，也不能解绑。即使您通过续费降配或者按量实例更改带宽等功能将公网带宽值设为0Mbit/s，您的实例不能访问公网，但公网IP地址仍会保留。

## 计费

内网通信产生的流量免费，即使用内网IP地址不产生流量费用。

公网出网带宽收取费用，入网带宽免费。详情请参见[公网带宽计费](/intl.zh-CN/产品定价/计费项/公网带宽计费.md)。

## 操作方式

-   内网IP地址

    经典网络类型ECS实例一经分配了内网IP地址后，不支持修改。禁止在操作系统内部自行变更内网IP地址，否则会导致内网通讯中断。

-   公网IP地址
    -   在创建ECS实例时，只要您选择**分配公网IP地址**，您的ECS实例就会分配一个公网IP地址。详细步骤请参见[使用向导创建实例](/intl.zh-CN/实例/创建实例/使用向导创建实例.md)。
    -   您可以在成功创建ECS实例的六小时内修改公网IP地址。详细步骤请参见[修改公网IP地址](/intl.zh-CN/网络/修改IPv4地址/修改公网IP地址.md)。
    -   如果在创建ECS实例时未分配公网IP地址，您可以通过修改公网出网带宽分配。包年包月ECS实例请参见[包年包月实例修改带宽](/intl.zh-CN/实例/升降配实例/修改带宽配置/包年包月实例修改带宽.md)，按量付费ECS实例请参见[按量付费实例修改带宽](/intl.zh-CN/实例/升降配实例/修改带宽配置/按量付费实例修改带宽.md)。

## 组播和广播

经典网络内网IP地址不支持组播和广播。

