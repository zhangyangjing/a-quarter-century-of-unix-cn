# DEC

第二章的很大部分内容都是在说数字设备公司(DEC)，这是因为在普林斯顿大学做出成果前，Unix只能运行在DEC生产的机器上:PDP系列(特别是PDP-11)和后来的VAX系列。但是DEC公司自身是不提供官方的Unix支持的，他们有自己的系统:FOCAL-11，VMS，TENEX。本质上DEC在前20年都有一种被Armando Stettner称为NIH的文化——这里就不再细说了。上Unix是贝尔实验室产品的事实足够取消DEC的工程师们。

但是在1970年后期，有一个不断增长的认识是Unix没有离去，硬件工程师们也意识到乐于助人的Unix用户非常重要。Ritchie和Thompson曾经去DEC访问过几次。现在DEC设置了一个Unix支持组——“我们是同一类实验室”。Armando Stettner在1979年后期离开贝尔实验室去了DEC，他是Usenet的早期发起人，Ultrix的架构师(DEC版的4.2BSD)，同时也是Unix车牌的首位用户。他告诉我:

> 我将拥护Unix的氛围带到了DEC，否则DEC就不会有在纳舒厄的Unix工程师组(UEG)。我们在新罕布希尔州的梅里马克工作。我们将Spitbrook路称为“Saliva Creek”。有一次服务和支持部门的人们知道我们在那里，他们给我们打了电话。

> 但是当Bill Joy来访问的时候，我仍在做着32V。当我们从波士顿洛根机场到新罕布什尔的时候时间太晚了，唯一还开着的地方是Denny的办公室。我们那天晚上做的事情是描绘出我们将要做什么。我们想维护所有我们身边的软件，修正配置文件，然后把这些发布成一个发行版。我办开玩笑的说“为什么我们不把Unix移植到DEC 20系统上?”。Joy说“看，这需要10天的时间，但是我在这里只能呆7天”。后来证明Bill有10天的时间。接下来我们晚上在VMS工程师组的实验室做VMS组的原型。Bill做VAX 780，Bill Shannon做750，我做730。基本上，我们会一起做出某些东西，然后分头到个自的机器上调试它。我们有一个RP06磁盘，我们将它称为5BSD，因为我们确信下一个发布的将会是5BSD。

> 我们复制了一个磁盘，Bill拿着它回了加利福尼亚。Shannon和我将磁盘复制到了decvax——一台780机器，我们的主力系统。Bill Joy接下来几天给我们打电话说“嗨，如果我们发布另一个发行版将会有很多授权方面的麻烦。那么我们为什么不把它称之为4.1BSD?”。

10年后的DEC似乎是在反对Unix。Steve Johnson向我评论说:

> 当然，当VAX机型出现的时候，很明显DEC认为它是一台很棒的机器，至少在硬件方面是这样，Unix可以为他们的销售额做什么？但他们仍然没有赞助。

我问Armando关于事情的情况。

> 我来到以后，UEG做了很多的支持工作——我们写设备驱动和做一些底层工作:Unix的硬件依赖部分。伯克利专注于高层。知道我们的顾客会告诉他们的驻场工程师给我们打电话。我们开发了一个测试和一个语言所以我们可以和驻场的人们有关系。当支持Unix的时候有一个很大的新人问题，当一台机器不能运行DEC的软件时驻场工程师不知道该怎么做。账号管理和客户满意度永远是一个问题。

> Spitbrook对Unix总是充满了敌意，坦白说是对整个公司...工程部门和管理部门尤为严重。Dave Cutler是DEC工程部门的中坚力量，他抓住了某些东西作为折中——我想是VMS上的SRI软件包。Cutler把Munson叫来，记得在AT&T和大学，Unix是DEC的一个大问题。因此Cutler被Munson叫来，Munson说他会让我们一些人过去看一看。所以Bill Shannon和我去了那里，大概有20分钟的路程。我们去了那里，Cutler正在他的办公室里。Bill和我坐在一个终端前，任何事情都不能做。Cutler问它有什么问题，我说它不能工作了。Cutler说“好的，谢谢你们”。我们回到梅里马克，Munson把我们叫到办公室(他是资深管理人员)，问我们“你们去那个地狱做了些什么？Cutler给我打电话对我念叨说对你们的工程师深表遗憾并且再也不想在Spitbrook见到你们”。

> 我想Cutler的轻蔑影响了他此后的工作。在DEC内部的RISC战争中，Cutler在新的Prism架构上做了另一个操作系统而不是使用Unix。Cutler的系统不能移植，但是从文化上兼容VMS。我想NT中的许多东西可以追溯到Prism(Cutler在1983年去微软工作)。

> 我们有一个Unix产品经理，有一天我们在走廊里走着，我说“Bill，你知道我觉得现在是啥时候为VAX做一个真正的Unix产品，一个VAX Unix”。我做了一个计划，Bill把它拿给Munson看，对他说“让我们做出来看看”。基本上，我的计划是基于4.2BSD的，如果伯克利没有发布4.2，那就使用替补计划的4.1。我对于4.2很有信心，因为我们已经拿到了测试版本，并且我们已经在使用它了。但是我们需要一个意外处理方案，也就是4.1。尽管这样，那时Sun已经宣布在伯克利之前宣布了4.2——Bill Joy才刚拿着4.1c离开。我们发现4.1在decvax上非常稳定。我那时是技术经理。

1980年在旧金山的USENIX会议上，Bill Munson宣布UEG的目标是“启发DEC发现Unix和它的机会”。Armando有另外一种启发。

> 1982年1月我在东海湾的圣莫妮卡参加USENIX会议，当Bill Munson冲出来的时候我们正要宣布DEC有一个Unix项目。Slsen在我们的后面。显然他带着我寄给他的Unix车牌，他把车牌挂到一些人的胸口然后对Munson说“去搞一个Unix产品，把它做好！”。所以Munson红着研究去东海岸发出上那个公告。

Armando最为值得记忆的“露面”是在1983年圣地亚哥USENIX会议上，我问他这次会议的情况。

> Bill Shannon刚刚买了一个新的Datsun，一个280ZX，我们开车去汉堡王把它们取回来。Bill有一个“UNIX”的车牌，我们想为USENIX会议做一些事情...每个人都有自己的小伎俩。所以我们说“让我们做一个海报”，又有人说“好，让我们拿一台VAX和一台终端，在木头上将它们建立起来”。我不记得我们为什么要把VAX放到木头里面去。我建议去拿实验室的780，在它上面画一个挡风玻璃，放上去一些VW轮胎并把Shannon的车牌放在挡风玻璃下面，然后用这些制作了一张海报。要想得到做这些事情的权限非常复杂，所以我去和PR的人谈了谈，正好他有所有这些目录。我看着这些目录和已经有的车牌，一个点子就冒出来了。Munson给了我800美元，我制作了3000个绿色UNIX车牌。

> 我记得我站起来说我想宣布你现在可以从DEC拿到Unix授权。台下所有这些来自几个Unix OEM厂商的家伙们都震惊了。我扶起车牌，死一样寂静的房间里爆发出大笑和鼓掌的声音。从房间的后面传出来一个声音:“Armando，你能从这件事学到什么?”，是Dave Yost说的。后来我们收到了一封来自贝尔律师的关于商标的信件。但是他们又打电话给我告诉我们他们不得不发送那封邮件来保护商标，但是我们能不能也给他们寄一些车牌。于是我们就寄了。

