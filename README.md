# 国外互联网公司大数据技术架构研究

## Google大数据技术架构探秘
### 一、Google

Google是大数据时代的奠基者 ，其大数据技术架构一直是互联网公司争相
学习和 研究的重点，也是行业大数据技术架构的标杆和示范。

#### 1、谷歌的数据中心

谷歌已经建立了世界上最快、最强大、最高质量的数据中心，它的8个主要
数据中心都远离其位于加州山景城的总部，分别位于美国南卡罗来纳州的伯克利
郡，爱荷华州的康瑟尔布拉夫斯，乔治亚州的道格拉斯郡，俄克拉荷马州的梅斯
郡，北卡罗来纳州的勒努瓦，俄勒冈州的达尔斯；另外2个在美国境外，分别是
芬兰的哈米纳和比利时的圣吉斯兰。此外，谷歌公司还在中国香港和中国台湾，
以及新加坡和智利建立了数据中心。

#### 2、谷歌新一代搜索引擎平台和大数据分析核心技术

Google是GFS MapReduce BigTable的缔造者，但Google 新一代搜索引擎平
台正逐步用更强计算能力的系统来替换原有系统，新一代搜索引擎平台有几个核
心技术系统：

一是用基于Percolator的增量处理索引系统来取代MapReduce批处理索引系
统，这个索引系统被称作Caffeine，它比MapReduce批处理索引系统搜索更快。

Google大数据技术架构探秘

二是专为BigTable设计的分布式存储Colossus，也被称为GFS2（二代
Google文件系统），它专为建立Caffeine搜索索引系统而用。

三是列存储数据库BigTable，但为了更好地支持大数据集的互动分析，
Google推出了Dremel和PowerDrill。Dremel被设计用来管理非常大量的大数据
集（指数据集的数量和每数据集的规模都大），而PowerDrill则设计用来分析少
量的大数据集（指数据集的规模大，但数据集的数量不多）时提供更强大的分析
性能。

四是为Google Instant提供服务的实时搜索引擎存储和分析架构。

五是Pregel，这是谷歌更快捷的网络和图算法。

在谷歌新一代搜索引擎平台上，每月40亿小时的视频，4.25亿Gmail
用户，150,000,000 GB Web索引，却能实现0.25秒搜索出结果。

#### 3、谷歌基础云服务

基于Colossus，谷歌为用户提供计算、存储和应用的云服务。计算服务包括
计算的引擎（ComputeEngine）和应用APP的引擎(AppEngine)；存储服务包括云
存储（CloudStorge）、云SQL(CLoudSQL)、云数据存储（Cloud DataStore）、永
久磁盘等服务；云应用服务包括BigQuery、云终端（Cloud Endpoints）、缓冲、
队列等。

#### 4、谷歌的大数据智能应用服务

Google提供的大数据分析智能应用包括客户情绪分析、交易风险（欺诈分析）、
产品推荐、消息路由、诊断、客户流失预测、法律文案分类、电子邮件内容过滤、
政治倾向预测、物种鉴定等多个方面。据称，大数据已经给Google每天带来2300
万美元的收入。

例如，一些典型应用如下：

（1）基于Map Reduce，Google的传统应用包括数据存储、数据分析、日志
分析、搜索质量以及其他数据分析应用。

（2）基于Dremel系统， Google推出其强大的数据分析软件和服务 —
BigQuery，它也是Google自己使用的互联网检索服务的一部分。Google已经开
始销售在线数据分析服务，试图与市场上类似亚马逊网络服务(Amazon Web
Services)这样的企业云计算服务竞争。这个服务，能帮助企业用户在数秒内完成
万亿字节的扫描。

（3）基于搜索统计算法，Google推出搜索引擎的输写纠错、统计型机器翻
译等服务。

（4）Google的趋势图应用。通过用户对于搜索词的关注度，很快的理解社
会上的热点是什么。对广告主来说，它的商业价值就是很快的知道现在用户在关
心什么，他们应该在什么地方投入一个广告。据此， Google公司也开发了一些
大数据产品，如“Brand Lift in Adwords”、“Active GRP”等，以帮助广告客户分析和
评估其广告活动的效率。

（5）Google Instant。输入关键词的过程，Google Instant 会边打边预测可
能的搜索结果。

谷歌的大数据平台架构仍在演进中，追去的目标是更大数据集、更快、更准
确的分析和计算。这将进一步引领大数据技术发展的方向。

http://s12.sinaimg.cn/bmiddle/4aa50b4dtx6DoIHk8Zl0b&690
## 二、Yahoo

Hadoop是当前最流行的大数据技术架构，很多大数据应用都是建立在
Hadoop平台基础之上。很多人都知道Hadoop是Apache基金会的顶级开源项目，
但并不是每个人都知道，在Hadoop的演进发展中，70%的贡献是来自Yahoo公
司。Yahoo公司是Hadoop平台最大的用户、最有力的应用支持者和Hadoop商
业化的重要推动者，Hadoop一直是Yahoo公司云计算平台的核心，Yahoo公司
最大的单个Hadoop集群由4000个节点组成，Yahoo公司的推荐系统、广告分析
等应用均建立在Hadoop分布式计算平台上，Yahoo公司通过开发者论坛等方式
每年培养了大量掌握Hadoop平台的专业技术人员，Yahoo公司分拆出来并投资
的Hadoop技术研发部门－Hortonworks目前是全球发展最快的Hadoop商业化公
司之一。Yahoo 公司并没有躺在这些成绩上沾沾自喜，相反他们在积极推进
Hadoop2.0——Yahoo新一代大数据技术架构。

Yahoo的新一代大数据技术架构由以下几个部分组成：

#### 1、核心YARN

YARN或称为MapReduce2.0是这个技术架构的核心，它可以看作Yahoo新一
代大数据平台的操作系统。为了解决Hadoop1.0的性能瓶颈问题，YARN将
MapReduce中一个JobTacker中所具有的两个主要功能（资源管理和作业调度/
监控）实现了分离，主要方法是创建一个全局的资源管理器（ResourceManager，
RM）和若干个针对应用程序的应用主服务器（ApplicationMaster，AM）。经过
这样的变化，YARN在扩展性方面有很大改进，可以支持10000+计算机集群，同
时改进了MapReduce的性能，并且支持Hadoop之外的其他计算框架，如低延时、
流计算等框架。

计算处理框架。除了支持批处理的Hadoop之外，还有Spark和Storm等计
算框架的集成。其中，Hadoop用于离线数据分析，Spark用于多迭代批处理数据
分析， Storm则是用于流数据的实时分析和预测。借助YARN，Yahoo将大数据
离线、近线和实时数据实现了整合。

### 2、Storm

Storm原本是Twitter的流计算工具。Yahoo在新一代技术架构实践中，将
Storm与YARN整合成为Storm-YARN来支持的实时的流计算分析。Storm是专门
针对实时数据类型（即流数据）的计算分析框架，在流数据不断变化运动的过程
中实时地进行分析，捕捉到可能对用户有用的信息，并把结果迅速发送出去。例
如，为了支持个性化搜索广告，系统需要实时处理来自几百万唯一用户每秒成千

http://s8.sinaimg.cn/bmiddle/4aa50b4dtx6DoJUe1Ztd7&690
上万次的查询，并即时分析用户的会话特征来提高广告相关性和预测模型的准确
度。

### 3、Spark

Spark是发源于美国加州大学伯克利分校AMPLab的集群计算平台，已正式
申请加入Apache孵化器，Yahoo新一代技术架构将其YARN进行整合。Spark立
足于内存计算，从多迭代批量处理出发，兼收并蓄数据仓库、流处理和图计算等
多种计算范式，具有轻量、快速计算等特点。Spark基于Scala语言，是一个比
Hadoop代码行少的轻量级系统，但它的计算速度非常快，对小数据集能达到亚
秒级的延迟，对大数据集典型的迭代机器学习、即席查询、图计算等应用，Spark
版本比基于MapReduce、Hive和Pregel的实现快上十倍到百倍。

### 4、存储层

底层存储则仍是基于Hadoop的文件系统HDFS和NOSQL数据库HBase。

尽管，目前以YARN为核心的新一代技术架构还有很多方面需要完善，但
其在Yahoo中战略地位已经基本确立。其一贯的开源策略，也将给大数据业界带
来福音。

## 三、Amazon

大数据分析通常需要依靠大量分布式的计算基础设施、分布式框架和计算存
储系统。但不是每个用户都有条件建立这些大数据基础设施。巨大市场需求和用
户有限的计算资源之间的矛盾越来越突出，在这种背景下，大数据云服务应运而
生。Amazon、Google等互联网公司都看中了大数据云服务市场的蛋糕，纷纷推
出大数据分析的WEB服务来提供给用户有偿使用。

### 1、Amazon Elastic MapReduce（EMR）

Amazon Elastic MapReduce（EMR）是Amazon提供的大数据分析云服务。
这是一个商业化的Hadoop基础设施服务，基于它所提供的分布式计算能力，企
业、研究人员、数据分析师和开发人员能够方便地根据自身需求来处理和分析大
量数据。它通过在 Amazon 云上运行的虚拟服务器的Hadoop集群来分析客户提
交的海量数据分析作业。自 2009 年以来，全球数千客户使用 Amazon EMR 来
启动数百万的集群。在 Hadoop 架构上面运行的开源项目，例如 Hive、Pig、HBase、
DistCp、Ganglia、Mahout 和 R，都已与 Amazon EMR 集成。Amazon EMR能即
时灵活配置自身所需容量大小，执行数据密集型应用计算，完成 Web 索引、数
据挖掘、日志文件分析、机器学习、财务分析、科学模拟和生物信息研究等任务。

云中共享的大数据分析服务

### 2、Amazon EC2和S3

Amazon EMR是基于 Amazon Elastic Compute Cloud (Amazon EC2) 技术和
Amazon Simple Storage Service (Amazon S3) 技术的 Web规模大数据分析基础设
施服务。Amazon EMR 服务与AWS的其他Web服务实现了高度集成。在 Amazon
EMR 上运行的 Hadoop 集群使用 Amazon EC2 实例作为虚拟 Linux 服务器用
于主节点和从属节点、将 Amazon S3 用于输入和输出数据的批量存储，并将
Amazon CloudWatch 用于监控集群性能和发出警报，可以使用 Amazon EMR 和
Hive 将数据迁移到 Amazon DynamoDB 以及从中迁出。所有这些操作都由启动
和管理 Hadoop 集群的 Amazon EMR 控制软件协调安排。当然，这些Web服务
的集成，大多是需要单独的使用费用。从EMR目前的定价看，基本上是按照计
算的时间来计算费用，具体价格可以在官网查询到。

### 3、新的大数据服务

2012年，AWS推出了两项新的大数据服务，以补充之前推出的Elastic Map
Reduce服务（EMR是一个在线Hadoop引擎，可以分析数据）。一项服务叫
DyamoDB，它是亚马逊的固态驱动器管理的NoSQL数据库，具有高度可扩展
性和容错性。自2007年以来，亚马逊就在内部部署，它可以优化亚马逊消费者
网站。还有一个服务就是RedShift，它是一个在线数据仓库。Redshift将结合亚
马逊的其他数据存储产品，其中最知名的就是其简单存储服务(S3)。亚马逊今年
早些时候还推出了Glacier作为长期的廉价存储选择。

## 四、Facebook

Facebook一直是大数据技术最积极的应用者，因为它拥有的数据量极其巨大，
一份资料显示2011年它拥有的压缩数据已经有25PB，未压缩数据150PB,每天产
生的未压缩的新数据有400TB。在Facebook，大数据技术被广泛应用在广告、新
闻源、消息/聊天、搜索、站点安全、特定分析、报告等各个领域。Facebook也
是Apache大数据开源项目的最大贡献者之一。Facebook是2007年前后正式转
向Hadoop计算框架，随之它向Apache基金会贡献了大名鼎鼎的Hive、ZooKeeper、
Scribe、Cassandra等开源工具，当前Facebook的开源进程仍在积极推进着。
Facebook大数据技术架构经历了三个演变阶段。

### 1、Facebook早期的大数据技术架构

Facebook早期的大数据技术架构是建立在Hadoop、HBase、Hive、Scribe等开
源工具基础上的。日志数据流从HTTP服务器产生，通过日志收集系统Scribe耗
费秒级时间传送到共享存储NFS文件系统，然后通过小时级的Copier/Loader（即

http://s15.sinaimg.cn/mw690/001mKEk5ty6DD9hxEXI3e&690
MapReduce作业）将数据文件上传到Hadoop。数据摘要通过每天例行的流水作
业产生，它是基于Hive的类SQL语言开发，结果会定期会更新到前端的Mysql
服务器，以便通过OLTP工具产生报表。Hadoop集群节点有3000个，扩展性和
容错性方面的问题能够很好地解决，但是早期系统的主要问题是整体的处理延迟
较大，从日志产生起1～2天后才能得到最终的报表。

### 2、Facebook当前的大数据技术架构

Facebook当前的大数据技术架构是在早期架构基础上对数据传输通道和数
据处理系统进行了优化，如图所示，主要分为分布式日志系统Scribe、分布式存
储系统HDFS和HBase、分布式计算和分析系统（MapReduce、Puma和Hive）等。

其中，Scribe日志系统用于聚合来自大量HTTP服务器的日志数据。Thrift是
Facebook提供的软件框架，用于跨语言的服务开发，能够在C++、Java、PHP 、
Python和Ruby等语言之间实现无缝的支持。采用Thrift RPC来调用Scribe日志
收集服务进行日志数据汇总。Scribe Policy是日志流量和模型管理节点，将元数
据传送给Scribe客户端和Scribe HDFS，采集的日志数据存储在Scribe HDFS。

Facebook对早期系统优化后的数据通道称为Data Freeway，能够处理峰值9GB/s
的数据并且端到端的延迟在10s以内，支持超过2500种的日志种类。Data Freeway
主要包括4个组件，Scribe、Calligraphus、Continuous Copier和PTail。Scribe用
于客户端，负责通过Thrift RPC发送数据；Calligraphus在中间层梳理数据并写到
HDFS，它提供了日志种类的管理，利用Zookeeper进行辅助；Continuous Copier
将文件从一个HDFS拷贝到另一个HDFS；PTail并行地tail多个HDFS上的目录，
并写文件数据到标准输出。在当前架构中，一部分数据处理仍然以批处理的方式
通过MapReduce进行小时级的处理，存储在中央的HDFS，每天通过Hive进行分
析处理。另一部分接近实时的数据流则通过Puma来进行分钟级的处理。Facebook
对专门分析提供Peregrine（Hipal）工具、对周期性分析提供Nocron工具进行分
析。

### 3、Facebook未来的大数据技术架构

Facebook未来的大数据技术架构的雏形已经出来。首先开源的是可能替代
Hadoop系统中MapReduce的Corona，类似于Yahoo提出的YARN。Corona最大
的一个进步是其集群管理器做到了基于CPU、内存和其他作业处理的需求资源的
管理，这可以使得Corona既可以处理MapReduce 作业，也可以处理非
MapReduce 作业，使Hadoop集群的应用领域更加广泛。二是Facebook最新的
交互式大数据查询系统Presto，类似于Cloudera的Impala和Hortonworks的
Stinger，解决了Facebook迅速膨胀的海量数据仓库快速查询需求。据Facebook
称，使用Presto进行简单的查询只需要几百毫秒，即使是非常复杂的查询，也
只需数分钟便可完成，它在内存中运行，并且不会向磁盘写入。第三是Wormhole

流计算系统，类似于Twiitter的Storm和Yahoo的Storm-YARN。第四个重要项目
是Prism，它能够运行一个超大的、能够将全球数据中心都连起来的Hadoop集
群，可能在一个数据中心宕掉的时候即时的将数据重新分布，这是一个与Google
的Spanner类似的项目。

Facebook的大数据技术架构演进路径代表了大数据技术的发展路线，难能可
贵的是，开源是Facebook一贯的路线，它和Yahoo等公司一起为大数据技术的
发展作出了巨大贡献。

## 五、Twitter

Twitter要上市了，再一次让全球瞩目，正是它所创造的twitte让互联网进入
了微创新的时代。虽然它没有进入中国，但受其启发的新浪微博和腾讯微博在中
国互联网上也成为一道亮丽的风景。Twitter在全球拥有巨大的用户群，海量的
社交信息流，支撑其运转的大数据技术架构也颇受人关注。

Twitter的大数据架构也是分为基于Hadoop的批处理和基于Storm的实时流
计算等主要类型，主要基于开源项目中进行开发和发展。

### 1、批处理架构

Twitter收集数据采用的是Facebook开源的日志工具Scribe,批处理地存储和
分析数据采用Hadoop+MapReduce,在大数据上的快速分析采用Pig。Pig是基于
Hadoop的并行计算高级编程语言，它提供一种类SQL的数据分析高级文本语言，
称为Pig Latin，该语言的编译器会把类SQL的数据分析请求转换为一系列经过优
化处理的MapReduce运算。Pig支持的常用数据分析主要有分组、过滤、合并等。

### 2、流计算架构

Storm是Twitter的开源流计算平台，Storm通过简单的API使开发者可以可
靠地处理无界持续的流数据，进行实时计算，开发语言为Clojure和Java。Storm
的应用场景很多，如实时分析、在线机器学习、持续计算等。

### 3、NOSQL数据库

Twitter的存储有很多工具，体现了其在不同发展阶段的作用，也试用于不同
的应用场景。NOSQL数据库至少包含了HBase、Cassandra和FlockDB等。HBase
被用于批处理的分析和数据集生成，Cassandra被用于在线系统，支持动态读写，
FlockDB则用于实时分布的社交图的存储。

### 4、Mesos操作系统

在大数据2.0的时代，Twitter的大数据技术架构也在不断吸收更多开源技术的
精华，兼容并蓄，不断进化。例如，Mesos被twitter引进用于分布式大数据技
术架构的操作系统，能够对Hadoop等计算存储资源进行合理调度。

## Twitter的大数据技术架构

### 5、Summingbird

再如，刚刚开源的Summingbird，实现了批处理和实时流计算在一个平台架构
下的整合，开发者可以使用非常接近原生的Scala或者Java 在Summingbird上执
行MapReduce作业，既可以使用Summingbird做“批处理”，也可以使用它做
“实时处理”，同时，还可以使用两种模式的混合。做到写一次逻辑，一次性解
决所有问题。Summingbird进一步的工作包括对Akka、Spark和Tez等平台的支
持，这有利于Twitter把更多平台和工具引入到自身的大数据技术架构体系中。

基于Twitter强大的大数据技术架构，它正在实现向大数据分析和服务商的
转型，越来越多的基于Twitter的分析工具、应用APP和商业模式被挖掘出来，
数据分析产业生态链逐步建立起来，其带来的想象空间非常巨大。我想，人们所
期待的新浪微博的秘密的大数据技术架构项目也一定是朝着这个方向进行着努
力。

