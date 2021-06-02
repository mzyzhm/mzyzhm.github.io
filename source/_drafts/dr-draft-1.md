---
layout: draft
title: dr_draft
date: 2021-02-01 20:05:53
tags:
---


DR工作记录

# 1. terraform plan报错

ecs cluster被手动删除后，terraform plan会报ClusterNotFoundException,

[ECS plan fails if cluster has been deleted outside Terraform](https://github.com/hashicorp/terraform-provider-aws/issues/15917)

解决办法1： 升级aws provider version到3.0+,高版本fix了这个bug， 同时也需要升级terraform版本

解决办法2: 从terraform state中删除报错的service

```terraform state rm aws_ecs_service.service```

# 2. postgre数据库做snapshot脚本实现

# 3. copy ecr image 从us-east-1到us-west-2脚本实现

# 4. dr环境不再创建不需要的repo

# 5. 注意redis cluster 6.x

使用rout53指向dr环境redis的DNS, 不修改api配置

# 6. lambda可以移除
lambda不再使用，修改脚本移除

# 7. dr环境禁止创建aws_instance



