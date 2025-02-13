# 一、数据库概述
## 1.1 聊聊数据库

---

- 数据库是一门独立的学科，只要是做软件开发的，数据库都要学。
- 数据库（电子化的文件柜）是“按照数据结构来组织、存储和管理数据的仓库”。是一个长期存储在计算机内的、有组织的、可共享的、统一管理的大量数据的集合。
- 它的存储空间很大，可以存放百万条、千万条、上亿条数据。
- 数据库并不是随意地将数据进行存放，是有一定的规则的，否则查询的效率会很低。
- 当今世界是一个充满着数据的互联网世界，充斥着大量的数据。即这个互联网世界就是数据世界。数据的来源有很多，比如出行记录、消费记录、浏览的网页、发送的消息等等。除了文本类型的数据，图像、音乐、声音都是数据。
- 数据库对应的英文单词是DataBase，简称DB。
## 1.2 数据库类型

---

- 关系型数据库
   - 关系型数据库是依据关系模型来创建的数据库。所谓关系模型就是“一对一、一对多、多对多”等关系模型，关系模型就是指二维表格模型，因而一个关系型数据库就是由二维表及其之间的联系组成的一个数据组织。
   - 关系型数据可以很好地存储一些关系模型的数据，比如一个老师对应多个学生的数据（“多对多”），一本书对应多个作者（“一对多”），一本书对应一个出版日期（“一对一”）。
   - 关系模型包括数据结构（数据存储的问题，二维表）、操作指令集合（SQL语句）、完整性约束(表内数据约束、表与表之间的约束)。
- 非关系型数据库（NoSQL）
   - NoSQL，泛指非关系型的数据库。随着互联网web2.0网站的兴起，传统的关系数据库在处理web2.0网站，特别是超大规模和高并发的SNS类型的web2.0纯动态网站已经显得力不从心，出现了很多难以克服的问题，而非关系型的数据库则由于其本身的特点得到了非常迅速的发展。
   - NoSQL数据库的产生就是为了解决大规模数据集合多重数据种类带来的挑战，特别是大数据应用难题。NoSQL最常见的解释是“non-relational”， “Not Only SQL”也被很多人接受。
   - NoSQL仅仅是一个概念，泛指非关系型的数据库，区别于关系数据库，它们不保证关系数据的ACID特性。NoSQL是一项全新的数据库革命性运动，其拥护者们提倡运用非关系型的数据存储，相对于铺天盖地的关系型数据库运用，这一概念无疑是一种全新的思维的注入。
   - NoSQL有如下优点：易扩展，NoSQL数据库种类繁多，但是一个共同的特点都是去掉关系数据库的关系型特性。数据之间无关系，这样就非常容易扩展。无形之间也在架构的层面上带来了可扩展的能力。大数据量，高性能，NoSQL数据库都具有非常高的读写性能，尤其在大数据量下，同样表现优秀。这得益于它的无关系性，数据库的结构简单。
## 1.3 数据库管理系统

---

- 数据库管理系统（Database Management System，简称DBMS）是为管理数据库而设计的电脑软件系统，一般具有存储、截取、安全保障、备份等基础功能。
- 数据库管理系统是数据库系统的核心组成部分，主要完成对数据库的操作与管理功能，实现数据库对象的创建、数据库存储数据的查询、添加、修改与删除操作和数据库的用户管理、权限管理等。
- 常见的数据库管理系统有：MySQL、Oracle、DB2、MS SQL Server、SQLite、PostgreSQL、Sybase等。
## 1.4 什么是SQL

---

- 结构化查询语言（Structured Query Language）简称SQL，是一种特殊目的的编程语言，是一种数据库查询和程序设计语言，用于存取数据以及查询、更新和管理关系数据库系统。
- 结构化查询语言是高级的非过程化编程语言，允许用户在高层数据结构上工作。它不要求用户指定对数据的存放方法，也不需要用户了解具体的数据存放方式，所以具有完全不同底层结构的不同数据库系统, 可以使用相同的结构化查询语言作为数据输入与管理的接口。结构化查询语言语句可以嵌套，这使它具有极大的灵活性和强大的功能。
- SQL的分类
   - DQL
      - 数据查询语言（Data Query Language, DQL）是SQL语言中，负责进行数据查询而不会对数据本身进行修改的语句，这是最基本的SQL语句。保留字SELECT是DQL（也是所有SQL）用得最多的动词，其他DQL常用的保留字有FROM，WHERE，GROUP BY，HAVING和ORDER BY。这些DQL保留字常与其他类型的SQL语句一起使用。
   - DDL
      - 数据定义语言 (Data Definition Language, DDL) 是SQL语言集中，负责数据结构定义与数据库对象定义的语言，由CREATE、ALTER与DROP三个语法所组成，最早是由 Codasyl (Conference on Data Systems Languages) 数据模型开始，现在被纳入 SQL 指令中作为其中一个子集。
   - DML
      - 数据操纵语言（Data Manipulation Language, DML）是SQL语言中，负责对数据库对象运行数据访问工作的指令集，以INSERT、UPDATE、DELETE三种指令为核心，分别代表插入、更新与删除。
   - DCL
      - 数据控制语言 (Data Control Language) 在SQL语言中，是一种可对数据访问权进行控制的指令，它可以控制特定用户账户对数据表、查看表、预存程序、用户自定义函数等数据库对象的控制权。由 GRANT 和 REVOKE 两个指令组成。DCL以控制用户的访问权限为主，GRANT为授权语句，对应的REVOKE是撤销授权语句。
   - TPL
      - 数据事务管理语言（Transaction Processing Language）它的语句能确保被DML语句影响的表的所有行及时得以更新。TPL语句包括BEGIN TRANSACTION，COMMIT和ROLLBACK。
   - CCL
      - 指针控制语言（Cursor Control Language），它的语句，像DECLARE CURSOR，FETCH INTO和UPDATE WHERE CURRENT用于对一个或多个表单独行的操作。
- DBMS、SQL、DB之间的关系
   - DBMS通过执行SQL来操作DB中的数据。
# 二、MySQL的安装与配置
## 2.1 MySQL概述

---

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619752945028-dbcb73aa-50e2-4b1c-947d-21da8d742e6d.png#averageHue=%23fef8f1&height=138&id=feuEs&originHeight=138&originWidth=209&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7176&status=done&style=shadow&title=&width=209)

- MySQL是一个关系型数据库管理系统，由瑞典MySQL AB公司开发，MySQL AB公司被Sun公司收购，Sun公司又被Oracle公司收购，目前属于Oracle公司。
- MySQL是目前最流行的关系型数据库管理系统，在WEB应用方面MySQL是最好的RDBMS应用软件之一。 国内淘宝网站就使用的是MySQL集群。
- MySQL特点
   - MySQL有开源版本和收费版本，你使用开源版本是不收费的。
   - MySQL支持大型数据库，可以处理上千万记录的大型数据库。
   - MySQL使用标准的SQL数据库语言形式。
   - MySQL在很多系统上面都支持。
   - MySQL对Java，C都有很好的支持，当然其他的语言也支持比如Python、PHP。
   - MySQL是可以定制的，采用了GPL协议，你可以修改源码来开发自己的MySQL系统。
## 2.2 MySQL的下载

---

- 第一种下载方式：官网下载
   - 第一步：打开MySQL官网[https://www.mysql.com/](https://www.mysql.com/)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619753207824-f47a5a2c-3ee1-4d73-881d-be1bb67a8019.png#averageHue=%23f7f9e1&height=414&id=LIcyu&originHeight=990&originWidth=1875&originalType=binary&ratio=1&rotation=0&showTitle=false&size=521061&status=done&style=shadow&title=&width=784)

   - 第二步：点击"DOWNLOADS"

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619754075151-2e1900d9-0ee0-4905-b3dc-97b5598061f1.png#averageHue=%239ca199&height=196&id=XJGNj&originHeight=392&originWidth=1073&originalType=binary&ratio=1&rotation=0&showTitle=false&size=67160&status=done&style=shadow&title=&width=536.5)

   - 第三步：当前页继续下拉，直到找到下图链接

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619754206255-ee47b52c-e183-4401-a8e7-7b0e51452a00.png#averageHue=%23fdfbfa&height=177&id=NI75H&originHeight=353&originWidth=966&originalType=binary&ratio=1&rotation=0&showTitle=false&size=43043&status=done&style=shadow&title=&width=483)

   - 第四步：点击上图链接，进入下面页面，其中“MySQL Community Server”是解压版mysql，“MySQL Installer for Windows”是安装版，这里我们选择解压版

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619754239811-b4151058-268c-406b-bcd3-72a6d5771e4b.png#averageHue=%23fefefd&height=336&id=za1XY&originHeight=672&originWidth=1035&originalType=binary&ratio=1&rotation=0&showTitle=false&size=89127&status=done&style=shadow&title=&width=517.5)

   - 第五步：点击上图“MySQL Community Server”

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620375449949-470a5fb1-8af6-4130-a424-129b8961cb8c.png#averageHue=%23d8e6c3&height=354&id=c5iWO&originHeight=707&originWidth=1228&originalType=binary&ratio=1&rotation=0&showTitle=false&size=154716&status=done&style=shadow&title=&width=614)

   - 第六步：点击上图第1个“Download”

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1619754349149-75c6289e-0461-4c82-bf0b-388471535683.png#averageHue=%23fafaf9&height=395&id=loI9w&originHeight=789&originWidth=1001&originalType=binary&ratio=1&rotation=0&showTitle=false&size=102325&status=done&style=shadow&title=&width=500.5)

   - 第七步：点击上图“No thanks, just start my download.”开始下载，直到下载完毕。

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620375547996-62d248ee-f33d-41a5-ba14-50cf38405d9b.png#averageHue=%23f6f2ed&height=33&id=H39JS&originHeight=33&originWidth=245&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2768&status=done&style=shadow&title=&width=245)

- 第二种下载方式：百度网盘
   - 链接：[https://pan.baidu.com/s/1Oxy4_X2VnuX5Gb3Vh0Cctg](https://pan.baidu.com/s/1Oxy4_X2VnuX5Gb3Vh0Cctg) 提取码：ho17 
## 2.3 MySQL安装与配置

---

- 将下载的zip压缩包解压，我这里直接解压到C盘的根目录下

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620375547996-62d248ee-f33d-41a5-ba14-50cf38405d9b.png#averageHue=%23f6f2ed&height=33&id=PdFDW&originHeight=33&originWidth=245&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2768&status=done&style=shadow&title=&width=245)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620376986790-01106d3e-b89f-453a-98cb-f2a86d4b2544.png#averageHue=%23f6f1ef&height=205&id=VR5Fm&originHeight=205&originWidth=305&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10933&status=done&style=shadow&title=&width=305)
mysql的根目录为：C:\mysql-8.0.24-winx64

- 将C:\mysql-8.0.24-winx64\bin目录配置到环境变量path当中

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620377142769-f797dd2c-4f82-4c8f-b5a2-d97bfbe52225.png#averageHue=%23f5f4f4&height=551&id=wovpn&originHeight=551&originWidth=515&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23226&status=done&style=shadow&title=&width=515)

- 初始化data目录
   - 使用管理员身份打开dos命令窗口（按win键，输入cmd，点击管理员身份运行）

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620377404683-4ed7c1d7-c8f1-44a3-ae32-0005183fcd09.png#averageHue=%23e3e3e3&height=635&id=enGFN&originHeight=635&originWidth=779&originalType=binary&ratio=1&rotation=0&showTitle=false&size=55630&status=done&style=shadow&title=&width=779)

   - cd命令切换到mysql的bin目录下，执行mysqld --initialize --console进行data目录初始化，此时会在控制台生成一个随机密码，下图红框中就是随机密码

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620379266865-b043168d-8825-44e9-99ab-35ce6f8c8e25.png#averageHue=%232d2d2d&height=298&id=RFgFN&originHeight=298&originWidth=1034&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28139&status=done&style=shadow&title=&width=1034)
技巧：左键选中密码，直接点击右键，此时密码已经复制到剪贴板中了，
然后随便找一个文件，将密码粘贴到文件中保存起来。

- 安装MySQL服务：cd命令切换到bin目录下，执行命令mysqld -install

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620379567159-f63f3527-3ba9-48fe-8a19-57e4c3767662.png#averageHue=%23181818&height=61&id=RZu5G&originHeight=61&originWidth=352&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2866&status=done&style=shadow&title=&width=352)

- 查看mysql服务名称：此电脑-右键-管理-服务和应用程序-服务-找MySQL服务，如下图mysql服务名称：MySQL

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620379678662-4b14e7a5-d17c-4c2b-917d-cc4d73b94ae5.png#averageHue=%23f6f4f2&height=521&id=P0jsU&originHeight=695&originWidth=796&originalType=binary&ratio=1&rotation=0&showTitle=false&size=117316&status=done&style=shadow&title=&width=597)

- 启动MySQL服务：net start mysql，注意start后面是mysql服务的名称

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620379806288-826de76c-2827-419e-ab16-b6fc72afdbca.png#averageHue=%231c1c1c&height=69&id=JLnqX&originHeight=69&originWidth=353&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3632&status=done&style=shadow&title=&width=353)
停止mysql服务的命令：net stop mysql
注意：启停mysql服务也可以在上一步的图中点击右键进行启停服务。

- 登录mysql：输入mysql -uroot -p，然后回车，输入刚才的随机密码，然后回车，看到下图表示成功登录mysql

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620379936249-1bfaef7c-9ca7-4ddd-978a-b518acd834b0.png#averageHue=%23141313&height=305&id=EiQKK&originHeight=305&originWidth=649&originalType=binary&ratio=1&rotation=0&showTitle=false&size=17739&status=done&style=shadow&title=&width=649)

- 修改MySQL的root账户密码：ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密码';

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620382836782-5a7fef8d-15ce-4dca-a5d0-831b6f60f56e.png#averageHue=%23282828&height=293&id=dVHAz&originHeight=293&originWidth=760&originalType=binary&ratio=1&rotation=0&showTitle=false&size=18567&status=done&style=shadow&title=&width=760)

- 使用新密码登录mysql

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620382883258-875c0c1a-00c7-40f8-a8dd-edb1d39e94e0.png#averageHue=%232a2a2a&height=310&id=WAkW8&originHeight=310&originWidth=687&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21698&status=done&style=shadow&title=&width=687)
## 2.4 MySQL卸载

---

- 停止mysql的服务

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620383089030-497a3bfc-74d5-43a6-9689-8f9e0b24dd73.png#averageHue=%231a1a1a&height=74&id=pHyXZ&originHeight=74&originWidth=362&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3592&status=done&style=shadow&title=&width=362)

- 删除mysql服务

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620383158420-3d5117c6-0c0f-421c-9570-407dac8c6612.png#averageHue=%23171717&height=58&id=OrAHb&originHeight=58&originWidth=407&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2850&status=done&style=shadow&title=&width=407)

- 删除mysql的目录

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620383199727-89d46dc3-b4cf-4883-9a18-b0ee0c0fe6e8.png#averageHue=%23faf4f2&height=207&id=A4FLD&originHeight=207&originWidth=343&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12988&status=done&style=shadow&title=&width=343)
## 2.5 登录MySQL

---

- 本地登录
   - 如果mysql的服务是启动的，打开dos命令窗口，输入：mysql -uroot -p，回车，然后输入root账户的密码

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620389190451-81319065-6d04-4094-97d0-13236236ad32.png#averageHue=%231c1b1a&height=414&id=EMVUZ&originHeight=552&originWidth=1067&originalType=binary&ratio=1&rotation=0&showTitle=false&size=51645&status=done&style=shadow&title=&width=800)
解释“mysql -uroot -p”：
mysql是一个命令，在bin目录下，对应的命令文件是mysql.exe，如果将bin目录配置到环境
变量path中，才可以在以上位置使用该命令。
-uroot 表示登录的用户是root，u实际上是user单词的首字母。
-p 表示登录时使用密码，p实际上是password单词的首字母。

   - 也可以将密码以明文的形式写到-p后面，这样做可能会导致你的密码泄露

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620389582655-74210644-318a-4e71-a242-192d61ef9fd9.png#averageHue=%231d1b1a&height=355&id=AthqC&originHeight=473&originWidth=1006&originalType=binary&ratio=1&rotation=0&showTitle=false&size=52443&status=done&style=shadow&title=&width=755)

- 远程登录
   - 假设mysql安装在A机器上，现在你要在B机器上连接mysql数据库，此时需要使用远程登录，远程登录时加上远程机器的ip地址即可

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620389951870-e1585ee0-d1cd-4b89-973b-b3e6c4a20539.png#averageHue=%23211f1e&height=330&id=Zncdu&originHeight=440&originWidth=994&originalType=binary&ratio=1&rotation=0&showTitle=false&size=52747&status=done&style=shadow&title=&width=746)
-h中的h实际上是host单词的首字母。在-h后面的是远程计算机的ip地址。
127.0.0.1是计算机默认的本机IP地址。
127.0.0.1又可以写作：localhost，他们是等效的。
注意：mysql默认情况下root账户是不支持远程登录的，其实这是一种安全策略，
为了保护root账户的安全。如果希望root账户支持远程登录，这是需要进行设置的。

# 三、初始化测试数据
## 3.1 MySQL命令行基本命令

---

1. 列出当前数据库管理系统中有哪些数据库。
```sql
show databases;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402104809-379ae418-d997-4758-9a02-45bbfad7178e.png#averageHue=%23151311&height=162&id=eQifD&originHeight=162&originWidth=220&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5485&status=done&style=shadow&title=&width=220)

2. 创建数据库，起名bjpowernode。
```sql
create database bjpowernode;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402231403-ddd2c76f-3b9f-4477-9504-502328fe64fc.png#averageHue=%2317110f&height=262&id=WUuwT&originHeight=262&originWidth=341&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13990&status=done&style=shadow&title=&width=341)

3.  使用bjpowernode数据库。
```sql
use bjpowernode;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402295297-4dbb2d54-4210-44c9-bc8f-c887327bfb8c.png#averageHue=%23151210&height=66&id=QOLYt&originHeight=66&originWidth=232&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3275&status=done&style=shadow&title=&width=232)

4. 查看当前用的是哪个数据库。
```sql
select database();
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402349349-2786c9cb-8683-4d17-bd26-c73a7b451847.png#averageHue=%23131110&height=130&id=aq6GB&originHeight=130&originWidth=268&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5590&status=done&style=shadow&title=&width=268)

5.  查看当前数据库中有哪些表。
```sql
show tables;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402397890-84d73980-1046-4e83-b6cb-bdcc68ba7b57.png#averageHue=%23151210&height=53&id=qqu40&originHeight=53&originWidth=207&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2593&status=done&style=shadow&title=&width=207)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402645490-1cd5d42e-5735-4c0a-8723-e4fb81c96b8a.png#averageHue=%23100f0e&height=461&id=fFKCv&originHeight=461&originWidth=516&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23780&status=done&style=shadow&title=&width=516)

6.  删除数据库bjpowernode。
```sql
drop database bjpowernode;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620402497021-d7ff9bf3-3c9a-4c9c-bc5d-f5dece31188f.png#averageHue=%2312110f&height=242&id=MeI71&originHeight=242&originWidth=363&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12799&status=done&style=shadow&title=&width=363)

7. 退出mysql
   1. exit
   2. quit
   3. ctrl + c
8. 查看当前mysql版本
```sql
select version();
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620468380301-0c326efb-a538-4271-b75d-ff5add0e453a.png#averageHue=%23121110&height=142&id=az14k&originHeight=142&originWidth=279&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5365&status=done&style=shadow&title=&width=279)
还可以使用mysql.exe命令来查看版本信息（在没有登录mysql之前使用）：mysql --version
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620468207568-77aa05ff-8d65-47f6-b90d-2c176893a52f.png#averageHue=%2313110f&height=59&id=Ialy0&originHeight=59&originWidth=624&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6797&status=done&style=shadow&title=&width=624)
## 3.2 数据库表的概述

---

| name | age | gender |
| --- | --- | --- |
| 张三 | 20 | 男 |
| 李四 | 22 | 女 |

- 以上就是数据库表格的直观展示形式。
- 表格英文单词table。
- 表是数据库存储数据的基本单元，数据库存储数据的时候，是将数据存储在表对象当中的。为什么将数据存储在表中呢？因为表存储数据非常直观。
- 任何一张表都有行和列：
   - 行：记录（一行就是一条数据）
   - 列：字段（name字段、age字段、gender字段）
- 每个字段包含以下属性：
   - 字段名：name、age、gender都是字段的名字
   - 字段的数据类型：每个字段都有数据类型，比如：字符类型、数字类型、日期类型
   - 字段的数据长度：每个字段有可能会有长度的限制
   - 字段的约束：比如某些字段要求该字段下的数据不能重复、不能为空等，用来保证表格中数据合法有效
## 3.3 初始化测试数据

---

为了方便后面内容的学习，老师提前准备了表以及表中的测试数据，以下是建表并且初始化数据的sql脚本
```sql
DROP TABLE IF EXISTS EMP;
DROP TABLE IF EXISTS DEPT;
DROP TABLE IF EXISTS SALGRADE;

CREATE TABLE DEPT(DEPTNO int(2) not null ,
	DNAME VARCHAR(14) ,
	LOC VARCHAR(13),
	primary key (DEPTNO)
);
CREATE TABLE EMP(EMPNO int(4)  not null ,
	ENAME VARCHAR(10),
	JOB VARCHAR(9),
	MGR INT(4),
	HIREDATE DATE  DEFAULT NULL,
	SAL DOUBLE(7,2),
	COMM DOUBLE(7,2),
	primary key (EMPNO),
	DEPTNO INT(2) 
);

CREATE TABLE SALGRADE( GRADE INT,
	LOSAL INT,
	HISAL INT
);

INSERT INTO DEPT ( DEPTNO, DNAME, LOC ) VALUES ( 10, 'ACCOUNTING', 'NEW YORK'); 
INSERT INTO DEPT ( DEPTNO, DNAME, LOC ) VALUES ( 20, 'RESEARCH', 'DALLAS'); 
INSERT INTO DEPT ( DEPTNO, DNAME, LOC ) VALUES ( 30, 'SALES', 'CHICAGO'); 
INSERT INTO DEPT ( DEPTNO, DNAME, LOC ) VALUES ( 40, 'OPERATIONS', 'BOSTON'); 
 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7369, 'SMITH', 'CLERK', 7902,  '1980-12-17', 800, NULL, 20); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7499, 'ALLEN', 'SALESMAN', 7698,  '1981-02-20', 1600, 300, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7521, 'WARD', 'SALESMAN', 7698,  '1981-02-22', 1250, 500, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7566, 'JONES', 'MANAGER', 7839,  '1981-04-02', 2975, NULL, 20); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7654, 'MARTIN', 'SALESMAN', 7698,  '1981-09-28', 1250, 1400, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7698, 'BLAKE', 'MANAGER', 7839,  '1981-05-01', 2850, NULL, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7782, 'CLARK', 'MANAGER', 7839,  '1981-06-09', 2450, NULL, 10); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7788, 'SCOTT', 'ANALYST', 7566,  '1987-04-19', 3000, NULL, 20); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7839, 'KING', 'PRESIDENT', NULL,  '1981-11-17', 5000, NULL, 10); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7844, 'TURNER', 'SALESMAN', 7698,  '1981-09-08', 1500, 0, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7876, 'ADAMS', 'CLERK', 7788,  '1987-05-23', 1100, NULL, 20); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7900, 'JAMES', 'CLERK', 7698,  '1981-12-03', 950, NULL, 30); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7902, 'FORD', 'ANALYST', 7566,  '1981-12-03', 3000, NULL, 20); 
INSERT INTO EMP ( EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM,DEPTNO ) VALUES ( 7934, 'MILLER', 'CLERK', 7782,  '1982-01-23', 1300, NULL, 10); 
 
INSERT INTO SALGRADE ( GRADE, LOSAL, HISAL ) VALUES ( 1, 700, 1200); 
INSERT INTO SALGRADE ( GRADE, LOSAL, HISAL ) VALUES ( 2, 1201, 1400); 
INSERT INTO SALGRADE ( GRADE, LOSAL, HISAL ) VALUES ( 3, 1401, 2000); 
INSERT INTO SALGRADE ( GRADE, LOSAL, HISAL ) VALUES ( 4, 2001, 3000); 
INSERT INTO SALGRADE ( GRADE, LOSAL, HISAL ) VALUES ( 5, 3001, 9999); 
commit;
```

- 什么是sql脚本：文件名是.sql，并且该文件中编写了大量的SQL语句，执行sql脚本程序就相当于批量执行SQL语句。
- 你入职的时候，项目一般都是进展了一部分，多数情况下你进项目组的时候数据库的表以及数据都是有的，项目经理第一天可能会给你一个较大的sql脚本文件，你需要执行这个脚本文件来初始化你的本地数据库。（当然，也有可能数据库是共享的。）
- 创建文件：bjpowernode.sql，把以上SQL语句全部复制到sql脚本文件中。
- 执行SQL脚本文件，初始化数据库
   - 第一步：命令窗口登录mysql
   - 第二步：创建数据库bjpowernode（如果之前已经创建就不需要再创建了）：create database bjpowernode;
   - 第三步：使用数据库bjpowernode：use bjpowernode;
   - 第四步：source命令执行sql脚本，注意：source命令后面是sql脚本文件的绝对路径。

        ![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620435073900-d9e19c5e-9b0e-4d09-a3ee-74471ec9ebb8.png#averageHue=%2315110f&height=225&id=EfIUK&originHeight=225&originWidth=444&originalType=binary&ratio=1&rotation=0&showTitle=false&size=18044&status=done&style=shadow&title=&width=444)

   - 第五步：查看是否初始化成功，执行：show tables;

        ![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620435161519-44d66617-3323-4834-8f57-5db6cc4c8cf3.png#averageHue=%23151312&height=170&id=ir680&originHeight=170&originWidth=253&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6666&status=done&style=shadow&title=&width=253)

- 使用其他的mysql客户端工具也可以执行sql脚本，比如navicat。使用source命令执行sql脚本的优点：**可支持大文件**。
## 3.4 熟悉测试数据

---

emp dept salgrade三张表分别存储什么信息

- emp：员工信息
- dept：部门信息
- salgrade：工资等级信息

查看表结构：desc或describe，语法格式：desc或describe +表名
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620441048844-4e9e7687-f9a2-4014-a014-f5a2c267b422.png#averageHue=%23131110&height=620&id=tvTgE&originHeight=620&originWidth=547&originalType=binary&ratio=1&rotation=0&showTitle=false&size=49182&status=done&style=shadow&title=&width=547)
以上的结果展示的不是表中的数据，而是表的结构。

- Field是字段名
- Type是这个字段的数据类型
- Null是这个字段是否允许为空
- Key是这个字段是否为主键或外键
- Default是这个字段的默认值

对以上表结构进行解释说明：

- emp表
   - empno：员工编号，int类型（整数），不能为空，主键（主键后期学习约束时会进行说明）
   - ename：员工姓名，varchar类型（字符串）
   - job：工作岗位，varchar类型
   - mgr：上级领导编号，int类型
   - hiredate：雇佣日期，date类型（日期类型）
   - sal：月薪，double类型（带有浮点的数字）
   - comm：补助津贴，double类型
   - deptno：部门编号，int类型
- dept表
   - deptno：部门编号，int类型，主键
   - dname：部门名称，varchar类型
   - loc：位置，varchar类型
- salgrade表
   - grade：等级，int类型
   - losal：最低工资，int类型
   - hisal：最高工资，int类型

对于以上表结构要提前了解，后面学习的内容需要你马上反应出：哪个字段是什么意思。
查看一下表中的数据，来加深一下印象（以下SQL语句会在后面课程中学习）：
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620442749316-53eb0de4-bc2f-4af4-b6fa-a39eafc5265e.png#averageHue=%23131110&height=779&id=KVYzM&originHeight=779&originWidth=744&originalType=binary&ratio=1&rotation=0&showTitle=false&size=86015&status=done&style=shadow&title=&width=744)
# 四、查询DQL专题
## 4.1 简单查询

---

查询是SQL语言的核心，用于表达SQL查询的select查询命令是功能最强也是最为复杂的SQL语句，它的作用就是从数据库中检索数据，并将查询结果返回给用户。 select语句由：select子句(查询内容)、from子句(查询对象)、where子句(查询条件)、order by子句(排序方式)、group by子句(分组方式)等组成。查询语句属于SQL语句中的DQL语句，是所有SQL语句中最为复杂也是最重要的语句，所以必须掌握。接下来我们先从简单查询语句开始学习。
### 4.1.1 查一个字段

---

查询一个字段说的是：一个表有多列，查询其中的一列。
语法格式：select 字段名 from 表名;

- select和from是关键字，不能随便写
- **一条SQL语句必须以“;”结尾**
- **对于SQL语句来说，大小写都可以**
- 字段名和表名属于标识符，按照表的实际情况填写，不知道字段名的，可以使用desc命令查看表结构

案例1：查询公司中所有员工编号
```sql
select empno from emp; 
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620444005101-f8b17d19-7943-42da-868a-4353bbc39d72.png#averageHue=%230f0e0e&height=364&id=iefCx&originHeight=364&originWidth=331&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12803&status=done&style=shadow&title=&width=331)
案例2：查询公司中所有员工姓名
```sql
SELECT ENAME FROM EMP;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620444051586-c22b328d-726d-43a1-84c5-b61b053e4c76.png#averageHue=%2311100f&height=368&id=t1BP2&originHeight=368&originWidth=323&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15288&status=done&style=shadow&title=&width=323)
在mysql命令行客户端中，sql语句没有分号是不会执行的：
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620444166592-310dfb98-9eed-43ed-afa5-b479e03e0a79.png#averageHue=%230d0d0c&height=249&id=W3RxL&originHeight=249&originWidth=210&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4063&status=done&style=shadow&title=&width=210)
末尾加上“;”就执行了：
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620444251765-5d3f1b6c-a491-4382-92a8-8ebb31a40b45.png#averageHue=%230e0d0d&height=236&id=AdNxg&originHeight=236&originWidth=943&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16079&status=done&style=shadow&title=&width=943)
以上sql虽然以分号结尾之后执行了，但是报错了，错误信息显示：语法错误。
假设一个SQL语句在书写过程中出错了，怎么终止这条SQL呢？\c
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620444994820-7b03fb95-5097-418c-bc6f-75e3613c7d17.png#averageHue=%2312100f&height=74&id=DCv3D&originHeight=74&originWidth=168&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2131&status=done&style=shadow&title=&width=168)

- [ ] 任务1：查询所有部门名称。
- [ ] 任务2：查询所有薪资等级。
### 4.1.2 查多个字段

---

查询多个字段时，在字段名和字段名之间添加“,”即可。
语法格式：select 字段名1,字段名2,字段名3 from 表名;
案例1：查询员工编号以及员工姓名。
```sql
select empno, ename from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620445192077-e454043b-9203-4ca0-83f3-7e7d991187c5.png#averageHue=%2311100f&height=362&id=sYqFg&originHeight=362&originWidth=380&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20812&status=done&style=shadow&title=&width=380)
字段的前后顺序无所谓（只是显示结果列的时候顺序变了）：
```sql
select ename, empno from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620445262526-49d81087-7e1b-44f2-afe7-e8bad59dc21d.png#averageHue=%2312100f&height=367&id=Na24p&originHeight=367&originWidth=368&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20595&status=done&style=shadow&title=&width=368)

- [ ] 任务1：查询部门编号、部门名称以及位置。
- [ ] 任务2：查询员工的名字以及工作岗位。
### 4.1.3 查所有字段

---

查询所有字段的可以将每个字段都列出来查询，也可以采用“*”来代表所有字段
案例1：查询员工的所有信息
```sql
select * from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620446156182-c5776f47-0d54-45e1-b0a6-af8196b3cbcd.png#averageHue=%23191613&height=365&id=LwKfy&originHeight=365&originWidth=734&originalType=binary&ratio=1&rotation=0&showTitle=false&size=57245&status=done&style=shadow&title=&width=734)
案例2：查询所有部门信息
```sql
select * from dept;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620452731531-c4b03af4-9f9f-46d8-acf5-7132317f89ae.png#averageHue=%23161311&height=186&id=ew3JJ&originHeight=186&originWidth=339&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12122&status=done&style=shadow&title=&width=339)
采用“*”进行查询存在的缺点：

- select * from dept; 在执行的时候会被解析为 select DEPTNO, DNAME, LOC from dept; 再执行，所以这种效率方面弱一些。
- 采用“*”的可读性较差，通过“*”很难看出都有哪些具体的字段。

什么时候使用“*”？

- 这个SQL语句不在项目编码中使用，如果平时自己想快速查看表中所有数据的话，这种写法还是很给力的。

- [ ] 任务1：查询所有的薪资等级以及每个薪资等级的最低工资和最高工资。
### 4.1.4 查询时字段可参与数学运算

---

在进行查询操作的时候，字段是可以参与数学运算的，例如加减乘除等。
案例1：查询每个员工的月薪
```sql
select ename, sal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620453626714-46aed4db-e9fb-49be-a9be-ce9662dbc962.png#averageHue=%2312100f&height=364&id=wOnEt&originHeight=364&originWidth=375&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21162&status=done&style=shadow&title=&width=375)
案例2：查询每个员工的年薪（月薪 * 12）
```sql
select ename, sal * 12 from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620453661204-ca783845-5f31-49fc-90d8-0f4426598cde.png#averageHue=%2313100f&height=364&id=Zkjv2&originHeight=364&originWidth=387&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22636&status=done&style=shadow&title=&width=387)

- [ ] 任务1：查询每个员工月薪加1000之后的月薪
- [ ] 任务2：查询每个员工月薪加1000之后的年薪
### 4.1.5 查询时字段可起别名

---

我们借用一下之前的SQL语句
```sql
select ename, sal * 12 from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620453661204-ca783845-5f31-49fc-90d8-0f4426598cde.png#averageHue=%2313100f&height=364&id=EQnXg&originHeight=364&originWidth=387&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22636&status=done&style=shadow&title=&width=387)
以上的查询结果列名“sal * 12”可读性较差，是否可以给查询结果的列名进行重命名呢？

- 使用as关键字
```sql
select ename, sal * 12 as yearsal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620454420847-c739365b-440e-4cf7-b1e2-2bcf6d5cdb8b.png#averageHue=%2312100f&height=372&id=NImNH&originHeight=372&originWidth=473&originalType=binary&ratio=1&rotation=0&showTitle=false&size=25001&status=done&style=shadow&title=&width=473)
通过as关键字起别名后，查询结果列显示yearsal，可读性增强。

- 其实as关键字可以省略，只要使用空格即可
```sql
select ename, sal * 12 yearsal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620466356467-fb4612f8-72f6-4506-b2bc-1744846c171d.png#averageHue=%2311100e&height=363&id=XWTbX&originHeight=363&originWidth=464&originalType=binary&ratio=1&rotation=0&showTitle=false&size=24234&status=done&style=shadow&title=&width=464)

- 通过以上测试，得知as可以省略，可以使用空格代替as，但如果别名中有空格呢？
```sql
select ename, sal * 12 year sal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620466540145-98adb10e-15a2-46df-9179-7e41ae1fc322.png#averageHue=%2313110f&height=87&id=LnbYI&originHeight=87&originWidth=946&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12503&status=done&style=shadow&title=&width=946)
可以看出，执行报错了，说语法有问题，这是为什么？分析一下：SQL语句编译器在检查该语句的时候，在year后面遇到了空格，会继续找from关键字，但year后面不是from关键字，所以编译器报错了。怎么解决这个问题？记住：如果别名中有空格的话，可以将这个别名使用双引号或者单引号将其括起来。
```sql
select ename, sal * 12 "year sal" from emp;
select ename, sal * 12 'year sal' from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620467027246-b5cce57e-3ca3-4b3f-9298-a21fc3bb77c3.png#averageHue=%23110f0e&height=744&id=kyi8P&originHeight=744&originWidth=558&originalType=binary&ratio=1&rotation=0&showTitle=false&size=53259&status=done&style=shadow&title=&width=558)
**在mysql中，字符串既可以使用双引号也可以使用单引号，但还是建议使用单引号，因为单引号属于标准SQL。**

- 如果别名采用中文呢？
```sql
select ename, sal * 12 年薪 from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1620467760618-b5df74f5-c8ee-4e39-88a9-e10fde59bb56.png#averageHue=%2311100e&height=373&id=AsiUs&originHeight=373&originWidth=445&originalType=binary&ratio=1&rotation=0&showTitle=false&size=24025&status=done&style=shadow&title=&width=445)
**别名是中文是可以的，但是对于低版本的mysql来说会报错，需要添加双引号或单引号。**我们当前使用的mysql版本是：8.0.24

- [ ] 任务：查询所有员工的信息，要求每个字段名采用中文显示。
## 4.2 条件查询

---

通常在进行查询操作的时候，都是查询符合某些条件的数据，很少将表中所有数据都取出来。怎么取出表的部分数据？需要在查询语句中添加条件进行数据的过滤。常见的过滤条件如下：

| **条件** | **说明** |
| --- | --- |
| = | 等于 |
| <>或!= | 不等于 |
| >= | 大于等于 |
| <= | 小于等于 |
| > | 大于 |
| < | 小于 |
| between...and... | 等同于 >= and <= |
| is null | 为空 |
| is not null | 不为空 |
| <=> | 安全等于（可读性差，很少使用了）。 |
| and 或 && | 并且 |
| or 或 &#124;&#124; | 或者 |
| in | 在指定的值当中 |
| not in | 不在指定的值当中 |
| exists |  |
| not exists |  |
| like | 模糊查询 |

### 4.2.1 条件查询语法格式

---

```sql
select 
  ...
from
  ...
where
  过滤条件;
```
过滤条件放在where子句当中，以上语句的执行顺序是：
    第一步：先执行from
    第二步：再通过where条件过滤
    第三步：最后执行select，查询并将结果展示到控制台
### 4.2.2 等于、不等于

---

- =

判断等量关系，支持多种数据类型，比如：数字、字符串、日期等。
案例1：查询月薪3000的员工编号及姓名
```sql
select 
  empno,ename
from
  emp
where
  sal = 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621907694609-eea9c573-f409-4291-b065-afdbf568e8c7.png#averageHue=%2312100f&height=267&id=Y8ZCX&originHeight=267&originWidth=306&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10989&status=done&style=shadow&title=&width=306)
案例2：查询员工FORD的岗位及月薪
```sql
select
	job, sal
from
	emp
where
	ename = 'FORD';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621907754724-3f628fe9-0c56-4057-8be7-60d0bf968b6c.png#averageHue=%2312100f&height=254&id=KB48O&originHeight=254&originWidth=309&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9820&status=done&style=shadow&title=&width=309)
存储在表emp中的员工姓名是FORD，全部大写，如果在查询的时候，写成全部小写会怎样呢？
```sql
select
	job, sal
from
	emp
where
	ename = 'ford';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621907908980-acfef2ac-247a-434a-846d-aebe132c534b.png#averageHue=%23131110&height=255&id=fOGhC&originHeight=255&originWidth=268&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9405&status=done&style=shadow&title=&width=268)
通过测试发现，即使写成小写ford，也是可以查询到结果的，**不过这里需要注意的是：在Oracle数据库当中是查询不到数据的，Oracle的语法要比MySQL的语法严谨。对于SQL语句本身来说是不区分大小写的，但是对于表中真实存储的数据，大写A和小写a还是不一样的，这一点Oracle做的很好。MySQL的语法更随性。另外在Oracle当中，字符串是必须使用单引号括起来的，但在MySQL当中，字符串可以使用单引号，也可以使用双引号**，如下：
```sql
select
	job, sal
from
  emp
where
  ename = "FORD";
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621908335672-ce3770ed-b906-44ad-8e6a-1255e620f77c.png#averageHue=%23110f0e&height=152&id=nVwF9&originHeight=152&originWidth=550&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9330&status=done&style=shadow&title=&width=550)
案例3：查询岗位是MANAGER的员工编号及姓名
```sql
select
  empno, ename
from
  emp
where
  job = 'MANAGER';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621908485311-e63dfa85-7530-4d2e-8652-f5885287dda7.png#averageHue=%23100f0e&height=190&id=vTZba&originHeight=190&originWidth=588&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13081&status=done&style=shadow&title=&width=588)

- [ ] 任务：查询工资级别是1的最低工资以及最高工资
- <> 或 !=

判断非等量关系，支持字符串、数字、日期类型等。不等号有两种写法，第一种<>，第二种!=，第二种写法和Java程序中的不等号相同，第一种写法比较诡异，不过也很好理解，比如<>3，表示小于3、大于3，就是不等于3。你get到了吗？
案例1：查询工资不是3000的员工编号、姓名、薪资
```sql
select
  empno,ename,sal
from
  emp
where
  sal <> 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909279969-92f574b8-825b-4774-ab25-b5ccb058ebd5.png#averageHue=%2312100f&height=365&id=x0euZ&originHeight=365&originWidth=577&originalType=binary&ratio=1&rotation=0&showTitle=false&size=31965&status=done&style=shadow&title=&width=577)
案例2：查询工作岗位不是MANAGER的员工姓名和岗位
```sql
select
  ename,job
from
	emp
where
	job <> 'MANAGER';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909394164-d589f9f5-30a1-477c-aef6-b659ae36d9e8.png#averageHue=%2311100f&height=351&id=X5qgA&originHeight=351&originWidth=575&originalType=binary&ratio=1&rotation=0&showTitle=false&size=26497&status=done&style=shadow&title=&width=575)

- [ ] 任务：查询不在部门编号为10的部门工作的员工信息
### 4.2.3 大于、大于等于、小于、小于等于

---

- 大于 >

案例：找出薪资大于3000的员工姓名、薪资
```sql
select 
  ename, sal
from
  emp
where
  sal > 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909653019-47b3d57f-3690-46fb-9f47-7906f0fd3245.png#averageHue=%2311100f&height=148&id=k0f1J&originHeight=148&originWidth=514&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8657&status=done&style=shadow&title=&width=514)

- 大于等于 >=

案例：找出薪资大于等于3000的员工姓名、薪资
```sql
select 
  ename, sal
from
  emp
where
  sal >= 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909723383-d1a6872b-5790-4d89-875b-e1116ea539cf.png#averageHue=%23110f0e&height=190&id=pnLPe&originHeight=190&originWidth=528&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11463&status=done&style=shadow&title=&width=528)

- 小于 <

案例：找出薪资小于3000的员工姓名、薪资
```sql
select 
  ename, sal
from
  emp
where
  sal < 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909833614-f9d57a1f-1d48-4d14-aaef-83c5bddb89a8.png#averageHue=%23110f0e&height=346&id=Ln9DW&originHeight=346&originWidth=535&originalType=binary&ratio=1&rotation=0&showTitle=false&size=24457&status=done&style=shadow&title=&width=535)

- 小于等于 <=

案例：找出薪资小于等于3000的员工姓名、薪资
```sql
select 
  ename, sal
from
  emp
where
  sal <= 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621909895715-9af5ab2f-b445-4b44-a643-fd2a312cac2c.png#averageHue=%23110f0e&height=387&id=ZVSfe&originHeight=387&originWidth=536&originalType=binary&ratio=1&rotation=0&showTitle=false&size=27408&status=done&style=shadow&title=&width=536)
### 4.2.4 and

---

and表示并且，还有另一种写法：&&
案例：找出薪资大于等于3000并且小于等于5000的员工姓名、薪资。
```sql
select
  ename,sal
from
  emp
where
  sal >= 3000 and sal <= 5000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621910545661-438867ac-b8d0-4a80-929e-5a758b44add4.png#averageHue=%23100f0e&height=193&id=GpkEk&originHeight=193&originWidth=681&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12734&status=done&style=shadow&title=&width=681)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621910577682-f852440b-94f8-4299-89ad-c0a88fefc0d1.png#averageHue=%23100f0e&height=187&id=AyScE&originHeight=187&originWidth=672&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13060&status=done&style=shadow&title=&width=672)

- [ ] 任务：找出工资级别为2~4（包含2和4）的最低工资和最高工资。
### 4.2.5 or

---

or表示或者，还有另一种写法：||
案例：找出工作岗位是MANAGER和SALESMAN的员工姓名、工作岗位
```sql
select 
  ename, job
from
  emp
where
  job = 'MANAGER' or job = 'SALESMAN';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621910850853-c7030458-0c8f-4040-bc29-c6fa66caca7c.png#averageHue=%23110f0e&height=376&id=tQUI3&originHeight=376&originWidth=492&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22698&status=done&style=shadow&title=&width=492)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621910943353-4a9fb152-67b9-4044-a2b4-b90a2fbf3f57.png#averageHue=%23110f0e&height=370&id=k83WP&originHeight=370&originWidth=471&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22916&status=done&style=shadow&title=&width=471)
注意：这个题目描述中有这样一句话：MANAGER和SALESMAN，有的同学一看到“和”，就直接使用“and”了，因为“和”对应的英文单词是“and”，如果是这样的话，就大错特错了，因为and表示并且，使用and表示工作岗位既是MANAGER又是SALESMAN的员工，这样的员工是不存在的，因为每一个员工只有一个岗位，不可能同时从事两个岗位。所以使用and是查询不到任何结果的。如下
```sql
select 
  ename, job
from
  emp
where
  job = 'MANAGER' and job = 'SALESMAN';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621911189669-be42f087-b388-4eb2-80b7-602766996b82.png#averageHue=%23100f0e&height=151&id=DRxAe&originHeight=151&originWidth=471&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8765&status=done&style=shadow&title=&width=471)

- [ ] 任务：查询20和30部门的员工信息。
### 4.2.6 and和or的优先级问题

---

and和or同时出现时，and优先级较高，会先执行，如果希望or先执行，这个时候需要给or条件添加小括号。另外，以后遇到不确定的优先级时，可以通过添加小括号的方式来解决。对于优先级问题没必要记忆。
案例：找出薪资小于1500，并且部门编号是20或30的员工姓名、薪资、部门编号。
先来看一下错误写法：
```sql
select
  ename,sal,deptno
from
  emp
where
  sal < 1500 and deptno = 20 or deptno = 30;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621912213872-f2b1fe9e-384c-404e-bf24-d81bd895ae23.png#averageHue=%2311100f&height=388&id=DymCc&originHeight=388&originWidth=524&originalType=binary&ratio=1&rotation=0&showTitle=false&size=26693&status=done&style=shadow&title=&width=524)
认真解读题意得知：薪资小于1500是一个大前提，要找出的是薪资小于1500的，满足这个条件的前提下，再找部门编号是20或30的，显然以上的运行结果中出现了薪资为1600的，为什么1600的会出现呢？这是因为“sal < 1500 and deptno = 20”结合在一起了，“depnto = 30”成了一个独立的条件。会导致部门编号为30的所有员工全部查询出来。我们应该让“deptno = 20 or deptno = 30”结合在一起，正确写法如下：
```sql
select
  ename,sal,deptno
from
  emp
where
  sal < 1500 and (deptno = 20 or deptno = 30);
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621912713447-a9b7aeee-4998-4eae-8e53-71353a405890.png#averageHue=%2311100e&height=330&id=g19B4&originHeight=330&originWidth=539&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21912&status=done&style=shadow&title=&width=539)

- [ ] 任务：找出薪资小于1500的，并且工作岗位是CLERK和SALESMAN的员工姓名、薪资、岗位。
### 4.2.7 between...and...

---

between...and...等同于 >= and <=
做区间判断的，包含左右两个边界值。
它支持数字、日期、字符串等数据类型。
between...and...在使用时一定是**左小右大**。左大右小时无法查询到数据。
between...and... 和 >= and <=只是在写法结构上有区别，执行原理和效率方面没有区别。
案例：找出薪资在1600到3000的员工姓名、薪资
```sql
select 
  ename,sal
from
  emp
where
	sal between 1600 and 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621913942714-15a74832-d5da-4215-8991-35a3d48f7061.png#averageHue=%2312100f&height=344&id=GTVA6&originHeight=344&originWidth=374&originalType=binary&ratio=1&rotation=0&showTitle=false&size=17629&status=done&style=shadow&title=&width=374)
采用左大右小的方式：
```sql
select 
  ename,sal
from
  emp
where
	sal between 3000 and 1600;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621914030809-2ebf83da-aba0-429d-970e-2f6906611f11.png#averageHue=%2311100f&height=147&id=OG0Ah&originHeight=147&originWidth=358&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7418&status=done&style=shadow&title=&width=358)
没有查询到任何数据，所以在使用的时候一定要注意：**左小右大**。

- [ ] 任务：查询在1982-01-23到1987-04-19之间入职的员工

![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621914250873-25bff9ba-b4e6-4145-a5f8-9036fba35627.png#averageHue=%23161312&height=169&id=IPUnM&originHeight=169&originWidth=783&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20676&status=done&style=shadow&title=&width=783)
注意：以上SQL语句中日期需要加上单引号。
### 4.2.8 is null、is not null

---

判断某个数据是否为null，不能使用等号，只能使用 is null
判断某个数据是否不为null，不能使用不等号，只能使用 is not null
在数据库中null不是一个值，不能用等号和不等号衡量，null代表什么也没有，没有数据，没有值
案例1：找出津贴为空的员工姓名、薪资、津贴。
```sql
select
  ename,sal,comm
from
  emp
where
  comm is null;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621914737738-74345239-9ea8-4afa-a4bf-68fb0bb26e98.png#averageHue=%23161310&height=427&id=B8Ayw&originHeight=427&originWidth=298&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23224&status=done&style=shadow&title=&width=298)
我们使用等号，尝试一下：
```sql
select
  ename,sal,comm
from
  emp
where
  comm = null;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621914817611-97c0858b-a248-4a10-9fba-e5152283b553.png#averageHue=%2312100f&height=149&id=p0pLx&originHeight=149&originWidth=247&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5999&status=done&style=shadow&title=&width=247)
查询不到任何数据，所以判断是否为空，不能用等号。

案例2：找出津贴不为空的员工姓名、薪资、津贴
```sql
select
  ename,sal,comm
from
  emp
where
  comm is not null;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621914906515-cfd5351e-22bc-4184-b6d5-785f27049020.png#averageHue=%23141210&height=311&id=hC9OP&originHeight=311&originWidth=315&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15140&status=done&style=shadow&title=&width=315)
### 4.2.9 安全等于（了解）

---

<=>安全等于，用的很少，因为它的缺点是可读性差，了解即可。
<=>安全等于可作为普通运算符=，安全等于除了可以达到等号=的效果之外，还可以使用comm<=>null 代替comm is null。使用!(comm<=>null)代替comm is not null
案例1：找出薪资3000的员工姓名、岗位
```sql
select
  ename,job
from
  emp
where
  sal <=> 3000;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621948917056-c56bb7df-9764-4991-98ea-215bf224a1c4.png#averageHue=%2312110f&height=311&id=MIj9u&originHeight=311&originWidth=317&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13860&status=done&style=shadow&title=&width=317)
案例2：查找津贴是空的员工姓名、薪资、津贴
```sql
select
  ename, sal, comm
from
  emp
where
  comm <=> null;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621949017900-f5dede8a-abe2-4604-b284-44908345eeec.png#averageHue=%23151210&height=516&id=Tv12y&originHeight=516&originWidth=358&originalType=binary&ratio=1&rotation=0&showTitle=false&size=31629&status=done&style=shadow&title=&width=358)
案例3：查找津贴不是空的员工姓名、薪资、津贴
```sql
select
  ename, sal, comm
from
  emp
where
  !(comm <=> null);
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621949205597-28ad68b8-396d-4051-a313-0b695e918c64.png#averageHue=%23141210&height=364&id=qWKzk&originHeight=364&originWidth=427&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21730&status=done&style=shadow&title=&width=427)
### 4.2.10 in、not in

---

- in

job in('MANAGER','SALESMAN','CLERK') 等同于 job = 'MANAGER' or job = 'SALESMAN' or job = 'CLERK'
sal in(1600, 3000, 5000) 等同于 sal = 1600 or sal = 3000 or sal = 5000
in后面有一个小括号，小括号当中有多个值，值和值之间采用逗号隔开
sal in(1500, 5000)，需要注意的是：这个并不是说薪资在1500到5000之间，in不代表区间，表示sal是1500的和sal是5000的
案例1：找出工作岗位是MANAGER和SALESMAN的员工姓名、薪资、工作岗位
第一种：使用or
```sql
select
  ename,sal,job
from
  emp
where
  job = 'MANAGER' or job = 'SALESMAN';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621979207586-14dece4a-ce7f-4db8-a43f-bbfee6fd6133.png#averageHue=%2313110f&height=435&id=O2KwT&originHeight=435&originWidth=549&originalType=binary&ratio=1&rotation=0&showTitle=false&size=35206&status=done&style=shadow&title=&width=549)
第二种：使用in
```sql
select
  ename,sal,job
from
  emp
where
  job in('MANAGER', 'SALESMAN');
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621979288013-a6975d0e-46f9-43d8-a226-6df047e6490e.png#averageHue=%23141210&height=438&id=GI28U&originHeight=438&originWidth=470&originalType=binary&ratio=1&rotation=0&showTitle=false&size=33948&status=done&style=shadow&title=&width=470)
案例2：找出薪资是1500/1600/3000的员工姓名、工作岗位
```sql
select
  ename,job
from
  emp
where
  sal in(1500, 1600, 3000);
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621979430766-b7dc80d4-568a-4216-a173-6ec7c49d1f9c.png#averageHue=%2311100f&height=371&id=vsqSR&originHeight=371&originWidth=433&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20173&status=done&style=shadow&title=&width=433)

- [ ] 任务：找出部门编号是10和20的员工编号、姓名。（要求使用两种方案）

- not in

job not in('MANAGER','SALESMAN') 等同于 job <> 'MANAGER' and job <> 'SALESMAN'
sal not in(1600, 5000) 等同于 sal <> 1600 and sal <> 5000
案例：找出工作岗位不是MANAGER和SALESMAN的员工姓名、工作岗位
第一种：使用and
```sql
select 
  ename,job
from
  emp
where
  job <> 'MANAGER' and job <> 'SALESMAN';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621980958567-7c01fd48-a1ec-4392-85e1-120b86865b99.png#averageHue=%23100f0e&height=406&id=N24ds&originHeight=406&originWidth=599&originalType=binary&ratio=1&rotation=0&showTitle=false&size=26784&status=done&style=shadow&title=&width=599)
第二种：使用not in
```sql
select 
  ename,job
from
  emp
where
  job not in('MANAGER', 'SALESMAN');
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621981036376-d6cecc7a-b7b8-4342-a83e-19ee49d77697.png#averageHue=%23110f0e&height=436&id=udgWf&originHeight=436&originWidth=537&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28126&status=done&style=shadow&title=&width=537)

- [ ] 任务：找出薪资不是1600和3000的员工姓名、薪资。

- **in、not in 与 NULL**

先来看一下emp表中的数据
```sql
select * from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621981605595-632500b0-a2a0-401c-8995-1573468ae1f1.png#averageHue=%23161311&height=492&id=mVQz1&originHeight=492&originWidth=968&originalType=binary&ratio=1&rotation=0&showTitle=false&size=85972&status=done&style=shadow&title=&width=968)
通过表中数据观察到，有4个员工的津贴不为NULL，剩下10个员工的津贴都是NULL。
写这样一条SQL语句：
```sql
select * from emp where comm in(NULL, 300);
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621981810022-80718321-ffdd-496b-af1d-620cf268c993.png#averageHue=%23141211&height=172&id=xG35u&originHeight=172&originWidth=922&originalType=binary&ratio=1&rotation=0&showTitle=false&size=19587&status=done&style=shadow&title=&width=922)
为什么以上执行结果只有一条记录呢？分析一下：
首先你要知道in的执行原理实际上是采用=和or的方式，也就是说，以上SQL语句实际上是：
```sql
select * from emp where comm = NULL or comm = 300;
```
其中NULL不能用等号=进行判断，所以comm = NULL结果是false，然而中间使用的是or，所以comm = NULL被忽略了。所以查询结果就以上一条数据。
通过以上的测试得知：**in是自动忽略NULL的**。
再写这样一条SQL语句：
```sql
select * from emp where comm not in(NULL, 300);
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1621982073198-d77677ed-77de-4086-aba9-4eaeda923a51.png#averageHue=%23141210&height=56&id=TPlkq&originHeight=56&originWidth=656&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6518&status=done&style=shadow&title=&width=656)
以上的执行结果奇怪了，为什么没有查到任何数据呢？我们分析一下：
首先你要知道not in的执行原理实际上是采用<>和and的方式，也就是说，以上SQL语句实际上是：
```sql
select * from emp where comm <> NULL and comm <> 300;
```
其中NULL的判断不能使用<>，所以comm <> NULL结果是false，由于后面是and，and表示并且，comm <> NULL已经是false了，所以and右边的就没必要运算了，comm <> NULL and comm <> 300的整体运算结果就是false。所以查询不到任何数据。
通过以上测试得知，**not in是不会自动忽略NULL的**，所以在使用not in的时候一定要提前过滤掉NULL。
### 4.2.11 in和or的效率比拼

---

在MySQL当中，如何统计一个SQL语句的执行时长？

- 可以使用这个命令：show profiles;  这个命令可以查看在mysql中执行的所有SQL以及命令的耗费时长。
- show profiles; 是在mysql5.0.37之后添加的。所以要确保你的mysql版本没问题。
- 如何开启时长统计功能：set profiling = 1;
- 查看时长统计功能是否开启：show variables like '%pro%';
- 查看每条SQL的耗时：show profiles;
- 查看其中某条SQL耗时明细：show profile for query query_id;
- 查看最新一条SQL的耗时明细：show profile;
- 查看cpu，io等信息：show profile block io, cpu for query query_id; 

or的效率为O(n)，而in的效率为O(logn), 当n越大的时候效率相差越明显。以下是测试过程：
第一步，创建测试表，并生成测试数据，测试数据为1000万条记录。数据库中关闭了query cache，因此数据库缓存不会对查询造成影响。具体的代码如下：
```sql
#创建测试的test表
DROP TABLE IF EXISTS test; 
CREATE TABLE test( 
    ID INT(10) NOT NULL, 
    `Name` VARCHAR(20) DEFAULT '' NOT NULL, 
    PRIMARY KEY( ID ) 
)ENGINE=INNODB DEFAULT CHARSET utf8; 

#创建生成测试数据的存储过程
DROP PROCEDURE IF EXISTS pre_test; 
DELIMITER //
CREATE PROCEDURE pre_test() 
BEGIN 
DECLARE i INT DEFAULT 0; 
SET autocommit = 0; 
WHILE i<10000000 DO 
INSERT INTO test ( ID,`Name` ) VALUES( i, CONCAT( 'Carl', i ) ); 
SET i = i+1; 
IF i%2000 = 0 THEN 
COMMIT; 
END IF; 
END WHILE; 
END; //
DELIMITER ;

#执行存储过程生成测试数据
CALL pre_test();
```
以上SQL看不懂没关系，先执行它，进行数据初始化准备工作。
第二步：分三种情况进行测试，分别是：
第1种情况：in和or所在列为主键的情形。
第2种情况：in和or所在列创建有索引的情形。
第3种情况：in和or所在列没有索引的情形。
每种情况又采用不同的in和or的数量进行测试。由于测试语句的数据量有4种情况，我这里就称为A组、B组、C组、D组，其中A组为3个值，B组为150个值，C组为300个值，D组为1000个值。具体的测试语句如下：
```sql
#A组
#in和or中有3条数据的情况
SELECT * FROM test WHERE id IN (1,23,48);
SELECT * FROM test WHERE id =1 OR id=23 OR id=48;

#B组
#in和or中有150条数据的情况
SELECT * FROM test WHERE id IN (59617932,98114476,89047409,26968186,56586105,35488201,53251989,18182139,71164231,57655852,7948544,60658339,50758185,66667117,34771253,68699137,27877290,44275282,1585444,71219424,90937482,83928635,24588528,81933207,9607562,12013895,84640278,85549596,53249244,8567444,85402877,15040223,54266509,17718135,91687882,22930500,94756430,66031097,13084573,18137443,89917778,46845456,43939093,35943480,18213703,46362815,49835919,83137546,2101409,74932951,11984477,93113331,77848222,68546065,33728734,90793684,44975642,61387237,52483391,97716233,49449060,22411182,30776331,60597240,6911731,45789095,62075344,8379933,97910423,86861971,81342386,93423963,83852896,18566482,22747687,51420625,75862064,26402882,93958561,85202979,97049369,67674725,9475653,92302381,78133617,49295001,36517340,81387142,15707241,60832834,93157830,64171432,58537826,70141767,7326025,36632075,9639624,8900056,99702164,35108945,87820933,57302965,16652391,41845132,62184393,70136913,79574630,32562398,94616790,61258220,73162018,81644480,19453596,97380163,1204733,33357040,84854495,13888863,49041868,89272326,38405345,571248,6349029,70755321,79307694,60619684,92624181,73135306,23279848,95612954,55845916,6223606,43836918,37459781,67969314,99398872,7616960,37189193,50151920,62881879,12364637,33204320,27135672,28441504,47373461,87967926,30631796,20053540,18735984,83406724);
SELECT * FROM test WHERE id=59617932 OR id=98114476 OR id=89047409 OR id=26968186 OR id=56586105 OR id=35488201 OR id=53251989 OR id=18182139 OR id=71164231 OR id=57655852 OR id=7948544 OR id=60658339 OR id=50758185 OR id=66667117 OR id=34771253 OR id=68699137 OR id=27877290 OR id=44275282 OR id=1585444 OR id=71219424 OR id=90937482 OR id=83928635 OR id=24588528 OR id=81933207 OR id=9607562 OR id=12013895 OR id=84640278 OR id=85549596 OR id=53249244 OR id=8567444 OR id=85402877 OR id=15040223 OR id=54266509 OR id=17718135 OR id=91687882 OR id=22930500 OR id=94756430 OR id=66031097 OR id=13084573 OR id=18137443 OR id=89917778 OR id=46845456 OR id=43939093 OR id=35943480 OR id=18213703 OR id=46362815 OR id=49835919 OR id=83137546 OR id=2101409 OR id=74932951 OR id=11984477 OR id=93113331 OR id=77848222 OR id=68546065 OR id=33728734 OR id=90793684 OR id=44975642 OR id=61387237 OR id=52483391 OR id=97716233 OR id=49449060 OR id=22411182 OR id=30776331 OR id=60597240 OR id=6911731 OR id=45789095 OR id=62075344 OR id=8379933 OR id=97910423 OR id=86861971 OR id=81342386 OR id=93423963 OR id=83852896 OR id=18566482 OR id=22747687 OR id=51420625 OR id=75862064 OR id=26402882 OR id=93958561 OR id=85202979 OR id=97049369 OR id=67674725 OR id=9475653 OR id=92302381 OR id=78133617 OR id=49295001 OR id=36517340 OR id=81387142 OR id=15707241 OR id=60832834 OR id=93157830 OR id=64171432 OR id=58537826 OR id=70141767 OR id=7326025 OR id=36632075 OR id=9639624 OR id=8900056 OR id=99702164 OR id=35108945 OR id=87820933 OR id=57302965 OR id=16652391 OR id=41845132 OR id=62184393 OR id=70136913 OR id=79574630 OR id=32562398 OR id=94616790 OR id=61258220 OR id=73162018 OR id=81644480 OR id=19453596 OR id=97380163 OR id=1204733 OR id=33357040 OR id=84854495 OR id=13888863 OR id=49041868 OR id=89272326 OR id=38405345 OR id=571248 OR id=6349029 OR id=70755321 OR id=79307694 OR id=60619684 OR id=92624181 OR id=73135306 OR id=23279848 OR id=95612954 OR id=55845916 OR id=6223606 OR id=43836918 OR id=37459781 OR id=67969314 OR id=99398872 OR id=7616960 OR id=37189193 OR id=50151920 OR id=62881879 OR id=12364637 OR id=33204320 OR id=27135672 OR id=28441504 OR id=47373461 OR id=87967926 OR id=30631796 OR id=20053540 OR id=18735984 OR id=83406724;


#C组
#in和or中有300条数据的情况
SELECT * FROM test WHERE id IN (37092877,94859722,74276090,8763830,38727241,95732954,93414819,55070016,3591352,73857925,92290525,15210159,83905516,54934589,83004136,31442143,6060569,22209206,27649629,11464943,77822402,28714780,10058522,62252663,13751461,38997875,47320577,64507359,36137908,54297630,97411161,56542672,22017966,55190708,70072386,24300664,93413617,23621629,74772508,62774612,43001947,46161388,85563006,70177147,63960440,18001207,81734850,10635060,6551152,54877885,44426798,73950635,18713144,21690065,82153543,26048520,79954773,22411093,97307339,74193176,1413532,88006544,36062746,24043946,17132007,95958217,26112542,27303972,17247403,56778979,60928031,69369613,90584759,86234538,41726089,25315005,27568726,25091624,15307765,83130887,42726438,75872353,18991223,47819224,75457713,54659391,54889687,65229322,17124556,38376043,1989975,45973571,48597804,58632319,43388664,97010450,94745635,13217373,40472912,40220510,58319808,48228318,48936085,86281500,65466706,96815281,11751559,50188155,76649755,35315411,20360954,17739218,10918461,51429591,41447650,65170472,26810295,80912347,17157209,75851858,61150903,4408208,61200404,6655467,66863737,51549112,61951371,14368308,14663119,8762531,31765056,30560647,41048147,95526521,94929131,56881239,79014587,62705983,15892901,66151473,98846144,79336731,35949035,26250054,97536202,40575682,6965144,91059908,97939380,30854180,1965937,17193347,76584991,70467475,6559872,97386594,13939914,20379091,84906436,45989448,17337270,4949675,96963499,12561575,77153018,73213368,68283041,33977574,86290771,70381017,73095085,454900,44614195,48171334,49603342,7430998,29447060,47643508,82393912,83169846,94256496,35275444,40024984,25377535,46571333,32510994,70927802,92017916,97302502,22859741,32726786,79071601,93977472,47409421,49311618,77366144,84838598,59401507,67110877,42075938,76962007,27984930,72982484,81363683,75017478,88624177,67220235,88290070,26311443,87681081,77960250,4996033,68448074,67762279,99650583,36766422,27233152,71436659,25428777,81481679,51070397,88351803,78755075,26783938,83610840,45650662,86305644,1717314,66176062,6507047,45084786,74402982,55661367,35721238,40424913,24294239,30223531,55367671,56777532,12604154,4870493,14750488,74039611,42549918,70710424,56247316,63002053,71117605,16510883,67417211,34057637,74185092,58603491,66987830,73584171,9178319,47096502,1554825,37756804,85168245,92690138,6120773,99586029,74696745,61803307,56631845,42681796,58965644,68703695,69660559,15879062,26713059,85186928,63117471,53007808,74576547,32187857,13701205,88645881,24507258,87453800,39624977,75862710,62419627,70804059,10461373,18265782,56366177,68093007,75760763,43931574,65808002,49148775,98019987,71183123,53762434,78851856,37767085,89124453,47566746);

SELECT * FROM test WHERE id=37092877 OR id=94859722 OR id=74276090 OR id=8763830 OR id=38727241 OR id=95732954 OR id=93414819 OR id=55070016 OR id=3591352 OR id=73857925 OR id=92290525 OR id=15210159 OR id=83905516 OR id=54934589 OR id=83004136 OR id=31442143 OR id=6060569 OR id=22209206 OR id=27649629 OR id=11464943 OR id=77822402 OR id=28714780 OR id=10058522 OR id=62252663 OR id=13751461 OR id=38997875 OR id=47320577 OR id=64507359 OR id=36137908 OR id=54297630 OR id=97411161 OR id=56542672 OR id=22017966 OR id=55190708 OR id=70072386 OR id=24300664 OR id=93413617 OR id=23621629 OR id=74772508 OR id=62774612 OR id=43001947 OR id=46161388 OR id=85563006 OR id=70177147 OR id=63960440 OR id=18001207 OR id=81734850 OR id=10635060 OR id=6551152 OR id=54877885 OR id=44426798 OR id=73950635 OR id=18713144 OR id=21690065 OR id=82153543 OR id=26048520 OR id=79954773 OR id=22411093 OR id=97307339 OR id=74193176 OR id=1413532 OR id=88006544 OR id=36062746 OR id=24043946 OR id=17132007 OR id=95958217 OR id=26112542 OR id=27303972 OR id=17247403 OR id=56778979 OR id=60928031 OR id=69369613 OR id=90584759 OR id=86234538 OR id=41726089 OR id=25315005 OR id=27568726 OR id=25091624 OR id=15307765 OR id=83130887 OR id=42726438 OR id=75872353 OR id=18991223 OR id=47819224 OR id=75457713 OR id=54659391 OR id=54889687 OR id=65229322 OR id=17124556 OR id=38376043 OR id=1989975 OR id=45973571 OR id=48597804 OR id=58632319 OR id=43388664 OR id=97010450 OR id=94745635 OR id=13217373 OR id=40472912 OR id=40220510 OR id=58319808 OR id=48228318 OR id=48936085 OR id=86281500 OR id=65466706 OR id=96815281 OR id=11751559 OR id=50188155 OR id=76649755 OR id=35315411 OR id=20360954 OR id=17739218 OR id=10918461 OR id=51429591 OR id=41447650 OR id=65170472 OR id=26810295 OR id=80912347 OR id=17157209 OR id=75851858 OR id=61150903 OR id=4408208 OR id=61200404 OR id=6655467 OR id=66863737 OR id=51549112 OR id=61951371 OR id=14368308 OR id=14663119 OR id=8762531 OR id=31765056 OR id=30560647 OR id=41048147 OR id=95526521 OR id=94929131 OR id=56881239 OR id=79014587 OR id=62705983 OR id=15892901 OR id=66151473 OR id=98846144 OR id=79336731 OR id=35949035 OR id=26250054 OR id=97536202 OR id=40575682 OR id=6965144 OR id=91059908 OR id=97939380 OR id=30854180 OR id=1965937 OR id=17193347 OR id=76584991 OR id=70467475 OR id=6559872 OR id=97386594 OR id=13939914 OR id=20379091 OR id=84906436 OR id=45989448 OR id=17337270 OR id=4949675 OR id=96963499 OR id=12561575 OR id=77153018 OR id=73213368 OR id=68283041 OR id=33977574 OR id=86290771 OR id=70381017 OR id=73095085 OR id=454900 OR id=44614195 OR id=48171334 OR id=49603342 OR id=7430998 OR id=29447060 OR id=47643508 OR id=82393912 OR id=83169846 OR id=94256496 OR id=35275444 OR id=40024984 OR id=25377535 OR id=46571333 OR id=32510994 OR id=70927802 OR id=92017916 OR id=97302502 OR id=22859741 OR id=32726786 OR id=79071601 OR id=93977472 OR id=47409421 OR id=49311618 OR id=77366144 OR id=84838598 OR id=59401507 OR id=67110877 OR id=42075938 OR id=76962007 OR id=27984930 OR id=72982484 OR id=81363683 OR id=75017478 OR id=88624177 OR id=67220235 OR id=88290070 OR id=26311443 OR id=87681081 OR id=77960250 OR id=4996033 OR id=68448074 OR id=67762279 OR id=99650583 OR id=36766422 OR id=27233152 OR id=71436659 OR id=25428777 OR id=81481679 OR id=51070397 OR id=88351803 OR id=78755075 OR id=26783938 OR id=83610840 OR id=45650662 OR id=86305644 OR id=1717314 OR id=66176062 OR id=6507047 OR id=45084786 OR id=74402982 OR id=55661367 OR id=35721238 OR id=40424913 OR id=24294239 OR id=30223531 OR id=55367671 OR id=56777532 OR id=12604154 OR id=4870493 OR id=14750488 OR id=74039611 OR id=42549918 OR id=70710424 OR id=56247316 OR id=63002053 OR id=71117605 OR id=16510883 OR id=67417211 OR id=34057637 OR id=74185092 OR id=58603491 OR id=66987830 OR id=73584171 OR id=9178319 OR id=47096502 OR id=1554825 OR id=37756804 OR id=85168245 OR id=92690138 OR id=6120773 OR id=99586029 OR id=74696745 OR id=61803307 OR id=56631845 OR id=42681796 OR id=58965644 OR id=68703695 OR id=69660559 OR id=15879062 OR id=26713059 OR id=85186928 OR id=63117471 OR id=53007808 OR id=74576547 OR id=32187857 OR id=13701205 OR id=88645881 OR id=24507258 OR id=87453800 OR id=39624977 OR id=75862710 OR id=62419627 OR id=70804059 OR id=10461373 OR id=18265782 OR id=56366177 OR id=68093007 OR id=75760763 OR id=43931574 OR id=65808002 OR id=49148775 OR id=98019987 OR id=71183123 OR id=53762434 OR id=78851856 OR id=37767085 OR id=89124453 OR id=47566746;


#D组
#in和or中有1000条数据的情况
SELECT * FROM test WHERE id IN (93674701,9720356,31732184,53855095,33144472,71864888,27541768,27238726,83648428,12942332,26918445,19781953,81861032,74800064,12286132,6624397,64942581,70512799,46356598,88292448,87069909,38175756,98121997,62570414,15900806,51527968,89092372,8084203,53772848,78871524,3608561,85909562,41702172,61800503,57877634,93407278,30824340,13159046,49055339,73058078,983603,73571456,51694978,75136628,82716874,83551181,7964224,47505945,92695321,15885152,79282709,18572099,27392970,14552787,19848227,4518183,11773920,22285326,71605145,2402625,63365854,70973600,10584706,83688869,84268419,6026005,36545233,24462648,19293921,17561083,52105483,59243514,35230465,34650779,30053489,24225251,59642405,81933853,94495716,26364324,25980634,5579237,14569289,89417845,71178959,4143920,20467990,53316808,21288525,82249537,37737589,44712689,36788133,15668654,4697556,63785060,11555169,36401204,92276179,4135929,75453019,28231031,8649240,11576980,20262028,56242424,11305608,5655216,90240601,28569373,5296027,10739594,72751648,22531251,12535926,36347415,19740655,69125465,7523885,88128548,88830806,25010302,29411467,99614288,32646290,16592563,69036910,32604729,88737786,90169676,57646877,72105460,40027541,70362483,37221415,25284914,69691185,17972978,1544661,47324366,25337670,91133621,63697117,48652228,18538437,79966496,26066529,65334307,8305141,86289387,20178085,88836090,74948034,14101728,7837868,83548120,65602502,83129211,24785681,65000269,49140174,62636621,31096695,52276400,28546681,83631937,57100225,42531528,28326396,38641032,93055463,20525612,66073509,35154065,29007664,12600294,76829494,73917074,67226149,12478806,39842542,70312958,82792046,49668650,46280815,96555182,22966062,83158116,87566530,66277804,7944142,90649884,64342810,9881875,14833854,82959569,50523207,48788762,3801076,14677723,63080506,96215352,36302231,35067168,11695282,19447382,66401373,40822285,41406321,48630216,78955925,57194625,52097877,16169037,44834346,2593695,29948466,41842778,50510473,39669493,64590865,26160800,94882286,2703212,41243905,89363549,82819429,25565895,86836890,58385785,55898457,99305620,43332680,98223672,4494624,25408421,28054121,48197701,90633404,25825550,90631154,24867226,61846156,38911183,67826056,10676975,57116645,474292,82387517,56211477,46555785,49282428,99468990,81172472,26720330,38692582,96073680,88412290,28829489,1816508,75321051,81650509,23175973,42008725,60743468,52532114,731909,77811415,86804961,29675484,33584929,180367,93687804,41093066,5987495,27291494,78229979,63194139,34357776,9992084,22643334,22407822,69740170,29581361,50036776,88768091,82537322,83709895,55361776,90616169,44595355,9468440,54552233,73496954,46104486,92947715,38522993,88515232,57725249,48507967,25309486,91597013,85635814,69579638,68775627,57556546,77900275,95965693,9601780,5448068,54075952,64335883,80114875,14793294,21016639,1959922,93176996,7893733,51407895,45849129,33857790,30096194,78021982,66555961,15842998,77678123,56648395,8171848,80152264,78616680,80098122,22882409,77242219,3124519,60865422,43164198,43256621,73261157,12541949,49780175,23167183,10509251,41809106,25655902,6752559,39850293,50992519,40061483,84526968,93056718,53267125,53914467,39404926,83672449,21484465,34147538,13437853,74079093,50400032,85705998,7557614,10300505,79264856,65669946,23899714,53506926,36081544,11113765,65755643,5826515,60392667,55562374,98132987,80904530,92663352,7283593,3709276,52078745,84847057,34235334,63889320,70036669,58603533,27394053,54766781,50920854,80202681,67618417,82912294,20150728,20042189,86403320,38738266,58393070,50887299,12170654,16212895,37361223,13677457,19503506,20213757,84240441,39618969,26401150,47937678,55871130,79189571,5717133,12444503,95283334,14827147,22008485,56345882,43237192,56980197,68699371,46407250,72120555,70694039,46438829,17774982,36484024,138767,89563532,54847019,7815592,44909604,50479084,17462504,96594465,58317102,92426225,91894699,4501659,43315607,9442814,19705166,87751308,95588126,92372510,20281564,19251355,10321183,34573093,19074704,84678191,24383998,27670253,50223562,34091936,99304371,32477827,54273037,86525073,73253547,33316827,6724062,76707318,78171148,44729510,16697684,68966388,57448392,51380186,35344477,98153122,51825492,27202774,26901641,37527637,88241695,15100257,30418000,21821200,95511035,9289513,83870196,54628801,39402988,88345504,84232433,13925255,70816934,6822742,14400466,430652,87397095,89773413,10883914,89939310,39597573,49356789,62857680,93292662,55644642,81922551,94304087,63705961,137763,22392805,65195561,39498904,22576234,59467794,46389072,66341462,44602153,18204976,45366397,3880945,98231882,27999162,38209350,10599910,77139550,35114264,57109708,93064441,34801782,24938667,84955486,53018874,37969943,64372852,69596670,21288762,12774121,97588451,23575359,10954061,50363988,56263940,61520763,85096643,36250068,19807406,20984386,24520668,44631794,62587890,44963362,7663521,78505677,98442373,90280978,14494324,16069861,11397153,87726305,26133866,42024935,93393929,72575268,76384597,42272046,81658814,40811718,86054463,35997739,51075676,62839927,68179261,19292480,10464999,6342696,75842285,28671096,30029838,19617648,94667632,75855376,83477767,456684,81197213,1961395,79590898,470693,64786459,90138714,30486571,75566704,64467558,21380112,17742907,7733647,92017,64615799,72272722,66873854,77198963,35594848,42694993,12431322,2247181,11020746,42416726,19127785,95444937,36842133,4203521,48149533,45322440,59710953,38250773,31370132,26889920,45927952,55298246,31197238,44744953,35531670,38850041,29759177,76433451,33696500,2823716,68574340,68889919,35744793,64772909,41562277,72606631,54617176,76086087,61060196,1593669,4666059,44201567,97015910,51039786,47534369,36899420,95163693,34278055,24361819,93200909,29991418,63172824,53644148,61454424,44726508,64910883,31088636,14005026,83267869,28497493,12406441,34686539,70646963,7687253,23115957,64556990,49701688,76843379,22370877,11199132,15492661,72101877,47154152,54969058,96696025,33567129,95788960,13301506,38695877,52992551,37817234,82136809,28111091,84977065,93404791,56350318,27576451,84170153,37381626,22432144,35119973,23922989,98961080,14336913,49612713,47410677,41559348,64216475,75502736,16203656,81726720,64541981,82181762,95869963,1086041,76856852,99484886,47292021,99746735,79082859,67416188,46391963,58631281,80994168,9464550,5851058,16534935,63307701,91875109,18716507,15870646,6003995,836024,35610568,39574140,76244639,83403189,51252728,6516065,94907007,81605606,40398075,40258386,6692981,50852074,2869416,97682971,44427361,9608914,58464559,81806036,20047387,66264452,58063775,54179837,48463792,17877188,31718426,64192249,35574859,3671766,88905164,78137697,46929619,21063327,83078770,93293821,41618319,3832324,91310612,79854291,68734227,8826717,80881657,95208907,7079422,30037415,5494004,44809486,97620027,35689182,13120783,26108678,1537176,16538727,50841024,36515680,82635278,11112660,16276555,72997511,93487848,88201238,53997085,15198916,61214583,78412499,3585265,1402827,56445518,47661453,25615629,58263458,62155263,46608555,15822703,82285214,76021596,84571697,45999350,40074628,8219220,5429523,74024203,22354037,17605466,60436920,52777032,65801717,43656316,10424270,48035786,29493228,83897372,62101275,84793857,56894828,70636689,72497148,67388694,68146510,64298548,97117498,25553211,54226533,90395845,24172623,91712292,98280822,54042497,25032894,6833135,39011254,9837753,63507766,26747954,45941264,99955245,80051546,78510759,71322333,92407609,95809491,18999217,23430377,11861293,42583098,24163209,11358738,3237302,3176665,87151132,2789150,63905882,59864282,3673596,19570439,22883042,72375525,51614404,47526636,98443133,99140135,33855918,28333489,81416033,2670097,4897577,24439616,36643479,40817600,76022791,40072872,95193435,96967607,24983145,49883271,94602753,83555050,85455145,34563229,72328311,12002151,71481181,72998351,1489188,38426973,91893116,61594591,89693630,6268166,20056665,62169880,17143472,35103925,22452590,54272289,34236829,78028543,84474414,40386926,50550952,49413559,48781941,22927237,44447815,29960478,47578119,10192558,87733936,88699383,38808712,79944807,84014713,31865463,72617685,19557568,47865990,39069638,20086122,1777562,29018078,78358083,94561719,46281152,99789008,86929490,16534451,55989144,52455669,54561585,97379646,20416183,87617750,76115505,3282482,8383619,45456319,29576432,67750627,61736333,33745442,51502165,35349384,78106651,23232822,94851387,78254073,82406754,10317954,70125940,45067526,27061875,25640164,52574899,93819227,93789607,96122951,31673246,70431904,54067896,37146857,37817889,14058940,60710246,64844350,91604383,71972005,13888349,19093493,27397281,61085409,66529387,82761299,72236310,19277077,96599501,68304096,48292937,97503321,88011133,29224803,79782945,79965966,83716914,90432214,48938902,12498489,30246261,91624049,68652396,23677785,44084687,3865123,37823170,45287730,38784682,28058351,68226368,61569897,44737876,70575908,25568463,24668386,88650569,35559584,1897737,77844785,29780669,84004602,29029776,91003545,48058106,9463847);

SELECT * FROM test WHERE id=93674701 OR id=9720356 OR id=31732184 OR id=53855095 OR id=33144472 OR id=71864888 OR id=27541768 OR id=27238726 OR id=83648428 OR id=12942332 OR id=26918445 OR id=19781953 OR id=81861032 OR id=74800064 OR id=12286132 OR id=6624397 OR id=64942581 OR id=70512799 OR id=46356598 OR id=88292448 OR id=87069909 OR id=38175756 OR id=98121997 OR id=62570414 OR id=15900806 OR id=51527968 OR id=89092372 OR id=8084203 OR id=53772848 OR id=78871524 OR id=3608561 OR id=85909562 OR id=41702172 OR id=61800503 OR id=57877634 OR id=93407278 OR id=30824340 OR id=13159046 OR id=49055339 OR id=73058078 OR id=983603 OR id=73571456 OR id=51694978 OR id=75136628 OR id=82716874 OR id=83551181 OR id=7964224 OR id=47505945 OR id=92695321 OR id=15885152 OR id=79282709 OR id=18572099 OR id=27392970 OR id=14552787 OR id=19848227 OR id=4518183 OR id=11773920 OR id=22285326 OR id=71605145 OR id=2402625 OR id=63365854 OR id=70973600 OR id=10584706 OR id=83688869 OR id=84268419 OR id=6026005 OR id=36545233 OR id=24462648 OR id=19293921 OR id=17561083 OR id=52105483 OR id=59243514 OR id=35230465 OR id=34650779 OR id=30053489 OR id=24225251 OR id=59642405 OR id=81933853 OR id=94495716 OR id=26364324 OR id=25980634 OR id=5579237 OR id=14569289 OR id=89417845 OR id=71178959 OR id=4143920 OR id=20467990 OR id=53316808 OR id=21288525 OR id=82249537 OR id=37737589 OR id=44712689 OR id=36788133 OR id=15668654 OR id=4697556 OR id=63785060 OR id=11555169 OR id=36401204 OR id=92276179 OR id=4135929 OR id=75453019 OR id=28231031 OR id=8649240 OR id=11576980 OR id=20262028 OR id=56242424 OR id=11305608 OR id=5655216 OR id=90240601 OR id=28569373 OR id=5296027 OR id=10739594 OR id=72751648 OR id=22531251 OR id=12535926 OR id=36347415 OR id=19740655 OR id=69125465 OR id=7523885 OR id=88128548 OR id=88830806 OR id=25010302 OR id=29411467 OR id=99614288 OR id=32646290 OR id=16592563 OR id=69036910 OR id=32604729 OR id=88737786 OR id=90169676 OR id=57646877 OR id=72105460 OR id=40027541 OR id=70362483 OR id=37221415 OR id=25284914 OR id=69691185 OR id=17972978 OR id=1544661 OR id=47324366 OR id=25337670 OR id=91133621 OR id=63697117 OR id=48652228 OR id=18538437 OR id=79966496 OR id=26066529 OR id=65334307 OR id=8305141 OR id=86289387 OR id=20178085 OR id=88836090 OR id=74948034 OR id=14101728 OR id=7837868 OR id=83548120 OR id=65602502 OR id=83129211 OR id=24785681 OR id=65000269 OR id=49140174 OR id=62636621 OR id=31096695 OR id=52276400 OR id=28546681 OR id=83631937 OR id=57100225 OR id=42531528 OR id=28326396 OR id=38641032 OR id=93055463 OR id=20525612 OR id=66073509 OR id=35154065 OR id=29007664 OR id=12600294 OR id=76829494 OR id=73917074 OR id=67226149 OR id=12478806 OR id=39842542 OR id=70312958 OR id=82792046 OR id=49668650 OR id=46280815 OR id=96555182 OR id=22966062 OR id=83158116 OR id=87566530 OR id=66277804 OR id=7944142 OR id=90649884 OR id=64342810 OR id=9881875 OR id=14833854 OR id=82959569 OR id=50523207 OR id=48788762 OR id=3801076 OR id=14677723 OR id=63080506 OR id=96215352 OR id=36302231 OR id=35067168 OR id=11695282 OR id=19447382 OR id=66401373 OR id=40822285 OR id=41406321 OR id=48630216 OR id=78955925 OR id=57194625 OR id=52097877 OR id=16169037 OR id=44834346 OR id=2593695 OR id=29948466 OR id=41842778 OR id=50510473 OR id=39669493 OR id=64590865 OR id=26160800 OR id=94882286 OR id=2703212 OR id=41243905 OR id=89363549 OR id=82819429 OR id=25565895 OR id=86836890 OR id=58385785 OR id=55898457 OR id=99305620 OR id=43332680 OR id=98223672 OR id=4494624 OR id=25408421 OR id=28054121 OR id=48197701 OR id=90633404 OR id=25825550 OR id=90631154 OR id=24867226 OR id=61846156 OR id=38911183 OR id=67826056 OR id=10676975 OR id=57116645 OR id=474292 OR id=82387517 OR id=56211477 OR id=46555785 OR id=49282428 OR id=99468990 OR id=81172472 OR id=26720330 OR id=38692582 OR id=96073680 OR id=88412290 OR id=28829489 OR id=1816508 OR id=75321051 OR id=81650509 OR id=23175973 OR id=42008725 OR id=60743468 OR id=52532114 OR id=731909 OR id=77811415 OR id=86804961 OR id=29675484 OR id=33584929 OR id=180367 OR id=93687804 OR id=41093066 OR id=5987495 OR id=27291494 OR id=78229979 OR id=63194139 OR id=34357776 OR id=9992084 OR id=22643334 OR id=22407822 OR id=69740170 OR id=29581361 OR id=50036776 OR id=88768091 OR id=82537322 OR id=83709895 OR id=55361776 OR id=90616169 OR id=44595355 OR id=9468440 OR id=54552233 OR id=73496954 OR id=46104486 OR id=92947715 OR id=38522993 OR id=88515232 OR id=57725249 OR id=48507967 OR id=25309486 OR id=91597013 OR id=85635814 OR id=69579638 OR id=68775627 OR id=57556546 OR id=77900275 OR id=95965693 OR id=9601780 OR id=5448068 OR id=54075952 OR id=64335883 OR id=80114875 OR id=14793294 OR id=21016639 OR id=1959922 OR id=93176996 OR id=7893733 OR id=51407895 OR id=45849129 OR id=33857790 OR id=30096194 OR id=78021982 OR id=66555961 OR id=15842998 OR id=77678123 OR id=56648395 OR id=8171848 OR id=80152264 OR id=78616680 OR id=80098122 OR id=22882409 OR id=77242219 OR id=3124519 OR id=60865422 OR id=43164198 OR id=43256621 OR id=73261157 OR id=12541949 OR id=49780175 OR id=23167183 OR id=10509251 OR id=41809106 OR id=25655902 OR id=6752559 OR id=39850293 OR id=50992519 OR id=40061483 OR id=84526968 OR id=93056718 OR id=53267125 OR id=53914467 OR id=39404926 OR id=83672449 OR id=21484465 OR id=34147538 OR id=13437853 OR id=74079093 OR id=50400032 OR id=85705998 OR id=7557614 OR id=10300505 OR id=79264856 OR id=65669946 OR id=23899714 OR id=53506926 OR id=36081544 OR id=11113765 OR id=65755643 OR id=5826515 OR id=60392667 OR id=55562374 OR id=98132987 OR id=80904530 OR id=92663352 OR id=7283593 OR id=3709276 OR id=52078745 OR id=84847057 OR id=34235334 OR id=63889320 OR id=70036669 OR id=58603533 OR id=27394053 OR id=54766781 OR id=50920854 OR id=80202681 OR id=67618417 OR id=82912294 OR id=20150728 OR id=20042189 OR id=86403320 OR id=38738266 OR id=58393070 OR id=50887299 OR id=12170654 OR id=16212895 OR id=37361223 OR id=13677457 OR id=19503506 OR id=20213757 OR id=84240441 OR id=39618969 OR id=26401150 OR id=47937678 OR id=55871130 OR id=79189571 OR id=5717133 OR id=12444503 OR id=95283334 OR id=14827147 OR id=22008485 OR id=56345882 OR id=43237192 OR id=56980197 OR id=68699371 OR id=46407250 OR id=72120555 OR id=70694039 OR id=46438829 OR id=17774982 OR id=36484024 OR id=138767 OR id=89563532 OR id=54847019 OR id=7815592 OR id=44909604 OR id=50479084 OR id=17462504 OR id=96594465 OR id=58317102 OR id=92426225 OR id=91894699 OR id=4501659 OR id=43315607 OR id=9442814 OR id=19705166 OR id=87751308 OR id=95588126 OR id=92372510 OR id=20281564 OR id=19251355 OR id=10321183 OR id=34573093 OR id=19074704 OR id=84678191 OR id=24383998 OR id=27670253 OR id=50223562 OR id=34091936 OR id=99304371 OR id=32477827 OR id=54273037 OR id=86525073 OR id=73253547 OR id=33316827 OR id=6724062 OR id=76707318 OR id=78171148 OR id=44729510 OR id=16697684 OR id=68966388 OR id=57448392 OR id=51380186 OR id=35344477 OR id=98153122 OR id=51825492 OR id=27202774 OR id=26901641 OR id=37527637 OR id=88241695 OR id=15100257 OR id=30418000 OR id=21821200 OR id=95511035 OR id=9289513 OR id=83870196 OR id=54628801 OR id=39402988 OR id=88345504 OR id=84232433 OR id=13925255 OR id=70816934 OR id=6822742 OR id=14400466 OR id=430652 OR id=87397095 OR id=89773413 OR id=10883914 OR id=89939310 OR id=39597573 OR id=49356789 OR id=62857680 OR id=93292662 OR id=55644642 OR id=81922551 OR id=94304087 OR id=63705961 OR id=137763 OR id=22392805 OR id=65195561 OR id=39498904 OR id=22576234 OR id=59467794 OR id=46389072 OR id=66341462 OR id=44602153 OR id=18204976 OR id=45366397 OR id=3880945 OR id=98231882 OR id=27999162 OR id=38209350 OR id=10599910 OR id=77139550 OR id=35114264 OR id=57109708 OR id=93064441 OR id=34801782 OR id=24938667 OR id=84955486 OR id=53018874 OR id=37969943 OR id=64372852 OR id=69596670 OR id=21288762 OR id=12774121 OR id=97588451 OR id=23575359 OR id=10954061 OR id=50363988 OR id=56263940 OR id=61520763 OR id=85096643 OR id=36250068 OR id=19807406 OR id=20984386 OR id=24520668 OR id=44631794 OR id=62587890 OR id=44963362 OR id=7663521 OR id=78505677 OR id=98442373 OR id=90280978 OR id=14494324 OR id=16069861 OR id=11397153 OR id=87726305 OR id=26133866 OR id=42024935 OR id=93393929 OR id=72575268 OR id=76384597 OR id=42272046 OR id=81658814 OR id=40811718 OR id=86054463 OR id=35997739 OR id=51075676 OR id=62839927 OR id=68179261 OR id=19292480 OR id=10464999 OR id=6342696 OR id=75842285 OR id=28671096 OR id=30029838 OR id=19617648 OR id=94667632 OR id=75855376 OR id=83477767 OR id=456684 OR id=81197213 OR id=1961395 OR id=79590898 OR id=470693 OR id=64786459 OR id=90138714 OR id=30486571 OR id=75566704 OR id=64467558 OR id=21380112 OR id=17742907 OR id=7733647 OR id=92017 OR id=64615799 OR id=72272722 OR id=66873854 OR id=77198963 OR id=35594848 OR id=42694993 OR id=12431322 OR id=2247181 OR id=11020746 OR id=42416726 OR id=19127785 OR id=95444937 OR id=36842133 OR id=4203521 OR id=48149533 OR id=45322440 OR id=59710953 OR id=38250773 OR id=31370132 OR id=26889920 OR id=45927952 OR id=55298246 OR id=31197238 OR id=44744953 OR id=35531670 OR id=38850041 OR id=29759177 OR id=76433451 OR id=33696500 OR id=2823716 OR id=68574340 OR id=68889919 OR id=35744793 OR id=64772909 OR id=41562277 OR id=72606631 OR id=54617176 OR id=76086087 OR id=61060196 OR id=1593669 OR id=4666059 OR id=44201567 OR id=97015910 OR id=51039786 OR id=47534369 OR id=36899420 OR id=95163693 OR id=34278055 OR id=24361819 OR id=93200909 OR id=29991418 OR id=63172824 OR id=53644148 OR id=61454424 OR id=44726508 OR id=64910883 OR id=31088636 OR id=14005026 OR id=83267869 OR id=28497493 OR id=12406441 OR id=34686539 OR id=70646963 OR id=7687253 OR id=23115957 OR id=64556990 OR id=49701688 OR id=76843379 OR id=22370877 OR id=11199132 OR id=15492661 OR id=72101877 OR id=47154152 OR id=54969058 OR id=96696025 OR id=33567129 OR id=95788960 OR id=13301506 OR id=38695877 OR id=52992551 OR id=37817234 OR id=82136809 OR id=28111091 OR id=84977065 OR id=93404791 OR id=56350318 OR id=27576451 OR id=84170153 OR id=37381626 OR id=22432144 OR id=35119973 OR id=23922989 OR id=98961080 OR id=14336913 OR id=49612713 OR id=47410677 OR id=41559348 OR id=64216475 OR id=75502736 OR id=16203656 OR id=81726720 OR id=64541981 OR id=82181762 OR id=95869963 OR id=1086041 OR id=76856852 OR id=99484886 OR id=47292021 OR id=99746735 OR id=79082859 OR id=67416188 OR id=46391963 OR id=58631281 OR id=80994168 OR id=9464550 OR id=5851058 OR id=16534935 OR id=63307701 OR id=91875109 OR id=18716507 OR id=15870646 OR id=6003995 OR id=836024 OR id=35610568 OR id=39574140 OR id=76244639 OR id=83403189 OR id=51252728 OR id=6516065 OR id=94907007 OR id=81605606 OR id=40398075 OR id=40258386 OR id=6692981 OR id=50852074 OR id=2869416 OR id=97682971 OR id=44427361 OR id=9608914 OR id=58464559 OR id=81806036 OR id=20047387 OR id=66264452 OR id=58063775 OR id=54179837 OR id=48463792 OR id=17877188 OR id=31718426 OR id=64192249 OR id=35574859 OR id=3671766 OR id=88905164 OR id=78137697 OR id=46929619 OR id=21063327 OR id=83078770 OR id=93293821 OR id=41618319 OR id=3832324 OR id=91310612 OR id=79854291 OR id=68734227 OR id=8826717 OR id=80881657 OR id=95208907 OR id=7079422 OR id=30037415 OR id=5494004 OR id=44809486 OR id=97620027 OR id=35689182 OR id=13120783 OR id=26108678 OR id=1537176 OR id=16538727 OR id=50841024 OR id=36515680 OR id=82635278 OR id=11112660 OR id=16276555 OR id=72997511 OR id=93487848 OR id=88201238 OR id=53997085 OR id=15198916 OR id=61214583 OR id=78412499 OR id=3585265 OR id=1402827 OR id=56445518 OR id=47661453 OR id=25615629 OR id=58263458 OR id=62155263 OR id=46608555 OR id=15822703 OR id=82285214 OR id=76021596 OR id=84571697 OR id=45999350 OR id=40074628 OR id=8219220 OR id=5429523 OR id=74024203 OR id=22354037 OR id=17605466 OR id=60436920 OR id=52777032 OR id=65801717 OR id=43656316 OR id=10424270 OR id=48035786 OR id=29493228 OR id=83897372 OR id=62101275 OR id=84793857 OR id=56894828 OR id=70636689 OR id=72497148 OR id=67388694 OR id=68146510 OR id=64298548 OR id=97117498 OR id=25553211 OR id=54226533 OR id=90395845 OR id=24172623 OR id=91712292 OR id=98280822 OR id=54042497 OR id=25032894 OR id=6833135 OR id=39011254 OR id=9837753 OR id=63507766 OR id=26747954 OR id=45941264 OR id=99955245 OR id=80051546 OR id=78510759 OR id=71322333 OR id=92407609 OR id=95809491 OR id=18999217 OR id=23430377 OR id=11861293 OR id=42583098 OR id=24163209 OR id=11358738 OR id=3237302 OR id=3176665 OR id=87151132 OR id=2789150 OR id=63905882 OR id=59864282 OR id=3673596 OR id=19570439 OR id=22883042 OR id=72375525 OR id=51614404 OR id=47526636 OR id=98443133 OR id=99140135 OR id=33855918 OR id=28333489 OR id=81416033 OR id=2670097 OR id=4897577 OR id=24439616 OR id=36643479 OR id=40817600 OR id=76022791 OR id=40072872 OR id=95193435 OR id=96967607 OR id=24983145 OR id=49883271 OR id=94602753 OR id=83555050 OR id=85455145 OR id=34563229 OR id=72328311 OR id=12002151 OR id=71481181 OR id=72998351 OR id=1489188 OR id=38426973 OR id=91893116 OR id=61594591 OR id=89693630 OR id=6268166 OR id=20056665 OR id=62169880 OR id=17143472 OR id=35103925 OR id=22452590 OR id=54272289 OR id=34236829 OR id=78028543 OR id=84474414 OR id=40386926 OR id=50550952 OR id=49413559 OR id=48781941 OR id=22927237 OR id=44447815 OR id=29960478 OR id=47578119 OR id=10192558 OR id=87733936 OR id=88699383 OR id=38808712 OR id=79944807 OR id=84014713 OR id=31865463 OR id=72617685 OR id=19557568 OR id=47865990 OR id=39069638 OR id=20086122 OR id=1777562 OR id=29018078 OR id=78358083 OR id=94561719 OR id=46281152 OR id=99789008 OR id=86929490 OR id=16534451 OR id=55989144 OR id=52455669 OR id=54561585 OR id=97379646 OR id=20416183 OR id=87617750 OR id=76115505 OR id=3282482 OR id=8383619 OR id=45456319 OR id=29576432 OR id=67750627 OR id=61736333 OR id=33745442 OR id=51502165 OR id=35349384 OR id=78106651 OR id=23232822 OR id=94851387 OR id=78254073 OR id=82406754 OR id=10317954 OR id=70125940 OR id=45067526 OR id=27061875 OR id=25640164 OR id=52574899 OR id=93819227 OR id=93789607 OR id=96122951 OR id=31673246 OR id=70431904 OR id=54067896 OR id=37146857 OR id=37817889 OR id=14058940 OR id=60710246 OR id=64844350 OR id=91604383 OR id=71972005 OR id=13888349 OR id=19093493 OR id=27397281 OR id=61085409 OR id=66529387 OR id=82761299 OR id=72236310 OR id=19277077 OR id=96599501 OR id=68304096 OR id=48292937 OR id=97503321 OR id=88011133 OR id=29224803 OR id=79782945 OR id=79965966 OR id=83716914 OR id=90432214 OR id=48938902 OR id=12498489 OR id=30246261 OR id=91624049 OR id=68652396 OR id=23677785 OR id=44084687 OR id=3865123 OR id=37823170 OR id=45287730 OR id=38784682 OR id=28058351 OR id=68226368 OR id=61569897 OR id=44737876 OR id=70575908 OR id=25568463 OR id=24668386 OR id=88650569 OR id=35559584 OR id=1897737 OR id=77844785 OR id=29780669 OR id=84004602 OR id=29029776 OR id=91003545 OR id=48058106 OR id=9463847;
```
测试结果如下：
第一种情况，ID列为主键的情况，4组测试执行计划一样，执行的时间也基本没有区别。
A组or和in的执行时间： or的执行时间为：0.002s     in的执行时间为：0.002s
B组or和in的执行时间： or的执行时间为：0.004s     in的执行时间为：0.004s
C组or和in的执行时间： or的执行时间为：0.006s     in的执行时间为：0.005s
D组or和in的执行时间： or的执行时间为：0.018s     in的执行时间为：0.014s
第二种情况，ID列为一般索引的情况，4组测试执行计划一样，执行的时间也基本没有区别。
A组or和in的执行时间： or的执行时间为：0.002s     in的执行时间为：0.002s
B组or和in的执行时间： or的执行时间为：0.006s     in的执行时间为：0.005s  
C组or和in的执行时间： or的执行时间为：0.008s     in的执行时间为：0.008s
D组or和in的执行时间： or的执行时间为：0.021s     in的执行时间为：0.020s  
第三种情况，ID列没有索引的情况，4组测试执行计划一样，执行的时间有很大的区别。
A组or和in的执行时间： or的执行时间为：5.016s      in的执行时间为：5.071s
B组or和in的执行时间： or的执行时间为：1min 02s     in的执行时间为：5.018s
C组or和in的执行时间： or的执行时间为：1min 55s     in的执行时间为：5.018s
D组or和in的执行时间： or的执行时间为：6min 17s     in的执行时间为：5.057s

结论：从上面的测试结果，可以看出如果in和or所在列有索引或者主键的话，or和in没啥差别，执行计划和执行时间都几乎一样。如果in和or所在列没有索引的话，性能差别就很大了。在没有索引的情况下，随着in或者or后面的数据量越多，in的效率不会有太大的下降，但是or会随着记录越多的话性能下降非常厉害，从第三种测试情况中可以很明显地看出了，基本上是指数级增长。因此在给in和or的效率下定义的时候，应该再加上一个条件，就是所在的列是否有索引或者是否是主键。如果有索引或者主键性能没啥差别，如果没有索引，性能差别不是一点点！ 
### 4.2.12 exists、not exists

---

### 4.2.13 in和exists的区别

---

### 4.2.14 模糊查询like

---

模糊查询又被称为模糊匹配，在实际开发中使用较多，比如：查询公司中所有姓张的，查询岗位中带有经理两个字的职位等等，这些都需要使用模糊查询。
模糊查询的语法格式如下：
```sql
select .. from .. where 字段 like '通配符表达式';
```
在模糊查询中，通配符主要包括两个：一个是%，一个是下划线_。其中%代表任意多个字符。下划线_代表任意一个字符。
案例1：查询员工名字以'S'开始的员工姓名
```sql
select ename from emp where ename like 'S%';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1622000884924-f3303ff0-cb9a-4393-831c-01d3e705606d.png#averageHue=%230f0e0d&height=201&id=nTI0r&originHeight=201&originWidth=636&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11624&status=done&style=shadow&title=&width=636)
案例2：查询员工名字以'T'结尾的员工姓名
```sql
select ename from emp where ename like '%T';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1622000970235-0265da36-1e10-4da5-abb8-c651452fad21.png#averageHue=%230f0e0d&height=188&id=skACT&originHeight=188&originWidth=624&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10432&status=done&style=shadow&title=&width=624)
案例3：查询员工名字中含有'O'的员工姓名
```sql
select ename from emp where ename like '%O%';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1622001027995-71da44df-e3b1-4e56-a6e2-922a50ccc2b7.png#averageHue=%230f0e0e&height=231&id=Aa56U&originHeight=231&originWidth=632&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13088&status=done&style=shadow&title=&width=632)
案例4：查询员工名字中第二个字母是'A'的员工姓名
```sql
select ename from emp where ename like '_A%';
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1622001108864-1abbac56-669f-4c35-9b48-6d80452ad8ce.png#averageHue=%230f0e0d&height=226&id=ICQ6h&originHeight=226&originWidth=636&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13307&status=done&style=shadow&title=&width=636)
案例5：查询学员名字中含有下划线的。
执行以下SQL语句，先准备测试数据：
```sql
drop table if exists student;
create table student(
  id int,
  name varchar(255)
);
insert into student(id,name) values(1, 'susan');
insert into student(id,name) values(2, 'lucy');
insert into student(id,name) values(3, 'jack_son');
select * from student;
```
![image.png](https://cdn.nlark.com/yuque/0/2021/png/21376908/1622001536746-e0d05c73-f941-4f28-9190-bbfcf248c41b.png#averageHue=%2311100f&height=222&id=ttwgx&originHeight=222&originWidth=371&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10496&status=done&style=shadow&title=&width=371)
查询学员名字中含有下划线的，执行以下SQL试试：
```sql
select * from student where name like '%_%';
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667523151909-c112a3cb-9968-4b4a-8bee-5a75c4b6a9f2.png#averageHue=%230f0e0e&clientId=ud0c47669-2d83-4&from=paste&height=232&id=u08a9aa32&originHeight=232&originWidth=664&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12182&status=done&style=shadow&taskId=u2055ec95-4933-45ca-b17f-c384a54205d&title=&width=664)
显然这个查询结果不是我们想要的，以上SQL之所以将所有数据全部显示了，因为下划线代表任意单个字符，如果你想让这个下划线变成一个普通的下划线字符，就要使用转义字符了，在mysql当中转义字符是“\”，这个和java语言中的转义字符是一样的：
```sql
select * from student where name like '%\_%';
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667523291579-62dc328f-17ef-4e97-a22a-374ade19e797.png#averageHue=%23100f0e&clientId=ud0c47669-2d83-4&from=paste&height=139&id=u14f2fd6c&originHeight=139&originWidth=635&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7682&status=done&style=shadow&taskId=u5f6488c4-25a2-4517-8936-801669b340e&title=&width=635)
## 4.3 排序操作

---

排序操作很常用，比如查询学员成绩，按照成绩降序排列。排序的SQL语法：
```sql
select .. from .. order by 字段 asc/desc
```
### 4.3.1 单一字段升序
查询员工的编号、姓名、薪资，按照薪资升序排列。
```sql
select empno,ename,sal from emp order by sal asc;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524015631-e1f1b6c3-0a5b-4f04-91d1-7a11df8fc7ff.png#averageHue=%2312100f&clientId=ud0c47669-2d83-4&from=paste&height=490&id=u337ff7e2&originHeight=490&originWidth=697&originalType=binary&ratio=1&rotation=0&showTitle=false&size=40038&status=done&style=shadow&taskId=uc89e7030-c586-4582-bdaa-6b231e3ab16&title=&width=697)
### 4.3.2 单一字段降序
查询员工的编号、姓名、薪资，按照薪资降序排列。
```sql
select empno,ename,sal from emp order by sal desc;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524068322-84c1f716-5b7a-4b72-8a41-c0f8ec433d57.png#averageHue=%2311100f&clientId=ud0c47669-2d83-4&from=paste&height=490&id=ub06f2a23&originHeight=490&originWidth=737&originalType=binary&ratio=1&rotation=0&showTitle=false&size=40326&status=done&style=shadow&taskId=ube0d34dc-9629-4733-ac61-e9df253d566&title=&width=737)
### 4.3.3 默认采用升序
查询员工的编号、姓名、薪资，按照薪资升序排列。
```sql
select empno,ename,sal from emp order by sal;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524117390-bd4560ff-accf-45ee-97f1-d098f86fd31f.png#averageHue=%2312100f&clientId=ud0c47669-2d83-4&from=paste&height=486&id=u288be0fb&originHeight=486&originWidth=664&originalType=binary&ratio=1&rotation=0&showTitle=false&size=39701&status=done&style=shadow&taskId=ucd8a5bf0-4f87-444a-a13b-dcbb808b75f&title=&width=664)
查询员工的编号、姓名，按照姓名升序排列。
```sql
select empno,ename from emp order by ename;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524169552-6abc923e-3638-4a65-ab97-741c22f885fa.png#averageHue=%23110f0e&clientId=ud0c47669-2d83-4&from=paste&height=488&id=ubf5dc2c5&originHeight=488&originWidth=626&originalType=binary&ratio=1&rotation=0&showTitle=false&size=32304&status=done&style=shadow&taskId=uf1ac3bd4-f65a-4d1a-ac9e-a6d5d5b7e8e&title=&width=626)
### 4.3.4 多个字段排序
查询员工的编号、姓名、薪资，按照薪资升序排列，如果薪资相同的，再按照姓名升序排列。
```sql
select empno,ename,sal from emp order by sal asc, ename asc;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524337952-bbef44e7-488e-4c3e-9317-1fda80054c92.png#averageHue=%23110f0e&clientId=ud0c47669-2d83-4&from=paste&height=490&id=ud4173d66&originHeight=490&originWidth=813&originalType=binary&ratio=1&rotation=0&showTitle=false&size=40815&status=done&style=shadow&taskId=u231edd4c-d353-41e1-ba19-ebcc71d1d7b&title=&width=813)
### 4.3.5 where和order by的位置
找出岗位是MANAGER的员工姓名和薪资，按照薪资升序排列。
```sql
select ename,sal from emp where job = 'MANAGER' order by sal asc;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1667524386864-8d24513b-85f9-4f31-9462-4fe094cb0843.png#averageHue=%230f0e0e&clientId=ud0c47669-2d83-4&from=paste&height=233&id=ub579bda3&originHeight=233&originWidth=887&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16318&status=done&style=shadow&taskId=u0fd108a3-5c49-4ec2-843b-b8e4f5861c3&title=&width=887)
**通过这个例子主要是想告诉大家：where先执行，order by语句是最后执行的。**
## 4.4 distinct去重
查询工作岗位
```sql
select job from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570471000-b0d2c628-c149-4b13-b44c-ae6f5edefcf6.png#averageHue=%23110f0e&clientId=u005f32df-cdfa-4&from=paste&height=570&id=u3464010b&originHeight=570&originWidth=461&originalType=binary&ratio=1&rotation=0&showTitle=false&size=27010&status=done&style=shadow&taskId=ud01ef31e-b7e3-444e-a422-927baef293a&title=&width=461)
可以看到工作岗位中有重复的记录，如何在显示的时候去除重复记录呢？在字段前添加distinct关键字。
```sql
select distinct job from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570545279-ba8dcff3-533d-4ca8-9cc9-4b544ae47e8c.png#averageHue=%23100f0e&clientId=u005f32df-cdfa-4&from=paste&height=316&id=u847f8b1c&originHeight=316&originWidth=512&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15359&status=done&style=shadow&taskId=uad426308-7527-406f-ac5a-83b5f426f2c&title=&width=512)
注意：这个去重只是将显示的结果去重，原表数据不会被更改。
接下来测试一下，在distinct关键字前添加其它字段是否可以？
```sql
select ename, distinct job from emp;
```
分析一下：ename是14条记录，distinct job是5条记录，可以同时显示吗？
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570696423-05844698-00b1-4e9e-aa98-1a53f465cff4.png#averageHue=%23151311&clientId=u005f32df-cdfa-4&from=paste&height=104&id=uc30b7a53&originHeight=104&originWidth=945&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15129&status=done&style=shadow&taskId=u877fbe24-2e82-46b5-85a4-fabccbe2c07&title=&width=945)
报错了，通过测试得知，distinct只能出现在所有字段的最前面。
当distinct出现后，后面多个字段一定是联合去重的，我们来做两个练习就知道了：
练习1：找出公司中所有的工作岗位。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570864793-732f34aa-5b7d-4389-b4af-51cbd964215f.png#averageHue=%23100f0e&clientId=u005f32df-cdfa-4&from=paste&height=316&id=ub89f2b22&originHeight=316&originWidth=540&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15489&status=done&style=shadow&taskId=u5dab6bed-8c9b-4ae8-b617-37c86a9d8f2&title=&width=540)
练习2：找出公司中不同部门的不同工作岗位。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570891921-9c547b9b-d20e-4695-9704-051863b5e868.png#averageHue=%23110f0e&clientId=u005f32df-cdfa-4&from=paste&height=429&id=u755429fe&originHeight=429&originWidth=634&originalType=binary&ratio=1&rotation=0&showTitle=false&size=26800&status=done&style=shadow&taskId=ub3689df0-e1a9-40c1-a4e6-1f2f509c001&title=&width=634)
## 4.5 数据处理函数

---

关于select语句，我们之前都是这样写：select 字段名 from 表名; 其实，这里的字段名可以看做“变量”，select后面既然可以跟变量，那么可以跟常量吗，尝试一下：
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668568118423-c5b5d189-4d32-41ab-a189-3f155d0d0efa.png#averageHue=%230e0d0d&clientId=u005f32df-cdfa-4&from=paste&height=502&id=uf4590195&originHeight=502&originWidth=866&originalType=binary&ratio=1&rotation=0&showTitle=false&size=24621&status=done&style=shadow&taskId=u9bf03714-2a03-4e7b-98d7-9996316a176&title=&width=866)
通过以上sql的测试得知，select后面既可以跟变量，又可以跟常量。
以上三条SQL中前两条中100和'abc'都是常量，最后一条SQL的abc没有添加单引号，它会被当做某个表的字段名，因为没有这个字段所以报错。 
### 4.5.1 字符串相关
**转大写upper和ucase**
```sql
# 查询所有员工名字，以大写形式展现
select upper(ename) as ename from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668565912887-88d14d6c-707b-4e50-ac47-f8ad61b40d14.png#averageHue=%230e0e0d&clientId=u005f32df-cdfa-4&from=paste&height=531&id=ud706ac81&originHeight=531&originWidth=711&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22988&status=done&style=shadow&taskId=ua5341942-dd96-4402-8f3e-05136a93880&title=&width=711)
还有一个和upper函数功能相同的函数ucase，也可以转大写，了解一下即可：
```sql
# 查询所有员工姓名，以大写形式展现
select ucase(ename) as ename from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668566229563-55802f88-f6d6-436a-b478-18832d7a0342.png#averageHue=%230f0e0d&clientId=u005f32df-cdfa-4&from=paste&height=534&id=uff6a6590&originHeight=534&originWidth=674&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23082&status=done&style=shadow&taskId=uface697c-6972-498a-86af-50b161e48cd&title=&width=674)
```sql
# 查询员工smith的岗位、薪资（假如你不知道数据库表中的人名是大写、小写还是大小写混合）
select ename, job, sal from emp where upper(ename) = 'SMITH';
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668566360054-6e77882a-21fc-4b6e-9a04-3e0098606db8.png#averageHue=%23100f0e&clientId=u005f32df-cdfa-4&from=paste&height=178&id=uf8993c00&originHeight=178&originWidth=982&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11947&status=done&style=shadow&taskId=u72025ccb-5725-4313-bf7b-3edebed799a&title=&width=982)
**转小写lower和lcase，很简单，不再赘述，直接上代码：**
```sql
# 查询员工姓名，以小写形式展现
select lower(ename) as ename from emp;
select lcase(ename) as ename from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668566699289-0a479f71-ecf4-4a3f-ac4c-8516a4f0fee8.png#averageHue=%230f0e0d&clientId=u005f32df-cdfa-4&from=paste&height=216&id=u0f889bef&originHeight=216&originWidth=646&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9493&status=done&style=shadow&taskId=u5f16833e-e425-424b-a769-1761dd7023f&title=&width=646)
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668566716526-c8fac5f9-7079-4738-a3d1-2a5c3c5e1145.png#averageHue=%230f0e0d&clientId=u005f32df-cdfa-4&from=paste&height=189&id=ue19b9b87&originHeight=189&originWidth=643&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8007&status=done&style=shadow&taskId=u7fc1e3dd-17d7-4f33-b8ed-b88901fb087&title=&width=643)
**截取字符串substr**
语法：substr('被截取的字符串', 起始下标, 截取长度)
有两种写法：
第一种：substr('被截取的字符串', 起始下标, 截取长度)
第二种：substr('被截取的字符串', 起始下标)，当第三个参数“截取长度”缺失时，截取到字符串末尾
注意：起始下标从1开始，不是从0开始。（1表示从左侧开始的第一个位置，-1表示从右侧开始的第一个位置。）
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668567142258-6748508c-c3bb-440f-8ad7-c64df6c0028d.png#averageHue=%23100f0e&clientId=u005f32df-cdfa-4&from=paste&height=648&id=u521d5ef0&originHeight=648&originWidth=664&originalType=binary&ratio=1&rotation=0&showTitle=false&size=35242&status=done&style=shadow&taskId=u50bb124d-9e6b-4c8a-b48c-76594e0ec3c&title=&width=664)
练习：找出员工名字中第二个字母是A的
```sql
select ename from emp where substr(ename, 2, 1) = 'A';
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668567271612-710d3592-6111-4ab5-97c1-12f809ac7645.png#averageHue=%230f0e0d&clientId=u005f32df-cdfa-4&from=paste&height=254&id=u2313b4ee&originHeight=254&originWidth=854&originalType=binary&ratio=1&rotation=0&showTitle=false&size=14523&status=done&style=shadow&taskId=u8ae9b244-f6d3-441c-89d0-4466eaa73e4&title=&width=854)
**获取字符串长度length**
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672736218451-70fddda1-2541-4c91-9f39-3f968a6b6e12.png#averageHue=%23100f0f&clientId=uc0e8c595-6b95-4&from=paste&height=167&id=u69789788&originHeight=167&originWidth=525&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7442&status=done&style=shadow&taskId=u39c20cea-67f3-49eb-9d8e-8c548360b72&title=&width=525)
注意：一个汉字是2个长度。
**获取字符的个数char_length**
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672736125194-177317bd-f65c-4c05-bda7-f58961b78fd7.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=168&id=uKcvT&originHeight=168&originWidth=582&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8283&status=done&style=shadow&taskId=u2abebb18-4522-415a-bf80-859153252d1&title=&width=582)
**字符串拼接**
语法：concat('字符串1', '字符串2', '字符串3'....)
拼接的字符串数量没有限制。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668569810019-a8c939c4-518d-4ed9-961a-27d4440d13d0.png#averageHue=%2311100f&clientId=u005f32df-cdfa-4&from=paste&height=437&id=u00e5d696&originHeight=437&originWidth=860&originalType=binary&ratio=1&rotation=0&showTitle=false&size=29849&status=done&style=shadow&taskId=ufbffbf88-a2ed-4341-a706-959748e2260&title=&width=860)
注意：在mysql8之前，双竖线||也是可以完成字符串拼接的。但在mysql8之后，||只作为逻辑运算符，不能再进行字符串拼接了。
```sql
select 'abc' || 'def' || 'xyz';
```
mysql8之后，|| 只作为“或者”运算符，例如：找出工资高于3000或者低于900的员工姓名和薪资：
```sql
select ename, sal from emp where sal > 3000 || sal < 900;
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669780282134-d3a16d8a-e0fc-4744-beff-83b3579f6161.png#averageHue=%230f0f0e&clientId=u6210fc1e-5e54-4&from=paste&height=196&id=uc7e77230&originHeight=196&originWidth=950&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11249&status=done&style=shadow&taskId=u19693054-9222-4df2-899e-3ed69a01a71&title=&width=950)
mysql中可以使用+进行字符串的拼接吗？不可以，在mysql中+只作加法运算，在进行加法运算时，会将加号两边的数据尽最大的努力转换成数字再求和，如果无法转换成数字，最终运算结果通通是0
**去除字符串前后空白trim**
```sql
select concat(trim('    abc    '), 'def');
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570023583-bcf0b431-c34c-486b-9ee0-e571ff3c158d.png#averageHue=%2310100f&clientId=u005f32df-cdfa-4&from=paste&height=204&id=u800e8929&originHeight=204&originWidth=715&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12536&status=done&style=shadow&taskId=uc6e946c5-bd11-4f08-83a5-34b7d5e1a78&title=&width=715)
默认是去除前后空白，也可以去除指定的前缀后缀，例如：
去除前置0
```sql
select trim(leading '0' from '000111000');
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570194415-8f78ced1-8f36-42d3-a829-b81fc4132c85.png#averageHue=%23121110&clientId=u005f32df-cdfa-4&from=paste&height=214&id=u54da0ae5&originHeight=214&originWidth=706&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12307&status=done&style=shadow&taskId=u4bd5c984-5076-4b41-936e-2cb2934e2a0&title=&width=706)
去除后置0
```sql
select trim(trailing '0' from '000111000');
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570218215-c862c7d8-1ee3-4066-8e25-055767efee61.png#averageHue=%2312100f&clientId=u005f32df-cdfa-4&from=paste&height=207&id=ud1b70c2d&originHeight=207&originWidth=704&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11888&status=done&style=shadow&taskId=u3680db7d-b909-4cfe-8636-aef9213b9cb&title=&width=704)
前置0和后置0全部去除
```sql
select trim(both '0' from '000111000');
```
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1668570238062-dff388d3-3106-457d-a9ae-819f41821792.png#averageHue=%2311100f&clientId=u005f32df-cdfa-4&from=paste&height=203&id=uca889e8f&originHeight=203&originWidth=678&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10559&status=done&style=shadow&taskId=u39829e4b-560a-42a1-b27c-315e566e9ae&title=&width=678)
### 4.5.2 数字相关
**rand()和rand(x)**
rand()生成0到1的随机浮点数。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669797997130-63b2c8d0-6169-4ee8-9b6b-c3087e9d733b.png#averageHue=%2311100f&clientId=u57006619-2538-4&from=paste&height=432&id=uc1af8ae1&originHeight=432&originWidth=488&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21196&status=done&style=shadow&taskId=uf2b4c16d-fc16-42a5-91c6-c840e24096b&title=&width=488)
rand(x)生成0到1的随机浮点数，通过指定整数x来确定每次获取到相同的浮点值。
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798044104-7fc0b727-ff91-4d3e-be33-9954d556afe2.png#averageHue=%23121110&clientId=u57006619-2538-4&from=paste&height=431&id=uddf41de3&originHeight=431&originWidth=404&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23014&status=done&style=shadow&taskId=uc8b8c1f9-b44d-4886-8442-9c6d0e0beb7&title=&width=404)
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798069147-75492782-759d-46d9-84c5-a83b3a63594c.png#averageHue=%23121110&clientId=u57006619-2538-4&from=paste&height=431&id=ud22d346e&originHeight=431&originWidth=417&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21817&status=done&style=shadow&taskId=u01cf1b31-7d8b-4bc0-8eba-573138f7c49&title=&width=417)
**round(x)和round(x,y)四舍五入**
round(x) 四舍五入，保留整数位，舍去所有小数
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798450055-e26955bd-ea2d-445a-be98-721b54d3ca35.png#averageHue=%2311100f&clientId=u57006619-2538-4&from=paste&height=427&id=u633ac709&originHeight=427&originWidth=438&originalType=binary&ratio=1&rotation=0&showTitle=false&size=19800&status=done&style=shadow&taskId=u5ae99c90-04bd-47b9-9338-3be2146f355&title=&width=438)
round(x,y) 四舍五入，保留y位小数
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798534269-9c494800-7878-4ccf-bacc-a8c4cdafbbe6.png#averageHue=%23100f0e&clientId=u57006619-2538-4&from=paste&height=656&id=ub44adc1f&originHeight=656&originWidth=467&originalType=binary&ratio=1&rotation=0&showTitle=false&size=30665&status=done&style=shadow&taskId=u06d2a339-d070-4c04-9d62-a6ca361ad3c&title=&width=467)
**truncate(x, y)舍去**
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798594158-7e51e7a5-27af-4f7f-8021-a751f425a316.png#averageHue=%2311100f&clientId=u57006619-2538-4&from=paste&height=220&id=u7586a0cc&originHeight=220&originWidth=492&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10521&status=done&style=shadow&taskId=u4aea8b0c-2612-4b7c-af22-e5b68687b80&title=&width=492)
以上SQL表示保留两位小数，剩下的全部舍去。
数字处理函数除了以上的之外，还有ceil和floor函数：

- ceil函数：返回大于或等于数值x的最小整数
- floor函数：返回小于或等于数值x的最大整数

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672735932932-f0dfc7de-1f77-4eb0-b6e9-b6c6c2ce7ae3.png#averageHue=%23100f0e&clientId=uc0e8c595-6b95-4&from=paste&height=433&id=ua803b791&originHeight=433&originWidth=402&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13778&status=done&style=shadow&taskId=uf4127f6b-bfd8-454a-8aa8-2e1fec9edab&title=&width=402)
### 4.5.3 空处理
ifnull(x, y)，空处理函数，当x为NULL时，将x当做y处理。
ifnull(comm, 0)，表示如果员工的津贴是NULL时当做0处理。
在SQL语句中，凡是有NULL参与的数学运算，最终的计算结果都是NULL：
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798864111-5cffd59f-d15c-4f6c-a2d8-0b623ec1f16c.png#averageHue=%23100f0e&clientId=u57006619-2538-4&from=paste&height=658&id=ue1cf6783&originHeight=658&originWidth=408&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23225&status=done&style=shadow&taskId=ua42e9e3c-fa93-4f6c-979d-d5444c21108&title=&width=408)
看这样一个需求：查询每个员工的年薪。（年薪 = (月薪 + 津贴) * 12个月。注意：有的员工津贴comm是NULL。）
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669798945415-90bccaa6-1dda-4ebd-bc50-63ab5ba2b89a.png#averageHue=%23100f0e&clientId=u57006619-2538-4&from=paste&height=573&id=u514525d4&originHeight=573&originWidth=850&originalType=binary&ratio=1&rotation=0&showTitle=false&size=36066&status=done&style=shadow&taskId=ubb59ae71-c22d-456f-85bf-df0182998af&title=&width=850)
以上查询结果中显示SMITH等人的年薪是NULL，这是为什么，这是因为SMITH等人的津贴comm是NULL，有NULL参与的数学运算，最终结果都是NULL，显然这个需要空处理，此时就用到了ifnull函数：
![image.png](https://cdn.nlark.com/yuque/0/2022/png/21376908/1669799067232-4896fa47-5c64-409a-b970-dddc31e06050.png#averageHue=%23100f0e&clientId=u57006619-2538-4&from=paste&height=573&id=u59b02703&originHeight=573&originWidth=982&originalType=binary&ratio=1&rotation=0&showTitle=false&size=42887&status=done&style=shadow&taskId=u063b2776-3482-4b4f-888c-3623426b77b&title=&width=982)
### 4.5.4 日期和时间相关函数

1. **获取当前日期和时间**

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672707310711-3115e4af-385c-4565-89c7-25bad76e8a6a.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=162&id=uc379723b&originHeight=162&originWidth=404&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7211&status=done&style=shadow&taskId=uedf1c447-2a71-4f9a-9f96-98b9f249622&title=&width=404)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672707382021-d8d296b7-9d9a-4072-b714-c99da604ac12.png#averageHue=%23151312&clientId=uc0e8c595-6b95-4&from=paste&height=163&id=ua9b22a07&originHeight=163&originWidth=377&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8104&status=done&style=shadow&taskId=u0aa13932-ae31-46ba-94b7-f5cee861153&title=&width=377)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672707469394-4fe3f0fb-ca9e-4484-b939-db716f6ddd38.png#averageHue=%23131211&clientId=uc0e8c595-6b95-4&from=paste&height=168&id=ue97dcb2c&originHeight=168&originWidth=801&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12054&status=done&style=shadow&taskId=uf047d345-596d-4f3c-a996-3d1f6850219&title=&width=801)
now()和sysdate()的区别：

- now()：获取的是执行select语句的时刻。
- sysdate()：获取的是执行sysdate()函数的时刻。
2. **获取当前日期**

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672707770762-e9723219-562f-4a53-9d8a-9055ee80c25d.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=543&id=ufc58343c&originHeight=655&originWidth=440&originalType=binary&ratio=1&rotation=0&showTitle=false&size=29141&status=done&style=shadow&taskId=u707d5711-bda8-4f35-89c5-f39da3e879f&title=&width=365)
获取当前日期有三种写法，掌握任意一种即可：

- curdate()
- current_date()
- current_date
3. **获取当前时间**

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672707856778-8eec2322-c3c8-4ddc-94c4-3e08eea430a8.png#averageHue=%23121010&clientId=uc0e8c595-6b95-4&from=paste&height=653&id=u57a306e4&originHeight=653&originWidth=430&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28651&status=done&style=shadow&taskId=ua03065f0-48bc-43c2-ae47-b77fab8249f&title=&width=430)
获取档期时间有三种写法，掌握其中一种即可：

- curtime()
- current_time()
- current_time
4. **获取单独的年、月、日、时、分、秒**

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672708190559-a1d93032-699d-49dc-87cc-4ccb045bee28.png#averageHue=%23100f0e&clientId=uc0e8c595-6b95-4&from=paste&height=651&id=u5badb85c&originHeight=651&originWidth=456&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28555&status=done&style=shadow&taskId=u742f8377-b4d8-44e9-950d-da020890e07&title=&width=456)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672708242288-89a20209-4ca2-4d1c-a1b0-5ad5f1179841.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=653&id=u7cfcb11b&originHeight=653&originWidth=483&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28868&status=done&style=shadow&taskId=u43769b4b-00e8-4dfb-a085-19858d725f1&title=&width=483)
注意：这些函数在使用的时候，需要传递一个日期参数给它，它可以获取到你给定的这个日期相关的年、月、日、时、分、秒的信息。
一次性提取一个给定日期的“年月日”部分，可以使用date()函数，例如：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672713926559-d9c4257b-3536-4124-b4f4-3fd3626a293e.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=168&id=u161f961c&originHeight=168&originWidth=438&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7552&status=done&style=shadow&taskId=ub9643e54-a1b4-424f-a2d7-e15c7538b83&title=&width=438)
一次性提取一个给定日期的“时分秒”部分，可以使用time()函数，例如：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672721340191-9c568184-73b5-4c26-9035-95245016ba4f.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=161&id=u0bb5bc88&originHeight=161&originWidth=428&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7598&status=done&style=shadow&taskId=u09037fc7-e074-481b-bf6a-ccc8fc49cf6&title=&width=428)

5. **date_add函数**

date_add函数的作用：给指定的日期添加间隔的时间，从而得到一个新的日期。
date_add函数的语法格式：date_add(日期, interval expr 单位)，例如：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672709352877-e64de4c0-d776-4e30-908b-4a96c04bc186.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=174&id=ub79687f8&originHeight=174&originWidth=771&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11929&status=done&style=shadow&taskId=u79db77b4-bf0f-41ee-91ba-e6e48424d32&title=&width=771)
以'2023-01-03'为基准，间隔3天之后的日期：'2023-01-06'
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672709436259-c6d671c6-ccc8-4109-9612-1f178801ef64.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=171&id=ub0dc1d88&originHeight=171&originWidth=778&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11798&status=done&style=shadow&taskId=u06a7162d-aafa-4469-8f12-d3ea81c1f63&title=&width=778)
以'2023-01-03'为基准，间隔3个月之后的日期：'2023-04-03'
详细解释一下这个函数的相关参数：

- 日期：一个日期类型的数据
- interval：关键字，翻译为“间隔”，固定写法
- expr：指定具体的间隔量，一般是一个数字。**也可以为负数，如果为负数，效果和date_sub函数相同**。
- 单位：
   - year：年
   - month：月
   - day：日
   - hour：时
   - minute：分
   - second：秒
   - microsecond：微秒（1秒等于1000毫秒，1毫秒等于1000微秒）
   - week：周
   - quarter：季度

请分析下面这条SQL语句所表达的含义：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672710673500-8afb96ad-3aa5-4adb-9160-9aaac4b4ff83.png#averageHue=%23131211&clientId=uc0e8c595-6b95-4&from=paste&height=162&id=u455ecd04&originHeight=162&originWidth=1036&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12957&status=done&style=shadow&taskId=u3148a05b-3fbe-432e-8492-373fde1d2db&title=&width=1036)
以上SQL表示：以2022-10-01 10:10:10为基准，在这个时间基础上添加-1微秒，也就是减去1微秒。
以上SQL也可以采用date_sub函数完成，例如：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672710799157-9775a5b0-143f-493b-a6f0-cd8db5c6ca31.png#averageHue=%23131211&clientId=uc0e8c595-6b95-4&from=paste&height=159&id=u70af0451&originHeight=159&originWidth=990&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13185&status=done&style=shadow&taskId=u7bf2be69-c836-4951-bd99-69c09f553ec&title=&width=990)
另外，单位也可以采用复合型单位，例如：

- SECOND_MICROSECOND
- MINUTE_MICROSECOND
- MINUTE_SECOND：几分几秒之后
- HOUR_MICROSECOND
- HOUR_SECOND
- HOUR_MINUTE：几小时几分之后
- DAY_MICROSECOND
- DAY_SECOND
- DAY_MINUTE
- DAY_HOUR：几天几小时之后
- YEAR_MONTH：几年几个月之后

如果单位采用复合型的话，expr该怎么写呢？例如单位采用：day_hour，假设我要表示3天2小时之后，怎么写？
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672711325140-0a281589-4bc2-4fc8-bd7f-9a5ff180ba71.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=171&id=u186c11d0&originHeight=171&originWidth=1009&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13317&status=done&style=shadow&taskId=u2827b5bf-37d2-486f-9db8-fa8b15ce510&title=&width=1009)
'3,2'这个应该很好理解，表示3天2个小时之后。'3,2'和day_hour是对应的。

6. **date_format日期格式化函数**

将日期转换成具有某种格式的日期字符串，通常用在查询操作当中。（date类型转换成char类型）
语法格式：date_format(日期, '日期格式')
该函数有两个参数：

- 第一个参数：日期。这个参数就是即将要被格式化的日期。类型是date类型。
- 第二个参数：指定要格式化的格式字符串。
   - %Y：四位年份
   - %y：两位年份
   - %m：月份（1..12）
   - %d：日（1..30）
   - %H：小时（0..23）
   - %i：分（0..59）
   - %s：秒（0..59）

例如：获取当前系统时间，让其以这个格式展示：2000-10-11 20:15:30
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672716928881-badddb77-c670-43f3-8b25-8e2eb4952a04.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=168&id=uf1769116&originHeight=168&originWidth=790&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12687&status=done&style=shadow&taskId=u0936983e-6c2d-4e0f-96a9-905426534b9&title=&width=790)
注意：在mysql当中，默认的日期格式就是：%Y-%m-%d %H:%i:%s，所以当你直接输出日期数据的时候，会自动转换成该格式的字符串：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672717081322-e99bdff0-76df-4fcc-958a-463bf9e65d9d.png#averageHue=%23131110&clientId=uc0e8c595-6b95-4&from=paste&height=164&id=udf0a9e15&originHeight=164&originWidth=369&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7005&status=done&style=shadow&taskId=ua8a7ba31-3b81-427d-8a55-a8a84114389&title=&width=369)

7. **str_to_date函数**

该函数的作用是将char类型的日期字符串转换成日期类型date，通常使用在插入和修改操作当中。（char类型转换成date类型）
假设有一个学生表t_student，学生有一个生日的字段，类型是date类型：
```sql
drop table if exists t_student;
create table t_student(
  name varchar(255),
  birth date
);
desc t_student;
```
我们要给这个表插入一条数据：姓名zhangsan，生日85年10月1日，执行以下insert语句：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672718111465-698c085a-b3f1-4523-9f3f-d27ceb4410d5.png#averageHue=%231b1815&clientId=uc0e8c595-6b95-4&from=paste&height=59&id=u816b6342&originHeight=59&originWidth=1163&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13327&status=done&style=shadow&taskId=u25e9289a-7274-49fc-9db5-e54cc764c7d&title=&width=1163)
错误原因：日期值不正确。意思是：birth字段需要一个日期，你给的这个字符串'10/01/1985'我识别不了。这种情况下，我们就可以使用str_to_date函数进行类型转换：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672718492868-58ab55ff-a4e7-481f-9c58-9c81014d1762.png#averageHue=%2315100f&clientId=uc0e8c595-6b95-4&from=paste&height=83&id=u3cdb0924&originHeight=83&originWidth=1379&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12797&status=done&style=shadow&taskId=u619f99b1-3107-44e6-8738-542c8b9aaf8&title=&width=1379)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672718610506-ec24a44e-7854-4037-8567-b42dfb9228c0.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=159&id=uf93570e5&originHeight=159&originWidth=533&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8550&status=done&style=shadow&taskId=ua5be6705-7bc3-46b4-9922-15d9020df6e&title=&width=533)
当然，如果你提供的日期字符串格式能够被mysql解析，str_to_date函数是可以省略的，底层会自动调用该函数进行类型转换：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672718807175-8b62c13a-e771-482d-a999-7548501da25e.png#averageHue=%23110f0e&clientId=uc0e8c595-6b95-4&from=paste&height=625&id=u14b85262&originHeight=625&originWidth=1088&originalType=binary&ratio=1&rotation=0&showTitle=false&size=66015&status=done&style=shadow&taskId=uae019b86-851f-4348-962a-a15199adc0f&title=&width=1088)
如果日期格式符合以上的几种格式，mysql都会自动进行类型转换的。

8. **dayofweek、dayofmonth、dayofyear函数**

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672719401783-7ea51704-954a-4f96-aa81-3a8da4b34582.png#averageHue=%23110f0e&clientId=uc0e8c595-6b95-4&from=paste&height=665&id=u1a4c7890&originHeight=665&originWidth=685&originalType=binary&ratio=1&rotation=0&showTitle=false&size=39505&status=done&style=shadow&taskId=u36f1ca0f-c525-47e4-8ccf-df5d8210281&title=&width=685)
dayofweek：一周中的第几天（1~7），周日是1，周六是7。
dayofmonth：一个月中的第几天（1~31）
dayofyear：一年中的第几天（1~366）

9. **last_day函数**

获取给定日期所在月的最后一天的日期：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672719572099-bba462b8-da22-42b7-9a40-9c2c545596ef.png#averageHue=%23121010&clientId=uc0e8c595-6b95-4&from=paste&height=163&id=u8cab6ec4&originHeight=163&originWidth=498&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8323&status=done&style=shadow&taskId=ucef40e03-23be-4936-a671-ac674c20438&title=&width=498)

10. **datediff函数**

计算两个日期之间所差天数：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672720897012-c5e7e6dd-29de-46b0-b2c1-e1de3e8d6e54.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=169&id=u9b900968&originHeight=169&originWidth=865&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10814&status=done&style=shadow&taskId=ufb6d4060-84b9-44b3-8694-a9cf990bc54&title=&width=865)
时分秒不算，只计算日期部分相差的天数。

11. **timediff函数**

计算两个日期所差时间，例如日期1和日期2所差10:20:30，表示差10小时20分钟30秒。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672721193551-f65b470a-9060-4010-b172-b34eb1787e55.png#averageHue=%23121110&clientId=uc0e8c595-6b95-4&from=paste&height=168&id=u56a06c8e&originHeight=168&originWidth=987&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11553&status=done&style=shadow&taskId=ua81b206f-eb6b-47b3-ad2a-e4b048fdd31&title=&width=987)
### 4.5.5 if函数
如果条件为TRUE则返回“YES”，如果条件为FALSE则返回“NO”：
```sql
SELECT IF(500<1000, "YES", "NO");
```
例如：如果工资高于3000，则输出1，反之则输出0
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672725980625-f929cbdc-41ec-49d4-a5de-bc753dfbe67e.png#averageHue=%230f0e0e&clientId=uc0e8c595-6b95-4&from=paste&height=536&id=ued7bfdee&originHeight=536&originWidth=747&originalType=binary&ratio=1&rotation=0&showTitle=false&size=29371&status=done&style=shadow&taskId=uec5813f3-7f94-4ae2-9644-78e1fd281f6&title=&width=747)
再例如：如果名字是SMITH的，工资上调10%，其他员工工资正常显示。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672726073468-51733168-6ebe-477d-9aba-267adcefd10a.png#averageHue=%23100f0e&clientId=uc0e8c595-6b95-4&from=paste&height=534&id=uf2148f3a&originHeight=534&originWidth=992&originalType=binary&ratio=1&rotation=0&showTitle=false&size=38069&status=done&style=shadow&taskId=u7679358d-9412-4000-b8cd-872e9980209&title=&width=992)
再例如：工作岗位是MANAGER的工资上调10%，是SALESMAN的工资上调20%，其他岗位工资正常。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672726371265-19128e1a-47cf-46b0-9b80-310d37010535.png#averageHue=%23100f0e&clientId=uc0e8c595-6b95-4&from=paste&height=532&id=u575eb753&originHeight=532&originWidth=1441&originalType=binary&ratio=1&rotation=0&showTitle=false&size=55630&status=done&style=shadow&taskId=uf0e71940-399c-4edf-bd67-14f893e719e&title=&width=1441)
上面这个需求也可以使用：case.. when.. then.. when.. then.. else.. end来完成：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672726864928-8206091b-3bd3-4f12-b784-173aff775d6f.png#averageHue=%23141210&clientId=uc0e8c595-6b95-4&from=paste&height=724&id=u37fc5544&originHeight=724&originWidth=561&originalType=binary&ratio=1&rotation=0&showTitle=false&size=57934&status=done&style=shadow&taskId=u812c7487-a5f1-4d90-a5bd-891e360d45b&title=&width=561)
### 4.5.6 cast函数
cast函数用于将值从一种数据类型转换为表达式中指定的另一种数据类型
语法：cast(值 as 数据类型)
例如：cast('2020-10-11' as date)，表示将字符串'2020-10-11'转换成日期date类型。
在使用cast函数时，可用的数据类型包括：

- date：日期类型
- time：时间类型
- datetime：日期时间类型
- signed：有符号的int类型（有符号指的是正数负数）
- char：定长字符串类型
- decimal：浮点型

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672737293605-d7e38772-e9c3-40ab-a7ea-3311aa14a1a9.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=662&id=u174ddf1e&originHeight=662&originWidth=778&originalType=binary&ratio=1&rotation=0&showTitle=false&size=34283&status=done&style=shadow&taskId=u2531ed29-bfef-4efc-a5b0-6ff107330b6&title=&width=778)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672737634602-96cdd564-1220-445e-9b18-b3f0a2a55379.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=435&id=ued100771&originHeight=435&originWidth=545&originalType=binary&ratio=1&rotation=0&showTitle=false&size=18617&status=done&style=shadow&taskId=u559bfe74-f2ec-4e05-a37f-2cd08b29cde&title=&width=545)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672737720321-3812fd42-d3a4-4985-96d2-629947d9ce48.png#averageHue=%23111010&clientId=uc0e8c595-6b95-4&from=paste&height=213&id=ua7df14ff&originHeight=213&originWidth=604&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10420&status=done&style=shadow&taskId=u66dc0647-a030-400f-8ec0-b3c2b22a844&title=&width=604)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672737802812-d04d581c-138c-4e4e-97d4-c979558e9b2e.png#averageHue=%2311100f&clientId=uc0e8c595-6b95-4&from=paste&height=170&id=u214f15ff&originHeight=170&originWidth=714&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8572&status=done&style=shadow&taskId=ud2929b4c-8582-4dc3-a2ba-8de75b96e58&title=&width=714)
### 4.5.7 加密函数
md5函数，可以将给定的字符串经过md5算法进行加密处理，字符串经过加密之后会生成一个固定长度32位的字符串，md5加密之后的密文通常是不能解密的：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1672737046172-5ee0458a-60c6-4bae-b075-94b7dee440ab.png#averageHue=%23131110&clientId=uc0e8c595-6b95-4&from=paste&height=220&id=u6e900f32&originHeight=220&originWidth=568&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10865&status=done&style=shadow&taskId=uabd2a6f3-e59b-4dac-ba4c-bcc743fafad&title=&width=568)
## 4.6 分组函数
分组函数的执行原则：先分组，然后对每一组数据执行分组函数。如果没有分组语句group by的话，整张表的数据自成一组。
分组函数包括五个：

- max：最大值
- min：最小值
- avg：平均值
- sum：求和
- count：计数

**找出员工的最高薪资**
select max(sal) from emp;
**找出员工的最低工资**
select min(sal) from emp;
**计算员工的平均薪资**
select avg(sal) from emp;
**计算员工的工资和**
select sum(sal) from emp;
**计算员工的津贴之和**
select sum(comm) from emp;
重点：所有的分组函数都是自动忽略NULL的。
**统计员工人数**
select count(ename) from emp;
select count(*) from emp;
select count(1) from emp;
count(*)和count(1)的效果一样，统计该组中总记录行数。
count(ename)统计的是这个ename字段中不为NULL个数总和。
例如：count(comm) 结果是 4，而不是14
**统计岗位数量**
select count(distinct job) from emp;
**分组函数组合使用**
select count(*),max(sal),min(sal),avg(sal),sum(sal) from emp;
**分组函数不能直接使用在where子句当中**
select ename,job from emp where sal > avg(sal); 这个会报错的
原因：分组的行为是在where执行之后才开始的。
## 4.7 分组查询

1. **group by**

按照某个字段分组，或者按照某些字段联合分组。注意：group by的执行是在where之后执行。
语法：
group by 字段
group by 字段1,字段2,字段3....
**找出每个岗位的平均薪资**
select job, avg(sal) from emp group by job;
**找出每个部门最高工资**
select deptno,max(sal) from emp group by deptno;
**找出每个部门不同岗位的平均薪资**
select deptno,job,avg(sal) from emp group by deptno,job;
**当select语句中有group by的话，select后面只能跟分组函数或参加分组的字段**
select ename,deptno,avg(sal) from emp group by deptno; // 这个SQL执行后会报错。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1676866192155-44d23157-87d0-4a58-a9d5-2641619d74fe.png#averageHue=%23171412&clientId=u417b9e29-4007-4&from=paste&height=140&id=uae74e6b8&originHeight=140&originWidth=1141&originalType=binary&ratio=1&rotation=0&showTitle=false&size=25591&status=done&style=shadow&taskId=u4097c74b-3d21-485a-a74f-1390352d2e3&title=&width=1141)

2. **having**

having写在group by的后面，当你对分组之后的数据不满意，可以继续通过having对分组之后的数据进行过滤。
where的过滤是在分组前进行过滤。
使用原则：尽量在where中过滤，实在不行，再使用having。越早过滤效率越高。
**找出除20部分之外，其它部门的平均薪资。**
select deptno,avg(sal) from emp where deptno<>20 group by deptno; // 建议
select deptno,avg(sal) from emp group by deptno having deptno <> 20; // 不建议
**查询每个部门平均薪资，找出平均薪资高于2000的。**
select deptno,avg(sal) from emp group by deptno having avg(sal) > 2000;

3. **总结单表的DQL语句**

select ...5
from ...1
where ...2
group by ...3
having ...4
order by ...6
重点掌握一个完整的DQL语句执行顺序。

4. **行转列，列转行**
5. **组内排序**

案例：找出每个工作岗位的工资排名在前两名的。
substring_index函数的使用：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678080182698-009c47d2-eb75-4f67-afaa-874c7904ed45.png#averageHue=%2312100f&clientId=ue32f086e-fc2b-4&from=paste&height=379&id=rhnfq&originHeight=379&originWidth=755&originalType=binary&ratio=1&rotation=0&showTitle=false&size=27939&status=done&style=shadow&taskId=u49228cac-a6a0-4d31-8dbc-abc432cd804&title=&width=755)
group_concat函数的使用：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678082111760-02413f4e-a8b0-4837-8cb0-3b201151293f.png#averageHue=%23100f0e&clientId=ue32f086e-fc2b-4&from=paste&height=272&id=bhhYI&originHeight=272&originWidth=904&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20533&status=done&style=shadow&taskId=uac8b6d07-c85c-47d4-9724-b29c1e8f927&title=&width=904)
## 4.9 连接查询

1. **什么是连接查询？**
   1. 从一张表中查询数据称为单表查询。
   2. 从两张或更多张表中联合查询数据称为多表查询，又叫做连接查询。
   3. 什么时候需要使用连接查询？
      1. 比如这样的需求：员工表中有员工姓名，部门表中有部门名字，要求查询每个员工所在的部门名字，这个时候就需要连接查询。
2. **连接查询的分类？**
   1. 根据语法出现的年代进行分类：
      1. SQL92（这种语法很少用，可以不用学。）
      2. SQL99（我们主要学习这种语法。）
   2. 根据连接方式的不同进行分类：
      1. 内连接
         1. 等值连接
         2. 非等值连接
         3. 自连接
      2. 外连接
         1. 左外连接（左连接）
         2. 右外连接（右连接）
      3. 全连接
3. **笛卡尔积现象？**
   1. 当两张表进行连接查询时，如果没有任何条件进行过滤，最终的查询结果条数是两张表条数的乘积。为了避免笛卡尔积现象的发生，需要添加条件进行筛选过滤。
   2. 需要注意：添加条件之后，虽然避免了笛卡尔积现象，但是匹配的次数没有减少。
   3. 为了SQL语句的可读性，为了执行效率，建议给表起别名。
4. **什么叫内连接？**

![内连接.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677398804476-afbffad7-7d5a-4318-9e86-a3f8092dfcc8.png#averageHue=%23f7f5f5&clientId=u1be67ea7-0240-4&from=paste&height=233&id=u4f6abf7d&originHeight=233&originWidth=300&originalType=binary&ratio=1&rotation=0&showTitle=false&size=29826&status=done&style=shadow&taskId=u51112874-93e5-4ef2-8366-f78cc265d04&title=&width=300)
满足条件的记录才会出现在结果集中。

5. **内连接之等值连接**

连接时，条件为等量关系。
案例：查询每个员工所在的部门名称，要求显示员工名、部门名。
```sql
select
	e.ename,d.dname
from
	emp e
inner join
	dept d
on
	e.deptno = d.deptno;
```
注意：inner可以省略。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677401675659-04e46e96-9f00-4210-8beb-e8148807ae10.png#averageHue=%231a1613&clientId=u1be67ea7-0240-4&from=paste&height=380&id=u91e060d7&originHeight=380&originWidth=258&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15942&status=done&style=shadow&taskId=u2319a8db-57a3-4bcb-a42b-b58c46e0381&title=&width=258)

6. **内连接之非等值连接**

连接时，条件是非等量关系。
案例：查询每个员工的工资等级，要求显示员工名、工资、工资等级。
```sql
select
	e.ename,e.sal,s.grade
from
	emp e
join
	salgrade s
on
	e.sal between s.losal and s.hisal;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677401628377-11f115a0-b961-4e10-b411-97ea04a89035.png#averageHue=%23191613&clientId=u1be67ea7-0240-4&from=paste&height=380&id=u9ef14890&originHeight=380&originWidth=279&originalType=binary&ratio=1&rotation=0&showTitle=false&size=17957&status=done&style=shadow&taskId=u97872f0c-74c1-40ef-b3bb-607697cbe62&title=&width=279)

7. **内连接之自连接**

连接时，一张表看做两张表，自己和自己进行连接。
案例：找出每个员工的直属领导，要求显示员工名、领导名。
```sql
select
	e.ename 员工名, l.ename 领导名
from
	emp e
join
	emp l
on
	e.mgr = l.empno;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677402107820-a3fc38cc-4e13-4a39-8bb4-f1d9de713cd9.png#averageHue=%23161311&clientId=u1be67ea7-0240-4&from=paste&height=363&id=ub784a9c1&originHeight=363&originWidth=256&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15854&status=done&style=shadow&taskId=u67543946-a969-42f9-a55b-91571731d16&title=&width=256)
思路：
将emp表当做员工表 e
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677401951879-b0967e07-82f4-41e3-861e-d61e7d679e71.png#averageHue=%23141210&clientId=u1be67ea7-0240-4&from=paste&height=409&id=u4a5d8630&originHeight=409&originWidth=409&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28580&status=done&style=shadow&taskId=ua9050736-6b86-415c-9f4d-e4e8d72c0b5&title=&width=409)
将emp表当做领导表 l
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677401973338-4bc03ba9-815d-4fca-90fb-de34e5848da3.png#averageHue=%2312100f&clientId=u1be67ea7-0240-4&from=paste&height=409&id=uffcf8f58&originHeight=409&originWidth=374&originalType=binary&ratio=1&rotation=0&showTitle=false&size=19851&status=done&style=shadow&taskId=uad8210e5-8156-449c-bc2f-25f2614109b&title=&width=374)
可以发现连接条件是：e.mgr = l.empno（员工的领导编号=领导的员工编号）
注意：KING这个员工没有查询出来。如果想将KING也查询出来，需要使用外连接。

8. **什么叫外连接？**

内连接是满足条件的记录查询出来。也就是两张表的交集。
外连接是除了满足条件的记录查询出来，再将其中一张表的记录全部查询出来，另一张表如果没有与之匹配的记录，自动模拟出NULL与其匹配。
左外连接：
![左连接.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677398828684-41b0bde2-1689-47a4-ae7b-3c5c4fb82ce6.png#averageHue=%23f5e6e4&clientId=u1be67ea7-0240-4&from=paste&height=233&id=ue0f4c04f&originHeight=233&originWidth=300&originalType=binary&ratio=1&rotation=0&showTitle=false&size=42064&status=done&style=shadow&taskId=u3697d149-d9f5-4090-8773-ffb0962ff90&title=&width=300)
右外连接：
![右连接.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677398837026-688ff40f-d74b-4da6-a2e4-9573f5ba1580.png#averageHue=%23f4e6e3&clientId=u1be67ea7-0240-4&from=paste&height=233&id=ua18b1d44&originHeight=233&originWidth=300&originalType=binary&ratio=1&rotation=0&showTitle=false&size=43272&status=done&style=shadow&taskId=u4bb1c6ab-4c51-4fe0-938b-a7950969180&title=&width=300)

9. **外连接之左外连接（左连接）**

案例：查询所有部门信息，并且找出每个部门下的员工。
```sql
select
  d.*,e.ename
from
  dept d
left outer join
  emp e
on
  d.deptno = e.deptno;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677402955987-bdcd956a-8dd4-481b-97de-c785b200e902.png#averageHue=%23171411&clientId=u1be67ea7-0240-4&from=paste&height=408&id=ud8f95a62&originHeight=408&originWidth=470&originalType=binary&ratio=1&rotation=0&showTitle=false&size=36154&status=done&style=shadow&taskId=u3263d663-860e-41a9-b973-50a3be9baa0&title=&width=470)
注意：outer可以省略。
任何一个左连接都可以写作右连接。

10. **外连接之右外连接（右连接）**

还是上面的案例，可以写作右连接。
```sql
select
  d.*,e.ename
from
  emp e
right outer join
  dept d
on
  d.deptno = e.deptno;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677403445932-325502d5-b568-46a5-8f7a-d91030f3cac3.png#averageHue=%23191411&clientId=u1be67ea7-0240-4&from=paste&height=412&id=ue32d3266&originHeight=412&originWidth=454&originalType=binary&ratio=1&rotation=0&showTitle=false&size=36142&status=done&style=shadow&taskId=u28ef1b62-f835-472a-b916-1ee2eb5299b&title=&width=454)
案例：找出所有员工的上级领导，要求显示员工名和领导名。
```sql
select 
  e.ename 员工名,l.ename 领导名 
from 
  emp e 
left join 
  emp l 
on
  e.mgr = l.empno;
```
```sql
select 
  e.ename 员工名,l.ename 领导名 
from 
  emp l 
right join 
  emp e 
on
  e.mgr = l.empno;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677403569294-c9688076-61e2-4e33-bb40-06d4307c6b43.png#averageHue=%23171210&clientId=u1be67ea7-0240-4&from=paste&height=386&id=ud80e0755&originHeight=386&originWidth=273&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16908&status=done&style=shadow&taskId=uded0f105-8d51-486b-97fb-acb24822774&title=&width=273)

11. **什么是全连接？**

MySQL不支持full join。oracle数据库支持。
![全连接.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677398846702-4a3f3e0f-16bb-4e00-8015-490dc44d114b.png#averageHue=%23f2d7d2&clientId=u1be67ea7-0240-4&from=paste&height=233&id=u050103a2&originHeight=233&originWidth=300&originalType=binary&ratio=1&rotation=0&showTitle=false&size=51399&status=done&style=shadow&taskId=ued746d97-47c2-46a3-83cd-097182ea146&title=&width=300)
两张表数据全部查询出来，没有匹配的记录，各自为对方模拟出NULL进行匹配。
客户表：t_customer
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677405118434-d9979d32-5647-4b0a-8d65-1ff6b61c6d44.png#averageHue=%23131210&clientId=u1be67ea7-0240-4&from=paste&height=137&id=u66bb1e76&originHeight=137&originWidth=235&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4218&status=done&style=shadow&taskId=u7d338668-6c7a-488f-851d-635afa97d29&title=&width=235)
订单表：t_order
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677405287024-4df811ac-9216-47c3-98b2-20f5d7ce2886.png#averageHue=%23151311&clientId=u1be67ea7-0240-4&from=paste&height=136&id=u8ef1b39a&originHeight=136&originWidth=261&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4032&status=done&style=shadow&taskId=u69ae2de5-204a-4a0b-8d2f-67ccbc73ad2&title=&width=261)
案例：查询所有的客户和订单。
```sql
select 
 c.*,o.* 
from 
 t_customer c 
full join 
 t_order o 
on 
 c.cid = o.cid;
```

12. **三张表甚至更多张表如何进行表连接**

案例：找出每个员工的部门，并且要求显示每个员工的薪资等级。
```sql
select 
 e.ename,d.dname,s.grade 
from 
 emp e 
join 
 dept d 
on 
 e.deptno = d.deptno 
join 
 salgrade s 
on 
 e.sal between s.losal and s.hisal;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677404511432-b8fe8eb2-c828-4913-8d7c-a7b47a0ee270.png#averageHue=%23171411&clientId=u1be67ea7-0240-4&from=paste&height=381&id=u6047af30&originHeight=381&originWidth=324&originalType=binary&ratio=1&rotation=0&showTitle=false&size=18547&status=done&style=shadow&taskId=uc90c12f6-bdbb-4221-abe5-dcc4e221c96&title=&width=324)
## 4.10 子查询

1. **什么是子查询？**
   1. select语句中嵌套select语句就叫做子查询。
   2. select语句可以嵌套在哪里？
      1. where后面、from后面、select后面都是可以的。
2. **where后面使用子查询**

案例：找出高于平均薪资的员工姓名和薪资。
错误的示范：
```sql
select ename,sal from emp where sal > avg(sal);
```
错误原因：where后面不能直接使用分组函数。
可以使用子查询：
```sql
select ename,sal from emp where sal > (select avg(sal) from emp);
```

3. **from后面使用子查询**

小窍门：from后面的子查询可以看做一张临时表。
案例：找出每个部门的平均工资的等级。
第一步：先找出每个部门平均工资。
```sql
select deptno, avg(sal) avgsal from emp group by deptno;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677477788393-e2525a0a-2092-4a5e-80e7-7f8df04f6a6c.png#averageHue=%23151311&clientId=ud7d035d7-9c64-4&from=paste&height=163&id=u397cf064&originHeight=163&originWidth=303&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5620&status=done&style=shadow&taskId=uc8a5cf34-abe3-446f-9948-e3cedf385f9&title=&width=303)
第二步：将以上查询结果当做临时表t，t表和salgrade表进行连接查询。条件：t.avgsal between s.losal and s.hisal
```sql
select t.*,s.grade from (select deptno, avg(sal) avgsal from emp group by deptno) t join salgrade s on t.avgsal between s.losal and s.hisal;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1677477892811-ef9b366b-82be-4407-86f1-8dfa81492d8c.png#averageHue=%23151311&clientId=ud7d035d7-9c64-4&from=paste&height=162&id=u5d9f4ab4&originHeight=162&originWidth=397&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7422&status=done&style=shadow&taskId=uc90565b7-edc2-43bf-ba54-1e7db925c63&title=&width=397)

4. **select后面使用子查询**
```sql
select e.ename,(select d.dname from dept d where e.deptno = d.deptno) as dname from emp e;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678063689524-a204a93a-6454-4ff7-a1c6-ac5229edae91.png#averageHue=%231a1714&clientId=ud9fded62-54bb-4&from=paste&height=428&id=u2b69cf05&originHeight=428&originWidth=276&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16342&status=done&style=shadow&taskId=ua4f4e977-d3e6-4e90-8781-42050638d4a&title=&width=276)

5. **any子查询**

和or、in类似，只不过any需要搭配比较符一起用。
in可以完成的，例如：找出工资是3000和5000的：
```sql
select ename,sal from emp where sal in(3000,5000);
```
or也可以完成：
```sql
select ename,sal from emp where sal = 3000 or sal = 5000;
```
or可以完成的，例如：找出工资大于3000或大于5000的：
```sql
select ename,sal from emp where sal > 3000 or sal > 5000;
```
以上如果采用in就完成不了，但可以采用any来完成：
```sql
select ename,sal from emp where sal > any(3000, 5000);
```
但这里要注意，以上sql是无法执行的，因为any后面只能跟子查询。
案例：找出工资高于岗位是ANALYST或PRESIDENT的员工姓名和工资。
```sql
select ename,sal from emp where sal > any(select sal from emp where job in('ANALYST', 'PRESIDENT'));
```

6. **some子查询**

some和any的效果相同。

7. **all子查询**

类似于and，例如：找出工资大于等于岗位是ANALYST并且PRESIDENT的员工姓名和工资。如果使用and实现：
```sql
select ename,sal from emp where sal >= (select distinct sal from emp where job='ANALYST') and sal >= (select distinct sal from emp where job='PRESIDENT');
```
使用all进行实现：
```sql
select ename,sal from emp where sal >= all(select sal from emp where job='ANALYST' or job='PRESIDENT');
```
## 4.11 union&union all
不管是union还是union all都可以将两个查询结果集进行合并。
union会对合并之后的查询结果集进行去重操作。
union all是直接将查询结果集合并，不进行去重操作。（union all和union都可以完成的话，优先选择union all，union all因为不需要去重，所以效率高一些。）
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678078225300-461e069f-0c80-4745-88a7-2969acccd076.png#averageHue=%23141210&clientId=ue32f086e-fc2b-4&from=paste&height=488&id=u46d82364&originHeight=488&originWidth=404&originalType=binary&ratio=1&rotation=0&showTitle=false&size=31584&status=done&style=shadow&taskId=u459bc800-2e1c-4247-866e-b06b0313a0c&title=&width=404)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678078278429-e97f96a1-7429-4b68-8df9-3bda3a890797.png#averageHue=%23151210&clientId=ue32f086e-fc2b-4&from=paste&height=884&id=u2ef6109a&originHeight=884&originWidth=408&originalType=binary&ratio=1&rotation=0&showTitle=false&size=60134&status=done&style=shadow&taskId=u8c39e0b0-c274-46f0-8866-347160e1418&title=&width=408)
案例：查询工作岗位是MANAGER和SALESMAN的员工。
```sql
select ename,sal from emp where job='MANAGER'
union all
select ename,sal from emp where job='SALESMAN';
```
以上案例采用or也可以完成，那or和union all有什么区别？考虑走索引优化之类的选择union all，其它选择or。
两个结果集合并时，列数量要相同：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678078078467-89b7ba88-52ae-4e70-b5cc-b4fe4a3daf76.png#averageHue=%2312110f&clientId=ue32f086e-fc2b-4&from=paste&height=101&id=u85e05b84&originHeight=101&originWidth=999&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11813&status=done&style=shadow&taskId=u29bd097d-8994-4842-be9e-3bcb8865687&title=&width=999)
## 4.12 limit

1. limit作用：查询第几条到第几条的记录。通常是因为表中数据量太大，需要分页显示。
2. limit语法格式：
   1. limit 开始下标, 长度
3. 案例：查询员工表前5条记录
```sql
select ename,sal from emp limit 0, 5;
```
如果下标是从0开始，可以简写为：
```sql
select ename,sal from emp limit 5;
```

4. 查询工资排名在前5名的员工（limit是在order by执行之后才会执行的）
```sql
select ename,sal from emp order by sal desc limit 5;
```

5. 通用的分页sql

假设每页显示3条记录：pageSize = 3
第1页：limit 0, 3
第2页：limit 3, 3
第3页：limit 6, 3
第pageNo页：limit (pageNo - 1)*pageSize, pageSize
## 4.13 SQL练手题

1. 取得每个部门最高薪水的人员名称
   1. 第一步：取得每个部门最高薪水
```sql
select deptno,max(sal) as maxsal from emp group by deptno;
```

   2. 第二步：将上面第一步的查询结果当做一张临时表t，进行表连接，条件是：t.deptno=e.deptno and t.maxsal=e.sal
```sql
select e.ename,t.* from emp e join (select deptno,max(sal) as maxsal from emp group by deptno) t on e.deptno = t.deptno and e.sal = t.maxsal;
```

2. 哪些人的薪水在部门的平均薪水之上
   1. 第一步：取得每个部门的平均薪水
```sql
select deptno,avg(sal) as avgsal from emp group by deptno;
```

   2. 第二步：将上面的查询结果当做临时表t，让t和emp e表进行表连接，条件是：t.deptno=e.deptno and e.sal>t.avgsal
```sql
select e.ename,e.sal,t.* from emp e join (select deptno,avg(sal) as avgsal from emp group by deptno) t on t.deptno=e.deptno and e.sal>t.avgsal;
```

3. 取得每个部门平均薪水的等级
   1. 第一步：取得每个部门的平均薪水
```sql
select deptno,avg(sal) as avgsal from emp group by deptno;
```

   2. 第二步：将上面的查询结果当做临时表t，然后t和salgrade s表进行连接，条件是：t.avgsal between s.losal and s.hisal
```sql
select t.*,s.grade from (select deptno,avg(sal) as avgsal from emp group by deptno) t join salgrade s on t.avgsal between s.losal and s.hisal;
```

4. 取得部门中（所有人的）平均的薪水等级
   1. 第一步：找出每个人的薪水等级
```sql
select e.ename,e.sal,s.grade from emp e join salgrade s on e.sal between s.losal and s.hisal;
```

   2. 第二步：在上面的查询结果当中继续按照部门编号进行分组，求平均值。（不需要将上面的查询结果当做临时表，继续基于它进行分组即可。）
```sql
select 
   e.deptno,avg(s.grade) 
from 
  emp e 
join 
  salgrade s 
on 
  e.sal between s.losal and s.hisal 
group by 
  e.deptno;
```

5. 不准用组函数（Max），取得最高薪水（给出两种解决方案）
   1.  第一种方案：按照薪资降序排列，取第一个。
```sql
select sal from emp order by sal desc limit 1;
```

   2. 第二种方案：采用表的自连接方式。
```sql
select ename,sal from emp where sal not in(select distinct a.sal from emp a join emp b on a.sal < b.sal);
```

6. 取得平均薪水最高的部门的部门编号（至少给出两种解决方案）
   1. 第一种方案：降序排列取第一个
```sql
select deptno,avg(sal) as avgsal from emp group by deptno order by avgsal desc limit 1;
```

   2. 第二种方案：max函数
```sql
select deptno,avg(sal) as avgsal from emp group by deptno having avg(sal)=(select max(t.avgsal) from (select avg(sal) as avgsal from emp group by deptno) t);
```

7. 取得平均薪水最高的部门的部门名称
   1. 比上面的题目多一个表连接，和dept表连接，按照部门名称进行分组。
```sql
select d.dname,avg(e.sal) as avgsal from emp e join dept d on e.deptno=d.deptno group by d.dname order by avgsal desc limit 1;
```

8. 求平均薪水的等级最低的部门的部门名称
   1. 第一步：求每个部门的平均薪水
```sql
select d.dname,avg(e.sal) as avgsal from emp e join dept d on e.deptno = d.deptno group by d.dname;
```

   2. 第二步：求每个部门的平均薪水等级（将以上的执行结果当做临时表t，t和salgrade s表进行连接，条件：t.avgsal between .s.losal and s.hisal）
```sql
select t.*,s.grade from (select d.dname,avg(e.sal) as avgsal from emp e join dept d on e.deptno = d.deptno group by d.dname) t join salgrade s on t.avgsal between s.losal and s.hisal;
```

   3. 第三步：找到最低的部门名称（以上结果继续按照grade进行升序，然后limit 1）
```sql
select t.*,s.grade from (select d.dname,avg(e.sal) as avgsal from emp e join dept d on e.deptno = d.deptno group by d.dname) t join salgrade s on t.avgsal between s.losal and s.hisal order by s.grade asc limit 1;
```

9. 取得比普通员工(员工代码没有在mgr字段上出现的)的最高薪水还要高的领导人姓名
   1. 第一步：找出所有的普通员工的最高薪水
```sql
select max(sal) from emp where empno not in(select mgr from emp where mgr is not null);
```

   2. 第二步：大于以上最高薪水的一定是要找的领导人。
```sql
select ename,sal from emp where sal > (select max(sal) from emp where empno not in(select mgr from emp where mgr is not null));
```

10. 取得薪水最高的前五名员工
```sql
select ename,sal from emp order by sal desc limit 5;
```

11. 取得薪水最高的第六到第十名员工
```sql
select ename,sal from emp order by sal desc limit 5, 5;
```

12. 取得最后入职的5名员工
```sql
select ename,sal,hiredate from emp order by hiredate desc limit 5;
```

13. 取得每个薪水等级有多少员工
   1. 第一步：找出每个员工的薪水等级
```sql
select e.ename,s.grade from emp e join salgrade s on e.sal between s.losal and s.hisal;
```

   2. 第二步：基于以上的记录继续根据等级分组，count即可。
```sql
select s.grade,count(*) from emp e join salgrade s on e.sal between s.losal and s.hisal group by s.grade;
```

14. 列出所有员工及领导的姓名
```sql
select e.ename 员工名, l.ename 领导名 from emp e left join emp l on e.mgr = l.empno;
```

15. 列出受雇日期早于其直接上级的所有员工的编号,姓名,部门名称
```sql
select e.ename 员工名,e.hiredate, l.ename 领导名,l.hiredate,d.dname from emp e join emp l on e.mgr = l.empno join dept d on e.deptno = d.deptno where e.hiredate < l.hiredate;
```

16. 列出部门名称和这些部门的员工信息,同时列出那些没有员工的部门
```sql
select d.dname,e.ename,e.sal from dept d left join emp e on d.deptno = e.deptno;
```

17. 列出至少有5个员工的所有部门
```sql
select deptno, count(*) from emp group by deptno having count(*) >= 5;
```

18. 列出薪金比"SMITH"多的所有员工信息
```sql
select ename,sal from emp where sal > (select sal from emp where ename = 'SMITH');
```

19. 列出所有"CLERK"(办事员)的姓名及其部门名称,部门的人数
```sql
select t1.ename,t1.dname,t2.total from (select e.ename,d.dname,d.deptno from emp e join dept d on e.deptno = d.deptno where e.job = 'CLERK') t1 join (select count(*) as total,deptno  from emp group by deptno) t2 on t1.deptno = t2.deptno;
```

20. 列出最低薪金大于1500的各种工作及从事此工作的全部雇员人数
```sql
select job,min(sal),count(*) from emp group by job having min(sal)>1500;
```

21. 列出在部门"SALES"<销售部>工作的员工的姓名,假定不知道销售部的部门编号
```sql
select e.ename,d.dname from emp e join dept d on e.deptno = d.deptno where d.dname='sales';
```

22. 列出薪金高于公司平均薪金的所有员工,所在部门,上级领导,雇员的工资等级
```sql
select e.ename 员工,l.ename 领导,d.dname,s.grade from 
emp e left join emp l on e.mgr = l.empno 
join dept d on e.deptno = d.deptno 
join salgrade s on e.sal between s.losal and s.hisal 
where e.sal > (select avg(sal) from emp);
```

23. 列出与"SCOTT"从事相同工作的所有员工及部门名称
```sql
select e.ename,d.dname,e.job from emp e join dept d on e.deptno=d.deptno where job=(select job from emp where ename ='scott');
```

24. 列出薪金等于部门30中员工的薪金的其他员工的姓名和薪金
```sql
select ename,sal,deptno from emp where sal in(select distinct sal from emp where deptno=30) and deptno <> 30;
```

25. 列出薪金高于在部门30工作的所有员工的薪金的员工姓名和薪金.部门名称
```sql
select e.ename,e.sal,d.dname from emp e join dept d on e.deptno = d.deptno where sal > (select max(sal) from emp where deptno=30);
```

26. 列出在每个部门工作的员工数量,平均工资和平均服务期限
```sql
select avg(sal),count(*),deptno,avg(datediff(now(),hiredate)) as avgtime from emp group by deptno;
```

27. 列出所有员工的姓名、部门名称和工资
```sql
select e.ename,e.sal,d.dname from emp e join dept d on e.deptno = d.deptno;
```

28. 列出所有部门的详细信息和人数
```sql
select d.deptno,d.dname,d.loc,count(e.deptno) from emp e right join dept d on e.deptno=d.deptno group by  d.deptno,d.dname,d.loc;
```

29. 列出各种工作的最低工资及从事此工作的雇员姓名
```sql
select t.job,t.minsal,e.ename from emp e join (select job,min(sal) as minsal from emp group by job) t on e.job=t.job and e.sal=t.minsal;
```

30. 列出各个部门的MANAGER(领导)的最低薪金
```sql
select deptno,min(sal) from emp where job='MANAGER' group by deptno
```

31. 列出所有员工的年工资,按年薪从低到高排序
```sql
select ename,(sal+ifnull(comm,0))*12 as yearsal from emp order by yearsal asc;
```

32. 求出员工领导的薪水超过3000的员工名称与领导名称
```sql
select e.ename 员工名, l.ename 领导名 from emp e join emp l on e.mgr = l.empno where l.sal>3000;
```

33. 求出部门名称中,带'S'字符的部门员工的工资合计、部门人数
```sql
select d.dname,ifnull(sum(sal),0) as sumsal,count(e.ename) from emp e right join dept d on e.deptno=d.deptno where d.dname like '%S%' group by d.dname;
```

34. 给任职日期超过30年的员工加薪10%
```sql
update emp set sal=sal*1.1 where datediff(now(),hiredate)/365 > 30;
```

35. 某公司面试题

有3个表S（学生表），C（课程表），SC（学生选课表）
S（SNO，SNAME）代表（学号，姓名）  
C（CNO，CNAME，CTEACHER）代表（课号，课名，教师）
SC（SNO，CNO，SCGRADE）代表（学号，课号，成绩）
```sql
CREATE TABLE SC
(
  SNO      VARCHAR(200),
  CNO      VARCHAR(200),
  SCGRADE  VARCHAR(200)
);

CREATE TABLE S
(
  SNO    VARCHAR(200 ),
  SNAME  VARCHAR(200)
);

CREATE TABLE C
(
  CNO       VARCHAR(200),
  CNAME     VARCHAR(200),
  CTEACHER  VARCHAR(200)
);

INSERT INTO C ( CNO, CNAME, CTEACHER ) VALUES ( '1', '语文', '张'); 
INSERT INTO C ( CNO, CNAME, CTEACHER ) VALUES ( '2', '政治', '王'); 
INSERT INTO C ( CNO, CNAME, CTEACHER ) VALUES ( '3', '英语', '李'); 
INSERT INTO C ( CNO, CNAME, CTEACHER ) VALUES ( '4', '数学', '赵'); 
INSERT INTO C ( CNO, CNAME, CTEACHER ) VALUES ( '5', '物理', '黎明'); 
commit;
 
INSERT INTO S ( SNO, SNAME ) VALUES ( '1', '学生1'); 
INSERT INTO S ( SNO, SNAME ) VALUES ( '2', '学生2'); 
INSERT INTO S ( SNO, SNAME ) VALUES ( '3', '学生3'); 
INSERT INTO S ( SNO, SNAME ) VALUES ( '4', '学生4'); 
commit;
 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '1', '1', '40'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '1', '2', '30'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '1', '3', '20'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '1', '4', '80'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '1', '5', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '2', '1', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '2', '2', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '2', '3', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '2', '4', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '2', '5', '40'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '3', '1', '60'); 
INSERT INTO SC ( SNO, CNO, SCGRADE ) VALUES ( '3', '3', '80'); 
commit;
```
问题：
1，找出没选过“黎明”老师的所有学生姓名。
```sql
select sname from s where sno not in(select sno from sc where cno=(select cno from c where cteacher='黎明'));
```
2，列出2门以上（含2门）不及格学生姓名及平均成绩。
```sql
select a.*,b.avgscore from (select s.sno,s.sname,count(sc.scgrade) as num from sc join s on sc.sno=s.sno where sc.scgrade < 60 group by s.sname,s.sno having count(sc.scgrade) >= 2) a join (select sno,avg(scgrade) avgscore from sc group by sno) b on a.sno = b.sno;
```
3，既学过1号课程又学过2号课所有学生的姓名。
```sql
select sc.sno,s.sname from sc join s on sc.sno=s.sno where sc.cno=1 and sc.sno in(select sno from sc where cno=2);
```
# 五、表
## 5.1 创建表
语法格式：
```sql
create table 表名(
  字段名1 数据类型,
  字段名2 数据类型,
  字段名3 数据类型,
  ......
);
```
例如：创建学生表
```sql
create table t_student(
  no int,
  name varchar,
  gender char(1) default '男'
);
```
## 5.2 插入数据
语法格式：
```sql
insert into 表名(字段名1, 字段名2, 字段名3,......) values (值1,值2,值3,......);
```
字段名和值要一一对应。类型要一一对应，数量要一一对应。
字段名也可以省略，如果字段名省略就表示把所有字段名都写上去了，并且顺序和建表时的顺序相同。
## 5.3 删除表
语法格式：
```sql
drop table 表名;
```
或者
```sql
drop table if exists 表名;
```
判断是否存在这个表，如果存在则删除。避免不存在时的报错。
## 5.4 MySQL数据类型
数据类型（data_type）是指系统中所允许的数据的类型。数据库中的每个列都应该有适当的数据类型，用于限制或允许该列中存储的数据。例如，列中存储的为数字，则相应的数据类型应该为数值类型。
如果使用错误的数据类型可能会严重影响应用程序的功能和性能，所以在设计表时，应该特别重视数据列所用的数据类型。更改包含数据的列不是一件小事，这样做可能会导致数据丢失。因此，在创建表时必须为每个列设置正确的数据类型和长度。
MySQL 的数据类型可以分为整数类型、浮点数类型、定点数类型、日期和时间类型、字符串类型、二进制类型等。
### 5.4.1 整数类型
tinyint：1个字节（微小整数）
smallint：2个字节（小整数）
mediumint：3个字节（中等大小的整数）
int（integer）：4个字节（普通大小整数）
bigint：8个字节（大整数）
### 5.4.2 浮点数类型
float：4个字节，单精度（最多5位小数）
double：8个字节，双精度（最多16位小数）
### 5.4.3 定点数类型
decimal：定点数类型。底层实际上采用字符串的形式存储数字。
语法：decimal(m, d)
例如：decimal(3, 2) 表示3个有效数字，2个小数。
### 5.4.4 日期和时间类型
year：1个字节，只存储年，格式YYYY
time：3个字节，只存储时间，格式HH:MM:SS / HHMMSS
date：3个字节，只存储年月日，格式：YYYY-MM-DD
datetime：8个字节，存储年月日+时分秒，格式：YYYY-MM-DD HH:MM:SS（从公元1000年~公元9999年）
timestamp：4个字节，存储年月日+时分秒，格式：YYYY-MM-DD HH:MM:SS（从公元1980年~公元2040年）或者格式为 YYYYMMDDHHMMSS（采用这种格式不需要使用单引号，当然你使用单引号也可以）
### 5.4.5 字符串类型
**char(m)：**m长度是0~255个字符。
固定长度字符串，在定义时指定字符串列长。当保存时，在右侧填充空格以达到指定的长度。m表示列的长度，范围是 0～255 个字符。
例如，CHAR(4) 定义了一个固定长度的字符串列，包含的字符个数最大为 4。当检索到 CHAR 值时，尾部的空格将被删除。
**varchar(m)：**m长度是0~16383个字符
长度可变的字符串。varchar 的最大实际长度由最长的行的大小和使用的字符集确定，而实际占用的空间为字符串的实际长度加 1。
例如，varchar(50) 定义了一个最大长度为 50 的字符串，如果插入的字符串只有 10 个字符，则实际存储的字符串为 10 个字符和一个字符串结束字符。varchar在值保存和检索时尾部的空格仍保留。
![640.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1678606760951-7d88aef7-4f6a-47cb-bd13-88af106eabbe.png#averageHue=%23f2f1ef&clientId=u18d9f4bd-818e-4&from=paste&height=258&id=uea1bb017&originHeight=258&originWidth=536&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5683&status=done&style=shadow&taskId=u953b7752-1411-45db-a168-f79005ee5a9&title=&width=536)
**text类型：**

- tinytext 表示长度为 255字符的 TEXT 列。
- text 表示长度为 65535字符的 TEXT 列。
- mediumtext 表示长度为 16777215字符的 TEXT 列。
- longtext 表示长度为 4294967295 或 4GB 字符的 TEXT 列。

**enum类型：**

- 语法：<字段名> enum('值1','值2',...)
- 该字段插入值时，只能是指定的枚举值。

**set类型：**

- 语法：<字段名> set('值1','值2','值3',...)   注意：值不可重复。
- 该字段插入值时，只能是指定的值。
### 5.4.6 二进制类型
BLOB类型：二进制大对象，可以存储图片、声音、视频等文件。

- blob：小的，最大长度65535个字节
- mediumblob：中等的，最大长度16777215个字节
- longblob：大的，最大长度4GB的字节
## 5.5 增删改表结构DDL
### 创建一个学生表
```sql
create table t_student(
  no bigint,
  name varchar(255),
  age int comment '年龄'
);
```
### 查看建表语句
```sql
show create table 表名;
```
### 修改表名
```sql
alter table 表名 rename 新表名;
```
### 新增字段
```sql
alter table 表名 add 字段名 数据类型;
```
### 修改字段名
```sql
alter table 表名 change 旧字段名 新字段名 数据类型;
```
### 修改字段数据类型
```sql
alter table 表名 modify column 字段名 数据类型;
```
### 删除字段
```sql
alter table 表名 drop 字段名;
```
## 5.6 DML语句
当我们对表中的数据进行增删改的时候，称它为DML语句。（数据操纵语言），主要包括：insert、delete、update
### 5.6.1 insert 增
语法格式：
```sql
insert into 表名(字段名1,字段名2,字段名3,...) values(值1,值2,值3,...);
```
表名后面的小括号当中的字段名如果省略掉，表示自动将所有字段都列出来了，并且字段的顺序和建表时的顺序一致。
一般为了可读性强，建议把字段名写上。
```sql
insert into 表名 values(值1,值2,值3,...);
```
一次可以插入多条记录：
```sql
insert into t_stu(no,name,age) values(1,'jack',20),(2,'lucy',30);
```
### 5.6.2 delete 删
语法格式：
```sql
# 将所有记录全部删除
delete from 表名;

# 删除符合条件的记录
delete from 表名 where 条件;
```
以上的删除属于DML的方式删除，这种删除的数据是可以通过事务回滚的方式重新恢复的，但是删除的效率较低。（这种删除是支持事务的。）
另外还有一种删除表中数据的方式，但是这种方式不支持事务，不可以回滚，删了之后数据是永远也找不回来了。这种删除叫做：表被截断。
注意：这个语句删除效率非常高，巨大的表，瞬间干掉所有数据。但不可恢复。
```sql
truncate table 表名;
```
### 5.6.3 update 改
语法格式：
```sql
update 表名 set 字段名1=值1, 字段名2=值2, 字段名3=值3 where 条件;
```
如果没有更新条件的话，所有记录全部更新。
## 5.7 约束constraint
创建表时，可以给表的字段添加约束，可以保证数据的完整性、有效性。比如大家上网注册用户时常见的：用户名不能为空。对不起，用户名已存在。等提示信息。
约束通常包括：

- 非空约束：not null
- 检查约束：check
- 唯一性约束：unique
- 主键约束：primary key
- 外键约束：foreign key
### 5.7.1 非空约束
语法格式：
```sql
create table t_stu(
  no int,
  name varchar(255) not null,
  age int
);
```
name字段不能为空。插入数据时如果没有给name指定值，则报错。
### 5.7.2 检查约束
```sql
create table t_stu(
  no int,
  name varchar(255),
  age int,
  check(age > 18)
);
```
### 5.7.3 唯一性约束
语法格式：
```sql
create table t_stu(
  no int,
  name varchar(255),
  email varchar(255) unique
);
```
email字段设置为唯一性，唯一性的字段值是可以为NULL的。但不能重复。以上在字段后面添加的约束，叫做列级约束。
当然，添加约束还有另一种方式：表级约束：
```sql
create table t_stu(
  no int,
  name varchar(255),
  email varchar(255),
  unique(email)
);
```
使用表级约束可以为多个字段添加联合唯一。
```sql
create table t_stu(
  no int,
  name varchar(255),
  email varchar(255),
  unique(name,email)
);
```
创建约束时也可以给约束起名字，将来可以通过约束的名字来删除约束：
```sql
create table t_stu(
  no int,
  name varchar(255),
  email varchar(255),
  constraint t_stu_name_email_unique unique(name,email)
);
```
所有的约束都存储在一个系统表当中：table_constraints。这个系统表在这个数据库当中：information_schema
### 5.7.4 主键约束

1. 主键：primary key，简称PK
2. 主键约束的字段不能为NULL，并且不能重复。
3. 任何一张表都应该有主键，没有主键的表可以视为无效表。
4. 主键值是这行记录的身份证号，是唯一标识。在数据库表中即使两条数据一模一样，但由于主键值不同，我们也会认为是两条完全的不同的数据。
5. 主键分类：
   1. 根据字段数量分类：
      1. 单一主键（1个字段作为主键）==>建议的
      2. 复合主键（2个或2个以上的字段作为主键）
   2. 根据业务分类：
      1. 自然主键（主键和任何业务都无关，只是一个单纯的自然数据）===>建议的
      2. 业务主键（主键和业务挂钩，例如：银行卡账号作为主键）
6. 单一主键（建议使用这种方式）
```sql
create table t_student(
  id bigint primary key,
  sno varchar(255) unique,
  sname varchar(255) not null
)
```

7. 复合主键（很少用，了解）
```sql
create table t_user(
  no int,
  name varchar(255),
  age int,
  constraint t_user_pk_no_name primary key(no,name)
);
```

8. 主键自增：既然主键值是一个自然的数字，mysql为主键值提供了一种自增机制，不需要我们程序员维护，mysql自动维护该字段
```sql
create table t_vip(
  no int primary key auto_increment,
  name varchar(255)
);
```
### 5.7.5 外键约束

1. 有这样一个需求：要求设计表，能够存储学生以及学校信息。
   1. 第一种方案：一张表

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679198700192-73c1c697-39a5-483e-b267-730fb808082d.png#averageHue=%23f2f58e&clientId=uf7a0608d-b7a1-4&from=paste&height=263&id=u385df011&originHeight=263&originWidth=881&originalType=binary&ratio=1&rotation=0&showTitle=false&size=11603&status=done&style=shadow&taskId=u6a97350e-9ae3-4c6d-b1ec-963559ebf2e&title=&width=881)
这种方式会导致数据冗余，浪费空间。

   2. 第二种方案：两张表：一张存储学生，一张存储学校

t_school 表
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679198814824-520944e2-5b83-49ba-97e7-b8830286127a.png#averageHue=%23c9d481&clientId=uf7a0608d-b7a1-4&from=paste&height=85&id=ud1ad0346&originHeight=85&originWidth=471&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2397&status=done&style=shadow&taskId=u76cd09e9-9753-41f7-81d7-729db7c551a&title=&width=471)
t_student 表
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679198856678-a80be906-abc8-4bf7-ac5e-e6a59b11c48a.png#averageHue=%23f3f77a&clientId=uf7a0608d-b7a1-4&from=paste&height=264&id=ufa1ef2a6&originHeight=264&originWidth=532&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4445&status=done&style=shadow&taskId=u30eaa682-24a0-4b6f-a1c5-3eed3bc24cc&title=&width=532)
如果采用以上两张表存储数据，对于学生表来说，sno这个字段的值是不能随便填的，这个sno是学校编号，必须要求这个字段中的值来自学校表的sno。
为了达到要求，此时就必须要给t_student表的sno字段添加外键约束了。

2. 外键约束：foreign key，简称FK。
3. 添加了外键约束的字段中的数据必须来自其他字段，不能随便填。
4. 假设给a字段添加了外键约束，要求a字段中的数据必须来自b字段，b字段不一定是主键，但至少要有唯一性。
5. 外键约束可以给单个字段添加，叫做单一外键。也可以给多个字段联合添加，叫做复合外键。复合外键很少用。
6. a表如果引用b表中的数据，可以把b表叫做父表，把a表叫做子表。
   1. 创建表时，先创建父表，再创建子表。
   2. 插入数据时，先插入父表，在插入子表。
   3. 删除数据时，先删除子表，再删除父表。
   4. 删除表时，先删除子表，再删除父表。
7. 如何添加外键：
```sql
create table t_school( 
  sno int primary key, 
  sname varchar(255) 
); 
create table t_student( 
  no int primary key, 
  name varchar(255), 
  age int, 
  sno int, 
  constraint t_school_sno_fk foreign key(sno) references t_school(sno) 
);
```

8. 级联删除

创建子表时，外键可以添加：on delete cascade，这样在删除父表数据时，子表会级联删除。谨慎使用。
```sql
create table t_student( 
  no int primary key, 
  name varchar(255), 
  age int, 
  sno int, 
  constraint t_school_sno_fk foreign key(sno) references t_school(sno) on delete cascade 
);
```
```sql
###删除约束
alert table t_student drop foreign key t_student_sno_fk;
###添加约束
alert table t_student add constraint t_student_sno_fk foreign key(sno) references t_school(sno) on delete cascade;
```

9. 级联更新 
```sql
create table t_student( 
  no int primary key, 
  name varchar(255), 
  age int, 
  sno int, 
  constraint t_school_sno_fk foreign key(sno) references t_school(sno) on update cascade 
);
```

10. 级联置空
```sql
create table t_student( 
  no int primary key, 
  name varchar(255), 
  age int, 
  sno int, 
  constraint t_school_sno_fk foreign key(sno) references t_school(sno) on delete set null 
);
```
# 六、数据库设计三范式

1. 什么是数据库设计三范式？
   1. 数据库表设计的原则。教你怎么设计数据库表有效，并且节省空间。
2. 三范式
   1. 第一范式：任何一张表都应该有主键，每个字段是原子性的不能再分
      1. 以下表的设计不符合第一范式：无主键，并且联系方式可拆分。

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679201425169-4ce0b510-2795-4ac8-a0ca-404ffcb6c044.png#averageHue=%23e6e2df&clientId=uf7a0608d-b7a1-4&from=paste&height=99&id=udf5679c6&originHeight=99&originWidth=429&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4785&status=done&style=shadow&taskId=ua7237fee-83ff-44dd-82a6-53445c89cce&title=&width=429)

      2. 应该这样设计：

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679201619568-bcb56e54-e4d5-4152-9833-49d97afa8d35.png#averageHue=%23dcdad8&clientId=uf7a0608d-b7a1-4&from=paste&height=106&id=ua1de331d&originHeight=106&originWidth=455&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5704&status=done&style=shadow&taskId=ua7aef1c7-2585-4b7f-8bdc-d468b6f5e71&title=&width=455)

   2. 第二范式：建立在第一范式基础上的，另外要求所有非主键字段完全依赖主键，不能产生部分依赖
      1. 以下表存储了学生和老师的信息

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679201885946-02cacd49-4288-4520-93fb-e4dae6cff5dc.png#averageHue=%23e3e2e2&clientId=uf7a0608d-b7a1-4&from=paste&height=127&id=u841b84e0&originHeight=127&originWidth=440&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4331&status=done&style=shadow&taskId=ua875c093-5656-40b7-bb25-7cd52eb2197&title=&width=440)
虽然符合第一范式，但是违背了第二范式，学生姓名、老师姓名都产生了部分依赖。导致数据冗余。

      2. 以下这种设计方式就是符合第二范式的：

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679202122322-da28bdc0-703b-4975-8fe4-0a7b6a222fee.png#averageHue=%23efefef&clientId=uf7a0608d-b7a1-4&from=paste&height=258&id=u6726dbc4&originHeight=258&originWidth=662&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6393&status=done&style=shadow&taskId=uec7f9cf8-9d6f-47fd-8585-4d896c74e0d&title=&width=662)

   3. 第三范式：建立在第二范式基础上的，非主键字段不能传递依赖于主键字段
      1. 以下设计方式就是违背第三范式的

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679202299108-66198c2a-933d-4bea-9e67-51425c31be7c.png#averageHue=%23e2e2e1&clientId=uf7a0608d-b7a1-4&from=paste&height=129&id=uc7c79455&originHeight=129&originWidth=435&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4338&status=done&style=shadow&taskId=u2f464a3a-5a10-4004-89bf-b89b7144111&title=&width=435)
以上因为产生了传递依赖，导致班级名称冗余。

      2. 以下这种方式就是符合第三范式的：

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679202402829-5040060c-c87f-4411-a599-6a60cc3836a0.png#averageHue=%23e8e7e7&clientId=uf7a0608d-b7a1-4&from=paste&height=270&id=u5495ef35&originHeight=270&originWidth=325&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5610&status=done&style=shadow&taskId=u197e8a0c-3b3f-4627-a574-464a40a019f&title=&width=325)

3. 一对多怎么设计？
   1. 口诀：一对多两张表，多的表加外键。
   2. ![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679200526299-5a9122fe-b7f6-423c-9fd8-5c28a960cb75.png#averageHue=%23cad480&clientId=uf7a0608d-b7a1-4&from=paste&height=84&id=u7e79770c&originHeight=84&originWidth=474&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2499&status=done&style=shadow&taskId=u67f05804-f17a-41aa-b626-21638d20ef9&title=&width=474)
   3. ![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679200546241-3a0db05e-74e8-4452-92b9-721c5b3d36d5.png#averageHue=%23f4f779&clientId=uf7a0608d-b7a1-4&from=paste&height=262&id=ue4c12bca&originHeight=262&originWidth=533&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6129&status=done&style=shadow&taskId=uf2d1bb71-1993-4ccf-b8ae-cc8c3e51671&title=&width=533)
4. 多对多怎么设计？
   1. 多对多三张表，关系表添加外键。
   2. ![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679200858013-26513a66-0af8-4b84-bd90-b52a240de65c.png#averageHue=%23efe9e9&clientId=uf7a0608d-b7a1-4&from=paste&height=283&id=ucc864c99&originHeight=283&originWidth=944&originalType=binary&ratio=1&rotation=0&showTitle=false&size=14583&status=done&style=shadow&taskId=u5e882710-c0a4-4a2c-b02f-fc57a3e10de&title=&width=944)
5. 一对一怎么设计？
   1. 两种方案：
      1. 第一种：主键共享
         1. ![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679201037367-a1b5661a-f127-42b0-87d9-609c61fa4839.png#averageHue=%23ededaa&clientId=uf7a0608d-b7a1-4&from=paste&height=111&id=u82a64286&originHeight=111&originWidth=501&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2087&status=done&style=shadow&taskId=u60e60695-8178-4aae-9c1b-1d9bf3b165d&title=&width=501)
      2. 第二种：外键唯一
         1. ![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679201084526-c5773a4e-75bf-4e6d-9ac4-f8b8272d1b46.png#averageHue=%23e6e6e6&clientId=uf7a0608d-b7a1-4&from=paste&height=115&id=ufe1dc281&originHeight=115&originWidth=697&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2496&status=done&style=shadow&taskId=u50c9eb60-c470-4498-ab25-2aa5f736dbd&title=&width=697)
6. 最终的设计？
   1. 最终以满足客户需求为原则，有的时候会拿空间换速度。
# 七、视图

1. 只能将select语句创建为视图。
2. 创建视图
```sql
create or replace view v_emp as select e.ename,d.dname from emp e join dept d on e.deptno = d.deptno;
```

3. 视图作用
   1. 如果开发中有一条非常复杂的SQL，而这个SQL在多处使用，会给开发和维护带来成本。使用视图可以降低开发和维护的成本。
   2. 视图可以隐藏表的字段名。
4. 修改视图
```sql
alter view v_emp as select e.ename,d.dname,d.deptno from emp e join dept d on e.deptno = d.deptno;
```

5. 删除视图
   1. drop view if exists v_emp;
6. 对视图增删改可以影响到原表数据。
# 八、事务

1. 什么是事务？
   1. 事务是一个最小的工作单元。在数据库当中，事务表示一件完整的事儿。
   2. 一个业务的完成可能需要多条DML语句共同配合才能完成，例如转账业务，需要执行两条DML语句，先更新张三账户的余额，再更新李四账户的余额，为了保证转账业务不出现问题，就必须保证要么同时成功，要么同时失败，怎么保证同时成功或者同时失败呢？就需要使用事务机制。
   3. 也就是说用了事务机制之后，在同一个事务当中，多条DML语句会同时成功，或者同时失败，不会出现一半成功，一半失败的现象。
2. 事务只针对DML语句有效：因为只有这三个语句是改变表中数据的。
   1. insert
   2. delete
   3. update
3. 事务四大特性：ACID
   1. 原子性（Atomicity）：是指事务包含的所有操作要么全部成功，要么同时失败。
   2. 一致性（Consistency）：是指事务开始前，和事务完成后，数据应该是一致的。例如张三和李四的钱加起来是5000，中间不管进行过多少次的转账操作(update)，总量5000是不会变的。这就是事务的一致性。
   3. 隔离性（Isolation）：隔离性是当多个⽤户并发访问数据库时，⽐如操作同⼀张表时，数据库为每⼀个⽤户开启的事务，不能被其他事务的操作所⼲扰，多个并发事务之间要相互隔离。
   4. 持久性（Durability）：持久性是指⼀个事务⼀旦被提交了，那么对数据库中的数据的改变就是永久性的，即便是在数据库系统遇到故障的情况下也不会丢失提交事务的操作。
4. 演示MySQL事务
   1. 在dos命令窗口中开启MySQL事务：start transaction; 或者：begin;
   2. 回滚事务：rollback; 
   3. 提交事务：commit;

只要执行以上的rollback或者commit，事务都会结束。
MySQL默认情况下采用的事务机制是：自动提交。所谓自动提交就是只要执行一条DML语句则提交一次。
了解内容：
savepoint p1; 将事务保存在某个点。
rollback to savepoint p1; 将事务回滚到保存点。

5. 事务隔离级别：

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679213953232-4c17a795-8b1f-45d2-907b-c5c16aff672d.png#averageHue=%23e6e3e1&clientId=u5f51673a-a60a-4&from=paste&height=203&id=ue588be16&originHeight=203&originWidth=788&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16611&status=done&style=shadow&taskId=uca6fc90a-5745-4c38-aa5b-62e77ac8997&title=&width=788)
脏读：能够读取到别人没有提交的数据。
不可重复读：在同一个事务中，第一次读取到的数据可能和第二次读取到的数据不同。
幻读：读取到的数据不够真实。

6. mysql默认的隔离级别：可重复读。
   1. 查看当前会话的隔离级别：select @@transaction_isolation;
   2. 查看全局的隔离级别：select @@gobal.transaction_isolation;
7. 设置事务隔离级别：
   1. 会话级：set transaction isolation level read committed;
   2. 全局级：set global transaction isolation level read committed;
8. 演示事务隔离级别。
# 九、DBA命令
## 1. 新建用户
创建一个用户名为java1，密码设置为123的本地用户：
```sql
create user 'java1'@'localhost' identified by '123';
```
创建一个用户名为java2，密码设置为123的外网用户：
```sql
create user 'java2'@'%' identified by '123';
```
采用以上方式新建的用户没有任何权限：系统表也只能看到以下两个
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679813363625-10cc7c30-76b3-4a1a-a83f-a1727489a420.png#averageHue=%23141211&clientId=u8834b383-d147-4&from=paste&height=197&id=u9bbde222&originHeight=197&originWidth=318&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6925&status=done&style=shadow&taskId=ub1483b88-60e6-4eac-a9d2-c1eb024463f&title=&width=318)
使用root用户查看系统中当前用户有哪些？
```sql
select user,host from mysql.user;
```
## 2. 给用户授权
授权语法：grant [权限1，权限2...] on 库名.表名 to '用户名'@'主机名/IP地址';
给本地用户授权：grant [权限1，权限2...] on 库名.表名 to '用户名'@'localhost';
给外网用户授权：grant [权限1，权限2...] on 库名.表名 to '用户名'@'%';
所有权限：all privileges
细粒度权限：select、insert、delete、update、alter、create、drop、index(索引)、usage(登录权限)......
库名可以使用 * ，它代表所有数据库
表名可以采用 * ，它代表所有表
也可以提供具体的数据库和表，例如：powernode.emp （powernode数据库的emp表）
```sql
# 将所有库所有表的查询权限赋予本地用户java1
grant select on *.* to 'java1'@'localhost';

# 将powernode库中所有表的所有权限赋予本地用户java1
grant all privileges on powernode.* to 'java1'@'localhost';
```
授权后必须刷新权限，才能生效：flush privileges
查看某个用户拥有哪些权限？
show grants for 'java1'@'localhost'
show grants for 'java2'@'%'
with grant option：
```sql
# with grant option的作用是：java2用户也可以给其他用户授权了。
grant select,insert,delete,update on powernode.* to 'java2'@'%' with grant option;
```
## 3. 撤销用户权限
revoke 权限 on 数据库名.表名 from '用户'@'IP地址';
```sql
# 撤销本地用户java1的insert、update、delete权限
revoke insert, update, delete on powernode.* from 'java1'@'localhost'

# 撤销外网用户java2的insert权限
revoke insert on powernode.* from 'java2'@'%'
```
撤销权限后也需要刷新权限：flush privileges
## 4. 修改用户的密码
具有管理用户权限的用户才能修改密码，例如root账户可以修改其他账户的密码：
```sql
# 本地用户修改密码
alter user 'java1'@'localhost' identified by '456';

# 外网用户修改密码
alter user 'java2'@'%' identified by '456';
```
修改密码后，也需要刷新权限才能生效：flush privileges
以上是MySQL8版本以后修改用户密码的方式。
## 5. 修改用户名
```sql
rename user '原始用户名'@'localhost' to '新用户名'@'localhost';
rename user '原始用户名'@'localhost' to '新用户名'@'%';

rename user 'java1'@'localhost' to 'java11'@'localhost';
rename user 'java11'@'localhost' to 'java123'@'%';
```
flush privileges;
## 6. 删除用户
```sql
drop user 'java123'@'localhost';
drop user 'java2'@'%';
```
flush privileges;
## 7. 数据备份

- 导出数据（请在登录mysql数据库之前进行）
```sql
# 导出powernode这个数据库中所有的表
mysqldump powernode > d:/powernode.sql -uroot -p123456

# 导出powernode中emp表的数据
mysqldump powernode emp > d:/powernode.sql -uroot -p123456
```

- 导入数据（请在登录mysql之后操作）
```sql
create  database powernode;
use powernode;
source d:/powernode.sql
```
# 十、MySQL客户端工具

1. 对于后端开发人员来说，一个好的MySQL客户端工具可以大大提升开发效率。目前企业中使用最多的是以下三个：
   1. Navicat for MySQL

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679825266467-a704f0ce-835d-48c6-ab37-4c7bf5a1be57.png#averageHue=%239de04f&clientId=u8834b383-d147-4&from=paste&height=93&id=ue8403e90&originHeight=263&originWidth=264&originalType=binary&ratio=1&rotation=0&showTitle=false&size=54043&status=done&style=shadow&taskId=u13e0ee5b-7dc9-4d41-a5e6-33d69114d58&title=&width=93)

   2. SQLyog

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679825351769-5a2abe9e-cabb-407f-87e5-1aafeada40bd.png#averageHue=%23f6f8f3&clientId=u8834b383-d147-4&from=paste&height=71&id=uf4a91db7&originHeight=88&originWidth=116&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9555&status=done&style=shadow&taskId=u9e276d30-97ad-48b9-a9b7-d3215334276&title=&width=94)

   3. MySQL Workbench

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1679825234020-fa921858-476d-44c8-8074-1c0b137f2eaf.png#averageHue=%23f9fefe&clientId=u8834b383-d147-4&from=paste&height=73&id=u2b8715ba&originHeight=73&originWidth=75&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6361&status=done&style=shadow&taskId=u702d576c-d3d1-4608-8bcc-bb2c68ba437&title=&width=75)

2. 安装Navicat for MySQL
3. 使用Navicat for MySQL
   1. 客户端连接MySQL服务器
   2. 创建数据库（字符集的选择）
   3. 创建表，设置主键，并且主键自增
   4. 添加数据（开启事务提交事务）
   5. 删除数据
   6. 修改数据
   7. 导出SQL脚本，导入SQL脚本
   8. 执行查询（全部执行和选择执行）
   9. 事务
   10. 外键
# 十一、企业真题
## 第一题
![1.jpg](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680103320228-5ed4903b-6a54-4ce8-81c6-e3f1738eac95.jpeg#averageHue=%2385868b&clientId=uaa2e6f21-7481-4&from=paste&height=960&id=u7e7ddb69&originHeight=960&originWidth=541&originalType=binary&ratio=1&rotation=0&showTitle=false&size=33263&status=done&style=shadow&taskId=u7351acee-03a5-4cf0-9f72-98dcc8c9a08&title=&width=541)
```sql
# 第一步：找小于等于80分的学员姓名
select distinct name from t_student where fenshu <= 80

# 第二步：not in
select distinct name from t_student where name not in(select distinct name from t_student where fenshu <= 80)
```
## 第二题
![2.jpg](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680103877015-ca07133d-716e-4cce-82f3-52118ff4c9ad.jpeg#averageHue=%2389857c&clientId=uaa2e6f21-7481-4&from=paste&height=461&id=u0043cb44&originHeight=461&originWidth=615&originalType=binary&ratio=1&rotation=0&showTitle=false&size=35758&status=done&style=shadow&taskId=u25d031eb-03ec-419c-8119-34b901a3a42&title=&width=615)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680104265213-8afaf5de-a962-47c6-a1cd-72aefe28f616.png#averageHue=%23dbe3e9&clientId=uaa2e6f21-7481-4&from=paste&height=342&id=uc0c3fef4&originHeight=342&originWidth=750&originalType=binary&ratio=1&rotation=0&showTitle=false&size=9419&status=done&style=shadow&taskId=u12d9f5f8-e531-4fd6-99b6-10f4ed7a039&title=&width=750)
其中，两个表的关联字段为申请单号。
1）查询身份证号为440401430103082的申请日期。
2）查询同一个身份证号码有两条以上记录的身份证号码及记录个数。
3）将身份证号码为440401430103082的记录在两个表中的申请状态均改为07。 
4）删除g_cardapplydetail表中所有姓李的记录。
模拟数据：考试做这种题目最重要的是要冷静下来，只有静下来SQL才能写好。要模拟数据。看到数据SQL就好写了。
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680105543048-1dd227b9-f2e8-4daf-8b1b-155db36db813.png#averageHue=%23e4eaef&clientId=uaa2e6f21-7481-4&from=paste&height=434&id=uc9094a08&originHeight=434&originWidth=1027&originalType=binary&ratio=1&rotation=0&showTitle=false&size=10053&status=done&style=shadow&taskId=u69af6e14-873e-4d37-bf9f-8090081fc11&title=&width=1027)
1）查询身份证号为440401430103082的申请日期。
bigint转date，可以使用from_unixtime函数。
```sql
select a.g_applydate from g_cardapply a join g_cardapplydetail b on a.g_applyno = b.g_applyno where b.g_idcard = '440401430103082'
```
2）查询同一个身份证号码有两条以上记录的身份证号码及记录个数。
```sql
select count(g_idcard),g_idcard from g_cardapplydetail group by g_idcard having count(g_idcard) >= 2
```
3）将身份证号码为440401430103082的记录在两个表中的申请状态均改为07。
```sql
UPDATE 
	g_cardapply
JOIN 
	g_cardapplydetail 
ON 
	g_cardapply.g_applyno = g_cardapplydetail.g_applyno 
AND
	g_cardapplydetail.g_idcard = '440401430103082'
SET g_cardapply.g_state = '07',
g_cardapplydetail.g_state = '07'
```
4）删除g_cardapplydetail表中所有姓李的记录。
```sql
delete t1,t2 from g_cardapply t1 join g_cardapplydetail t2 on t1.g_applyno=t2.g_applyno where t2.g_name like '李%';
```
## 第三题
![面试题3.jpg](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680142491993-8e350bec-9af7-4304-b7d6-92f2f313997e.jpeg#averageHue=%23a59f9a&clientId=uc0287a15-0bb5-4&from=paste&height=1136&id=u22aaff9c&originHeight=1136&originWidth=852&originalType=binary&ratio=1&rotation=0&showTitle=false&size=71883&status=done&style=shadow&taskId=u55012cef-437e-448d-8cc9-d45d69e6cbe&title=&width=852)
![面试题5.jpg](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680142491981-3d90f70c-a859-4937-bdb7-60988985ea54.jpeg#averageHue=%239c9691&clientId=uc0287a15-0bb5-4&from=paste&height=1136&id=SqUCT&originHeight=1136&originWidth=852&originalType=binary&ratio=1&rotation=0&showTitle=false&size=66386&status=done&style=shadow&taskId=u1d4c868e-fd06-437f-b678-0dc4870d944&title=&width=852)
表名：stuscore
1）统计如下：课程不及格[0~59]的多少个，良[60~80]多少个，优[81-100]多少个。
2）计算科科及格的人的平均成绩。
## 第四题
![QQ图片20151126234632.jpg](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680144969653-7096e822-b1e5-44d4-bc34-55dacc9322b4.jpeg?x-oss-process=image/auto-orient,1#averageHue=%23c1c3be&clientId=uc0287a15-0bb5-4&from=paste&height=1136&id=u9a38f7f2&originHeight=1136&originWidth=852&originalType=binary&ratio=1&rotation=0&showTitle=false&size=80491&status=done&style=shadow&taskId=udaf33971-93f4-47eb-aaf8-2c246beec8b&title=&width=852)
1）请用一条SQL语句查询出不同部门中担任“钳工”的职工平均工资。
2）请用一条SQL语句查询出不同部门中担任“钳工”的职工平均工资高于2000的部门。
## 第五题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680398222140-816dc325-2887-46aa-96ba-57b6f1c52c25.png#averageHue=%238b8f8e&clientId=u170b2320-f065-4&from=paste&height=460&id=ucad96633&originHeight=460&originWidth=1221&originalType=binary&ratio=1&rotation=0&showTitle=false&size=226374&status=done&style=shadow&taskId=uc063bf61-cb24-4b98-ad3d-ddb2222fa62&title=&width=1221)
Employee是雇员信息表：
雇员姓名（主键）：person-name
街道：street
城市：city
Company是公司信息表：
公司名称（主键）：company-name
城市：city
Works是雇员工作信息表：
雇员姓名（主键）：person-name
公司名称：company-name
年薪：salary
Manages是雇员工作关系表：
雇员姓名（主键）：person-name
经理姓名：manager-name
模拟数据：
员工表：employee
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680402378306-a5369a92-0751-468b-8ef2-2e65aee24d31.png#averageHue=%23f6f4f3&clientId=u170b2320-f065-4&from=paste&height=266&id=ufe13588e&originHeight=266&originWidth=333&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13936&status=done&style=shadow&taskId=uf127c7fa-aa8a-48cb-b32c-eb68c2e0d1f&title=&width=333)
公司表：company
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680402457539-3684d5f1-8e7e-470b-95f7-56b3d48e4cee.png#averageHue=%23dab674&clientId=u170b2320-f065-4&from=paste&height=112&id=u3dddee1e&originHeight=112&originWidth=349&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4687&status=done&style=shadow&taskId=u91f1036e-127c-4b16-a5b1-b79ca7a55cb&title=&width=349)
雇员工作信息表：Works
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680402493037-5384139c-9959-4e34-8ce8-d0be11ea4563.png#averageHue=%23f8f7f5&clientId=u170b2320-f065-4&from=paste&height=274&id=u49603cde&originHeight=274&originWidth=440&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13746&status=done&style=shadow&taskId=u536e509d-d220-49d9-afe8-e8c265f9aa8&title=&width=440)
雇员工作关系表：Manages
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680402526039-fe04bfb3-e33b-4cbb-bc94-f680f0ae2a8e.png#averageHue=%23f9f9f8&clientId=u170b2320-f065-4&from=paste&height=265&id=uf9a3f0d7&originHeight=265&originWidth=311&originalType=binary&ratio=1&rotation=0&showTitle=false&size=8183&status=done&style=shadow&taskId=u487349a5-5eeb-43e5-8753-1e37c60eca7&title=&width=311)

请给出下面每一个查询的SQL语句：

1. 找出所有居住地与工作的公司在同一城市的员工的姓名。
2. 找出比Small Bank Corporation的所有员工收入都高的所有员工的姓名。
3. 找出平均年薪在10000美元以上的公司及其平均年薪。
## 第六题
![IMG_1621.JPG](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680399293078-ccb0ac3b-7273-4308-8f01-12705c3ed1fd.jpeg#averageHue=%23969a98&clientId=u170b2320-f065-4&from=paste&height=1280&id=u2b567848&originHeight=1280&originWidth=768&originalType=binary&ratio=1&rotation=0&showTitle=false&size=47870&status=done&style=shadow&taskId=u96afa047-24e4-47e0-b852-a0cca055f51&title=&width=768)![IMG_1616.JPG](https://cdn.nlark.com/yuque/0/2023/jpeg/21376908/1680399293094-1a4ca298-63ad-48db-9e8b-27ce4a6846a2.jpeg#averageHue=%2388868c&clientId=u170b2320-f065-4&from=paste&height=768&id=u5a98a01b&originHeight=768&originWidth=1280&originalType=binary&ratio=1&rotation=0&showTitle=false&size=41934&status=done&style=shadow&taskId=u2b8b1cba-0a2f-487e-966a-9ddd6d32e5b&title=&width=1280)
客户表Client
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680399899003-07e5e8a6-78d4-4939-b914-bf9280dcc3eb.png#averageHue=%23f2f0ee&clientId=u170b2320-f065-4&from=paste&height=185&id=u038cbc02&originHeight=185&originWidth=389&originalType=binary&ratio=1&rotation=0&showTitle=false&size=13762&status=done&style=shadow&taskId=ud65f66b7-4ffc-4fdf-af31-a7e7ea4e872&title=&width=389)
订单表Order
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680400992647-08ba0bcf-1ff6-45c7-a82e-3918a9f9e950.png#averageHue=%23fbfaf9&clientId=u170b2320-f065-4&from=paste&height=208&id=uab01aaf9&originHeight=208&originWidth=244&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4140&status=done&style=shadow&taskId=ue1ebe17e-18ee-4fc4-b5a4-f6193b774b9&title=&width=244)
客户订单表ClientOrder
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680400979869-ea2a1837-751b-4744-98a5-e04c9808b568.png#averageHue=%23fbfaf9&clientId=u170b2320-f065-4&from=paste&height=211&id=ud9ab36c4&originHeight=211&originWidth=223&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3731&status=done&style=shadow&taskId=ub22f900e-39a8-459b-9e78-cb15fa4fed4&title=&width=223)
图书表Book
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680401007501-200e3826-48ed-4638-8095-7be52757bdf1.png#averageHue=%23f5f3f1&clientId=u170b2320-f065-4&from=paste&height=131&id=u364c289b&originHeight=131&originWidth=320&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7145&status=done&style=shadow&taskId=u790fb5ee-03be-4efd-aa17-6f70cf09106&title=&width=320)

1. 请写出一条SQL语句，查询出每个客户的所有订单并按照地址排序，要求输出格式为：address client_name phone order_id
2. 请写出一条SQL语句，查询出每个客户订购的图书总价。要求输出格式为：client_name total_price
3. 如果要求每个订单可以包含多种图书，应该如何修改Order表的主键？为了保证每个订单只被一个客户拥有，应该在ClientOrder表上增加怎样的约束？
## 第七题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680403317776-7cd6d3bc-b547-4d94-9521-186a89ab67df.png#averageHue=%23afafa9&clientId=u170b2320-f065-4&from=paste&height=505&id=uc9118435&originHeight=505&originWidth=665&originalType=binary&ratio=1&rotation=0&showTitle=false&size=207077&status=done&style=shadow&taskId=uc5e6c887-ea47-4872-a5f6-b36d3aa2b8b&title=&width=665)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680403354657-0faf25ca-bb17-44ea-ade0-8a4e386756f3.png#averageHue=%23cfcec7&clientId=u170b2320-f065-4&from=paste&height=367&id=u9dbd6b45&originHeight=367&originWidth=744&originalType=binary&ratio=1&rotation=0&showTitle=false&size=108642&status=done&style=shadow&taskId=u9ec2ce66-95d7-4dce-a926-f781ad60236&title=&width=744)
模拟数据：
学生表：student
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680405687756-49b16a32-1f8b-42b5-b4a3-cd8c231e79f0.png#averageHue=%23f6f5f4&clientId=ucbeccebf-714c-4&from=paste&height=128&id=uf6f677b4&originHeight=128&originWidth=323&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5058&status=done&style=shadow&taskId=u94b42f3c-0e0a-431b-a8dd-5f00291873a&title=&width=323)
课程表：course
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680405700061-a86b3354-1d10-4be5-96fe-63ba01c8d7b4.png#averageHue=%23f9f8f7&clientId=ucbeccebf-714c-4&from=paste&height=124&id=udbbec214&originHeight=124&originWidth=268&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4188&status=done&style=shadow&taskId=u0c263cf1-ed36-4356-bbed-7a7af2c520a&title=&width=268)
成绩表：sc
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680405996312-907e4929-7d55-4d62-9e8d-1281bdafe91a.png#averageHue=%23fbfbfa&clientId=ucbeccebf-714c-4&from=paste&height=337&id=uf86bf234&originHeight=337&originWidth=291&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7772&status=done&style=shadow&taskId=u704f40c5-1d25-4641-8565-6d3da624398&title=&width=291)
教师表：teacher
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680406005728-731d61b6-02a6-448d-8a66-000b0aa3a9e6.png#averageHue=%23d8b571&clientId=ucbeccebf-714c-4&from=paste&height=92&id=u506eaf98&originHeight=92&originWidth=197&originalType=binary&ratio=1&rotation=0&showTitle=false&size=1920&status=done&style=shadow&taskId=u357535c2-7d55-4cb7-b7c7-95439dea833&title=&width=197)

1. 查询1号课比2号课成绩高的所有学生学号。
2. 查询平均成绩大于60分的学号和平均成绩。
3. 查询所有学生学号、姓名、选课数、总成绩。
4. 查询姓“李”的老师的个数。
5. 查询没学过“叶平”老师课的学号、姓名。
## 第八题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680403650729-b44beed8-c599-4077-8f43-8f862b94bfcd.png#averageHue=%239c9b98&clientId=u170b2320-f065-4&from=paste&height=591&id=DrAUb&originHeight=591&originWidth=603&originalType=binary&ratio=1&rotation=0&showTitle=false&size=153164&status=done&style=shadow&taskId=uc128e8d0-6f55-4639-ac54-76e70d093f6&title=&width=603)
学生表：student
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680406785079-9ec12300-6db8-48b8-ad77-7d64ebcf4292.png#averageHue=%23f7f6f5&clientId=ucbeccebf-714c-4&from=paste&height=130&id=uf5187384&originHeight=130&originWidth=195&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3024&status=done&style=shadow&taskId=uc537588f-10dd-49d1-a430-9d7acff4a7d&title=&width=195)
课程表：class
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680406801984-082cd575-80cc-432e-9c19-c247c194fa40.png#averageHue=%23faf9f8&clientId=ucbeccebf-714c-4&from=paste&height=116&id=ub01fb31c&originHeight=116&originWidth=220&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2858&status=done&style=shadow&taskId=u459c368e-0955-44ae-9c9f-d5d651392ae&title=&width=220)
选课表：chosen_class
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680406813282-256975bc-ab6c-49f9-8d83-e5f60d2a00ed.png#averageHue=%23faf9f8&clientId=ucbeccebf-714c-4&from=paste&height=200&id=u4ba72e6a&originHeight=200&originWidth=340&originalType=binary&ratio=1&rotation=0&showTitle=false&size=5464&status=done&style=shadow&taskId=u9afb016e-e693-452b-966b-4e45c9b7191&title=&width=340)

1. 没有选修课程编号为C1的学生姓名
2. 列出每门课程名称和平均成绩，并按照成绩排序
3. 选了2门课以上的学生姓名。
## 第九题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680403903386-c1b30b13-93ed-4b1a-a331-e4107c17d411.png#averageHue=%239f9ea3&clientId=u170b2320-f065-4&from=paste&height=460&id=uc48a45dc&originHeight=460&originWidth=556&originalType=binary&ratio=1&rotation=0&showTitle=false&size=171582&status=done&style=shadow&taskId=ue743e685-010a-4d7d-88d4-fb389bafa94&title=&width=556)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688106505123-a5edeb3b-0cdb-4ee3-befd-4a462fccbddd.png#averageHue=%23f6f4f3&clientId=u5ffc187d-9c9e-4&from=paste&height=275&id=u5ecb421a&originHeight=275&originWidth=461&originalType=binary&ratio=1&rotation=0&showTitle=false&size=17297&status=done&style=shadow&taskId=uc5832d94-4aea-449c-a8e5-af7238887f0&title=&width=461)
要转换成：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688106694493-9f831520-223c-4904-963a-3df0a7edb66a.png#averageHue=%23ca9c57&clientId=u5ffc187d-9c9e-4&from=paste&height=82&id=u6c20837f&originHeight=82&originWidth=391&originalType=binary&ratio=1&rotation=0&showTitle=false&size=3574&status=done&style=shadow&taskId=uf2fa2d09-dc7d-4be0-bdc8-c9f4d5e4ef5&title=&width=391)

### MySQL行转列

MySQL行转列又叫做**数据透视**。什么叫做行转列？将原本横向排列的数据透视成纵向排列的数据，进而进行计算、分析、展示等操作。

假设有一个学生选课成绩表，包含学生姓名（stu_name）、课程名称（course_name）和分数（score）三个字段。在原始数据中，每个学生在不同的课程中都有自己的得分情况，数据样例如下：

| stu_name | course_name | score |
| --- | --- | --- |
| 张三 | 数学 | 80 |
| 张三 | 英语 | 85 |
| 张三 | 历史 | 90 |
| 李四 | 数学 | 75 |
| 李四 | 英语 | 92 |
| 李四 | 历史 | 85 |
| 王五 | 数学 | 88 |
| 王五 | 英语 | 90 |
| 王五 | 历史 | 95 |


可以使用行转列操作，将每个学生在不同课程中的分数拆分成多条记录，每条记录包含一个课程以及对应的分数。转换后的数据样例如下：

| stu_name | 数学 | 英语 | 历史 |
| --- | --- | --- | --- |
| 张三 | 80 | 85 | 90 |
| 李四 | 75 | 92 | 85 |
| 王五 | 88 | 90 | 95 |


从上表中可以看出，在行转列之后，每一行记录都表示了一个学生在不同课程中的分数。这样更便于对不同科目的分数进行比较、计算平均值等分析操作。

#### 使用case when+group by完成
```sql
drop table if exists t_student;
create table t_student(
  stu_name varchar(10),
  course_name varchar(10),
  score int
);
insert into t_student(stu_name, course_name, score) values('张三', '数学', 80);
insert into t_student(stu_name, course_name, score) values('张三', '英语', 85);
insert into t_student(stu_name, course_name, score) values('张三', '历史', 90);
insert into t_student(stu_name, course_name, score) values('李四', '数学', 75);
insert into t_student(stu_name, course_name, score) values('李四', '英语', 92);
insert into t_student(stu_name, course_name, score) values('李四', '历史', 85);
insert into t_student(stu_name, course_name, score) values('王五', '数学', 88);
insert into t_student(stu_name, course_name, score) values('王五', '英语', 90);
insert into t_student(stu_name, course_name, score) values('王五', '历史', 95);
commit;
select * from t_student;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688106054073-451f919c-a97a-4c49-af03-991c86d78107.png#averageHue=%23f5f3f2&clientId=u5ffc187d-9c9e-4&from=paste&height=297&id=u9e9bf1f5&originHeight=297&originWidth=362&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16318&status=done&style=shadow&taskId=u17210bc5-00ed-4815-96ea-db8ea540918&title=&width=362)
行转列后的效果是：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688106114109-3c583e45-5324-47f7-b53c-f90e31dcdc82.png#averageHue=%23d8ad68&clientId=u5ffc187d-9c9e-4&from=paste&height=107&id=u69df24d2&originHeight=107&originWidth=337&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4879&status=done&style=shadow&taskId=u712979ed-c054-40d3-97fe-a85e23959e9&title=&width=337)
sql如下：
```sql
select
	stu_name,
	max(case course_name when '数学' then score else 0 end) as '数学',
	max(case course_name when '英语' then score else 0 end) as '英语', 
	max(case course_name when '历史' then score else 0 end) as '历史' 
from 
	t_student
group by 
	stu_name;
```

通过以上内容的学习，我们这个面试题就迎刃而解了：
```sql
select
	year,
	max(case season when '一季度' then count else 0 end) as '一季度',
	max(case season when '二季度' then count else 0 end) as '二季度',
	max(case season when '三季度' then count else 0 end) as '三季度',
	max(case season when '四季度' then count else 0 end) as '四季度'
from 
	t_temp 
group by 
	year;
```
#### 
## 第十题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1680403550525-8f28573a-a583-4aaa-9e91-b5dde5ffa2f3.png#averageHue=%23909092&clientId=u170b2320-f065-4&from=paste&height=424&id=YlEzc&originHeight=424&originWidth=578&originalType=binary&ratio=1&rotation=0&showTitle=false&size=224946&status=done&style=shadow&taskId=uce0f516b-9d95-40ed-bd7a-e9dfc0c9591&title=&width=578)
```sql
select 
	x.a 开始数字, y.a 结束数字
from 
	(select m.a,row_number() over(order by m.a) as rownum from (select a, lag(a) over(order by a asc) as pre_a from t) m where m.a - m.pre_a != 1 or m.pre_a is null) x 
join 
	(select n.a,row_number() over(order by n.a) as rownum from (select a, lead(a) over(order by a asc) as next_a from t) n where n.next_a - n.a != 1 or n.next_a is null) y 
on 
	x.rownum = y.rownum;
```
解答上面这个题目需要具备以下知识点：

- lag函数
- lead函数
- row_number函数

**lag函数**：获取当前行的上一行数据
```sql
select empno,ename,sal,(lag(sal) over(order by sal asc)) as pre_sal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688354808296-69cf1cf1-34e3-4b99-b4a2-2c575b0e2378.png#averageHue=%23d8a762&clientId=ub653133f-848a-4&from=paste&height=344&id=u978c2e7e&originHeight=344&originWidth=327&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16336&status=done&style=shadow&taskId=u52f42846-9936-4b59-9c02-e28399e5d6b&title=&width=327)
注意：over函数用来指定“在.....范围内”，通常和lag函数联用。

**lead函数**：获取当前行的下一行数据
```sql
select empno,ename,sal,(lead(sal) over(order by sal asc)) as next_sal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688355552758-57bb77a0-65d4-4717-8410-35c1f6c13e0e.png#averageHue=%23d7a864&clientId=ub653133f-848a-4&from=paste&height=343&id=u0d08f238&originHeight=343&originWidth=329&originalType=binary&ratio=1&rotation=0&showTitle=false&size=16211&status=done&style=shadow&taskId=u50f77934-4edb-48ad-bf11-7d04a74c054&title=&width=329)
注意：over函数用来指定“在.....范围内”，通常和lead函数联用。

**row_number函数**：可以为查询结果集生成行号：
```sql
select empno,ename,sal,row_number() over(order by sal) as rownum from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688372778734-b8b7d759-d86d-43d5-807a-8447c8de7da4.png#averageHue=%23d7a763&clientId=ub653133f-848a-4&from=paste&height=339&id=u33ad221d&originHeight=339&originWidth=321&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15785&status=done&style=shadow&taskId=ue2446e9a-2f9b-477d-ac3d-9750607746e&title=&width=321)

利用row_number函数，将两个不相关的列拼接在一起显示：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688372898512-55c19a9b-401d-49db-8ad3-10e64b2fc161.png#averageHue=%23f5f4f4&clientId=ub653133f-848a-4&from=paste&height=157&id=u7722567c&originHeight=157&originWidth=320&originalType=binary&ratio=1&rotation=0&showTitle=false&size=6920&status=done&style=shadow&taskId=ueb29a45f-3cd8-425f-abe2-44a5d1f2562&title=&width=320)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688372915619-8c9bb2e9-7023-43e7-88f1-ca17090825f0.png#averageHue=%23f5f4f3&clientId=ub653133f-848a-4&from=paste&height=162&id=uec70c452&originHeight=162&originWidth=320&originalType=binary&ratio=1&rotation=0&showTitle=false&size=7053&status=done&style=shadow&taskId=u1451081a-dda0-4561-a99e-c924529106b&title=&width=320)
```sql
select 
	x.a, y.b 
from 
	(select a,row_number() over(order by a) as rownum from t1) x 
join 
	(select b,row_number() over(order by b) as rownum from t2) y 
on 
	x.rownum = y.rownum;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688373063344-4437fa76-e5b6-4747-b189-9c3ae2ace4c0.png#averageHue=%23d0a25e&clientId=ub653133f-848a-4&from=paste&height=97&id=udf41357f&originHeight=97&originWidth=169&originalType=binary&ratio=1&rotation=0&showTitle=false&size=1520&status=done&style=shadow&taskId=u538f43c4-e174-4c86-bd55-b7ee900cf9f&title=&width=169)

CTE语法（公用表表达式）：Common Table Expression。创建临时表的一种语法：
```sql
-- 查询每个部门平均工资的工资等级
-- 第一种写法
select 
	t.deptno,t.avgsal,s.grade 
from 
	(select deptno,avg(sal) as avgsal from emp group by deptno) t 
join 
	salgrade s 
on 
	t.avgsal between s.losal and s.hisal;

-- 第二种写法：使用CTE语法
with cte_exp as(select deptno,avg(sal) as avgsal from emp group by deptno)
select 
	cte_exp.deptno,cte_exp.avgsal,s.grade
from
	cte_exp
join
	salgrade s
on
	cte_exp.avgsal between s.losal and s.hisal;
```

partition by：将数据分区，和group by区别是：group by是分组，然后和分组函数一起用。partition by分区不需要和分组函数一起使用
```sql
select deptno, empno,ename,sal,(lag(sal) over(partition by deptno order by sal asc)) as pre_sal from emp;
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1688355470071-e5e90e50-2b69-4126-bd79-a2118fb80e66.png#averageHue=%23f7f5f1&clientId=ub653133f-848a-4&from=paste&height=346&id=u1ce2bd86&originHeight=346&originWidth=421&originalType=binary&ratio=1&rotation=0&showTitle=false&size=20420&status=done&style=shadow&taskId=uf20a1c61-b9cb-47d4-a110-070aa47ecc4&title=&width=421)

MySQL 8.0及以上版本中支持如下常用的窗口函数：

1. ROW_NUMBER()：排名函数，返回当前结果集中每个行的行号；
2. RANK()：排名函数，计算分组结果中的排名，相同的行排名相同且没有空缺，下一个行排名跳过空缺；
3. DENSE_RANK()：排名函数，计算分组结果中的排名，相同的行排名相同，排名连续，没有空缺；
4. NTILE()：将分组结果等分为指定的组数，计算每组的大小；
5. LAG()：返回分组内前一行的值；
6. LEAD()：返回分组内后一行的值；
7. FIRST_VALUE()：返回分组内第一个值；
8. LAST_VALUE()：返回分组内最后一个值；
9. AVG()、SUM()、COUNT()、MIN()、MAX()：聚合函数，可以配合OVER()进行窗口操作。

需要注意的是，MySQL的窗口函数和其他DBMS中的窗口函数相比较，可能略有不同，需要根据MySQL的文档进行使用。 
# 十二、存储过程
## 1. 什么是存储过程？
存储过程可称为过程化SQL语言，是在普通SQL语句的基础上增加了编程语言的特点，把数据操作语句(DML)和查询语句(DQL)组织在过程化代码中，通过逻辑判断、循环等操作实现复杂计算的程序语言。
换句话说，存储过程其实就是数据库内置的一种编程语言，这种编程语言也有自己的变量、if语句、循环语句等。在一个存储过程中可以将多条SQL语句以逻辑代码的方式将其串联起来，执行这个存储过程就是将这些SQL语句按照一定的逻辑去执行，所以一个存储过程也可以看做是一组为了完成特定功能的SQL 语句集。
每一个存储过程都是一个数据库对象，就像table和view一样，存储在数据库当中，一次编译永久有效。并且每一个存储过程都有自己的名字。客户端程序通过存储过程的名字来调用存储过程。
在数据量特别庞大的情况下利用存储过程能达到倍速的效率提升。 
## 2. 存储过程的优点和缺点？
优点：速度快。

      - 降低了**应用服务器**和**数据库服务器**之间网络通讯的开销。尤其在数据量庞大的情况下效果显著。

缺点：移植性差。编写难度大。维护性差。

      - 每一个数据库都有自己的存储过程的语法规则，这种语法规则不是通用的。一旦使用了存储过程，则数据库产品很难更换，例如：编写了mysql的存储过程，这段代码只能在mysql中运行，无法在oracle数据库中运行。
      - 对于数据库存储过程这种语法来说，没有专业的IDE工具（集成开发环境），所以编码速度较低。自然维护的成本也会较高。

在实际开发中，存储过程还是很少使用的。只有在系统遇到了性能瓶颈，在进行优化的时候，对于大数量的应用来说，可以考虑使用一些。
## 3. 第一个存储过程
### 存储过程的创建
```plsql
create procedure p1()
begin
	select empno,ename from emp;
end;
```
### 存储过程的调用
```plsql
call p1();
```
### 存储过程的查看
```plsql
show create procedure p1;
```
```sql
select * from information_schema.routines where routine_name = 'p1';
```
information_schema.ROUTINES 是 MySQL 数据库中一个系统表，存储了所有存储过程和函数的详细信息，包括它们的名称、类型、定义文件、创建时间、修改时间等。这个系统表的信息是基于当前连接到的 MySQL 服务器上的所有数据库。
information_schema.ROUTINES 表中的一些重要的列包括：

- ROUTINE_SCHEMA：存储过程或函数所在的数据库名称。
- ROUTINE_NAME：存储过程或函数的名称。
- ROUTINE_TYPE：存储过程或函数的类型，可以是 PROCEDURE 或 FUNCTION。
- ROUTINE_DEFINITION：存储过程或函数的定义语句。
- CREATED：存储过程或函数的创建时间。
- LAST_ALTERED：存储过程或函数的最后修改时间。

通过查询 information_schema.ROUTINES，可以获取存储过程和函数的详细元数据信息，并对它们进行管理和维护。比如，可以使用该表来获取数据库中所有的存储过程和函数，并查找特定的对象，以便对它们进行修改或删除。
需要注意的是，information_schema.ROUTINES 表中的信息是只读的，不允许直接更新数据。如果需要修改存储过程或函数，需要使用 ALTER PROCEDURE 或 ALTER FUNCTION 等语句进行修改。
### 存储过程的删除
```plsql
drop procedure if exists p1;
```
### delimiter命令
在 MySQL 中，`delimiter` 命令用于改变 MySQL 解释语句的定界符。MySQL 默认使用分号 `;` 作为语句的定界符。而使用 `delimiter` 命令可以将分号 `;` 更改为其他字符，从而可以在 SQL 语句中使用分号 `;`。

例如，假设需要创建一个存储过程。在存储过程中通常会包括多条 SQL 语句，而这些语句都需要以分号 `;` 结尾。但默认情况下，执行到第一条语句的分号 `;` 后，MySQL 就会停止解释，导致后续的语句无法执行。解决方式就是使用 `delimiter` 命令将分号改为其他字符，使分号 `;` 不再是语句定界符。例如：

```sql
delimiter //

CREATE PROCEDURE my_proc ()
BEGIN
SELECT * FROM my_table;
INSERT INTO my_table (col1, col2) VALUES ('value1', 'value2');
END //

delimiter ;
```

在这个例子中，我们使用 `delimiter //` 命令将定界符改为两个斜线 `//`。在存储过程中，以分号 `;` 结尾的语句不再被解释为语句的结束。而使用 `delimiter ;` 可以将分号恢复为语句定界符。

总之，`delimiter` 命令可以改变 MySQL 数据库系统中 SQL 查询语句的分隔符，从而可使一条 SQL 查询语句包含多个 SQL 语句。这样的话，就方便了我们在一个语句里面加入多个语句，而且不会被错

## 4. 变量
mysql中的变量包括：系统变量、用户变量、局部变量。
### 系统变量
MySQL 系统变量是指在 MySQL 服务器运行时控制其行为的参数。这些变量可以被设置为特定的值来改变服务器的默认设置，以满足不同的需求。
MySQL 系统变量可以具有全局（global）或会话（session）作用域。全局作用域是指对所有连接和所有数据库都适用；会话作用域是指只对当前连接和当前数据库适用。

查看系统变量
```sql
show [global|session] variables;

show [global|session] variables like '';

select @@[global|session.]系统变量名;
```
注意：没有指定session或global时，默认是session。

设置系统变量
```sql
set [global | session] 系统变量名 = 值;

set @@[global | session.]系统变量名 = 值;
```
注意：无论是全局设置还是会话设置，当mysql服务重启之后，之前配置都会失效。可以通过修改MySQL根目录下的my.ini配置文件达到永久修改的效果。（my.ini是MySQL数据库默认的系统级配置文件，默认是不存在的，需要新建，并参考一些资料进行配置。）

### 用户变量
用户自定义的变量。只在当前会话有效。所有的用户变量'@'开始。

给用户变量赋值
```sql
set @name = 'jackson';
set @age := 30;
set @gender := '男', @addr := '北京大兴区';
select @email := 'jackson@123.com';
select sal into @sal from emp where ename ='SMITH';
```

读取用户变量的值
```sql
select @name, @age, @gender, @addr, @email, @sal;
```
注意：mysql中变量不需要声明。直接赋值就行。如果没有声明变量，直接读取该变量，返回null

### 局部变量
在存储过程中可以使用局部变量。使用declare声明。在begin和end之间有效。

变量的声明
```sql
declare 变量名 数据类型 [default ...];
```
变量的数据类型就是表字段的数据类型，例如：int、bigint、char、varchar、date、time、datetime等。
**注意：declare通常出现在begin end之间的开始部分。**

变量的赋值
```sql
set 变量名 = 值;
set 变量名 := 值;
select 字段名 into 变量名 from 表名 ...;
```

例如：以下程序演示局部变量的声明、赋值、读取：
```sql
create procedure p2()
begin
	declare emp_count varchar default 0;
	select count(*) into emp_count from emp;
	select emp_count;
end;
```
```sql
call p2();
```

## 5. if语句
语法格式：
```sql
if 条件 then
......
elseif 条件 then
......
elseif 条件 then
......
else
......
end if
```

案例：员工月薪sal，超过10000的属于“高收入”，6000到10000的属于“中收入”，少于6000的属于“低收入”。
```sql
create procedure p3()
begin
	declare sal int default 5000;
	declare grade varchar(20);
	if sal > 10000 then
  	set grade := '高收入';
	elseif sal >= 6000 then
  	set grade := '中收入';
	else
  	set grade := '低收入';
	end if;
	select grade;
end;
```
```sql
call p3();
```

## 6. 参数
存储过程的参数包括三种形式：

- in：入参（未指定时，默认是in）
- out：出参
- inout：既是入参，又是出参

案例：员工月薪sal，超过10000的属于“高收入”，6000到10000的属于“中收入”，少于6000的属于“低收入”。
```sql
create procedure p4(in sal int, out grade varchar(20))
begin
	if sal > 10000 then
  	set grade := '高收入';
	elseif sal >= 6000 then
  	set grade := '中收入';
	else
  	set grade := '低收入';
	end if;
end;
```
```sql
call p4(5000, @grade);
select @grade;
```

案例：将传入的工资sal上调10%
```sql
create procedure p5(inout sal int)
begin
	set sal := sal * 1.1;
end;
```
```sql
set @sal := 10000;
call p5(@sal);
select @sal;
```

## 7. case语句
语法格式：
```sql
case 值
	when 值1 then
	......
	when 值2 then
	......
	when 值3 then
	......
	else
	......
end case;
```
```sql
case
	when 条件1 then
	......
	when 条件2 then
	......
	when 条件3 then
	......
	else
	......
end case;
```

案例：根据不同月份，输出不同的季节。3 4 5月份春季。6 7 8月份夏季。9 10 11月份秋季。12 1 2 冬季。其他非法。
```sql
create procedure mypro(in month int, out result varchar(100))
begin 
	case month
		when 3 then set result := '春季';
		when 4 then set result := '春季';
		when 5 then set result := '春季';
		when 6 then set result := '夏季';
		when 7 then set result := '夏季';
		when 8 then set result := '夏季';
		when 9 then set result := '秋季';
		when 10 then set result := '秋季';
		when 11 then set result := '秋季';
		when 12 then set result := '冬季';
		when 1 then set result := '冬季';
		when 2 then set result := '冬季';
		else set result := '非法月份';
	end case;
end;
```
```sql
create procedure mypro(in month int, out result varchar(100))
begin 
	case 
		when month = 3 or month = 4 or month = 5 then 
			set result := '春季';
		when  month = 6 or month = 7 or month = 8  then 
			set result := '夏季';
		when  month = 9 or month = 10 or month = 11  then 
			set result := '秋季';
		when  month = 12 or month = 1 or month = 2  then 
			set result := '冬季';
		else 
			set result := '非法月份';
	end case;
end;
```
```sql
call mypro(9, @season);
select @season;
```

## 8. while循环
语法格式：
```sql
while 条件 do
	循环体;
end while;
```

案例：传入一个数字n，计算1~n中所有偶数的和。
```sql
create procedure mypro(in n int)
begin
	declare sum int default 0;
	while n > 0 do
  	if n % 2 = 0 then
    	set sum := sum + n;
  	end if;
  	set n := n - 1;
	end while;
	select sum;
end;
```
```sql
call mypro(10);
```

## 9. repeat循环
语法格式：
```sql
repeat
	循环体;
	until 条件
end repeat;
```
注意：条件成立时结束循环。

案例：传入一个数字n，计算1~n中所有偶数的和。
```sql
create procedure mypro(in n int, out sum int)
begin 
	set sum := 0;
	repeat 
		if n % 2 = 0 then 
		  set sum := sum + n;
		end if;
		set n := n - 1;
		until n <= 0
	end repeat;
end;
```
```sql
call mypro(10, @sum);
select @sum;
```

## 10. loop循环
语法格式：
```sql
create procedure mypro()
begin 
	declare i int default 0;
  mylp:loop 
		set i := i + 1;
		if i = 5 then 
			leave mylp;
		end if;
		select i;
	end loop;
end;
```
```sql
create procedure mypro()
begin 
	declare i int default 0;
  mylp:loop 
		set i := i + 1;
		if i = 5 then 
			iterate mylp;
		end if;
		if i = 10 then 
		  leave mylp;
		end if;
		select i;
	end loop;
end;
```

## 11. 游标cursor
游标（cursor）可以理解为一个指向结果集中某条记录的指针，允许程序逐一访问结果集中的每条记录，并对其进行逐行操作和处理。

使用游标时，需要在存储过程或函数中定义一个游标变量，并通过 `DECLARE` 语句进行声明和初始化。然后，使用 `OPEN` 语句打开游标，使用 `FETCH` 语句逐行获取游标指向的记录，并进行处理。最后，使用 `CLOSE` 语句关闭游标，释放相关资源。游标可以大大地提高数据库查询的灵活性和效率。

声明游标的语法：
```sql
declare 游标名称 cursor for 查询语句;
```
打开游标的语法：
```sql
open 游标名称;
```
通过游标取数据的语法：
```sql
fetch 游标名称 into 变量[,变量,变量......]
```
关闭游标的语法：
```sql
close 游标名称;
```

案例：从dept表查询部门编号和部门名，创建一张新表dept2，将查询结果插入到新表中。
```plsql
drop procedure if exists mypro;

create procedure mypro()
begin 

	declare no int;
	declare name varchar(100);
	declare dept_cursor cursor for select deptno,dname from dept;

	drop table if exists dept2;
	create table dept2(
		no int primary key,
		name varchar(100)
	);
	
	open dept_cursor;
	
	while true do
		fetch dept_cursor into no, name;
		insert into dept2(no,name) values(no,name);
	end while;
	
	close dept_cursor;
end;

call mypro();
```
执行结果：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687222276547-6381cff6-311f-40a0-984c-0a79f6954a50.png#averageHue=%23fbfaf9&clientId=ua8e0f13a-20b6-4&from=paste&height=78&id=u0eb9a0cb&originHeight=78&originWidth=392&originalType=binary&ratio=1&rotation=0&showTitle=false&size=1792&status=done&style=shadow&taskId=u26df3d97-46f1-47c0-b98c-64e8715dea4&title=&width=392)
出现了异常：异常信息中显示没有数据了。这是因为while true循环导致的。

不过虽然出现了异常，但是表创建成功了，数据也插入成功了：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687222354577-99ea5bb0-40c8-4bca-9a9a-605894b195bb.png#averageHue=%23f4f3f2&clientId=ua8e0f13a-20b6-4&from=paste&height=243&id=u5e8d1f82&originHeight=243&originWidth=360&originalType=binary&ratio=1&rotation=0&showTitle=false&size=12923&status=done&style=shadow&taskId=u4100f2d2-0b52-4976-8711-96d5e9ab89d&title=&width=360)
**注意：声明局部变量和声明游标有顺序要求，局部变量的声明需要在游标声明之前完成。**

## 12. 捕捉异常并处理
语法格式：
```plsql
DECLARE handler_name HANDLER FOR condition_value action_statement
```

1. handler_name 表示异常处理程序的名称，重要取值包括：
   1. CONTINUE：发生异常后，程序不会终止，会正常执行后续的过程。
   2. EXIT：发生异常后，终止存储过程的执行。
2. condition_value 是指捕获的异常，重要取值包括：
   1. SQLSTATE sqlstate_value，例如：SQLSTATE 01130
   2. SQLWARNING，代表所有01开头的SQLSTATE
   3. NOT FOUND，代表所有02开头的SQLSTATE
   4. SQLEXCEPTION，代表除了01和02开头的所有SQLSTATE
3. action_statement 是指异常发生时执行的语句，例如：close cursor

给之前的游标添加异常处理机制：
```plsql
drop procedure if exists mypro;

create procedure mypro()
begin 

	declare no int;
	declare name varchar(100);
	declare dept_cursor cursor for select deptno,dname from dept;

	declare exit handler for not found close dept_cursor;

	drop table if exists dept2;
	create table dept2(
		no int primary key,
		name varchar(100)
	);
	
	open dept_cursor;
	
	while true do
		fetch dept_cursor into no, name;
		insert into dept2(no,name) values(no,name);
	end while;
	
	close dept_cursor;
end;

call mypro();
```

## 13. 存储函数
存储函数：带返回值的存储过程。参数只允许是in。没有out，也没有inout。不写默认就是in参数。
语法格式：
```plsql
CREATE FUNCTION 存储函数名称(参数列表)
RETURNS 数据类型 [特征]
BEGIN
	--函数体
	RETURN ...;
END;
```

“特征”的可取重要值如下：

- deterministic：用该特征标记该函数为确定性函数（什么是确定性函数？每次调用函数时传同一个参数的时候，返回值都是固定的）。这是一种优化策略，这种情况下整个函数体的执行就会省略了，直接返回之前缓存的结果，来提高函数的执行效率。
- no sql：用该特征标记该函数执行过程中不会查询数据库，如果确实没有查询语句建议使用。告诉 MySQL 优化器不需要考虑使用查询缓存和优化器缓存来优化这个函数，这样就可以避免不必要的查询消耗产生，从而提高性能。
- reads sql data：用该特征标记该函数会进行查询操作，告诉 MySQL 优化器这个函数需要查询数据库的数据，可以使用查询缓存来缓存结果，从而提高查询性能；同时 MySQL 还会针对该函数的查询进行优化器缓存处理。

案例：计算1~n的所有偶数之和
```plsql
-- 删除函数
drop function if exists sum_fun;

-- 创建函数
create function sum_fun(n int)
returns int deterministic 
begin 
	declare result int default 0;
	while n > 0 do 
		if n % 2 = 0 then 
			set result := result + n;
		end if;
		set n := n - 1;
	end while;
	return result;
end;

-- 调用函数
set @result = sum_fun(100);
select @result;
```

## 14. 触发器
MySQL 触发器是一种数据库对象，它是与表相关联的特殊程序。它可以在特定的数据操作（例如插入（INSERT）、更新（UPDATE）或删除（DELETE））触发时自动执行。MySQL 触发器使数据库开发人员能够在数据的不同状态之间维护一致性和完整性，并且可以为特定的数据库表自动执行操作。

触发器的作用主要有以下几个方面：

1.  强制实施业务规则：触发器可以帮助确保数据表中的业务规则得到强制执行，例如检查插入或更新的数据是否符合某些规则。 
2.  数据审计：触发器可以声明在执行数据修改时自动记日志或审计数据变化的操作，使数据对数据库管理员和 SQL 审计人员更易于追踪和审计。 
3.  执行特定业务操作：触发器可以自动执行特定的业务操作，例如计算数据行的总数、计算平均值或总和等。 

MySQL 触发器分为两种类型: BEFORE 和 AFTER。BEFORE 触发器在执行 INSERT、UPDATE、DELETE 语句之前执行，而 AFTER 触发器在执行 INSERT、UPDATE、DELETE 语句之后执行。

创建触发器的语法如下：

```plsql
CREATE TRIGGER trigger_name
BEFORE/AFTER INSERT/UPDATE/DELETE ON table_name
FOR EACH ROW
BEGIN
-- 触发器执行的 SQL 语句
END;
```

其中：

- trigger_name：触发器的名称
- BEFORE/AFTER：触发器的类型，可以是 BEFORE 或者 AFTER
- INSERT/UPDATE/DELETE：触发器所监控的 DML 调用类型
- table_name：触发器所绑定的表名
- FOR EACH ROW：表示触发器在每行受到 DML 的影响之后都会执行
- 触发器执行的 SQL 语句：该语句会在触发器被触发时执行

需要注意的是，触发器是一种高级的数据库功能，只有在必要的情况下才应该使用，例如在需要实施强制性业务规则时。过多的触发器和复杂的触发器逻辑可能会影响查询性能和扩展性。

**关于触发器的NEW和OLD关键字：**
在 MySQL 触发器中，NEW 和 OLD 是两个特殊的关键字，用于引用在触发器中受到修改的行的新值和旧值。具体而言：

- NEW：在触发 INSERT 或 UPDATE 操作期间，NEW 用于引用将要插入或更新到表中的新行的值。
- OLD：在触发 UPDATE 或 DELETE 操作期间，OLD 用于引用更新或删除之前在表中的旧行的值。

通俗的讲，NEW 是指触发器执行的操作所要插入或更新到当前行中的新数据；而 OLD 则是指当前行在触发器执行前原本的数据。

在MySQL 触发器中，NEW 和 OLD 使用方法是相似的。在触发器中，可以像引用表的其他列一样引用 NEW 和 OLD。例如，可以使用 OLD.column_name 从旧行中引用列值，也可以使用 NEW.column_name 从新行中引用列值。

示例：

假设有一个名为 my_table 的表，其中包含一个名为 quantity 的列。当在该表上执行 UPDATE 操作时，以下触发器会将旧值 OLD.quantity 累加到新值 NEW.quantity 中：

```plsql
CREATE TRIGGER my_trigger
BEFORE UPDATE ON my_table
FOR EACH ROW
BEGIN
SET NEW.quantity = NEW.quantity + OLD.quantity;
END;
```

在此触发器中，OLD.quantity 引用原始行的 quantity 值（旧值），而 NEW.quantity 引用更新行的 quantity 值（新值）。在触发器执行期间，数据行的 quantity 值将设置为旧值加上新值。

需要注意的是，在使用 NEW 和 OLD 时，需要根据 DML 操作的类型进行判断，以确定哪个关键字表示新值，哪个关键字则表示旧值。

案例：当我们对dept表中的数据进行insert delete update的时候，请将这些操作记录到日志表当中，日志表如下：
```sql
drop table if exists oper_log;

create table oper_log(
  id bigint primary key auto_increment,
  table_name varchar(100) not null comment '操作的哪张表',
  oper_type varchar(100) not null comment '操作类型包括insert delete update',
  oper_time datetime not null comment '操作时间',
  oper_id bigint not null comment '操作的那行记录的id',
  oper_desc text comment '操作描述'
);
```

触发器1：向dept表中插入数据时，记录日志
```plsql
create trigger dept_trigger_insert 
after insert on dept
for each row
begin
	insert into oper_log(id,table_name,oper_type,oper_time,oper_id,oper_desc) values
(null,'dept','insert',now(),new.deptno,concat('插入数据：deptno=', new.deptno, ',dname=', new.dname,',loc=', new.loc));
end;
```

查看触发器：
```plsql
show triggers;
```

删除触发器：
```sql
drop trigger if exists dept_trigger_insert;
```

向dept表中插入一条记录：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687250537958-36fdd3ce-6aa3-48e9-aa34-39dac470c82f.png#averageHue=%23f2f0ed&clientId=ua8e0f13a-20b6-4&from=paste&height=254&id=u2d5b23b7&originHeight=254&originWidth=327&originalType=binary&ratio=1&rotation=0&showTitle=false&size=14090&status=done&style=shadow&taskId=u0b945c07-f0a0-4c61-b2e3-a27a514ddb8&title=&width=327)
日志表中多了一条记录：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687250572044-f7216711-ee12-49bf-b687-b21b7b5856cd.png#averageHue=%23f3f1f0&clientId=ua8e0f13a-20b6-4&from=paste&height=145&id=u94fbdc8c&originHeight=145&originWidth=1014&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15305&status=done&style=shadow&taskId=u7fad2861-b2e6-4220-af3e-0a22c454cf0&title=&width=1014)

触发器2：修改dept表中数据时，记录日志
```plsql
create trigger dept_trigger_update
after update on dept
for each row
begin
	insert into oper_log(id,table_name,oper_type,oper_time,oper_id,oper_desc) values
(null,'dept','update',now(),new.deptno,concat('更新前：deptno=', old.deptno, ',dname=', old.dname,',loc=', old.loc, 
                                              ',更新后：deptno=', new.deptno, ',dname=', new.dname,',loc=', new.loc));
end;
```
更新一条记录：
```sql
update dept set loc = '北京' where deptno = 60;
```
日志表中多了一条记录：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687250964502-f6af7d92-c4a5-4910-9efa-d08090647643.png#averageHue=%23f5f4f3&clientId=ua8e0f13a-20b6-4&from=paste&height=186&id=u505e3af3&originHeight=186&originWidth=1237&originalType=binary&ratio=1&rotation=0&showTitle=false&size=19556&status=done&style=shadow&taskId=u9ffa318a-67b1-477d-b3c7-851a438b483&title=&width=1237)
**注意：更新一条记录则对应一条日志。如果一次更新3条记录，那么日志表中插入3条记录。**

触发器3：删除dept表中数据时，记录日志
```plsql
create trigger dept_trigger_delete
after delete on dept
for each row
begin
	insert into oper_log(id,table_name,oper_type,oper_time,oper_id,oper_desc) values
(null,'dept','delete',now(),old.deptno,concat('删除了数据：deptno=', old.deptno, ',dname=', old.dname,',loc=', old.loc));
end;
```

删除一条记录：
```sql
delete from dept where deptno = 60;
```

日志表中多了一条记录：
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21376908/1687251196650-5527bf1a-370d-47c8-bf45-2b7babc5e1a5.png#averageHue=%23f4f3f1&clientId=ua8e0f13a-20b6-4&from=paste&height=186&id=u7fa2da22&originHeight=186&originWidth=1282&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22331&status=done&style=shadow&taskId=u82995139-6935-439b-b17e-5232b0195cf&title=&width=1282)

# 十三、存储引擎
	什么是存储引擎
	常见的存储引擎有哪些
	MySQL默认的存储引擎是什么
	常见存储引擎的优缺点及选用
# 十四、索引&SQL优化
	什么是索引，数据库表的索引有什么作用
	概述索引的实现原理
	索引的分类
	怎么创建和删除索引
	什么条件满足的时候添加索引
	导致索引失效的原因
