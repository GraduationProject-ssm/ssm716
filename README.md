# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# ssm716基于web的山东红色旅游信息管理系统的设计与实现+jsp

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Tm8QeZE4a?p=113)


# 绪论
## 1.1研究背景
从古到今，信息的录入，存储，检索都受制于社会生产力的发展，不仅仅浪费大量的人力资源还需要浪费大量的社会物资，并且不能长时间的保留，信息检索随着时间的跨度呈几何级的难于检索，并且如果对有些数据进行核对校验或者分析统计，需要用到的时间还有人力更是不可估计。但是随着计算机网络的发展，这些事情都不再是痛点，计算机语言的发展就是对传统行业各个方面进行了变革，尤其是信息管理方面。比如计算机各个系列各种型号，多种适配，哪些零件可以与其他零件进行组合，哪些不可以，这些如果是传统行业会弄成好多本书籍进行记录，但是通过软件的信息录入整合，程序进行判断，可以有效的提升效率。在这样的背景下，各行各业都在梳理自己的信息管理流程和需求。本设计就是在这样的环境下，针对山东红色旅游设计的山东红色旅游信息管理系统，用来解决山东红色旅游信息管理问题的痛点和难点，让山东红色旅游信息管理变得更加高效节能。
## 1.2目的和意义
开发这套系统的目的，就是让不同的人员对不同的信息进行录入，查询，汇总，分析，让职责更明了，权限更清晰，职能更细致，响应更及时。能快速提升信息检索效率，只需要输入自己想要的条件进行查询汇总，就能及时的得到信息，能快速的应对市场反应提升各个部门的协作效率，信息的存储更加的安全，不在害怕水火，信息备份更简便，只需要设计数据库定时备份，定时迁移，数据存储和数据迁移的成本微乎其微。如果还用之前的信息管理模式，就会发现在市场上失去了竞争力，在同行业内失去了先进性，负担更重，前进更缓慢。使用更先进的互联网信息管理模式，数据可以及时的进行处理，可以根据数据处理结果进行更直观更明锐的判断，在提升自我竞争力的同时也能节能环保，为社会绿化人类的美好家园增加了贡献。
## 1.3论文结构安排
本文对山东红色旅游信息管理系统的设计开发过程分为7个部分进行介绍。其中包括绪论部分，系统开发技术部分，系统分析，设计，实现，测试都会作为一个章节进行说明。

第1章绪论：这部分是论文的开头，主要介绍系统的背景，介绍系统的开发意义。

第2章开发环境：这部分主要针对系统开发的环境进行说明，主要有工具介绍，数据库介绍等。

第3章系统分析：这部分主要还是根据用户的操作需要，分析系统功能，也会分析系统是否值得开发的可行性问题。

第4章系统设计：这部分是在功能分析的层面上，进行更深层次的分析，设计，最终的设计成果是数据库结构与E-R图的设计，和功能结构图的设计。

第5章系统实现：这部分是程序开发的重点，主要还是依靠过硬的编程知识实现系统的功能。

第6章系统测试：这部分主要还是检验程序的合格性，各项指标，比如功能，性能，界面等是否达标。

第7章结论：这部分主要总结设计工作，并对未来工作进行展望。
# 2 开发环境
## 2.1 Mysql数据库
MYSQL数据库是由瑞典的一家名称为MySQL-AB的公司开发出一款延续至今的关系型数据库，接着被数据库公司老大Oracle给收购了，之前好多人认为Oralce公司收购之后会雪藏，然后把道路让给Oracle公司的拳头产品也就是Oracle数据库，没想到的是Oracle公司后续支持mysql数据库让它成为了公司另一个拳头产品，与Oracle市场定位完全不同，使Oracle公司在数据库行业的市场占有率遥遥领先，发展的越来越好。

MYSQL数据库有自带的客户端管理工具，比如SQLYon，或者是native for mysql，或者是mysql-font，这些都是很友好的MySQL使用工具，可以视图化处理相关数据。虽然某些模块是收费的版本，但是作为课题来讲，免费功能是完全满足程序的需要，还有就是他的安装配置方面很简单，学习起来也是遵循于SQL语法的，网上也有充足的学习资料可以进行随时随地的学习，所以最终选择的数据库就是MYSQL数据库。
## 2.2 SSM框架
SSM框架，是Spring + Spring MVC + MyBatis的缩写，这个是继SSH之后，目前比较主流的Java EE企业级框架，适用于搭建各种大型的企业级应用系统。
## 2.3 IDEA 开发工具
IDEA 全称IntelliJ IDEA，是用于java语言开发的集成环境(也可用于其他语言)，IntelliJ在业界被公认为最好的java开发工具之一，尤其在智能代码助手、代码自动提示、重构、J2EE支持、Ant、JUnit、CVS整合、代码审查、 创新的GUI设计等方面的功能可以说是超常的。IDEA是JetBrains公司的产品，这家公司总部位于捷克共和国的首都布拉格，开发人员以严谨著称的东欧程序员为主。
## 2.4 JSP技术
JSP的全称是Java Server Pages，即Java的服务器页面。JSP的主要作用是代替Servlet程序回传HTML页面的数据。SP页面本质上是一个Servlet程序，第一次访问JSP页面时(运行Tomcat服务器后在浏览器地址栏输入路径)，Tomcat服务器会将此JSP页面翻译成为一个Java源文件，并对其进行编译成为.class字节码文件(一个.java，一个.class)。




# 3 系统分析
## 3.1系统可行性分析
在初步确定设计的课题之后，首先就需要对该课题的可行性问题进行思考，通常程序的开发是一个长期并对专业知识要求较高的任务。在决定制作之前，要进行充分的分析与考虑，对其进行可行性分析也是衡量程序的投入成本与产生的效益问题，假如投入成本远远大于产生的效益，那么此程序就可以不用进行制作了，只有当其产生的效益远远大于投入的成本时，并可以确定程序是可以制作出来，以及使用中并不存在操作困难的前提下，才可以将程序的开发提上议程。
### 3.1.1 时间可行性分析
首先此程序的制作主要是学院的统一安排，所以在时间上，学院给出的时间以及安排的各个时间节点对应的配套任务都可以保证程序的开发如期完成。也就是说只要跟随学院的时间安排进行设计制作作品，是可以完成开发任务的。
### 3.1.2 技术可行性分析
此程序是作为计算机专业学生的一个毕业答辩项目，它运用到的专业知识，大学期间，学校老师都已经讲授过，并且也在学习期间以及期末考核中，老师们安排了一些类似课程设计这样的作业，本人也通过这些作业进行了练习，也知晓程序的设计流程，也熟悉软件环境的安装，通过平时的实践，本人也具备一定的开发基础以及经验，并具备一定的学以致用的能力。因此，此程序开发在技术上准备充分，开发确实可行！
### 3.1.3 经济可行性分析
通过对程序制作中需要花费的资金进行分析，可以得出此程序无需考虑资金投入问题。首先程序制作涉及到软件以及硬件环境都有现成的资源，硬件环境就是一台可以上网的笔记本，也可以是学院的图书馆的机房里面的电脑，软件环境也能从各大浏览器进行下载安装，无论软件还是硬件上所需要的资源都不需要资金投入。对于程序完成制作之后，在使用者的使用期间，此程序还会节省人工成本，节省时间成本，并给使用者带来较客观的收益。
### 3.1.4 操作可行性分析
程序的各个操作功能都有对应的界面，每个功能界面都有相应的功能提示，比如导航条是每个程序必备的界面设置，点击程序的各个功能导航条，会进入相应的操作界面，从这个角度来看，可以得出的信息就是，该程序的操作逻辑并不复杂，就算生活中的普通用户操作该程序，也能根据程序里面的功能提示进行操作。因此，程序的运行使用是可以进行的。

总而言之，此程序从技术角度分析可以进行开发，从时间角度分析，预留时间完全够用，从操作角度分析，程序的操作难度较低，使用者可以顺利操作等，因此，程序也就可以投入人力与时间进行制作。
## 3.2系统性能分析
如何制作出一款性能优良的程序也是需要提前分析和考虑的，程序的性能首先要保证稳定性，主要是让使用者可以信赖程序。程序现有的功能需求是为了解决当前面临的问题，在此基础上，也需要把社会的进步，科技的发展考虑在内。多年以后，相信用户的需求就不仅仅是现在提出来的需求了，肯定会额外增加许多新的功能，因为在早期，由于用户需求还有程序开发者的技术水平的影响，早期的程序大都只是简单的增加，删除，以及数据更新等，并不存在数据的分析功能，比如数据统计等。然而，现在科学也在进步，开发技术也在迭代更新，开发者的开发经验以及开发技能也得到提升，程序具备的功能也是在同步更新，比如以前的程序，基本就是数据的增加，修改等功能，现在开发的程序都开始考虑对数据进行统计与分析的功能。因此，对于一般系统的开发或者对于旧系统的更新等，都需要涉及到升级，一个是性能上保持优越，另一个是功能上保持更加齐全等，这些都需要在原来的系统上进行改变，并达到升级的目的，所以，任何可开发程序都要模块化，也都要具备可扩展性，并且在进行程序功能扩展时，程序原本正常运行的功能可以继续使用，程序本身的整体结构保持原样。一个稳定性强，并可迭代升级的程序，在满足使用者日常操作需求的同时，也能更好应对当前时代的变化。
## 3.3系统流程分析
流程图更能反映程序处理信息的逻辑，本部分内容对程序的流程进行说明。

信息添加流程：程序里面的所有数据都是是操作者录入的数据，之所以可以成功录入这些数据，主要还是逻辑判断，判断输入的信息合理，程序数据库才会保存数据。

![](/md/blog.001.png)

图3.1 信息添加流程图

信息修改流程：程序里面的所有数据也是需要使用者不断检查的，当检查某个数据项的信息有错误，也能修改。所以程序设置的修改功能，主要还是帮助用户更高效地更正程序数据，保持数据的正确性与可用性。

![](/md/blog.002.png)

图3.2 信息修改流程图

信息查询流程：程序后台存放的数据很多，当用户需要某种信息时，不可能再去一行行寻找，所以查询功能的设置也是必要的，相应的程序查询流程（见下图）也是需要检验用户填写的查询条件的合理性与可靠性。

![](/md/blog.003.png)

图3.3 信息查询流程图

# 4 系统设计
程序的系统设计阶段任务比较重，需要具体设计程序功能，也需要设计存储数据的数据库。设计功能可以以功能结构图展示设计结果，设计数据库，可以以E-R图和表结构展示设计的数据库。
## 4.1系统功能结构设计
在使用用例图绘制管理员的功能之后，需要对管理员的功能进行更加细致的设计，也是为下阶段的系统实现做好准备。设计管理员的功能使用结构图展示（见下图）。管理员功能有个人中心，用户管理，景点类型管理，景点信息管理，门票购买管理，特产类型管理，产品商城管理，订单信息管理，天气预报管理，系统管理。

![](/md/blog.004.png)

图4.1 管理员功能结构图
## 4.2数据库设计
操作者使用程序，不管是信息添加，信息删除和查询等都是在处理和访问程序数据，程序的数据只会越来越多，所以一个专门保存数据的工具就显得很有必要。这个工具就是数据库，为了让所选数据库更好的服务于开发的程序，就要对这个数据库创建相应的数据库文件，并进行规则设计，让数据库在应对程序的各种数据处理请求时可以及时进行反馈。
### 4.2.1数据库E-R图
在分析出并设计好程序的相关功能之后，还有一个比较重要的设计任务，就是参照程序的功能设计出此程序的数据库，这部分内容设计到数据库实体的确定，主要是绘制其E-R图，也涉及到在数据库中创建表，完成表结构的具体设计。说到E-R图的绘制，市场上也有很多绘制其的软件，它们大都提供了E-R图的基本表示符号，所以通过鼠标的选择与拖拽就可以完成初步的绘制，由于使用习惯的问题，本人更加倾向于微软的Visio，对PowerDesigner建模工具，还有对比较受欢迎的Navicat等工具接触较少，为了如期提交作品，这里就不再花费额外的时间去学习一些E-R图的建模工具了，仅仅使用常用的，比较熟悉的Visio工具就行了。代表E-R图符号的有矩形，椭圆，菱形。它们分别表示不同的信息，第一种是矩形符号，绘制实体时选用，第二种是椭圆符号，专门代表矩形实体的属性，第三种是菱形符号，专门代表各个矩形实体当中的某种联系。

（1）此数据库设计了管理员实体，它对应的E-R图（见下图）需要使用Visio工具绘制。

![](/md/blog.005.png)

图4.7 管理员实体E-R图

（2）此数据库设计了用户实体，它对应的E-R图（见下图）需要使用Visio工具绘制。

![](/md/blog.006.png)

图4.8 用户实体E-R图

（3）此数据库设计了景点实体，它对应的E-R图（见下图）需要使用Visio工具绘制。

![](/md/blog.007.png)

图4.9 图书实体E-R图
### 4.2.2 数据库表结构
存储程序数据需要一定的规则进行，这样才可以确保后期在对数据库的数据进行使用时，可以使用一定的规则进行查询并显示出来。数据库里面的每个表的结构设计都是不一样的，但是都包含了字段名，字段对应的数据类型，以及数据类型的长度值等。每当设计好一个数据表结构时，在程序运行中，就会依照这样的表结构依次存储数据，所以在程序进行数据添加时，数据库中就会新增数据，程序进行数据更新时，数据库也是同步更新数据。程序执行删除功能时，也会在对应数据表中清除相应的数据。所以，每当使用者在执行功能时，都会在操作界面查看实时变化的数据，这些数据同样也是在数据库当中进行变化，最后会把数据库当中的已经发生变化的信息同步显示在程序操作界面。所以，数据表的结构的设计一定要多花时间进行思考。设计出最优秀的结构，可以减少数据冗余，让数据检索更快捷，让数据存储可以更方便，让程序的整体性能可以提升。

1公告信息表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|title|String|标题|是|
|4|introduction|String|简介|是|
|5|picture|String|图片|是|
|6|content|String|内容|是|
2景点类型表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|jingdianleixing|String|景点类型|是|
3天气预报表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|chengshi|String|城市|是|
|4|tianqi|String|天气|是|
|5|qiwen|String|气温|是|
|6|shidu|String|湿度|是|
|7|fengmian|String|封面|是|
|8|fengxiang|String|风向|是|
|9|fengsu|String|风速|是|
|10|bianhuatixing|String|变化提醒|是|
|11|gengxinshijian|datetime|更新时间|是|
4订单信息表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|dingdanbianhao|String|订单编号|是|
|4|techanmingcheng|String|特产名称|是|
|5|techanleixing|String|特产类型|是|
|6|jiage|float|价格|是|
|7|shuliang|Integer|数量|是|
|8|zongjiage|float|总价格|是|
|9|xiadanshijian|datetime|下单时间|是|
|10|yonghuming|String|用户名|是|
|11|xingming|String|姓名|是|
|12|shouji|String|手机|是|
|13|ispay|String|是否支付|是|
5景点信息表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|jingdianmingcheng|String|景点名称|是|
|4|jingdianleixing|String|景点类型|是|
|5|dengji|String|等级|是|
|6|tupian|String|图片|是|
|7|piaojia|Integer|票价|是|
|8|piaoshu|Integer|票数|是|
|9|chengshi|String|城市|是|
|10|kaifangshijian|String|开放时间|是|
|11|fuwudianhua|String|服务电话|是|
|12|xiangxidizhi|String|详细地址|是|
|13|jingdianjieshao|String|景点介绍|是|
6产品商城评论表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|refid|Integer|关联表id|是|
|4|userid|Integer|用户id|是|
|5|nickname|String|用户名|是|
|6|content|String|评论内容|是|
|7|reply|String|回复内容|是|
7收藏表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|userid|Integer|用户id|是|
|4|refid|Integer|收藏id|是|
|5|tablename|String|表名|是|
|6|name|String|收藏名称|是|
|7|picture|String|收藏图片|是|
|8|type|String|类型(1:收藏,21:赞,22:踩)|是|
|9|inteltype|String|推荐类型|是|
8用户表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|username|String|用户名|是|
|3|password|String|密码|是|
|4|role|String|角色|是|
|5|addtime|Date|新增时间|是|
9token表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|userid|Integer|用户id|是|
|3|username|String|用户名|是|
|4|tablename|String|表名|是|
|5|role|String|角色|是|
|6|token|String|密码|是|
|7|addtime|Date|新增时间|是|
|8|expiratedtime|Date|过期时间|是|
10特产类型表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|techanleixing|String|特产类型|是|
11门票购买表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|dingdanbianhao|String|订单编号|是|
|4|jingdianmingcheng|String|景点名称|是|
|5|jingdianleixing|String|景点类型|是|
|6|piaojia|String|票价|是|
|7|piaoshu|Integer|票数|是|
|8|zongjiage|Integer|总价格|是|
|9|goumairiqi|datetime|购买日期|是|
|10|yonghuming|String|用户名|是|
|11|xingming|String|姓名|是|
|12|shouji|String|手机|是|
|13|ispay|String|是否支付|是|
12用户表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|yonghuming|String|用户名|是|
|4|mima|String|密码|是|
|5|xingming|String|姓名|是|
|6|xingbie|String|性别|是|
|7|touxiang|String|头像|是|
|8|youxiang|String|邮箱|是|
|9|shouji|String|手机|是|
13景点信息评论表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|refid|Integer|关联表id|是|
|4|userid|Integer|用户id|是|
|5|nickname|String|用户名|是|
|6|content|String|评论内容|是|
|7|reply|String|回复内容|是|
14配置文件表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|name|String|配置参数名称|是|
|3|value|String|配置参数值|是|
15产品商城表

|序号|列名|数据类型|说明|允许空|
| :-: | :-: | :-: | :-: | :-: |
|1|Id|Int|id|否|
|2|addtime|Date|创建时间|是|
|3|techanmingcheng|String|特产名称|是|
|4|techanleixing|String|特产类型|是|
|5|tupian|String|图片|是|
|6|jiage|Integer|价格|是|
|7|shuliang|Integer|数量|是|
|8|techanjieshao|String|特产介绍|是|

# 5 系统实现
程序设计阶段的完成，就可以使用设计结果，比如功能结构的设计结果，数据库的设计结果来指导程序的开发内容，主要还是使用开发技术来实现程序功能。实现部分不仅包括了界面的布局与排版，也涉及到对功能的实现。
## 5.1管理员功能介绍
### 5.1.1用户信息管理模块
管理员可以查询和删除以及批量删除用户的注册信息。

![](/md/blog.008.png)

图5.1 用户信息管理模块页面
### 5.1.2 景点信息管理模块
管理员可以添加，修改，删除查询景点信息。

![](/md/blog.009.png)

图5.2 景点信息管理模块页面
### 5.1.3 产品商城管理模块
管理员可以添加，修改，删除，查询商城产品信息。

![](/md/blog.010.png)

图5.3 产品商城管理模块页面
### 5.1.4订单信息管理模块
管理员可以查看和搜索用户提交的产品订单信息。

![](/md/blog.011.png)

图5.4 订单信息管理模块页面
## 5.2 用户功能介绍
### 5.2.1景点信息模块
用户可以在景点信息里购票操作。

![](/md/blog.012.png)

图5.5 景点信息查询模块页面
### 5.2.2产品商城模块
用户可以在产品商城里面购买产品。

![](/md/blog.013.png)

图5.6 产品商城模块页面
### 5.2.3门票购买模块
用户可以在门票购买里面查看自己的订单，并且可以查询和支付。

![](/md/blog.014.png)

图5.7 门票购买模块页面
### 5.2.4订单信息模块
用户可以在订单信息里面查看购买的产品信息，并且可以进行支付操作。

![](/md/blog.015.png)

图5.8 订单信息模块页面


# 系统










