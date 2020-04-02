**以下是本Project的企划内容, 正在编辑中**

# A Project about Building a Forum about Competitive Programming

## 核心目的

构造一个相对质量较高且严格控制水分的关于算法竞赛的论坛

我们注意到, 当前OI领域的较为严肃的讨论很多都在各大Online Judge的用户群组中. 但是在这些群组中, 我们不可避免的会遇到包括但不限于以下的问题:

+ 多线并行, 需要脑内链接pthread
+ 不支持 $\LaTeX$ 公式, 需要脑内插件
+ 复读机
+ QQ在机房被ban(少见情况)
+ 难以定位潜在的回答者
+ 记录难以查阅

而各大Online Judge自带的讨论系统则不是功能过于简单就是有效讨论很少

为了解决上述问题, 我建立了一些系统来在一个Forum里实现严肃的CP讨论

## 核心系统

### 论坛功能

初步设想为设置以下板块

+ /p/ Problem 板块, 发布以特定题目为讨论中心的thread
+ /c/ Contest 板块, 发布以某场特定比赛为讨论中心的thread
+ /a/ Algorithm 板块, 发布以某个特定算法为讨论中心的thread
+ /t/ Tutorial 板块, 并不包含thread, 而是提供一个博文索引, 支持以赞同数量以及更新时间排序

### 索引功能

为了快速在可能海量的thread中找到所需信息, 初步设想为树状tag. 如:

添加tag `#P.UOJ.1 ` 之后, 搜索tag `#UOJ` 和 `#UOJ.1` 均可索引至此

又如tag `#A.BST.Splay` 表示Algorithm>Binary Search Tree>Splay Tree, 搜索链中任意一个tag均可检索到

### 关注提醒

为了能让问题快速传达给潜在的回答者, 用户可以绑定自己在各大OJ的用户, 然后系统会读取Accepted/Attempted题目并自动关注

同时用户也可以关注自己擅长/缺陷的算法tag以便第一时间收到该tag下的通知

### User Authorization System

这个系统是为了控制水分以及实现可持续化维护社区秩序而设计

#### Authorized User

类似于Wikipedia中的"自动确认用户", 我们对具有一定算法竞赛水平的用户进行auth并给予较高的公共编辑以及秩序维持权限.

我们注意到, 以社区活跃程度来衡量用户的算法竞赛以及社区维护能力是不充分的. 于是我们要求Authed User满足如下条件:

+ NOI系列赛中达到CCF程序设计水平Lv8+
+ Codeforces 中达到Master Title或在其他大型比赛平台的相似水平

考虑到并不是所有的有能力用户都参加过比赛, 我们还设置有如下Auth规则:

+ 有不少于5位authed user进行确认

#### Power User



### Advanced Mode



### 自动关注题目tag

