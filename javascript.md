# [JavaScript 教程](https://wangdoc.com/javascript/index.html)

这里只列出一些感兴趣的要点。

1. [导论](https://wangdoc.com/javascript/basic/introduction.html)

    - JavaScript 是一种轻量级的脚本语言。所谓“脚本语言”（script language），指的是它不具备开发操作系统的能力，而是只用来编写控制其他大型应用程序（比如浏览器）的“脚本”。

    - JavaScript 的核心语法部分相当精简，只包括两个部分：基本的语法构造（比如操作符、控制结构、语句）和标准库（就是一系列具有各种功能的对象比如Array、Date、Math等）。除此之外，各种宿主环境提供额外的 API（即只能在该环境使用的接口），以便 JavaScript 调用。以浏览器为例，它提供的额外 API 可以分成三大类。

      - 浏览器控制类：操作浏览器
      - DOM 类：操作网页的各种元素
      - Web 类：实现互联网的各种功能

    - 如果宿主环境是服务器，则会提供各种操作系统的 API，比如文件操作 API、网络通信 API等等。

    - JavaScript 甚至也可以用来操作数据库。NoSQL 数据库这个概念，本身就是在 JSON（JavaScript Object Notation）格式的基础上诞生的，大部分 NoSQL 数据库允许 JavaScript 直接操作。基于 SQL 语言的开源数据库 PostgreSQL 支持 JavaScript 作为操作语言，可以部分取代 SQL 查询语言。

    - JavaScript 语言本身，虽然是一种解释型语言，但是在现代浏览器中，JavaScript 都是**编译后运行**。程序会被高度优化，运行效率接近二进制程序。而且，JavaScript 引擎正在快速发展，性能将越来越好。

    - JavaScript 程序可以采用事件驱动（event-driven）和非阻塞式（non-blocking）设计，在服务器端适合高并发环境，普通的硬件就可以承受很大的访问量。

2. [JavaScript 语言的历史](https://wangdoc.com/javascript/basic/history.html)

    - 1990年底，欧洲核能研究组织（CERN）科学家 Tim Berners-Lee，在全世界最大的电脑网络——互联网的基础上，发明了万维网（World Wide Web），从此可以在网上浏览网页文件。

    - 1992年底，美国国家超级电脑应用中心（NCSA）开始开发一个独立的浏览器，叫做 Mosaic。这是人类历史上第一个浏览器，从此网页可以在图形界面的窗口浏览。

    - Netscape 公司很快发现，Navigator 浏览器需要一种可以嵌入网页的脚本语言，用来控制浏览器行为。当时，网速很慢而且上网费很贵，有些操作不宜在服务器端完成。比如，如果用户忘记填写“用户名”，就点了“发送”按钮，到服务器再发现这一点就有点太晚了，最好能在用户发出数据之前，就告诉用户“请填写用户名”。这就需要在网页中嵌入小程序，让浏览器检查每一栏是否都填写了。

    - Netscape 公司决定与 Sun 公司合作，浏览器支持嵌入 Java 小程序（后来称为 Java applet）。

    - 1995年，Netscape 公司雇佣了程序员 Brendan Eich 开发这种网页脚本语言。Brendan Eich 有很强的函数式编程背景，希望以 Scheme 语言（函数式语言鼻祖 LISP 语言的一种方言）为蓝本，实现这种新语言。

    - 1995年5月，Brendan Eich 只用了10天，就设计完成了这种语言的第一版。它是一个大杂烩，语法有多个来源。

      - 基本语法：借鉴 C 语言和 Java 语言。
      - 数据结构：借鉴 Java 语言，包括将值分成原始值和对象两大类。
      - 函数的用法：借鉴 Scheme 语言和 Awk 语言，将函数当作第一等公民，并引入闭包。
      - 原型继承模型：借鉴 Self 语言（Smalltalk 的一种变种）。
      - 正则表达式：借鉴 Perl 语言。
      - 字符串和数组处理：借鉴 Python 语言。

    - 为了保持简单，这种脚本语言缺少一些关键的功能，比如块级作用域、模块、子类型（subtyping）等等，但是可以利用现有功能找出解决办法。

    - 这种功能的不足，直接导致了后来 JavaScript 的一个显著特点：对于其他语言，你需要学习语言的各种功能，而对于 JavaScript，你常常需要学习各种解决问题的模式。

    - 由于来源多样，从一开始就注定，JavaScript 的编程风格是函数式编程和面向对象编程的一种混合体。

    - Netscape 公司的这种浏览器脚本语言，最初名字叫做 Mocha，1995年9月改为 LiveScript。12月，Netscape 公司与 Sun 公司（Java 语言的发明者和所有者）达成协议，后者允许将这种语言叫做 JavaScript。这样一来，Netscape 公司可以借助 Java 语言的声势，而 Sun 公司则将自己的影响力扩展到了浏览器。

    - JavaScript 这个名字的原意是“很像Java的脚本语言”。

    - JavaScript 语言的函数是一种独立的数据类型，以及采用基于原型对象（prototype）的继承链。这是它与 Java 语法最大的两点区别。JavaScript 语法要比 Java 自由得多。

    - 1997年7月，ECMA 组织发布262号标准文件（ECMA-262）的第一版，规定了浏览器脚本语言的标准，并将这种语言称为 ECMAScript。这个版本就是 ECMAScript 1.0 版。

    - ECMAScript 和 JavaScript 的关系是，前者是后者的规格，后者是前者的一种实现。
