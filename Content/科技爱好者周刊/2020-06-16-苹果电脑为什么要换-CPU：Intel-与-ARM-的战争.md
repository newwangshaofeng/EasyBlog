---
tags:
  - 科技爱好者周刊
---
Title: 苹果电脑为什么要换 CPU：Intel 与 ARM 的战争

URL Source: http://www.ruanyifeng.com/blog/2020/06/cpu-architecture.html

Markdown Content:
三个月前，新款 iPad Pro 发布，支持触摸板和鼠标。

![Image 1](https://www.wangbase.com/blogimg/asset/202006/bg2020061501.jpg)

上图的黑点就是鼠标。苹果公司显然打算，平板电脑当作笔记本使用。

我们知道，iPad 的操作系统跟 iPhone 是一样的，都是基于 iOS。如果 iOS 可以用于笔记本，就意味着可以跟桌面系统 MacOS 统一了。如果 MacBook 和 iPhone 都用同一个操作系统，App 就能通用了。

苹果公司显然也是这么打算的。几天后的6月22日将举行 WWDC（苹果全球开发者大会）。媒体报道，苹果公司将在那一天宣布，更换 Mac 电脑的 CPU，从 Intel 公司的 x86 架构改成 ARM 架构。

![Image 2](https://www.wangbase.com/blogimg/asset/202006/bg2020061521.jpg)

一旦 Mac 跟 iPhone 使用同样架构的 CPU，那就铺平了统一操作系统的道路。操作系统无法通用的最主要原因，就是 CPU 架构不同。

本文回顾苹果公司的 CPU 架构变化历史，帮助大家理解这件事的技术含义，以及未来的影响。

一、CPU 架构是什么
-----------

CPU 的全称是"中央处理单元"，它是计算机的核心，计算都由它来完成。但是，CPU 本身只是一个概念，每家芯片公司都有自己的具体实现。

**不同的 CPU 设计实现，就称为" CPU 架构"（CPU architecture）。** 不同的 CPU 架构有不同的指令集，彼此不通用，这导致运行在上面的软件也不兼容，必须重新编译。如果没有做适配，一个架构下的软件就无法移植到另一个架构。

![Image 3](https://www.wangbase.com/blogimg/asset/202006/bg2020061503.jpg)

历史上，有过[多种](https://www.quora.com/What-are-the-types-of-computer-architectures-in-a-CPU/answer/Gyanu-Kumar-27) CPU 架构。目前最常见的架构只剩下两种：x86 架构和 ARM 架构。

![Image 4](https://www.wangbase.com/blogimg/asset/202006/bg2020061504.jpg)

x86 架构性能好，但是耗电多、电压高，主要用于桌面电脑和服务器，生产厂商为 Intel 公司和 AMD 公司。ARM 架构耗电小、电压低，但是单核性能不如 x86，主要用于移动设备。

ARM 芯片的生产商有许多家，这是因为它的[商业模式](https://www.ruanyifeng.com/blog/2011/01/brief_history_of_arm.html)是授权制。英国的 ARM 公司出售指令集的授权，购买授权的公司可以基于公版的设计，开发自己的 ARM 芯片。高通、三星、华为、苹果等公司的芯片，都属于这个模式。

苹果公司同时使用这两种架构的芯片，iPhone 和 iPad 的芯片是 ARM 架构，Mac 电脑的芯片是 x86 架构，这导致 iPhone 的 App 无法在 Mac 电脑运行。

近几年，x86 架构发展迟缓，ARM 架构则进步显著，已经从移动设备向桌面电脑和服务器进军了。Mac 电脑这一次更换 CPU，就是准备从 x86 架构改为 ARM 架构。

二、Mac 电脑的 CPU 架构
----------------

历史上，Mac 电脑发生过两次 CPU 架构更改。

1984年，第一代 Macintosh 问世，CPU 是摩托罗拉公司的68000芯片。

1994年，摩托罗拉将68000芯片升级为 PowerPC 芯片，Mac 电脑跟着升级，这是第一次 CPU 架构更改。

2005年，乔布斯宣布，Mac 电脑将放弃 PowerPC 芯片，改用 Intel 公司的 x86 CPU。这是第二次架构更改。

![Image 5](https://www.wangbase.com/blogimg/asset/202006/bg2020061507.jpg)

那次架构更改，主要有两个原因。一是 Intel 的 CPU 比 PowerPC 性能强，并且由于产量大，价格也便宜。二是 Windows 电脑使用的是 x86 芯片，改了架构以后，Mac 电脑就也能安装 Windows，做到"一机双系统"。这可以促进当时处于市场劣势的 Mac 的销售。

乔布斯用特有的极具煽动力的语言，这样解释："最重要的原因是，向前看时......我们想象了各种我们希望为你打造的惊人产品，但是我们不知道如何使用 PowerPC 来实现它们。"

三、第三次架构更改的背景
------------

15年过去了，情况发生了很大的变化。

Mac 的 CPU 架构跟 Windows 保持一致，已经不构成吸引力了。据统计，2010年15％的消费者购买 Mac 电脑后，会安装双系统，今天只剩下了2％。大多数用户购买 Mac 电脑，根本没想过安装 Windows，或者运行 Windows 特有的软件。此外，虽然 CPU 架构一致，但是 Windows 的游戏软件并没有移植到 Mac 电脑，游戏开发商依然不支持 Mac。

更大的市场变化是，消费者和技术投资的主流已经转向了移动设备， 桌面设备已经不那么重要了。

![Image 6](https://www.wangbase.com/blogimg/asset/202006/bg2020061508.jpg)

苹果公司的主要业务和利润来源，现在都来自移动领域，iPhone 的市场规模已经远远大于 Mac。所有的移动设备使用的都是 ARM 芯片，苹果的投资和技术成果也主要在这个领域，而不是在 x86 相关领域。

苹果正在围绕移动设备，重塑它的战略。它的软件工具（LLVM 编译器、Swift 语言、Xcode 开发工具、App Store 商店）和硬件设备（Apple Watch、AirPods 等），都是围绕 iPhone 开发的。桌面设备已经不是这个战略的重点了。

这就是 Mac 第三次更换 CPU 架构的背景。

四、Intel 的失败
-----------

Mac 电脑更换 CPU 架构，也与 Intel 公司多年来创新乏力、产品没有突破有关。

2007年推出 iPhone 之前，苹果曾希望使用 Intel 的 ARM 芯片 XScale 作为手机的 CPU。但是，英特尔当时的 CEO 保罗·欧德宁，不看好苹果的这个项目，而且也不愿意在 ARM 芯片上投资，最后不仅放过了 iPhone，还将 XScale 产品线卖给了 Marvell 公司。

后来的历史证明，这是一个灾难级别的错误，iPhone 取得了辉煌的成功。英特尔这下急了，又反过来开发基于 x86 架构的移动设备 CPU，就是 Atom 芯片。但是，苹果没有在手机上再给 Intel 机会，x86 架构也被证明不适合手机，Atom 没有成功。

![Image 7](https://www.wangbase.com/blogimg/asset/202006/bg2020061509.jpg)

Intel 在手机业务上失败，在桌面业务上则陷入停滞。MacBook Pro 的 CPU， 2010年是2核的 2.66 GHz 的 i7，2020年是8核的 2.6 GHz 的 i9，过去10年基本上只是改进了工艺，增加了核心数量，没有实质的重大突破。除了性能以外，苹果最在意的两点----功率和散热---- Intel 也没有解决。

对于苹果来说，Intel 的 x86 CPU 早就不是 Mac 电脑的卖点了，反而成了拖慢创新的障碍，使苹果在 CPU 这个核心设备上受制于 Intel。

五、苹果自己的 ARM 芯片
--------------

iPhone 的前三代---- iPhone、iPhone 3G、iPhone 3GS-------- CPU 是三星的。但是，苹果从一开始就打算推出自己的芯片，因为 ARM 采用授权模式，只要购买授权，就可以添加自己的设计，然后再让三星代工生产。

2010年发布的 iPhone 4，第一次采用苹果自己设计的 CPU，名称是 Apple A4。

![Image 8](https://www.wangbase.com/blogimg/asset/202006/bg2020061510.jpg)

大概从 A4 发布的这一天开始，苹果就有用自己的芯片替换 Intel 的打算了。因为当年推出的 Apple TV 第二代，也用了 A4 芯片。但是，Apple TV 第一代用的是 Intel 的 x86 芯片，被做成缩小版的 Mac。到了第二代，CPU 改了以后，就变成 iOS 设备。

Apple TV 这种设备使用 x86 芯片，根本没有获得任何好处。因为它不需要考虑 Windows 兼容性，也不需要很强的性能。另一方面，使用 ARM 芯片以后，功耗和散热都变小了，价格也降下来，从229美元变成了99美元。下图是 Apple TV 第一代和第二代的大小对比。

![Image 9](https://www.wangbase.com/blogimg/asset/202006/bg2020061511.jpg)

此后，苹果一直在加强芯片研究，每一代 iPhone 用的都是苹果自己的 CPU，从 iPhone 4S 的 A5 到最新 iPhone 11 的 A13。现在的苹果芯片在效能、功耗和功能各方面，都属于世界顶尖级别的 ARM 芯片。

![Image 10](https://www.wangbase.com/blogimg/asset/202006/bg2020061512.jpg)

目前，Mac 电脑是唯一使用 x86 芯片的苹果设备，其他的所有设备（iPhone、iPad、Apple TV、Apple Watch、Airpods）用的都是苹果自己设计的 ARM 芯片。

六、更换 CPU 架构的好处
--------------

几天后的 WWDC 2020，可能就会宣布采用 A14 芯片的 MacBook 笔记本。这个转变不是突如其来，而是很久之前就开始了，苹果早就尝试在 MacBook 里面加入 ARM 芯片，把自己在 iPhone 的技术积累引入 Mac。

2016年，苹果在 MacBook Pro 里面加了一块自己设计的 Apple T1 芯片，把 TouchID、FaceTime、TouchBar 等功都做进去了，让这块 ARM 芯片分担一些 Intel CPU 的工作。

2018年，苹果又推出了 Apple T2。这块芯片跟 iPhone 7 的 A10 基本一致，比上一代有更强的运算能力，加入了更多的功能，比如硬件加速、媒体编解码、Siri 支持等。

![Image 11](https://www.wangbase.com/blogimg/asset/202006/bg2020061513.jpg)

可以想象，如果笔记本的整个 CPU 都由苹果自己设计，一定会有更多的功能集成进来，苹果手机的安全特性、图形支持、视频处理、音频处理、加密解密、人工智能都可以放进桌面设备。苹果也能对它进行更好的优化，批量生产，降低成本。

一旦苹果可以控制芯片、硬件、软件整个堆栈，就能让它们更好的协同，创造出更多多令人激动的新功能。

Mac 电脑采用 ARM 架构后，还能实现统一的 Apple 生态，而不是现在分隔开来的 Mac 生态和 iPhone/iPad 生态。不同设备都有同样的架构，运行同样的程序，差别只是外形尺寸与性能。

七、过渡安排
------

2018年，苹果宣布了 [Project Catalyst](https://developer.apple.com/mac-catalyst/) 项目，可以将 iPhone 和 iPad 应用自动转为 Mac 应用，反之则不行。现在看来，这个项目就是为移动应用移植到桌面电脑做准备。苹果的目标就是，同一个 App 最终可以在 iPhone、iPad 和 Mac 上运行。

苹果应该不可能把现在的桌面型号，一下子就升级为 ARM 架构。很多人猜测，它会先推出一款12吋的、采用 ARM CPU 的 MacBook。这样比较保险，因为笔记本不需要特别强劲的性能，也不需要扩充卡，不会影响到那些需要高性能、大量外围设备、或依赖旧软件的用户。而且，降低功耗对笔记本特别重要，因为可以延长电池寿命。

回顾历史，Mac 电脑从 PowerPC 转为 x86 架构，整整花了6年。2005年的 Mac OS X 10.4版（Tiger）同时有 PowerPC 和 Intel 两个版本，2011年的 Mac OS X 10.7 （Lion）才不再支持 PowerPC。这次从 x86 转为 ARM 架构，估计也需要同样长的时间，即将面世的 Mac OS X 10.16 可能也有 x86 和 ARM 两个版本。现有桌面设备（MacBook Pro 和 Mac Pro）的 ARM 升级版，可能要等到2022年才会问世。

（完）
