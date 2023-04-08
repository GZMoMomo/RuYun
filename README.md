# RuYun
儒韵电商工作日志

## 2023.3.13
1. 入职
2. 通过情报通的电商产品数据发掘一个电子影音品类做自有品牌。
3. 初步思路：先将数据存储在数据库中，进行数据清洗，根据bi分析出产品类目（耳机、音响、唱片机），再分析出二级分类（蓝牙音响、便捷音响），再根据用户消费画像和产品特点数据确定产品的属性（颜色、材质），再结合爆款商品的外貌、功能给予参考。

## 2023.3.14
1. 将情报通中关于品类的销量、销售额数据抽取到ods并清洗建立dwd层。
2. 编写rpa程序自动化抽取每个子品类的top100宝贝。

## 2023.3.15
1. 将子品类的top100数据抽取到ods层并建立dwd层，冗余销售额排名和销量排名的数据。
2. 将top100数据与品类销量销售额数据建立宽表。
3. 划分时间维度、地域维度、产品类目维度。
4. 关注指标
-  关注产品成交均价（价格段）
-  平均销量、销售额（市场规模）
-  平均销量、销售额增长率（增长趋势）
-  总销售额、销量排名
-  销售额、销量增长率
-  市场占有率
-  各品类top100产品份额占比

## 2023.3.16
1.做BI报表，新增指标
- 销售额市场占比与销量市场占比差值（这个数反映了产品的平均销售价格（ASP，Average Selling Price）相对于市场平均水平的表现。当总销售金额市场占比高于总销售数量市场占比时，说明该产品的平均销售价格较高；相反，如果总销售数量市场占比高于总销售金额市场占比，则说明该产品的平均销售价格较低。这个数可以用来评估产品定价策略的合理性，或者用于与竞争对手的产品进行比较。）

## 2023.3.17
1. 安装Superset并配置环境。
2. 使用echarts绘图。

## 2023.3.20
1. 学习docker zookeeper Kafka
2. 清洗数据做etl并优化报表。

## 2023.3.21
1. 根据不同地点的天气数据（温度、最高温、最低温）重构维度 列转行。使用MySQL中的UNION ALL和SELECT语句来实现这个转换

## 2023.3.22
1. 使用chatgpt编写python代码，实现价格段数据复杂数据结构的转换

## 2023.3.23 -3.25
1. 使用powerBI做耳机、音响数据分析报告，清洗细分类目属性数据
2. 学会看文档和源码解决配置问题。

## 2023.3.27-3.29
### chatgpt接入钉钉
[ChatGPT-接入钉钉机器人技术架构.pdf](https://github.com/GZMoMomo/RuYun/files/11097228/ChatGPT-.pdf)

## 2023.3.30 - 4.3
1. chatgpt应用开发，接入钉钉，使用mysql实现联系用户历史信息上下文，采用多线程提高程序响应效率（在多人同时请求的情况下）
2. 蓝牙耳机市场分析报告
3. 流式数据架构发展 
    - mysql-Kafka connect-Kafka-fink-clickhouse
    - mysql-debezium-kafka-flink-clickhouse 实现cdc，通过监控mysql日志
    - mysql-streamset-clickhouse ETL一体式平台 最新版本已经闭源了
    - mysql-flinkcdc-flink-clickhouse 使用flinkcdc，一体化ETL，减少维护成本

## 2023.4.4-2023.4.6
1. chatgpt应用开发，使用redis缓存用户聊天记录，接入dall e 图像生成API。
2. 完成耳机数据报告 包含用户画像

## 2023.4.7-2023.4.8
1. gpt出现问题，多用户同时发送请求时，由于API生成答案速度慢，会出现timeout和代理服务器阻塞掉。引入消息队列和多线程并发处理请求。
