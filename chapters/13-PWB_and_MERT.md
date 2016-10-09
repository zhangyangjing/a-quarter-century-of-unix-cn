# PWB和MERT

回忆Thompson和Ritchie为PDP-7写的第一个系统，第一版是在1971年为PDP-11/20写的。第四版是贝尔实验室于1973年末在第三版的基础上用C语言重写的，当它使另一个项目获得成长:程序员的工作台(PWB)。它的第一版帮助Charlie Roberts思考。Bob Morris说Rudd Canaday从来没有得到他提供的贷款。对Roberts来说也是这样。MERT(多环境实时)是Roberts的发明，虽然它的大部分是由Heinz Lycklama和Doug Bayer写的。Roberts告诉我:

> 1970年早期，我知道在PDP-11上有一个Unix，它是用B语言实现的。但在我看来Steve Johnson已经在谈论C语言。在1970年10月我离开莫里山计算机中心回到科研。我作为客户已经意识到专利，并且我回顾思考1127将Unix视为分时系统来为文档做准备。计算机科学研究就像很多的学术部门:它有两部分。Sam Morgan领导了包含有Dennis，Ken，还有Doug McIlroy的计算机科学那部分。Hank McDonald则是系统计算研究部门的总监。我在哪里为Hank工作，他想为80年代建立下一代的ESS。

> 我们在15楼，正好在Doug和其他伙计们的下面。我有Heinz Lycklama，Dick House以及Carl Christensen为我工作，还有其他一些程序员。Carl和Heinz那时工作于数字数据处理器DDP516，那是一个小的计算机，它有自己的操作系统和硬件。但我曾经读了Per Brinch Hansen的一些文章。他后来把所有的内容都卸载了*操作系统原理 1973年*这本书里，他让我思考像微内核，操作系统层还有其他很多直到Mach 3和Chorus以及Windows NT才真正成熟的东西。在我看来Unix作为一个分时系统有些太过于聚焦，我想使用一个专注的自定义系统工作——为交换和大数据库，实时和交易处理。

> 好了，71年的时候Hank帮我搞到买大容量磁盘11/45机器的钱，接下来几个月我都在为我的系统工作，它的名字叫OSKER——**OS KERnel**。在10月和圣诞节间的某个时间，我引诱Heinz Lycklama离开了DDP。他和Carl看不到我想实现的概念。但Hank孤立Heinz来和我一起工作并且在72年晚期的时候我们得到足够的钱去雇佣一些人，Doug Bayer在73年的时候加入我们，Heinz真的将OSKER开发出来。在那个时候，我和部门的头Doug McIlroy又一次谈话，他建议联合起来合作。但是我看不到可能性并且担心这会让我的员工放弃OSKER去为Unix工作。那时Heinz建议我们“将Unix构建在OSKER上面”，然后那就成了MERT。我们同时有了Unix和实时处理，这很了不起。但是Heinz对内核失去了兴趣，Doug是一个新手。我感到巨大的压力，1973年我决定搬到霍姆德尔将工作更多的放在通信和图像处理上。

> 当我离开的时候，Heinz开始开发Unix MERT:那是系统实验室74年的工作内容，他们从来没有进行过内核方面的工作。MERT在Berk Tague组建USG的时候搬到了哥伦布和印第安山。印第安山在78年创建了多路复用MERT——DMERT，它不是一个可移植的微内核，非常依赖硬件。它运行在3B20D上，但它今天仍然运行在每个4ESS和5ESS上。