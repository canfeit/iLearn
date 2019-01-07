es1 es3
es5 get/set
esnext

1994 年,网景领航者（Netscape Navigator）。 内部代号“Mozilla”，User-agent
开发一种 “用于浏览器的 Scheme”。Scheme 是一种 Lisp 的方言，语法很简单，它动态而强大，并且本质上是函数式的。而 Web 需要类似这样的语言：语法容易掌握；动态的，以减少代码，加快开发；并且强大。Eich 看到有机会可以从事自己喜欢的事情，于是就入伙了。

上级：开发一种 “用于浏览器的 java“

当时，迫于压力，必须尽快赶出一个工作原型。当时原名为 Oak 的 Java 语言正开始推动。Sun Microsystems 正大力推进 Java，网景通讯公司即将与他们达成一项协议，让 Java 可以用在浏览器上。那么为什么要开发 Mocha（JavaScript 早期的名字）呢？为什么已经有了 Java，却还要开发一个全新的语言呢？当时的想法是，Java 不适合 Mocha 的目标受众：测试脚本编写人员、业余爱好者、设计师。对于用在浏览器这个角色上来说，Java 确实太大太重了。所以当时他们的想法是让 Java 用于大型专业级组件开发；而 Mocha 将用于小型脚本任务。

此时有很多来自于内部的压力，要尽可能快地选择一门语言。Python、Tcl 以及 Scheme 本身都是可能的候选。所以，Eich 必须快搞。不过，他比别人有两个优势：可以自由挑选适合的特性集、可以直达拍板的人。不幸的是，他也有一个大的劣势：没有时间。必须要做出很多重要的决定，而做出决定的可用时间又很短。JavaScript，即 Mocha，就是在这种背景下诞生的。几周之内，一个工作原型就推出了，然后就被集成到 Netscape Communicator 中。

于是，本应是用于浏览器的 Scheme，现在就大相径庭了。与 Sun 达成协议的压力，以及让 Mocha 变成 Java 的脚本同伴，束缚住了 Eich 的手脚。新语言需要采用类似 Java 的语法，对于很多常用语还采用了熟悉的语义。所以 Mocha 一点也不像 Scheme。它表面上看像是一种动态的 Java

第一版的 JavaScript 敲定了该语言中很多现在知名的特性，特别是其对象模型以及函数式特性在此版本中已经出现了。

主要设计特点
选择 Scheme 式的一等函数以及 Self 式（尽管很怪异）的原型作为主干
至于 Java 的影响，主要是把数据分成基本类型和对象类型两种（比如字符串和 String 对象）

网景通讯的创始人及前 Mosaic 团队的成员 Marc Andreessen 预见到 Web 需要某种方法变得更动态。动画、交互和其它形式的小动画应该是未来 Web 的一份子。所以 Web 需要一种能与 DOM 交互（不是跟你现在看到的这样一成不变）的小脚本语言。不过，这种脚本语言不应该面向大佬开发者，以及在软件工程方面有经验的人们——在当时这是一种重要的战略呼声。当时 Java 也在兴起，并且 Java applets 很快就要成为现实。所以这个用于 Web 的脚本语言需要迎合另一群受众：设计师。实际上，那时 Web 是静态的。HTML 依然年轻，并且足够简单，非程序员也很容易学得会。所以，要让 Web 变得更动态，不管是浏览器的哪一部分，都应该让非程序员容易理解。这样 Mocha 的想法就诞生了。Mocha 要成为用于 Web 的一种脚本语言，它必须是简单、动态的，并且让非程序员容易理解。

1995 年 BE（Brendan Eich 布兰登·艾奇）开发 js
其中包括一个可在浏览器和服务器使用的脚本语言，Sun 与 Netscape 联合声明名为 JavaScript。JavaScript 和 Java 一样成为 SUN 的注册商标
1995 年，微软公司发布互网络探索者(Internet Explorer)浏览器。IE，并搭载了一个 JavaScript 的克隆版 JScript

盖茨背着微软私下约见竞争对手美国在线 CEO 寻求合作，事后美国在线 CEO 奔赴网景 CEO 家中，共同商讨抵制微软，并将微软比作希特勒。但是，当时占尽优势的网景极尽傲慢，手持美国在线的橄榄枝却未表现出丝毫诚意。而微软却再次放低姿态，表示愿意为美国在线定制浏览器，并在 windows 中内置注册美国在线的服务图标，此举导致大量微软在线的骨干离职。最终，美国在线与微软达成合作。
1997 年，乔布斯回归苹果。微软向苹果公司注资了 1.5 亿美元，IE 成为苹果 Mac 的默认浏览器。随着 IE 浏览器的不断完善，IBM 等各大巨头纷纷倒向微软。

微软与网景分庭抗礼，JavaScript 语法分裂加剧。 网页显示效果的不同，增加了网页制作成本，网景领航者无法正常访问的网页变多，市场占有率持续下降。

1997 年， 由来自 Netscape、Sun、微软、Borland 等公司的程序员组成的 欧洲计算机制造商协会（ECMA）第 39 技术委员会（TC39）制定出了 ECMAScript 标准，简称 ES。
1998 年，Windows 98 捆绑 ie 发布。
1998 年，网景被美国在线收购， 美国在线起诉微软垄断。 NN 开源，成立 Mozilla 非营利组织维护 NN。后来，NN 逐渐消失，取而代之的是后来 Mozilla 基金会的 firefox 浏览器。

1999 年 12 月，ECMAScript 3.0 版发布，成为 JavaScript 的通行标准，得到了广泛支持。

2007 年 10 月，ECMAScript 4.0 版草案发布，对 3.0 版做了大幅升级，预计次年 8 月发布正式版本。草案发布后，由于 4.0 版的目标过于激进，各方对于是否通过这个标准，发生了严重分歧。以 Yahoo、Microsoft、Google 为首的大公司，反对 JavaScript 的大幅升级，主张小幅改动；以 JavaScript 创造者 Brendan Eich 为首的 Mozilla 公司，则坚持当前的草案。

2008 年 7 月，由于对于下一个版本应该包括哪些功能，各方分歧太大，争论过于激进，ECMA 开会决定，中止 ECMAScript 4.0 的开发，将其中涉及现有功能改善的一小部分，发布为 ECMAScript 3.1，而将其他激进的设想扩大范围，放入以后的版本，由于会议的气氛，该版本的项目代号起名为 Harmony（和谐）。会后不久，ECMAScript 3.1 就改名为 ECMAScript 5。

ES3 之后的 JS 语言进化的尝试很早就开始了，同时有若干个方案，有具体实现的包括 JScript.NET、ActionScript 3 等。但作为 ES4/JS2 而为人所知的，是 Mozilla 的草案。草案本身不是 BE 写的，而是 Waldemar Horwat。对这个草案到现在我还留有深刻印象的一个有趣特性就是基于 namespace 的 API version。

2005 年，ES4 开始制定，由于实际上抛弃了 Mozilla 的草案，而转而以 ActionScript 3 为基础，当时 Mozilla 和 Adobe 走得很近，Adobe 还开源了自己的 VM 送给 Mozilla。这草案在某些方面比现在的 ES6 要走得更远，比如有相当强大的类型系统，支持泛型、nullable、interface、union type 等——当然从现在的趋势看，ES7 或 ES8 早晚会加入这些东西。这草案也继承了老的 Mozilla JS2 草案中的一些特性。比如前面提到的 namespace——这特性与 C++/C#中的 namespace 不同，我理解更接近某种弱化的 annotation，比如 public/private 是以内置 namespace 实现的。
2005 年开始弄 ES4 的主要是 Brendan Eich 和开发了 AS3 的 macromedia（后来是收购 macromedia 的 Adobe）
M$(MS，Microsoft,讽刺其金钱至上)和 Yahoo（主要是DC Douglas Crockford）一开始是表示合作的
2007 年，BE 和 Adobe 已经在 ES4 上花了两年时间，但 M$ 和 DC 突然表示觉得 ES4 太过庞大，并添加了太多他们不想要的东西。
2007 年 4 月，DC 和 M$开始平行起草另一个提案，一开始叫 ES3.1，也就是后来的 ES5，整体上是一个更为保守、渐进的提案。当时 TG-1 内部对 3.1 的定位有疑问，但允许了其存在。BE 对 ES4 的前景感到担忧，2007 年 10 月发布了 ES4 提案预览。M$ 和 DC 认为 BE 操之过急，发表了一些负面评论，双方闹翻。BE 对 M$的行为非常光火，并且认为 M$ 在背地里运作引导业界舆论反对 ES4。ES4 难产，与此同时，随着 ajax 概念的提出，业界开始冒出各种 js 库，对 js 工程化开始进行初步的探索。2009 年，各方最终同意将 ES3.1 改为 ES5 并正式发布。同时，开始进行下一个版本的规范 Harmony/ES6 的起草。

3. ES4 被干掉我个人觉得很大程度上是“政治”原因而非技术原因。注意本段均为带有强烈个人观点的阴谋论叙述。事情发生变化就是起于 Macromedia 被 Adobe 收购。当时 Flash 平台如日中天，Adobe 收购 MM 之后一下子成为了足以和微软对抗的巨头——既有垄断性平台，又有极其完整的涵盖从设计到开发所有工具的产品线。现在连 Web 唯一的开发语言都要以 AS3 为底本了！这个时候，搅屎棍 DC 出现了。他作为 Yahoo!这个落后生产力的公司代表的个人代表，以其技术偏见为由，私下找到微软密谋。微软正愁如何对付 Adobe，这下一拍即合，当即由 DC 为主炮制了 ES 3.1 出来跟 ES4 分庭抗礼，为此连自家的http://JScript.NET也做了炮灰。另一方面，自大的Adobe却似乎在梦游，除了傻兮兮的拿ES4作为广告标签来宣传自己的AS3（当然后来被叫停，但也已造成社区对其的不满），在ECMA TC39 中却听不到它们的声音——我一直都没搞清在 ECMA TC39 中谁是 Adobe 的代表。在关键公司中，Google 当时还没有进入此领域（V8 是 2008 年开始的），Apple 还处在复兴前夜（iPhone 是 2007 年发布的，WebKit 在 2005 年刚刚开源），Opera 从来就没有什么话语权，Adobe 在梦游……网站方面，今天引领 Web 开发的 Facebook 和 Twitter 当时不知道在干什么，唯一代表 Yahoo!就那个德行。在开发者社区这里，当时 Node 还没出现（2009 年），JS 语言社区主要都是缺乏语言设计和大型编程经验的网页开发者，水平低、容易忽悠。总之，能决定 JS 未来的，只有 Mozilla 和 Microsoft，或者说只有微软——因为此时 Microsoft 在浏览器相关领域仍然具有垄断话语权。于是，DC 狐假虎威，BE 孤掌难鸣，后来发生的事情就像

@尤雨溪

描述的那样了。

4. 客观的说，ES5 除了从 ES4 中吸收的 get/set 之外，都只是小小的补丁，就这么些东西，折腾了好几年，实在是作死的节奏，极端让人失望。要不是 Node 横空出世和 Web App 大爆发，JavaScript 的前景还真是一片灰暗。

5. 我还是很敬佩 BE 的。虽然他被 DC 摆了一道，让整个语言发展大开倒车，当时连我都觉得不能忍，但是他还是找到了妥协（Harmony）的道路。ES3.1 改名为 ES5 其实有僭越（就这么点东西好意思叫 ES5？），但是也为 ES6 铺平了道路。ES4 草案中还是有相当数量的特性最终被 ES6 继承了。包括 let、destructuring assign、generator 等。另一些特性则以更好的方式重生，如 ES6 module 之于 ES4 package，ES6 Symbol 之于 ES4 namespace 等。其他那些特性如 array comprehensions、运算符重载、decimal 类型等，无论会不会在未来加入，自 ES6 开始的语言进化的道路已经确定，不再是搅屎棍或某个公司所能阻碍的了。

我能够想到，是哪些人希望 JS 加上类、模块、类型，又是哪些人觉得不改就挺好。前一种多半是做 Web 应用的，也就是在浏览器中开发“软件”的，后一种多半是做“页面”的。这两种产品形态的差异，导致双方对开发语言的需求大为不同，前者恨不得不要用 JS，改用 C#，后者连现在已有的 JS 都可能觉得啰嗦。

这两种人其实是无法调和的，并且分歧会越来越大。Web 应用开发者在 ES4 的时代相对弱势，所以 ES4 就悲剧了，而现在，这类人占比越来越高，话语权也越来越强，所以 ES6 就这样了，再往后，页面开发者更觉得难以忍受了。

所以有时候我真觉得，干脆别搞 ES6 什么的了，保留现有 JS 不变，像 Google 搞 Dart 那样，重新标准化一门新语言，然后大家各取所需，搞页面的就用现在的 JS，搞应用的就用新语言，各自演进，大家都快乐，多好啊。

以目前这种状况，搞应用的嫌 ES6 步子小，搞页面的嫌大，再往后，多迈一步都是很困难的，因为反对的声音将越来越大，难办啊。

我其实很喜欢 ECMAScript 4 的，因为我写 ActionScript

时过境迁，不可同日而语了，如果当时前端已迈入工程化的大门，ES4 早就普及了

ES4 的故事相当复杂... 我一时八卦心起整理了一下：

当年的 TC39 还叫 TC39-TG1
JScript.NET、ActionScript3
2005 年开始弄 ES4 的主要是 Brendan Eich 和开发了 AS3 的 macromedia（后来是收购 macromedia 的 Adobe）
M$（Pratap Lakshman） 和 Yahoo（主要是 Douglas Crockford）一开始是表示合作的
2007 年，BE 和 Adobe 已经在 ES4 上花了两年时间，但 M$ 和 DC 突然表示觉得 ES4 太过庞大，并添加了太多他们不想要的东西。这里具体的理由我们无从得知，只能做一些揣测：DC 的龟毛大家都知道的，从 JavaScript: The Good Parts 就可以看出他的偏好和 ES4 出入很大。M$在 ES4 的制定过程中并没有积极参与，可能是因为与会的 Pratap Lakshman 和上层的沟通不足，然后某天跟上层一汇报，上层觉得 ES4 和 ES3 差别过大，实现起来难度大，而且会导致他们丧失对规范的控制权，所以突然就决定抵制 ES4 了。
2007 年 4月，DC 和 M$ 开始平行起草另一个提案，一开始叫 ES3.1，也就是后来的 ES5，整体上是一个更为保守、渐进的提案。当时 TG-1 内部对 3.1 的定位有疑问，但允许了其存在。
BE 对 ES4 的前景感到担忧，2007 年 10 月发布了 ES4 提案预览。M$和 DC 认为 BE 操之过急，发表了一些负面评论，双方闹翻。BE 对 M$ 的行为非常光火，并且认为 M\$ 在背地里运作引导业界舆论反对 ES4。
ES4 难产，与此同时，随着 ajax 概念的提出，业界开始冒出各种 js 库，对 js 工程化开始进行初步的探索。
2009 年，各方最终同意将 ES3.1 改为 ES5 并正式发布。同时，开始进行下一个版本的规范 Harmony/ES6 的起草。

--- 历史的分割线 ---

时至今天，我们会发现 ES6 的业界环境和 ES4 有很多不同：

当年反对 ES4 的 M\$/Yahoo 话语权已今不如昔，而且本身的态度也已经改变。IE 的市场份额持续下跌，在实现上也已长期处于追赶而非当年引领的地位。Yahoo 在互联网界的地位一落千丈，DC 在 TC39 也不像当年那么活跃。
Google 伴随着 Chrome 飙升的占有率，以及靠着 web 发家的背景强势加入 TC39，现在可能是最有话语权也是最积极的玩家，因为推动 web 这个平台和 Google 本身的市场空间直接相关。
整体上 web 前端应用化、工程化的趋势不可逆转，对于支持工程化的语言特性需求也确实比当年高。随着 Node.js 的爆发，JS 在后端的需求增长的同时也开始暴露出语言本身对大型工程的不足。根本上来讲，就是 ES4 的时候业界对 js 工程化的需求没有那么高，所以 ES4 那些考量受众不足。当年 ES4 未能发布的一个原因是步子过大的同时，没有有效的对新特性进行实践考验的方法。这一点在今天借助各类 transpiler 得以实现。比如 CoffeeScript 的一些特性大家用了都说好，那么 TC39 就可以放心地采用到 ES6 当中。TypeScript 的 class 大家用着觉得不错，那么也可以采用。同理，业界对模块化的探索比如 AMD 和 CommonJS 也对 ES6 module 的最终定稿有着巨大的影响。简言之就是没有实践的检验你很难光靠嘴巴说服所有人。

综上，个人认为 ES6 不太可能会重蹈 ES4 的覆辙（目前的计划发布时间是 2015 年 6 月）

最早的版本，ES1 和 ES2，并不广为人知也没有大范围地被实现。ES3 是 JavaScript 第一次广泛传播的基准线，并且构成了像 IE6-8 和更早的 Android 2.x 移动浏览器的 JavaScript 标准。由于一些超出我们讨论范围的政治原因，命运多舛的 ES4 从未问世。

在 2009 年，ES5 正式定稿（在 2011 年出现了 ES5.1），它在浏览器的现代革新和爆发性增长（比如 Firefox，Chrome，Opera，Safari，和其他许多）中广泛传播，并作为 JS 标准稳定下来。

预计下一个版本的 JS（从 2013 年到 2014 年和之后的 2015 年中的内容），在人们的讨论中显然地经常被称为 ES6。

然而，在 ES6 规范的晚些时候，有建议提及未来的版本号也许会切换到编年制，比如用 ES2016（也叫 ES7）来指代在 2016 年末之前被定稿的任何版本。有些人对此持否定意见，但是相对于后来的 ES2015 来说，ES6 将很可能继续维持它占统治地位的影响力。可是，ES2016 事实上可能标志了新的编年制。

还可以看到，JS 进化的频度即使与一年一度的定版相比都要快得多。只要一个想法开始标准化讨论的进程，浏览器就开始为这种特性建造原型，而且早期的采用者就开始在代码中进行实验。

通常在一个特性被盖上官方承认的印章以前，由于这些早期的引擎/工具的原型它实际上已经被标准化了。所以也可以认为未来的 JS 版本将是一个特性一个特性的更新，而非一组主要特性的随意集合的更新（就像现在），也不是一年一年的更新（就像可能将变成的那样）。

简而言之，版本号不再那么重要了，JavaScript 开始变得更像一个常青的，活的标准。应对它的最佳方法是，举例来说，不再将你的代码库认为是“基于 ES6”的，而是考虑它支持的一个个特性。
es4 工程化 需求地 失败
google chrome facebook typescript CoffeeScript dart nodejs-》es6 工程化 成功
ES6 和 ES4 比较起来反而是开倒车
微软干掉了 es4，基于 es4 开发了（JScript.NET）

dc
他是 JSON、JSLint、JSMin 和 ADSafe 的创造者，也是名著《JavaScript: The Good Parts》（中文版《JavaScript 语言精粹》）的作者