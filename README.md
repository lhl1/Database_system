# Database_system

**数据库要点**

[**第一章****........................................................................................** **1**](#_Toc518041621)

[**第二章****........................................................................................** **5**](#_Toc518041622)

[**第三章****........................................................................................** **6**](#_Toc518041623)

[**第四章****......................................................................................** **14**](#_Toc518041624)

[**第五章****......................................................................................** **16**](#_Toc518041625)

[**第六章****......................................................................................** **16**](#_Toc518041626)

[**第七章****......................................................................................** **17**](#_Toc518041627)

[**第八章****......................................................................................** **19**](#_Toc518041628)

[**第九章****......................................................................................** **19**](#_Toc518041629)

[**第十章****......................................................................................** **20**](#_Toc518041630)

[**第十一章****..................................................................................** **20**](#_Toc518041631)

 

# 第一章

·数据：描述事务的符号记录、数据库中存储的基本对象

·数据库：数据库是长期储存在计算机内、有组织的、可共享的大量数据的集合

  （数据库中的数据具有永久存储、有组织和可共享的特点）

  （数据库的核心是共享）

·数据库存储的是通用化的相关数据集合，它不仅包括数据本身，而是包括数据之间的联系（选择题）

·数据库系统（DBS）：由数据库、数据库管理系统、应用程序、数据库管理员组成的存储、管理、处理和维护数据的系统（即采用数据库技术的计算机系统）

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173557.gif?token=ANNFVK2SAOSCYXVKN6HKXC3A4AX3U)

​                 填空题                

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173558.jpg?token=ANNFVK2GT53L26TWPATX2XTA4AX3W)



![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173559.gif?token=ANNFVK4QGR2TDSRWL43YO2LA4AX34)

·数据库管理的三个阶段

  ①人工管理阶段

​    \* 数据不保存

​    \* 应用程序管理数据

​    \* 数据不共享

​    \* 数据不具有独立性

  ②文件系统阶段

​    \* 数据可以长期保存

​    \* 文件系统管理数据

​    \* 数据共享性差冗余度大

​    \* 数据独立性差

  ③数据库系统阶段（**简答题**）【数据库系统的特点】

​    \* 数据结构化

​      数据库系统实现整体数据的结构化，这是数据库主要特征之一，也是数     据库系统与文件系统的本质区别

​    \* 数据的共享性高、冗余度低、易扩充

​      数据共享可以大大减少数据冗余，节约存储空间。数据共享还能够避免    数据之间的不相容性与不一致性

​    \* 数据独立性高

​      数据独立性包括物理独立性和逻辑独立性

​    \* 数据由数据库管理系统统一管理和控制

​    （a.数据的安全性保护 

​     b.数据的完整性检查

​     c.并发控制

​     d.数据库恢复）

·数据模型【数据库系统的核心和基础】

  数据模型通常由数据结构、数据操作和数据的完整性约束条件三部分组成

  (

​    \* 数据结构：数据结构描述数据库的组成对象以及对象之间的联系

​    \* 数据操作：数据操作是指对数据库中各种对象的实例允许执行的操作集    合，包括操作及有关的操作规则

​    \* 数据的完整性约束条件是一组完整性规则

  )

  **数据模型分类**

  \* 第一类：概念模型（常用E-R图描述）

​    \- E-R图（实体-联系方法）

  \* 第二类是逻辑模型和物理模型

  \* 主要的逻辑数据模型：

​    ①层次模型

​      1、条件

​       （1）有且只有一个结点没有双亲结点，这个结点称为根节点

​       （2）根以外的其他结点有且只有一个双亲结点

​      2、特点：任何一个给定的记录值只能按其层次路径查看，没有一个子       女记录值能够脱离双亲记录值而独立存在。（子女结点与双亲        结点的联系是唯一的）

​      3、数据操纵：查询、插入、删除和更新

​      4、优点：

​         a.数据结构比较简单清晰

​         b.层次数据库的查询效率高

​         c.提供了良好的完整性支持

​    ②网状模型（代表：DBTG系统，又称CODASYL系统）

​      1、条件

​       （1）允许有一个以上的结点无双亲

​       （2）一个结点可以有多余一个的双亲

​      2、子女结点与双亲结点的联系可以不唯一

【层次模型和网状模型统称为格式化模型（非关系模型）】 （注：考1分:两者特点）

​    ③关系模型（**优缺点**）

1、数据结构

​       （1）关系：一个关系对应通常说的一张表

​       （2）元组：表中的一行即为一个元组

​       （3）属性：表中的一列即为一个属性

​       （4）码：表中的某个属性组，可以唯一确定一个元组

​       （5）域：一组具有相同数据类型的值的集合

​       （6）分量：元组中的一个属性值（每个分量不可分）

2、关系模型中的数据操作是集合操作

3、优点

 （1）与格式化模型不同，它是建立在严格的数学概念的基础上的

 （2）关系模型的概念单一

 （3）存取路径对用户透明

4、缺点：查询效率往往不如格式化数据模型，增加了开发数据库管理系统的难度

​    ④面向对象数据模型

​    ⑤对象关系数据模型

​    ⑥半结构化数据模型

·数据模型中有“型”（type）和“值”（value）的概念

·数据库系统的三级模式结构：外模式+模式+内模式

​              \* 模式（也称逻辑模式）：是所有用户的公共数据视图、是数据库中全体数据的逻辑结构和特征的描述（一个数据库只有一个模式）

  \* 外模式（子模式、用户模式）：模式的子集（一个数据库可以有多个外模式）

​       是保证数据库安全性的一个有力措施。

  \* 内模式（存储模式）：是数据在数据库内部的组织方式

​      （一个数据库只有一个内模式）

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173600.gif?token=ANNFVK3G53KFD6DROE5PD33A4AX4A)

 

· 数据库的二级印像

\* 模式/外模式映像，保证了数据与程序的逻辑独立性，简称数据的逻辑独立性。

  \* 模式/内模式映像，保证了数据与程序的物理独立性，简称数据的物理独立性。（唯一的）

# 第二章

·Eg：班级ID（需要一致性高的，以创建实体类解决）

·域：域是一组具有相同数据类型的值的集合 （{0,1}，{男，女}）

·某一属性组的值能唯一地标识一个元组，而子集不能了，则称该属性组为候选码

  \* 候选码的诸属性称为主属性，不包含在任何候选码中的属性称为非主属性或非码属性

  \* 最极端的情况下，关系模式的所有属性是这个关系模式的候选码，称为全码

·关系

  关系可以有三种类型：基本关系（基本表、基表）、查询表、视图表

​    \* 基本关系的性质

​      （1）列是同质的，即每一列中的分量是用一个类型的数据，来自同一          个域

​      （2）不用列可出自同一个域

​      （3）列的顺序可以任意交换

​      （4）任意两个元组的候选码不能取相同的值

​      （5）行的顺序可以任意交换

​      （6）分量必须取原子值，即每一个分量都不可分

​    规范的最基本的一条就是：关系的每一个分量必须是一个不可分的数据项

  关系的描述称为关系模型，可以形式化地表示为R（U，D，DOM，F）

​    \* R（U，D，DOM，F）

​      R：关系名

​      U：组成该关系的属性名集合

​      D**：**U中属性所来自的域

​      DOM：属性向域的映像集合

​      F：属性间数据的依赖关系集合

·结构化查询语言SQL

·基本关系操作：选择、投影、并、差、笛卡尔积

·关系完整性：实体完整性、参照完整性、用户定义完整性

（其中实体完整性和参照完整性是关系模型必须满足的完整性约束条件，被称作是关系的两个不变性，用户定义的完整性是引用领域需要遵循的约束条件，体现了具体领域中的语义约束）

·**关系代数（例题P56）必考**

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173601.jpg?token=ANNFVKZRSXAPEKVYX7I6DN3A4AX4G)

·悬浮元组：在表与表进行连接的时候，被舍弃的元组

·外连接：把悬浮元组也保存在结果关系中，而在其他属性上填空值（NULL）

  \* 保留左边关系的悬浮元组叫做左外连接（左边都在）

  \* 保留右边关系的悬浮元组叫做右外连接（右边都在）

·所有关系集合构成一个关系数据库

# 第三章

·非关系模型（层次模型、网状模型）的数据语言

  \* 模式数据定义语言（模式DDL）

  \* 外模式数据定义语言（外模式DDL或子模式DDL）

  \* 数据存储有关的描述语言（DSDL）

  \* 数据操纵语言（DML）

·

| **SQL****功能** | **动词**               |
| --------------- | ---------------------- |
| 数据查询        | select                 |
| 数据定义        | create、drop、alter    |
| 数据操纵        | insert、update、delete |
| 数据控制        | grant、revoke          |

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173602.jpg?token=ANNFVK4W4747FMYFAXR2OQTA4AX4I)

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173603.jpg?token=ANNFVK5QDWEY3UA2MB3ZMV3A4AX4K)

  \* 定义模式 create schema <模式名> authorization <用户名>;

​    (必须是有权限才能创建)

​    删除模式 drop schema <模式名><cascade|restrict>

​      \- cascade(级联)：模式中所有数据库对象全部删除

​      \- restrict(限制)：只有模式中没有任何下属的对象才能执行删除语句

  \* **定义表** create table <表名> (<列名><数据类型>[列级完整性约束],…，                [表级完整性约束])

​       Eg: create table sc(

​              id int not null AUTO_INCREMENT,

​              sno char(4) not null ,

​              cno char(4)not null comment‘xxx’,

​              grade int default 0,

​              primary key(sno,cno),

​              foreign key(sno) references student(sno),

​              foreign key(sno) references student(sno),

​                  );

  \* 修改基本表alter table<表名>

​         [add [column] <新列名><数据类型> [完整性约束]]

​         [add <表级完整性约束>]

​         [drop [column] <列名> [cascade|restrict]]  

​         [drop constraint<完整性约束名>[cascade|restrict]]

​         [alter column <列名><数据类型>];

  \* 删除基本表drop table<表名>[cascade|restrict];(默认restrict)

**![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173604.jpg?token=ANNFVK5RPXWC5KRJOAOOCZLA4AX4O)**

  模式与表

​    每一个基本表都属于某一个模式，一个模式包含多个基本表

​      \- 在表名中明显地给出模式名(create table `xxx`.student(…);)

​      \- 在创建模式语句中同时创建表(create…<用户名> create table…)

​      \- 设置所属的模式，这样在创建表时不必给出模式名

  \* 建立索引 create [unique] [cluster] index<索引名> 

​       on <表名>(<列名>[<次序>],[,<列名>[<次序>]]…); 

​      Eg: create unique index stusno on student(sno);

  \* 修改索引 alter index<旧索引名> rename to <新索引名>;

  \* 删除索引 drop index <索引名>;

·数据查询

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173605.gif?token=ANNFVK5FD4RLM3LSBWBAL4TA4AX4Q)![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173606.gif?token=ANNFVK5DD7AM7MJEY5C5PNLA4AX4Q)![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173607.gif?token=ANNFVK2IR5DUAON7EVT6NBDA4AX4S)![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173608.jpg?token=ANNFVK4UC4JBCOLKIXO3W7DA4AX4U)

  \- distinct (去重复)

  \- group by (分组|不能用where，只能用having)

  \- order by xxx asc|desc (排序|asc默认升序)

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173609.gif?token=ANNFVK2ETTOAGWF3WFKP67LA4AX4Y)

PS:空值一定要用is null 或者is not null判断

\* 模糊匹配

  [not] like ‘<匹配串>’ [escape‘<换码字符>’]

  \- ‘%’ 代表任意长度

  \- ‘_’ 代表任意单个字符

  Eg: 

​    ① … where name like ‘_梓%’;(第二个字为梓)

​    ② … where id like ‘student\_id’ escape‘\’; (student_id)

·聚集函数

  \* count(*)             统计元组个数

  \* count([distinct|all]<列名>)    统计一列中值的个数

  \* sum([distinct|all]<列名>)     计算一列值的总和（必须为数值）

  \* avg([distinct|all]<列名>)     计算一列值的平均值（必须是数值）

  \* max([distinct|all]<列名>)     求一列值中的最大值

  \* min([distinct|all]<列名>)     求一列值中的最小值

PS: 

  ①当遇到空值null时，除了count(*)外，都跳过空值而只处理非空值

  ② where子句不能使用聚集函数作为条件表达式，select子句和group by中的 having子句可以使用

·当连接运算符为 = 时，为等值连接，使用其他运算称为非等值连接

·相关子查询和不相关子查询

  \* 不相关子查询：子查询的查询条件不依赖父查询

  \* 相关子查询：子查询条件依赖于父查询

​    Eg：相关子查询例子

​      select Sno,Cno 

​      from **SC x**

​      where Grade >= (

​             select avg(Grade) from SC y where **y.Sno=x.Sno**);

·带有 ANY（SOME） 或 ALL 谓词的子查询

  \* >/< ANY     大于/小于 子查询结果中的某个值

  \* >/< ALL     大于/小于 子查询结果中的所有值

  \* = ANY       值

  \* = ALL      等于子查询结果中的所有值（通常没有实际意义）

  \* !=(或<>) ANY   不等于子查询中的某个值

  \* !=(或<>)ALL   不等于子查询结果中的任何一个值

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173610.jpg?token=ANNFVKYVGG3IJRO4W7BPMGDA4AX42)

·exists（只产生逻辑值，不返回任何数据）

  \* 查询结果非空，则返回true

PS：书P111例[3.63]

·集合查询

  \* union(并操作)

  \* intersect(交操作)

  \* except(差操作)

​    Eg：

​      select * from sc where cno=‘1’;

​      union

​      select * from sc where cno=‘2’;

**·SQL的特点**（**简答题**）

  SQL可以分为数据定义、数据查询、数据更新、数据控制四大部分

  ①综合统一：SQL集数据定义语言、操纵语言和控制语言的功能于一体，语言风格统一，可以独立完成数据库生命周期中的全部活动

  ②高度非过程化：存取路径的选择以及SQL的操作过程由系统自动完成

  ③面向集合的操作方式：面向集合的操作方式是元组的集合，操纵对象、查找结果、插入、删除、更新操纵的对象可以是元组的集合

  ④同一种语法结果提供多种使用方式：SQL即是嵌入式语言，又是独立的语言

  ⑤语言简洁，易学易用：SQL功能强大，语言简洁，完成核心功能只用了9个动词

·插入语句

  \* insert into <表名>([属性名],[…],[…],…) values(xxx,xxx,xxx,…)；

  \* insert into <表名>([新列名],…) select xxx,… from 表 wehre …;

·更新语句

  \* update <表名> set <列名>=<表达式>[,<列名>=<表达式>]… where…;

·删除语句

  \* delete from <表名> where …;

·空值的处理

  \* 空值与另一个值（包括一个空值）的算术运算的结果为**空值**

  \* 空值与另一个值（包括一个空值）的比较运算结果为**UNKNOWN**

**![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173611.jpg?token=ANNFVK72SJ23XLVIEVE3RBLA4AX44)**

**·P115 ！**

# 第四章

·三类计算机系统安全性问题：技术安全类、管理安全类、政策法律类

·数据库管理系统提供的安全措施主要包括：用户身份鉴别、存取控制、视图等

·从四个方面描述安全性级别划分的指标：安全策略、责任、保证、文档

·TCSEC/TDI的安全级别划分：A1、B3、B2、B1、C2、C1、D

·用户身份鉴别：静态口令鉴别、动态口令鉴别、生物特征鉴别、智能卡鉴别

·数据库管理系统安全性控制模型

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173612.jpg?token=ANNFVK5KAFIP7ECD3DKEBUTA4AX5C)

·用户权限由两个要素组成：数据库对象和操作类型

·**存取控制机制**主要包括定义用户权限和合法权限检查

  \* C2级的数据库管理系统支持自主存取控制（DAC）

  \* B1级的数据库管理系统支持强制存取控制（MAC）

·在数据库系统中，定义存取权限称为授权

  \* 存取控制的对象不仅有数据本身（数据、属性列上的数据），还有数据库模式 （包括数据库、基本表、视图、索引）

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173613.jpg?token=ANNFVK6K6CH4ZKUMPM3NFU3A4AX5G)

·授权与收回

  \* GRANT（grant）

​    GRANT <权限>[,<权限>]…

​    ON <对象类型><对象名>,[<对象类型><对象名>]…

​    TO<用户>[,<用户>]…

​    [WITH GRANT OPTION]; 

​    // 获得某种权限的用户还可以把这种权限再授予其他用户

​    // 接受权限的用户可以是一个或多个具体用户，也可以PUBLIC（全体用户）

​      Eg：

​       ①grant select on table Student to U1;

​         //把查询Student表的权限授给用户U1

​       ②grant all privileges on table Student to U1;

​         //把Student表的所有权限都给U1

​       ③grant update(Sno),select on table Student to public with        grant option;

​         //把Student表的select权限和对属性列Sno的update权限       //给所有用户，并且所有用户可以给其他用户传播此权限

​         //利用有向图不能形成闭环，避免循环授权

  \* REVOKE（revoke）

​    REVOKE <权限> [,<权限>]…

​    ON <对象类型><对象名>[,<对象类型><对象名>]…

​    FROM <用户>[,<用户>]… [cascade|restrict];

​      Eg:

​       ①revoke insert on table SC from public;

​       ②revoke insert on table SC from U5 cascade;

·创建角色

  \* CREATE ROLE<角色名>;

·给角色授权

  \* GRANT <角色>[,<角色>]… ON <对象类型>对象名… TO<角色>[,<角色>];

·将一个角色授予其他的角色或用户

  \* GRANT <角色1>[,<角色2>]… TO <角色3>[,<用户1>]… [with admin option];

·P97例【3.43】、例【3.44】

·P98 例【3.45】

·P104 嵌套查询

# 第五章

·为维护数据库的完整性，数据库管理系统必须能实现如下功能：

  ***** 提供定义完整性约束条件的机制

  ***** 提供完整性检查的方法

  ***** 进行违约处理

·触发器：**实验6**

# 第六章

·**范式**：https://www.cnblogs.com/ulli/archive/2012/02/26/2367910.html

  \* 第零范式：第零范式就是指没有使用任何范式的设计

  \* 第一范式（1NF）：指表中的所有字段都是**原子的、不可再分**的

  \* 第二范式（2NF）：第二范式是满足属性对**主键是完全函数依赖**的（消除部分依赖）

  \* 第三范式（3NF）：第三范式是指在满足第二范式的情况下，消除表中的传递依赖

  \* BCNF：在3NF的基础上，表中任何字段对任一候选关键字段的传递函数依赖都不存在（消除主键到主键再到非主键的传递依赖关系）

·P185【例6.7】

# 第七章

·**数据库设计的特点**：

  \* 数据库建设的基本规律：三分技术、七分管理、十二分基础数据

  \* 结构（数据）设计和行为（处理）的设计相结合

·**数据库设计方法**：新奥尔良方法、基于E-R模型的设计方法、3NF的设计方法、面向对象的数据库设计方法、统一建模语言等

·数据库设计的基本步骤：

 ![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173614.jpg?token=ANNFVK4QAFNJ5LHF3WRE5TDA4AX5K)

  \* 需求分析阶段

  \* 概念结构设计阶段

  \* 逻辑结构设计阶段

  \* 物理结构设计阶段

  \* 数据库实施阶段

  \* 数据库运行和维护阶段

·需求分析

  \* 调查的重点是“数据”和“处理”，通过调查、收集与分析，获得用户对数据库的如下要求：

​    \- 信息要求

​    \- 处理要求

​    \- 安全性与完整性要求

·数据字典（产生在需求分析阶段）

  \* 它是关于数据库中数据的描述，即元数据，而不是数据本身。在数据库设计过程中不断修改、充实、完善

  \* 数据字典包括：

​    \- 数据项 ：数据项是不可再分的数据单元

​    \- 数据结构：数据结构反映了数据之间的组合关系

​    \- 数据流：数据流是数据结构在系统内传输的路径

​    \- 数据存储：数据存储是数据结构停留或保存的地方，也是数据流的来源    和去向之一

​    \- 处理过程：处理过程的具体处理逻辑一般用判定表或判定树来描述

# 第八章

·**将SQL语句查询数据库的结果交主语言处理，主要用主变量和游标实现**

·**P247 游标**

·**P249**

  不使用游标的SQL语句：说明性语句、数据定义语句、数据控制语句、查询结果为单记录的select语句、非current形式的增删改语句

·**P251**

  使用游标的SQL语句：查询结果为多条记录的select语句、current形式的update和delete语句

·存储过程的优点：

  ***** 运行效率高

  ***** 存储过程降低了客户机和服务器之间的通行量

  ***** 方便实施企业规则

# 第九章

·关系数据库管理系统查询处理的**4**个阶段：查询分析、查询检查、查询优化、查询执行

  \* 查询分析：对查询语句进行扫描、词法分析和语法分析

  \* 查询检查：对合法的查询语句进行语义检查，根据数据字典中的用户权 限和完整性约束定义对用户的存取权限进行检查

  \* 查询优化：选择一个高效执行的查询处理策略

  \* 查询执行：依据优化器得到的执行策略生成查询计划并执行语句

·**P282**

  ① 代数优化：有选择和连接操作时，应当先做选择操作

  ② 物理优化：采用索引连接代价也较少

# 第十章

**（通读一遍）**

·事务（恢复和并发控制的基本单位）

  所谓事务是用户定义的一个数据库操作序列，这些操作要么全做，要么全不做，是一个不可分割的工作单位

·事务特性（ACID特性）：原子性、一致性、隔离性、持续性

·故障的种类：

  ① 事务内部的故障（这类恢复操作叫事务撤销）

  ② 系统故障（重做所有已提交的事务、软故障）

  ③ 介质故障（硬故障）

  ④ 计算机病毒

·恢复的实现技术

  \* 恢复操作的基本原理：冗余

  \* 恢复机制涉及的两个关键问题

​    \- 如何建立冗余数据（核心任务）

​    \- 如何利用这些冗余数据实施数据库恢复

  \* 建立冗余数据最常用的技术：数据转储、登记日志文件

·恢复策略：事务故障的恢复、系统故障的恢复、介质故障的恢复

# 第十一章

·并发控制概述

  \* 事务是并发控制的基本单位

  \* 为了保证书屋的隔离性和一致性

  \* 并发操作带来的不一致性包括：

​      ① **丢失修改**

​       （两个事务T1、T2同时读入数据并修改）

​      ② **不可重复读**

​       （

​         \- 事务T1读取数据后，事务T2执行更新操作，T1再次读该数        据时，得到不同的结果

​         \- 事务T1读取数据后，事务T2删除某些记录，T1再次读取发        现数据消失

​         \- 事务T1读取数据后，事务T2插入某些记录，T1再次读取发        现出现新数据

​         （后面两种不可重复读也称为幻影现象）

​       ） 

​      ③ **读“脏”数据**

​       （事务T1修改某一数据并写入磁盘，事务T2读取同一数据后，T1       由于某种原因被撤销，这时T1修改过的数据恢复原值，T2读到的        数据就与数据库中的数据不一致，即为读到“脏”数据）

**![img](https://raw.githubusercontent.com/lhl1/PicGo/master/20210703173615.jpg?token=ANNFVK2BMGVU5S2OBDIBAZLA4AX5O)**

·并发控制的主要技术有封锁、时间戳、乐观控制法、多版本并发控制等

·封锁

  \* 基本的封锁类型

​      \- 排他锁（X锁、写锁）

​      \- 共享锁（S锁、读锁）

·封锁协议（P313）

  ***** 一级封锁协议

​    \- 指事务T在修改数据R之前必须先对其加X锁，直到事务结束才释放

  ***** 二级封锁协议

​    \- 指在一级封锁协议基础上增加事务T在读取数据R之前必须先对其加S    锁，读完后即可释放S锁

  ***** 三级封锁协议

​    \- 指在一级封锁协议的基础上增加事务T在读取数据R之前必须先对其加S   锁，直到事务结束才释放

![img](https://raw.githubusercontent.com/lhl1/PicGo/master/clip_image036.jpg?token=ANNFVK2URLJLTOIFXMK6UKLA4AXPS)

·活锁和死锁（**什么情况、如何解决**）

  ***** **活锁**

​    \- 事务T1封锁数据R，事务T2又请求封锁R，事务T3也请求封锁R。当    T1释放了R上的封锁后，系统首先批准了T3的请求，以此类推，T2可能    永远在等待，这就是**活锁**

​    \- 避免活锁的简单方法就是采用先来先服务的策略

  ***** **死锁**

​    \- 事务T1在等待事务T2，而T2又在等待T1的局面，T1和T2两个事务永  远不能结束，形成**死锁**

   **-** **死锁的预防**

​     **① 一次封锁法：**要求每个事务必须一次将所有要使用的数据全部加锁

​     **② 顺序封锁法：**预先对数据对象规定一个封锁顺序，所有事务都按这      个顺序实施封锁

  ***** **死锁的诊断与解除**

   \- 一般使用超时法或事务等待图法

·并发调度的可串行性

  \* （可串行化调度）定义：多个事务并发执行是正确的，当且仅当其结果与按 某一次序串行地执行这些事务时的结果相同

  \* 可串行性是并发事务的正确调度准则，按这个准则规定，一个给定的并发调度，当且仅当它是可串行化的，才认为是正确调度

**—— RZK**
