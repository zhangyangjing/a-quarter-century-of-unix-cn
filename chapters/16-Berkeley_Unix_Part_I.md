# 伯克利Unix 第一部分

伯克利加利福尼亚大学的Robert Fabry教授在1973年工作于SOSP程序。它对Thompson的报告有着非常深刻的印象。当他返回科瑞教学楼的时候，Fabry的第一份工作是尝试让计算机科学系，统计系，还有数学系合资购买一台PDP-11/45。他向Thompson订购了纸带，在1974年由毕业生Keith Standiford安装了Unix。就像Kirk McKusick所说的，Ken Thompson参与此前所有安装，但是不包含这一个，因为“有几个奇怪的系统崩溃需要他去解决”。Thompson会打电话给在机房里的Keith Standiford，电话随后换成了300波特率声学调制解调器，Thompson通过会通过电话线“在新泽西远程调试bug”。

接下来出现了一个问题，因为数学系和统计系想使用DEC的RSTS系统。因此一天的时间被分成了几部分:RSTS运行16小时后，Unix接着运行剩下的8小时。当时在那里接触到Unix的学生Eric Allman说:

> 我那时学习操作系统课程，他们在6400上使用一个叫做*玩具系统*的操作系统。但是他们想去使用11/40上面的Unix，我们一天只能使用8小时，而且每天使用的时间都不固定。我努力回忆:我看了手册，我记得没有理解为什么你要使用**echo**命令，非常奇怪。当然我现在知道了。第4版相当古怪，只有研究人员才会喜欢上这个系统。它很慢，只有很少的工具。接下来我们听说了Ingres项目。

> Michael Stonebraker和Eugene Wong两位教授的Ingres数据库项目是第一批移植到Unix的软件。由于他们不满意分配的时间，1974年春天他们自己买了PDP-11/40。但自此之后，学生们就没有足够的时间在11/45上面上机。1974年6月Stonebraker和Fabry两位教授计划为计算机科学系再购买两台教学用11/45。他们在1975年早期得到资金，刚好那时DEC宣布了11/79机型，他们觉得这个型号非常合适，于是资金汇集起来。11/70机器在秋天运了过来，正赶上Ken Thompson来这里以访问教授的身份进行一年的学术休假。Thompson，Bob Kridle，还有Jeff Schriebman在新买的11/70上面安装了第6版Unix。

还有一个意外结果是“50 fixes”纸带。Thompson告诉我:

> 我们意识到的第一件事情是外界都在使用Unix发布版(V4，V5，V6，V7)而我们没有使用。我们的观点是连续的。我们在某个时间点拥有过V5，但因为不断地放进模型到处很容易就过期了。

> 在第6版以后，我准备回到伯克利教一年书。我将一个系统的纸带放在一起拿着。因为它几乎是一个发布版，我在V6上做了一个**diff**。去伯克利的路上，我在厄本那香槟分校停了下来，照看Greg Chesson完成他的博士学位。我留下diff的纸带在那里并且告诉他我会留意它是否传播开(我想我可能还把它给了Katz)。(O'brien提到diff纸带一定是来时Chesson)。

> 我感到它非常重要，因为我发现了非常多的多道程序(异步)bug需要修改。发布的版本没有提供更新。在用户非公开交流的时候对此有很很多咒骂。整个情形看起来已经无法继续，我感到我应该去做些什么。

Lou Katz的说法有些不一样:

> 大量的bug修正被搜集起来，相比于一次发布一个，Ken制作了一个合集纸带(“50 fixes”)。虽然我没有特别记住哪一个，但是这里面有一些修正非常重要。我怀疑这其中有很大一部分是贝尔实验室意外的人制作的。Ken试图将它寄出去，但是律师一次又一次的拖延下去。

> 最后，在完全厌烦下，有人“在山岳大道发现了一个存有修复的纸带”(贝尔实验室位于新泽西莫里山600山岳大道)。

> 当律师发现这件事情，他们打电话给每一个授权单位试图问出他们是怎么拿到纸带的，并且恐吓他们如果不销毁纸带的话将会有可怕的后果。我猜没有一个人会真的告诉他们纸带是怎么来的(我就没有)。这只是律师证明他们的存在并试图杀死Unix众多行为的第一次。不得不说为Unix工作的律师要远多于技术人员。同时授权条款也开始更改，费用开始迅速的上涨。

也是在那个秋天两个毕业生去了伯克利校园:Chuck Haley和Bill Joy。他们对新系统着了迷，并且和Ken Thompson一起开发Pascal系统。Haley和Joy将Pascal系统提高以至于成为学生编程系统的选择。但是当ADM-3屏幕终端代替了33型号的电传打字终端，Hale和Joy对**ed**行编辑器感到不满。他们使用了一个叫做**em**的编辑器，它是伦敦皇后玛莉学院的Coulouris开发的，然后开发了每次一行编辑器**ex**。1973年Coulouris成为英国第一个接受Unix的人，他告诉我:

> 我在1975年秋天在圣母玛莉学院开发了**em**，它可以更有效的利用我们刚拿到的vdu终端。我们有在图形显示器上开发应用程序的经验，不论是鼠标定位还是触摸板定位(这个经验来自William Newman，他花了一年半的时间和我们一起为Utah和Xerox PARC工作)。我猜测Unix终端输入的的“原始”模式在那个时候完全没有被利用，使用它可以即时看到编辑结果，让人们更方便的编辑文本。 我们将它用于我们的单用户图形系统，这让我开发了**em**。

> 换句话说，**em**的含义是**给人用的编辑器**，我是在Ken Thompson访问圣母玛莉学院以后给它命名的。Ken看了它然后说“很棒，我看到过类似这样的编辑器，但是我并不觉得我需要它们，我在编辑文件时不想看到它们的状态”。

> 因为Ken表现出来的态度，贝尔实验室可能从来没有考虑过开发一个屏幕编辑器，这也使得他们很多年的时间里都没有合适的终端。他们继续使用了TTYs和其他打印终端很长时间，当他们给Unix组里每一个人都买了一台Tektronix 4014s屏幕，一种巨大的贮存管显示器。你不能在贮存管显示器上运行屏幕编辑器，因为它们的图像不能更新！于是这让其他人成了Unix屏幕编辑器的先驱，并且这才只是开始，我们为此持续工作了很多年。

> 然后我在1976年夏天作为访问者去了伯克利大学的计算机科学部门。我在一个堆满了Unix电传打字终端的房子里工作。我将**em**存储在DEC纸带上带到那里并且在我使用机器前安装了它(虽然**em**是为vdus设计的，但是它的单字符交互仍然可以在TTYs里使用，在每次交互后都会将当前行重新打印，慢的让人心碎)。

> 有一天，我坐在旁边终端机上的人是完全疯狂的黑客/博士/学生Bill Joy，他告诉我他写了一个Pascal编译器。我给他看了**em**，然后他说“这很好，使用这个系统的人可能会对它感兴趣”。他将我介绍给了其他人。他们有几台PDP-11s通过9600波特率电路支持着满满几个房间的vdu终端，这真是一个可以让**em**发挥作用的环境。

> 我解释**em**是**ed**的一个扩展，它为单行编辑提供了按键级别的交互，即时在屏幕上显示正在编辑的文本行(一种单行文本屏幕编辑器)。我解释这是通过将终端设置成为“原始”模式来做到输入单个字符的时候就可以在屏幕上看到——在1976年这是一个怪异的程序。

> 系统支持人员Jeff Schriebman曾经说过类似这样的话:“那是非常好的东西，但是如果让我们所有用户都用上这个软件，它在原始模式运行(每次有按键被按下都要进行处理)的开销会耗光cpu”。

> 我更为这种交互感到苦恼，想着“我想我开发了一个不切实际的编辑器，它的运行成本是如此之高——它可以在我们的小型系统里运行，但是它在伯克利的Unix环境下就无法使用”。

> 尽管如此，Bill和系统支持小组的人还是从我这拿走一份源码的拷贝看看他们是不是能用它。我之后去了东海岸大约一周的时间。当我回来的时候，我发现Bill已经将我的代码作为起点开始向着**ex**和之后的**vi**这个漫长的方向开发，并且这个新的编辑器已经安装到了服务器上——当然它仍然需要“原始”模式，但是很明显它带来的好处远大于开销。

> 看到可能是**em**提醒了Bill Joy和BSD的人们Unix上屏幕行编辑器的可能性。如果我没有开发**em**或者没有带着它去访问伯克利，早期版本的BSD Unix可能不会包含一个屏幕编辑器。这可以当创意反向跨越大西洋的一个小例子。

> 不幸的是，**vi**没有继承到**em**中的一些人机接口理论，在圣母玛莉学院我们已经断定模态交互是一个糟糕的主意，并且我已经做了很多事情来确保在**em**的交互中每一个键都不会有重复的含义。这个理论被**vi**的插入和编辑模式严重的破坏了。

> 因此我们在圣母玛莉学院从来没有用过**vi**。作为替代，一个叫Richard Bornat的同事和我的博士生Harold Thimbleby基于听来的交互理论设计了一个全屏编辑器，这个编辑器叫做**ded**(display editor)。它除了需要几个合理的功能键，几乎就是无模式的。它在70年代末期和80年代早期的欧洲被广泛使用，但是后来被**vi**和**emacs**逐渐取代。

同一时间的另一个地方，康奈尔大学被称为“JCL黑客”的Kirk McKusick，经过在特拉华州立大学学习的同学介绍接触到了Unix。“他像我展示了你该如何在上面玩游戏”，McKusick告诉我

> 在我1976年去伯克利之前我真的没有了解过Unix。我在春天去那里去寻找研究生项目，那时他们正处于春假，所以并没有很多人。但是当我在机房里见到Bill Joy时他正忙着研究一些东西，他说“Hi，我是Bill Joy，这是我们工作的内容——一个运行在Unix上的Pascal系统”。我说“你能用Unix做什么？”。因此他回答“你可以编辑文件，编译文件，你还可以玩象棋。让我帮你登陆进去”。因此我我在那个惬意的下午一直在玩象棋。然后我确认我喜欢伯克利，我来对了地方。

当Thompson在1976年夏末返回贝尔实验室的时候，Haley和Joy的兴趣变成了内核。让Schriebman惊喜的是他们安装了“50 fixes”纸带。学习了如何维护源码后，他们开始建议提高改善。

就在同时，Pascal编译器的新闻开始到处传播(1978年)，Joy开始制作伯克利软件发行版(BSD)。1978年3月它通过一封信提供给Tom Ferrin。“授权”写在信纸的另一面。Tom在3月13日签收了这封邮件。这份磁带包括:

1. Unix Pascal系统
2. Ex文本编辑器

... 作者是

1. W.N.Joy，S.L.Graham，C.B.Haley，K.Thompson
2. W.N.Joy

说明页伴随着授权许可

> 此发行版是标准的“tp”格式，800分辨率磁带。一个1200脚卷轴是最低也是最好的大学。

它的定价是50美金。

这是一个太长的故事，我不得不就此打断，因为我认为Unix的前十年是典型的代表，使它成为一个如此流行的操作系统。

贝尔实验室创建了一些东西，它被以源码方式发布。一个英国的用户基于它创建了一些东西。另一个加利福尼亚的用户同时完善了原始和英国的版本。它按照成本发布给社区。完善版本又包含进了下一个贝尔实验室发布本。

专利和授权根本没法控制着一切，并且系统总是越来越好，使用范围越来越广。

Bill Joy就像是发行版的秘书，在1978年发出了30份“自由”的BSD拷贝。随着一批支持光标定位的ADM-3a型号终端到来，使得Bill可以开发vi(visual editor)。但是这让他去做了其他的事情:优化几个不同终端的代码。Joy决定通过使用一种解释程序重绘屏幕来加强屏幕管理。这个解释程序是被终端的特性驱动的——**termcap**诞生了。

1978年中期已经做完了足够多的事情(Pascal系统更加强健，它可以运行在PDP-11/34s，**vi**和**termcap**也都可以)，第2版BSD发行版被放在磁带上。Bill Joy回复电话，将发新版放在一起，将用户反馈搜集到系统。他也买了接近75份第2版BSD。(PDP-11最新的Unix版本是1.10.1，来自1989年USENIX协会。它大约有80Mb，售价200美元。真实一笔大交易)。

Paula Hawthorn向我回忆这段时间:

> Kashtan刚刚发布了Unix和VMS的对比结果，我已经为我的论文完成了很多工作，所以那应该是发生在77年到78年的冬天。一群EECS的学生在周末去越野滑雪。Bill Joy，Mike UBell和我还有其他一些人就在那里。我们坐在我们租的公寓的厨房地板上(因为要谈论工作，所以从客厅客厅来到厨房)。Bill读了Kashtan更好的新能数据，Bill和Mike读了Unix的源码，我解释了磁盘和缓冲在其他操作系统是如何工作的。我的硕士性能测量在一台运行Kronos的CDC 6600上测试的，我的博士研究是测试Ingres的性能，Ingres的性能非常依赖逻辑上的连续数据是否可以在物理上顺序读取。Unix需要相等的盘区。哦，兄弟，没人想听到这个，但是我测量个性能，Kashtan也测量过。因此我们翻开Unix的代码，找找哪里可以让程序更快一些。这是Unix成为高性能系统的开始...

Mike Ubell(他后来写了历史)说:

> 我记得Bill做其他事情时花了很多时间看代码。他在多底层的cpu优化，减少指令。

Ubell也对我说了shell历史的实现机制:

> Bill在**csh**下实现了一个历史机制。我爱他因为我那臭名昭著的总是拼错单词并且ADM3a上不能复制粘贴。我想他是把历史数据写到了一个文件里，但他并不喜欢这种实现方式，于是j就删除了它。失去一个生产力工具，我猜测它使用shell已经使用了的了内存分析架构。Bill喜欢这种实现方式并且采用了它。我做的那个shell在伯克利持续用了几个月，直到Bill做出新的版本。

C shell的man帮助页(在“历史记录”中)仍然描绘了Ubell的拼写问题:

> 历史记录允许你使用之前在命令行输入的命令。这简化了拼写纠正和重复输入复杂的命令或参数。

Ubell的经历也非常吻合Eric Allman说的:一个通用的软件设计规则是你应该写你想用的程序。

**早期版本和PDP**

|Unix版本|PDP型号|
|:--|:--|
|1st|PDP-7|
|3rd|PDP-11; 11/20|
|●||
|●|PDP-11/45|
|●||
|6th|PDP-11/70|
|7th|PDP-11, Interdata 8/32|




---
**译者注**

* [editor history](https://github.com/mhinz/editor-history)
