## 2016 级大三必修课的考题整理（极不完全）

### 通信软件设计

所有题目都没有要求写文字的语法（比如 signal，timer）这样的，但还是建议背一下，因为最后一道大题要用

#### 填空（1题3分）

- 要求画出一些 sdl 和 msc 的图示
  - 如：建立进程实例的符号是什么？
- sdl 语言中系统之外的部分被称为？
- sdl simulator 生成出来的代码是什么编程语言的？
- 电话交换机中，当用户摘机之后，应当给用户播放`________`音？

#### 选择题：(1题3分，很多题目只有3个选择)
- 给了一些 msc 图，询问了很简单的问题
- 给出三张 SDL 图，问哪张是错误的
  - 涉及到课本 P120 5.4.11 图形符号连接关系
  - 有的符号不能连在别的符号底下

#### 判断题（1题3分）

- SDL 的进程、MSC 的消息、SDL 的信号，哪些能带参数，哪些不能？
  - 看书即可得到答案
- 还有一些别的基础知识

#### 简答题（10分）

协议分析的过程中需要做哪些工作？

#### MSC 绘制（15分）

火车站里有一台取票机，该取票机有打印机、键盘、触控屏等输入设备，视作外部设备。该取票机与中央取票系统（称为“后台”）相连，从后台获取用户火车票相关的信息。该取票机的使用流程如下：

1. 用户刷身份证，取票机向后台申请认证该用户；
2. 后台向用户发送取票短信，上面有该用户的取票密码；
3. 取票机向后台发送用户输入的密码；
4. 验证成功后，后台给取票机发送用户所购买的火车票信息；
5. 用户在取票机上选择想要打印的火车票；
6. 取票机向打印机发送打印指令，打印所选火车票。

在火车票最终被打印之前，用户都可以随时退出该系统。在退出该系统之后，用户必须重新刷身份证才能重新使用。用户操作有时间限制，若超时，视为用户退出该系统。

请为下列情况绘制MSC图：

1. 用户成功取到火车票
2. 用户超时未输入取票密码
3. 用户在打印火车票前中途退出系统

#### SDL 绘制（15分）

画出取票机控制软件的进程状态机图。



### 计算机网络

因为很多题目回忆不起来了，甚至连题型都记不起来了，所以请参考14级的题目。

这里重点讲一些比较难的知识点：

- 时分复用、频分复用和码分复用是什么意思？
- 信号调制的几种方法分别是什么？
  - 但是没考星座图
- CRC 码是一种 `___` 码。
  - 让我很震惊的是，没有考计算 CRC
- 给你两个字节，问你汉明距离是多少
  - 令我极度震惊的是，没有考计算汉明码
- 在什么协议下会出现隐爆终端问题？
  - 中文课本 P215，英文课本 4.2.5 节
- 虚电路与包转发相关
  - 虚电路需要沿路建立连接吗？
  - TCP 协议建立连接后，每一个包都会在网络上走同一条路线吗？
- 和电子邮件相关的一些协议有哪些？分别是干嘛的？
- 填空题考了一道作业题：ip 地址聚合
- tcp 的 fin flag 有什么用？
- 什么网络使用交换机这一设备？
- 经典以太网用的是什么样的介质访问控制（MAC）协议？
- 用于域内/域外路由的有哪些协议？
- TCP 里**每一个字节**都有一个序号吗？
- TCP 用什么机制进行错误处理？
- Wi-Fi 基于无线电，容易受到干扰而出错，那么里面有没有使用**纠**错码呢？
  - 注意不是**检**错码
- 大题：为什么实时音视频业务需要使用 UDP 协议？请给出两个基于 UDP 的协议。
- 大题：为什么用于域内路由的协议不能用于域外路由？
- 大题：链路状态路由的原理是什么？



### 软件过程改进

题目太多忘了。请背 PPT，推荐背~~黄色资源~~标有黄字的 PPT。这次考的内容非常细致，甚至考了你开例会的时候要做什么这种题。本次考试的题目没什么价值，因为很容易改题目。总而言之 PPT 全部背下来是没错的。



### 面向对象分析与设计

期中题目全都是带带相传的大题，请参考往届学长资料。这里讨论期末试题：

1. 4 分简答题
   1. DCD <u>stands for（的全称是）</u> 什么？
      1. ~~高慧（监考中）：「DCD 就是设计类图的意思啊！」~~
      2. ~~鉴于高慧都忍不住在考试中说了答案，这道题以后应该不会再考~~
   2. pattern（模式）是什么？
   3. 我们写 operation contract（操作契约）的 purpose（目的）是什么？
   4. ……以及别的带带相传的大题。
      1. RUP 是不会考的，放心。
      2. ~~知乎，2014：[RUP 早就被业界抛弃了](https://www.zhihu.com/question/23208040/answer/23949523)~~
2. 20 分大题
   1. GRASP 的最常用的三个模式是什么？举例说明在哪些场景下能够使用
   2. GoF 中有三个模式常常在一起使用，请问这三个模式是什么，并说明它们面对的问题和解决的答案
   3. 给出形如下面代码的通信图（考试时给出的是通信图，为了不插入图片，在此用代码代替），其中系统操作（第 0 个方法调用）是构造了一个`Controller`对象。画出对应的 UML 顺序图：

```java
// 你接下来看到的不是代码而是 UML 通信图
// 请脑补这张通信图的样子...

class Register {
    public Register(ProductCatalog catalog) {
        // do something...
    }
}

class Controller {
    public Controller() {
        var catalog = new ProductCatalog();
        var register = new Register(catalog);
    }
}

class ProductCatalog {
    private Map<int, Product> products;

    public ProductCatalog() {
        products = new Map<int, Product>();
        this.createSpec();
    }

    public void createSpec() {
        while (true) {
            // 你不需要管 id, price, name 是从哪来的
            var prod = new Product(id, price, name);
            products.put(id, prod);
        }
    }
}

class Product {
    public Product(int productId, int price, String name) {
        // 省略...
    }
}

// ......

public static void main(String[] args) {
    var controller = new Controller();
}

```



### 软件项目管理（SPM）

SPM 慕课上的题目非常重要，毕竟老师为了控制难度，会多出慕课上面的原题给大家放水。如果不背慕课原题就吃大亏了。

#### 填空题（15 分，1 分/小题）

此处填空题也出现了不少慕课原题。这里只描述需要背的内容：

- WBS 的全称
- 马斯洛需求层次中最高级别的需求是什么
- 需求规格审计属于什么类型的*活动？*
- Scrum 模型的四个管理会议是什么

#### 选择题（20 分）、判断题（15 分）

都是慕课原题，背就是了

#### 大题 1：PERT（10 分）

考察用 PERT 进行项目历时估算。题目给出了如下任务图：

```
    +-----+     +-------+     +-------+     +-------+
    |     |     |       |     |       |     |       |
    | 开始 +--- >+ 任务1 +---->+ 任务2  +---->+ 结束   |
    |     |     |       |     |       |     |       |
    +-----+     +-------+     +-------+     +-------+

```

问：

1. 这是 PDM 还是 ADM？
2. 【题目给出任务 1、任务 2 的乐观、悲观、最可能耗时】，请问任务 1、2 完成的时间期望？
3. 项目在 20 天内完成的概率是？
   1. 最气的是，题目并没有给出 +σ、+2σ、+3σ 对应的概率取值，明明连高考都给出来了。请把 68.27%、95.45% 和 99.73% 这三个数字背下来。

#### 大题 2：PDM 网络图（15 分）

题目给出一张 PDM 网络图，涉及到了 A、B、C……G 共 7 个任务，问：

1. 画出关系依赖矩阵
   1. 如果 i 到 j 有一条有向边，那么 P<sub>ij</sub>=1
2. 将最早开始时间、最晚开始时间等填入图中
3. 找出关键路径
4. 项目的总耗时是多少？
5. 任务 F 的**总**浮动是多少？
   1. 注意区分总浮动和**自由**浮动
6. 任务 G 的最晚开始时间是由什么计算出来的？

#### 大题 3：挣值分析

题目给出了一个项目 - 预算 - 成本 - 完成度表，并要求基于这个表格进行挣值分析：

（以下数据是瞎编的，仅用于说明题目）

表 1、预算表

| 周     | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 任务 1 | 10   | 15   | 5    |      |      |      |      |      |
| 任务 2 |      |      | 10   | 15   | 5    | 10   | 15   | 5    |
| 任务 3 |      |      |      |      |      |      | 5    | 5    |

表 2、实际成本表

| 周     | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 任务 1 | 10   | 15   | 5    |      |      |      |      |      |
| 任务 2 |      |      | 10   | 15   | 5    | 10   | 15   | 5    |
| 任务 3 |      |      |      |      |      |      | 5    | 5    |

表 3、实际完成情况表

| 周     | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 任务 1 | 5%   | 15%  | 100% |      |      |      |      |      |
| 任务 2 |      |      | 10%  | 15%  | 5%   | 10%  | 15%  | 5%   |
| 任务 3 |      |      |      |      |      |      | 5%   | 5%   |

- 考察了 5 大输入、8 大输出，这些全都要背

- 画出项目的燃尽图

#### 大题 4：决策树（5 分）

模板题。给出甲、乙两套方案，并给出这两套方案的成功、失败概率和收益，问方案选择。

#### 大题 5：敏捷项目实验（5 分）

给出你们 SPM 项目的一个 Epic，以及它分解得出的 Story，然后用标准格式写出一个 Story。