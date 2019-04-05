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

    - 2015年6月，ECMAScript 6 正式发布，并且更名为“ECMAScript 2015”。

    - 1996年，样式表标准 CSS 第一版发布。

    - 1997年，DHTML（Dynamic HTML，动态 HTML）发布，允许动态改变网页内容。这标志着 DOM 模式（Document Object Model，文档对象模型）正式应用。

    - 1999年，IE 5部署了 XMLHttpRequest 接口，允许 JavaScript 发出 HTTP 请求，为后来大行其道的 Ajax 应用创造了条件。

    - 2001年，Douglas Crockford 提出了 JSON 格式，用于取代 XML 格式，进行服务器和网页之间的数据交换。JavaScript 可以原生支持这种格式，不需要额外部署代码。

    - 2004年，Google 公司发布了 Gmail，促成了互联网应用程序（Web Application）这个概念的诞生。由于 Gmail 是在4月1日发布的，很多人起初以为这只是一个玩笑。

    - 2005年，Ajax 方法（Asynchronous JavaScript and XML）正式诞生，Jesse James Garrett 发明了这个词汇。它开始流行的标志是，2月份发布的 Google Maps 项目大量采用该方法。它几乎成了新一代网站的标准做法，促成了 Web 2.0时代的来临。

    - 2006年，jQuery 函数库诞生，作者为John Resig。jQuery 为操作网页 DOM 结构提供了非常强大易用的接口，成为了使用最广泛的函数库，并且让 JavaScript 语言的应用难度大大降低，推动了这种语言的流行。

    - 2008年，V8 编译器诞生。这是 Google 公司为 Chrome 浏览器而开发的，它的特点是让 JavaScript 的运行变得非常快。它提高了 JavaScript 的性能，推动了语法的改进和标准化，改变外界对 JavaScript 的不佳印象。同时，V8 是开源的，任何人想要一种快速的嵌入式脚本语言，都可以采用 V8，这拓展了 JavaScript 的应用领域。

    - 2009年，Node.js 项目诞生，创始人为 Ryan Dahl，它标志着 JavaScript 可以用于服务器端编程，从此网站的前端和后端可以使用同一种语言开发。并且，Node.js 可以承受很大的并发流量，使得开发某些互联网大规模的实时应用变得容易。

    - 2010年，三个重要的项目诞生，分别是 NPM、BackboneJS 和 RequireJS，标志着 JavaScript 进入模块化开发的时代。

    - 2011年，Google 发布了 Dart 语言，目的是为了结束 JavaScript 语言在浏览器中的垄断，提供更合理、更强大的语法和功能。Chromium浏览器有内置的 Dart 虚拟机，可以运行 Dart 程序，但 Dart 程序也可以被编译成 JavaScript 程序运行。

    - 2012年，微软发布 TypeScript 语言。该语言被设计成 JavaScript 的超集，这意味着所有 JavaScript 程序，都可以不经修改地在 TypeScript 中运行。同时，TypeScript 添加了很多新的语法特性，主要目的是为了开发大型程序，然后还可以被编译成 JavaScript 运行。

    - 2013年5月，Facebook 发布 UI 框架库 React，引入了新的 JSX 语法，使得 UI 层可以用组件开发，同时引入了网页应用是状态机的概念。

    - 2015年3月，Facebook 公司发布了 React Native 项目，将 React 框架移植到了手机端，可以用来开发手机 App。它会将 JavaScript 代码转为 iOS 平台的 Objective-C 代码，或者 Android 平台的 Java 代码，从而为 JavaScript 语言开发高性能的原生 App 打开了一条道路。

    - 2015年5月，Node 模块管理器 NPM 超越 CPAN，标志着 JavaScript 成为世界上软件模块最多的语言。

    - 2015年6月，ECMA 标准化组织正式批准了 ECMAScript 6 语言标准，定名为《ECMAScript 2015 标准》。JavaScript 语言正式进入了下一个阶段，成为一种企业级的、开发大规模应用的语言。这个标准从提出到批准，历时10年，而 JavaScript 语言从诞生至今也已经20年了。

    - 2017年6月，《ECMAScript 2017 标准》发布，正式引入了 async 函数，使得异步操作的写法出现了根本的变化。

    - 2017年11月，所有主流浏览器全部支持 WebAssembly，这意味着任何语言都可以编译成 JavaScript，在浏览器运行。

3. [JavaScript 的基本语法](https://wangdoc.com/javascript/basic/grammar.html)

    - 语句和表达式的区别在于，前者主要为了进行某种操作，一般情况下不需要返回值；后者则是为了得到返回值，一定会返回一个值。

    - 如果只是声明变量而没有赋值，则该变量的值是undefined。undefined是一个特殊的值，表示“无定义”。

    - JavaScript 引擎的工作方式是，先解析代码，获取所有被声明的变量，然后再一行一行地运行。这造成的结果，就是所有的变量的声明语句，都会被提升到代码的头部，这就叫做变量提升（hoisting）。

        ```js
        console.log(a);
        var a = 1;
        ```

    - JavaScript 有一些保留字，不能用作标识符：arguments、break、case、catch、class、const、continue、debugger、default、delete、do、else、enum、eval、export、extends、false、finally、for、function、if、implements、import、in、instanceof、interface、let、new、null、package、private、protected、public、return、static、super、switch、this、throw、true、try、typeof、var、void、while、with、yield。

    - 对于var命令来说，JavaScript 的区块不构成单独的作用域（scope）。

        ```js
        {
          var a = 1;
        }

        a // 1
        ```

        如果使用**let**的话则与其他语言传统一致。

        ```js
        {
          let b = 1;
        }

        b // Uncaught ReferenceError: b is not defined
        ```

    - 多个if...else连在一起使用的时候，可以转为使用更方便的switch结构。

        ```js
        switch (fruit) {
          case "banana":
            // ...
            break;
          case "apple":
            // ...
            break;
          default:
            // ...
        }
        ```

        ```text
        与C语言等规则相反，Go语言不需要用break来明确退出一个case
        ```

    - switch语句部分和case语句部分，都可以使用表达式。

        ```js
        switch (1 + 3) {
          case 2 + 2:
            f();
            break;
          default:
            neverHappens();
        }
        ```

    - 需要注意的是，switch语句后面的表达式，与case语句后面的表示式比较运行结果时，采用的是严格相等运算符（===），而不是相等运算符（==），这意味着比较时不会发生类型转换。

    - 标签通常与break语句和continue语句配合使用，跳出特定的循环。

        ```js
        top:
          for (var i = 0; i < 3; i++){
            for (var j = 0; j < 3; j++){
              if (i === 1 && j === 1) break top;
              console.log('i=' + i + ', j=' + j);
            }
          }
        // i=0, j=0
        // i=0, j=1
        // i=0, j=2
        // i=1, j=0
        ```

        ```js
        foo: {
          console.log(1);
          break foo;
          console.log('本行不会输出');
        }
        console.log(2);
        // 1
        // 2
        ```

    - continue语句也可以与标签配合使用。

        ```js
        top:
          for (var i = 0; i < 3; i++){
            for (var j = 0; j < 3; j++){
              if (i === 1 && j === 1) continue top;
              console.log('i=' + i + ', j=' + j);
            }
          }
        // i=0, j=0
        // i=0, j=1
        // i=0, j=2
        // i=1, j=0
        // i=2, j=0
        // i=2, j=1
        // i=2, j=2
        ```

        上面代码中，continue命令后面有一个标签名，满足条件时，会跳过当前循环，直接进入下一轮外层循环。如果continue语句后面不使用标签，则只能进入下一轮的内层循环。

4. [数据类型概述](https://wangdoc.com/javascript/types/general.html)

    - JavaScript 语言的每一个值，都属于某一种数据类型。JavaScript 的数据类型，共有六种。（ES6 又新增了第七种 Symbol 类型的值，本教程不涉及。）

      - 数值（number）：整数和小数（比如1和3.14）
      - 字符串（string）：文本（比如Hello World）。
      - 布尔值（boolean）：表示真伪的两个特殊值，即true（真）和false（假）
      - undefined：表示“未定义”或不存在，即由于目前没有定义，所以此处暂时没有任何值
      - null：表示空值，即此处的值为空。
      - 对象（object）：各种值组成的集合。

    - 通常，数值、字符串、布尔值这三种类型，合称为原始类型（primitive type）的值，即它们是最基本的数据类型，不能再细分了。对象则称为合成类型（complex type）的值，因为一个对象往往是多个原始类型的值的合成，可以看作是一个存放各种值的容器。至于undefined和null，一般将它们看成两个特殊值。

    - 对象是最复杂的数据类型，又可以分成三个子类型。

      - 狭义的对象（object）
      - 数组（array）
      - 函数（function）

    - 函数其实是处理数据的方法，JavaScript 把它当成一种数据类型，可以赋值给变量，这为编程带来了很大的灵活性，也为 JavaScript 的“函数式编程”奠定了基础。

    - JavaScript 有三种方法，可以确定一个值到底是什么类型。

      - typeof运算符
      - instanceof运算符
      - Object.prototype.toString方法

    - typeof运算符可以返回一个值的数据类型。

    - 数值、字符串、布尔值分别返回number、string、boolean。

        ```js
        typeof 123 // "number"
        typeof '123' // "string"
        typeof false // "boolean"
        ```

    - 函数返回function。

        ```js
        function f() {}
        typeof f
        // "function"
        ```

    - undefined返回undefined。

        ```js
        typeof undefined
        // "undefined"
        ```

    - 利用这一点，typeof可以用来检查一个没有声明的变量，而不报错。

        ```js
        v
        // ReferenceError: v is not defined

        typeof v
        // "undefined"
        ```

        上面代码中，变量v没有用var命令声明，直接使用就会报错。但是，放在typeof后面，就不报错了，而是返回undefined。

        实际编程中，这个特点通常用在判断语句。

        ```js
        // 错误的写法
        if (v) {
          // ...
        }
        // ReferenceError: v is not defined

        // 正确的写法
        if (typeof v === "undefined") {
          // ...
        }
        ```

    - 对象返回object。

        ```js
        typeof window // "object"
        typeof {} // "object"
        typeof [] // "object"
        ```

    - instanceof运算符可以区分数组和对象。

        ```js
        var o = {};
        var a = [];

        o instanceof Array // false
        a instanceof Array // true
        ```

    - null返回object。

        ```js
        typeof null // "object"
        ```

        null的类型是object，这是由于历史原因造成的。1995年的 JavaScript 语言第一版，只设计了五种数据类型（对象、整数、浮点数、字符串和布尔值），没考虑null，只把它当作object的一种特殊值。后来null独立出来，作为一种单独的数据类型，为了兼容以前的代码，typeof null返回object就没法改变了。

5. [null, undefined 和布尔值](https://wangdoc.com/javascript/types/null-undefined-boolean.html)

    - null与undefined都可以表示“没有”，含义非常相似。将一个变量赋值为undefined或null，老实说，语法效果几乎没区别。

    - 在if语句中，它们都会被自动转为false，相等运算符（==）甚至直接报告两者相等。

    - 谷歌公司开发的 JavaScript 语言的替代品 Dart 语言，就明确规定只有null，没有undefined！

    - 根据 C 语言的传统，null可以自动转为0。

        ```js
        Number(null) // 0
        5 + null // 5
        ```

    - 那时的 JavaScript 不包括错误处理机制，Brendan Eich 觉得，如果null自动转为0，很不容易发现错误。因此，他又设计了一个undefined。区别是这样的：null是一个表示“空”的对象，转为数值时为0；undefined是一个表示"此处无定义"的原始值，转为数值时为NaN。

        ```js
        Number(undefined) // NaN
        5 + undefined // NaN
        ```

    - null表示空值，即该处的值现在为空。调用函数时，某个参数未设置任何值，这时就可以传入null，表示该参数为空。

    - undefined表示“未定义”，下面是返回undefined的典型场景。

        ```js
        // 变量声明了，但没有赋值
        var i;
        i // undefined

        // 调用函数时，应该提供的参数没有提供，该参数等于 undefined
        function f(x) {
          return x;
        }
        f() // undefined

        // 对象没有赋值的属性
        var  o = new Object();
        o.p // undefined

        // 函数没有返回值时，默认返回 undefined
        function f() {}
        f() // undefined
        ```

    - 如果 JavaScript 预期某个位置应该是布尔值，会将该位置上现有的值自动转为布尔值。转换规则是除了下面六个值被转为false，其他值都视为true。

        ```js
        undefined
        null
        false
        0
        NaN
        ""或''（空字符串）
        ```

    - 注意，空数组（[]）和空对象（{}）对应的布尔值，都是true。

        ```js
        if ([]) {
          console.log('true');
        }
        // true

        if ({}) {
          console.log('true');
        }
        // true
        ```

6. [数值](https://wangdoc.com/javascript/types/number.html)

    - JavaScript 内部，所有数字都是以64位浮点数形式储存，即使整数也是如此。所以，1与1.0是相同的，是同一个数。

        ```js
        1 === 1.0 // true
        ```

    - 由于浮点数不是精确的值，所以涉及小数的比较和运算要特别小心。

        ```js
        0.1 + 0.2 === 0.3
        // false

        0.3 / 0.1
        // 2.9999999999999996

        (0.3 - 0.2) === (0.2 - 0.1)
        // false
        ```

    - 大于2的53次方以后，整数运算的结果开始出现错误。所以，大于2的53次方的数值，都无法保持精度。

        ```js
        Math.pow(2, 53)
        // 9007199254740992

        Math.pow(2, 53) + 1
        // 9007199254740992

        Math.pow(2, 53) + 2
        // 9007199254740994

        Math.pow(2, 53) + 3
        // 9007199254740996

        Math.pow(2, 53) + 4
        // 9007199254740996
        ```

    - JavaScript 对15位的十进制数都可以精确处理。

    - JavaScript 能够表示的数值范围为21024到2-1023（开区间），超出这个范围的数无法表示。

    - 如果一个数大于等于2的1024次方，那么就会发生“正向溢出”，即 JavaScript 无法表示这么大的数，这时就会返回Infinity。

        ```js
        Math.pow(2, 1024) // Infinity
        ```

    - 如果一个数小于等于2的-1075次方（指数部分最小值-1023，再加上小数部分的52位），那么就会发生为“负向溢出”，即 JavaScript 无法表示这么小的数，这时会直接返回0。

        ```js
        Math.pow(2, -1075) // 0
        ```

    - JavaScript 提供Number对象的MAX_VALUE和MIN_VALUE属性，返回可以表示的具体的最大值和最小值。

        ```js
        Number.MAX_VALUE // 1.7976931348623157e+308
        Number.MIN_VALUE // 5e-324
        ```

    - 以下两种情况，JavaScript 会自动将数值转为科学计数法表示，其他情况都采用字面形式直接表示。

        （1）小数点前的数字多于21位。
        （2）小数点后的零多于5个。

    - 使用字面量（literal）直接表示一个数值时，JavaScript 对整数提供四种进制的表示方法：十进制、十六进制、八进制、二进制。

      - 十进制：没有前导0的数值。
      - 八进制：有前缀0o或0O的数值，或者有前导0、且只用到0-7的八个阿拉伯数字的数值。
      - 十六进制：有前缀0x或0X的数值。
      - 二进制：有前缀0b或0B的数值。

    - 几乎所有场合，正零和负零都会被当作正常的0。唯一有区别的场合是，+0或-0当作分母，返回的值是不相等的。

        ```js
        (1 / +0) === (1 / -0) // false
        ```

        上面的代码之所以出现这样结果，是因为除以正零得到+Infinity，除以负零得到-Infinity，这两者是不相等的。

    - NaN是 JavaScript 的特殊值，表示“非数字”（Not a Number），主要出现在将字符串解析成数字出错的场合。

    - NaN不等于任何值，包括它本身。

        ```js
        NaN === NaN // false
        ```

    - 数组的indexOf方法内部使用的是严格相等运算符，所以该方法对NaN不成立。

        ```js
        [NaN].indexOf(NaN) // -1
        ```

    - 由于数值正向溢出（overflow）、负向溢出（underflow）和被0除，JavaScript 都不报错，所以单纯的数学运算几乎没有可能抛出错误。

    - Infinity与NaN比较，总是返回false。

        ```js
        Infinity > NaN // false
        -Infinity > NaN // false

        Infinity < NaN // false
        -Infinity < NaN // false
        ```

    - Infinity的四则运算，符合无穷的数学计算规则。

        ```js
        5 * Infinity // Infinity
        5 - Infinity // -Infinity
        Infinity / 5 // Infinity
        5 / Infinity // 0
        ```

    - parseInt方法用于将字符串转为整数。字符串转为整数的时候，是一个个字符依次转换，如果遇到不能转为数字的字符，就不再进行下去，返回已经转好的部分。

        ```js
        parseInt('8a') // 8
        parseInt('12**') // 12
        parseInt('12.34') // 12
        parseInt('15e2') // 15
        parseInt('15px') // 15
        ```

    - 如果parseInt的参数不是字符串，则会先转为字符串再转换。

    - 对于那些会自动转为科学计数法的数字，parseInt会将科学计数法的表示方法视为字符串，因此导致一些奇怪的结果。

        ```js
        parseInt(1000000000000000000000.5) // 1
        // 等同于
        parseInt('1e+21') // 1

        parseInt(0.0000008) // 8
        // 等同于
        parseInt('8e-7') // 8
        ```

    - parseInt方法还可以接受第二个参数（2到36之间），表示被解析的值的进制，返回该值对应的十进制数。默认情况下，parseInt的第二个参数为10，即默认是十进制转十进制。

    - parseFloat方法用于将一个字符串转为浮点数。

    - parseFloat的转换结果不同于Number函数。

        ```js
        parseFloat(true)  // NaN
        Number(true) // 1

        parseFloat(null) // NaN
        Number(null) // 0

        parseFloat('') // NaN
        Number('') // 0

        parseFloat('123.45#') // 123.45
        Number('123.45#') // NaN
        ```

    - isNaN方法可以用来判断一个值是否为NaN。

    - isNaN只对数值有效，如果传入其他值，会被先转成数值。比如，传入字符串的时候，字符串会被先转成NaN，所以最后返回true，这一点要特别引起注意。

    - 对于对象和数组，isNaN也返回true。但是，对于空数组和只有一个数值成员的数组，isNaN返回false。

        ```js
        isNaN('Hello') // true
        // 相当于
        isNaN(Number('Hello')) // true

        isNaN({}) // true
        // 等同于
        isNaN(Number({})) // true

        isNaN(['xzy']) // true
        // 等同于
        isNaN(Number(['xzy'])) // true

        isNaN([]) // false
        isNaN([123]) // false
        isNaN(['123']) // false
        ```

    - 判断NaN更可靠的方法是，利用NaN为唯一不等于自身的值的这个特点，进行判断。

        ```js
        function myIsNaN(value) {
          return value !== value;
        }
        ```

    - isFinite方法返回一个布尔值，表示某个值是否为正常的数值。

        ```js
        isFinite(Infinity) // false
        isFinite(-Infinity) // false
        isFinite(NaN) // false
        isFinite(undefined) // false
        isFinite(null) // true
        isFinite(-1) // true
        ```

        除了Infinity、-Infinity、NaN和undefined这几个值会返回false，isFinite对于其他的数值都会返回true。

7. [字符串](https://wangdoc.com/javascript/types/string.html)

    - 由于 HTML 语言的属性值使用双引号，所以很多项目约定 JavaScript 语言的字符串只使用单引号。

    - 字符串可以被视为字符数组，因此可以使用数组的方括号运算符，用来返回某个位置的字符（位置编号从0开始）。

        ```js
        var s = 'hello';
        s[0] // "h"
        s[1] // "e"
        s[4] // "o"

        // 直接对字符串使用方括号运算符
        'hello'[1] // "e"
        ```

    - 字符串与数组的相似性仅此而已。实际上，无法改变字符串之中的单个字符。

        ```js
        var s = 'hello';

        delete s[0];
        s // "hello"

        s[1] = 'a';
        s // "hello"

        s[5] = '!';
        s // "hello"
        ```

    - length属性返回字符串的长度。

    - 每个字符在 JavaScript 内部都是以16位（即2个字节）的 UTF-16 格式储存。也就是说，JavaScript 的单位字符长度固定为16位长度，即2个字节。

    - 但是，UTF-16 有两种长度：对于码点在U+0000到U+FFFF之间的字符，长度为16位（即2个字节）；对于码点在U+10000到U+10FFFF之间的字符，长度为32位（即4个字节），而且前两个字节在0xD800到0xDBFF之间，后两个字节在0xDC00到0xDFFF之间。

    - JavaScript 对 UTF-16 的支持是不完整的，由于历史原因，只支持两字节的字符，不支持四字节的字符。这是因为 JavaScript 第一版发布的时候，Unicode 的码点只编到U+FFFF，因此两字节足够表示了。后来，Unicode 纳入的字符越来越多，出现了四字节的编码。但是，JavaScript 的标准此时已经定型了，统一将字符长度限制在两字节，导致无法识别四字节的字符。

    - 对于码点在U+10000到U+10FFFF之间的字符，JavaScript 总是认为它们是两个字符（length属性为2）。所以处理的时候，必须把这一点考虑在内，也就是说，JavaScript 返回的字符串长度可能是不正确的。

    - 所谓 Base64 就是一种编码方法，可以将任意值转成 0～9、A～Z、a-z、+和/这64个字符组成的可打印字符。使用它的主要目的，不是为了加密，而是为了不出现特殊字符，简化程序的处理

8. [对象](https://wangdoc.com/javascript/types/object.html)

    - 对象（object）是 JavaScript 语言的核心概念，也是最重要的数据类型。

    - 对象的所有键名都是字符串（ES6 又引入了 Symbol 值也可以作为键名），所以加不加引号都可以。

    - 如果键名是数值，会被自动转为字符串。

    - 对象的每一个键名又称为“属性”（property），它的“键值”可以是任何数据类型。如果一个属性的值为函数，通常把这个属性称为“方法”，它可以像函数那样调用。

    - 对象采用大括号表示，这导致了一个问题：如果行首是一个大括号，它到底是表达式还是语句？

        ```js
        { foo: 123 }
        ```

        为了避免这种歧义，JavaScript 引擎的做法是，如果遇到这种情况，无法确定是对象还是代码块，一律解释为代码块。

        如果要解释为对象，最好在大括号前加上圆括号。因为圆括号的里面，只能是表达式，所以确保大括号只能解释为对象。

        这种差异在eval语句（作用是对字符串求值）中反映得最明显。

        ```js
        eval('{foo: 123}') // 123
        eval('({foo: 123})') // {foo: 123}
        ```

        上面代码中，如果没有圆括号，eval将其理解为一个代码块；加上圆括号以后，就理解成一个对象。

    - 读取对象的属性，有两种方法，一种是使用点运算符，还有一种是使用方括号运算符。

        ```js
        var obj = {
          p: 'Hello World'
        };

        obj.p // "Hello World"
        obj['p'] // "Hello World"
        ```

    - 数字键可以不加引号，因为会自动转成字符串。

        ```js
        var obj = {
          0.7: 'Hello World'
        };

        obj['0.7'] // "Hello World"
        obj[0.7] // "Hello World"
        ```

    - 点运算符和方括号运算符，不仅可以用来读取值，还可以用来赋值。

        ```js
        var obj = {};

        obj.foo = 'Hello';
        obj['bar'] = 'World';
        ```

    - 查看一个对象本身的所有属性，可以使用Object.keys方法。

    - delete命令用于删除对象的属性，删除成功后返回true。

    - 只有一种情况，delete命令会返回false，那就是该属性存在，且不得删除。

        ```js
        var obj = Object.defineProperty({}, 'p', {
          value: 123,
          configurable: false
        });

        obj.p // 123
        delete obj.p // false
        ```

    - in运算符用于检查对象是否包含某个属性（注意，检查的是键名，不是键值），如果包含就返回true，否则返回false。它的左边是一个字符串，表示属性名，右边是一个对象。

        ```js
        var obj = { p: 1 };
        'p' in obj // true
        'toString' in obj // true
        ```

    - in运算符的一个问题是，它不能识别哪些属性是对象自身的，哪些属性是继承的。就像上面代码中，对象obj本身并没有toString属性，但是in运算符会返回true，因为这个属性是继承的。

        这时，可以使用对象的hasOwnProperty方法判断一下，是否为对象自身的属性。

    - for...in循环用来遍历一个对象的全部属性。

    - for...in循环有两个使用注意点。

      - 它遍历的是对象所有可遍历（enumerable）的属性，会跳过不可遍历的属性。
      - 它不仅遍历对象自身的属性，还遍历继承的属性。

    - 对象都继承了toString属性，但是for...in循环不会遍历到这个属性。

    - 如果继承的属性是可遍历的，那么就会被for...in循环遍历到。但是，一般情况下，都是只想遍历对象自身的属性，所以使用for...in的时候，应该结合使用hasOwnProperty方法，在循环内部判断一下，某个属性是否为对象自身的属性。

        ```js
        var person = { name: '老张' };

        for (var key in person) {
          if (person.hasOwnProperty(key)) {
            console.log(key);
          }
        }
        // name
        ```

    - with语句的作用是操作同一个对象的多个属性时，提供一些书写的方便。

        ```js
        // 例一
        var obj = {
          p1: 1,
          p2: 2,
        };
        with (obj) {
          p1 = 4;
          p2 = 5;
        }
        // 等同于
        obj.p1 = 4;
        obj.p2 = 5;

        // 例二
        with (document.links[0]){
          console.log(href);
          console.log(title);
          console.log(style);
        }
        // 等同于
        console.log(document.links[0].href);
        console.log(document.links[0].title);
        console.log(document.links[0].style);
        ```

    - 注意，如果with区块内部有变量的赋值操作，必须是当前对象已经存在的属性，否则会创造一个当前作用域的全局变量。

        ```js
        var obj = {};
        with (obj) {
          p1 = 4;
          p2 = 5;
        }

        obj.p1 // undefined
        p1 // 4
        ```

    - 因为with区块没有改变作用域，它的内部依然是当前作用域。这造成了with语句的一个很大的弊病，就是绑定对象不明确。

        ```js
        with (obj) {
          console.log(x);
        }
        ```

        单纯从上面的代码块，根本无法判断x到底是全局变量，还是对象obj的一个属性。这非常不利于代码的除错和模块化，编译器也无法对这段代码进行优化，只能留到运行时判断，这就拖慢了运行速度。因此，建议不要使用with语句，可以考虑用一个临时变量代替with。

        ```js
        with(obj1.obj2.obj3) {
          console.log(p1 + p2);
        }

        // 可以写成
        var temp = obj1.obj2.obj3;
        console.log(temp.p1 + temp.p2);
        ```

9. [函数](https://wangdoc.com/javascript/types/function.html)
