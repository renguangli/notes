## 2021

### 04-05 04-11

1. 点码整理（已完成）
2. 大数据平台架构文档组件版本、介绍、扩容方案补充
3. 数据权限申请优化
4. 数据治理空值/死值稽核校验

### 04-12 04-18

1. 数据治理功能演示
2. 整理不符合点码规则的场站
3. 数据写入cirroData times 的 flink 程序开发与部署
4. 云南大龙潭和西街口场站数据采集与入库
5. 数据治理空值稽核

### 04-19 04-25

1. 数据权限申请页面重构
2. 数据权限申请页面后台接口优化
4. 用户注册使用手册编写
5. cloudiip 自定义算子文档编写
6. 数据权限申请程序部署及使用手册编写
6. 数据采集程序部署使用文档编写
7. 所有文档转化为html页面并部署到服务器
8. 解决数据库连接不断开导致数据库崩溃的问题
9. 后台接口更新，前端页面修改部署更新

###　05-10 05-17

1. 服务器修改ip，数据治理，cloudiip，hadoop修改配置
2. 实时数据写入influxdb的flink程序开发
3. 历史数据采集程序开发
4. 更新升级cloudiip平台，修复电码不能有特殊字符的问题
6. 更新数据治理license
6. 风电历史数据采集
7. 将数据按省分库，按场站分表
8. 光伏聚合数据导出1个月数据



1. 光伏历史数据写入hdfs。
2. 风电数据写入influx和hdfs。
3. 聚合数据接口开发

### 05-18 05-25

1. 组分测量系统更新模型算法
2. 光伏历史数据写入 hdfs
3. 场站实时数据/聚合数据接口开发
4. influxdb/hadoop 数据目录迁移
5. 10分钟聚合数据写入到hdfs
6. 配合甲方检查数据质量
7. flink实时告警任务开发
8. 储能数据接入
9. 储能接口开发
10. 点码导入到cloudiip平台并按照省份、场站分组



1. flink实时告警任务自定义规则开发
2. influxdb时序数据迁移
3. 储能相关接口开发

### 05-31 06-01

1. hbase 数据转换程序测试部署
2. 实时历史聚合数据接口测试环境搭建（安装mysql，influxdb，接口应用部署）
4. 部署数据治理平台
4. rds连接测试，使用数据治理平台开发rds数据迁移作业调度
5. 数据治理服务器部署普罗米修斯exporter

### 06-05 06-13

1. xdyz/hnyz 光伏场站实时历史数据接入
2. flink实时报警任务开发

### 06-13 06-20

1. 十分钟聚合数据表重建：按天分区。将源表数据导入到分区表中
2. shell脚本定时检测 influxdb 进程，挂掉重启
3. yarn 上每天 0 点会起一个任务把资源占满，导致其他任务无法执行，（找不到在哪提交的，也不知道是什么任务）现在的解决方案是：定时脚本0点10分杀掉所有yarn任务
4. 拉取 不力格光伏场站5.27到6.8历史数据，李汉梁5.1到6.17历史数据
5. 修复 向 hdfs 写入文件时偶尔出现坏块的问题
6. 修复储能 flink 告警任务无数据的问题
7. 海上风电导出1000个点5.1到6.1的数据
8. 完善用户注册，数据接入，数据申请文档

### 06-20 06-27

1. 储能告警新增3个字段

### 07-12 -07-19

1. ntp 时间同步服务器配置
2. 修改 hive 字段名称



## 项目周报

### 华能

1. http接口数据采集程序开发/部署
2. 数据采集程序新增采集个别点数据的脚本
3. 编写数据采集程序使用文档
4. 开发、部署kafka数据写入到hive的flink程序
5. 整理点码并导入到MySQL数据库中,一个省的点码一个表
6. 在cloudiip按照省份分类为191个电场创建mqtt接入，并整理成csv文件
7. iotdb集群/单机部署
8. mqtt / kafka 数据采集调试
9. 数据权限申请/查看/审批/点码下载页面及后端接口开发，集成 cas 单点登录 
10. 实时、历史数据接口开发,调试
11. 大数据平台架构文档组件版本、介绍、扩容方案补充

 **数据治理**

1. 数据治理平台迁移映射/任务调度等功能测试
2. 数据治理基础目录创建
3. 开发数据治理死数和空值稽核模板
4. 创建相关稽核表
5. 编辑死数和空值稽核校验的使用文档
6. 使用数据治理调度器调度死数和空值稽核校验任务

## 绩效考核

## 2021 

### 第一季度

|      |                    |                                                              |      |                                                              |
| ---- | ------------------ | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| 1    | XM-20210202-204581 | 明确商机-2020-国电新能源-新能源场站智能管控平台研建          | 22   | 1.http接口数据采集程序开发与部署2.数据写入hdfs和cirrdata times的flink程序开发与部署3.数据权限申请、审批页面与后端接口开发与部署。4.历史、实时数据接口开发与部署5.数据治理空值稽核 |
| 2    | XM-20200910-203036 | 明确商机-2020-忻州神达-神达集团安全生产综合信息化平台        | 7    | 1.煤炭全组分测量系统前后端开发、现场环境搭建、部署、测试与维护2.后端实时读txt文件写入csv，按分钟切割，供py算法使用3.后端每分钟调用py算法模型，将结果保存，供前端展示历史曲线使用 |
| 3    | XM-20201012-203203 | 实施-2020年-冀北电科院-2020年新能源所新能源大数据分析平台二期扩建 | 71   | 1.光伏储能模块接口对接2.大屏接口调整3.大屏接口优化，应用接口优化4.风电模块涉网预警脱网预警算法重构5.解决光伏储能页面不能跳转门户页面问题 |
