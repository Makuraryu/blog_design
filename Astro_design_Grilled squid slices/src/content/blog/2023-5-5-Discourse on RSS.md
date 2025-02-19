---
title: '浅谈RSS技术'
description: ''
pubDate: 2023-5-5
tags: ['技术']
---

我们普遍的称这个时代叫“信息时代”，我想这的确没错：现实的世界越来越不重要，而信息化的世界却作为另一种符号体系充斥我们的大脑。然而，这不单单是媒介与形式的转换，更是我们认识世界的方式转换。信息的流转增快，数据的流量增大，我们从未如此目不暇接地吸纳世界图像，一切都爆炸般在我们的思想中展开，我们更是以赤身裸体的方式接纳这个世界，史无前例的将绝对的私人生活暴露给他人……但这不是我们所生活的地方，这本不是我们的生活方式，并不被作为一个物质性生物的我们所适应，不是吗？当然大多数人不那么觉得，因为这太过愉悦（愉悦的原因不在此详谈），但这样的危害早就暴漏无疑：我们无法深入地考察世界，我们的情绪也以一种原始的姿态爆发，我们的时间仿佛被偷走一般消失……我很难想象有什么样的生活方式比这更加糟糕。这不是我们的错，这是来自现代性的入侵！我的直觉早早地高声疾呼：捍卫我们的生活方式！而有那么一种“武器”，RSS(Really Simple Syndication)，早就等在那里了。

# 什么是RSS

> RSS（英文全称：RDF Site Summary 或 Really Simple Syndication），中文译作简易资讯聚合，也称聚合内容，是一种消息来源格式规范，用以聚合多个网站更新的内容并自动通知网站订阅者。使用 RSS 后，网站订阅者便无需再手动查看网站是否有新的内容，同时 RSS 可将多个网站更新的内容进行整合，以摘要的形式呈现，有助于订阅者快速获取重要信息，并选择性地点阅查看。

这是[维基百科](https://zh.wikipedia.org/wiki/RSS)上对RSS的定义，简单来说，RSS就是一种使用应用通过链接订阅网站，并整合在一起的技术手段。比如我的网站，点击页面底部的“订阅”添加（或者右击复制链接），使用[innoreader](https://www.innoreader.com)这一网站订阅，就像这个样子：

![p9UUdhT.png](https://s1.ax1x.com/2023/05/05/p9UUdhT.png)

# RSS的价值

这样一种技术，首先就其名称而言就显而易见一种价值：聚合信息。因为不同的平台总是有着不同的倾向和受众，再加上各种反垄断政策，一定不会存在一个集合所有媒体的平台，而任何一个有一定的社会关注的人，就必然不会陷在同一个平台上，更不用说还有各种各样的博客和独立互联网刊物。那么多平台，单是记住不同媒体在哪里，并且找到它们就要花一番时间，更不用说管理和阅读了。而RSS技术就给了我们一个这样的渠道：通过RSS链接订阅不同的网站，把他们集结整合在一起，实现统一的管理和阅读。

更重要的是，RSS使用一种订阅的模式，打破了信息流的互联网使用方式，把主动权重新交回给使用者本身。

过去使用优酷时，我每日仅仅打开关注列表，查看自己的关注的主播；后来使用[Bilibili](https://www.bilibili.com)，我仍然主要依靠关注列表，但每看完一个视频后，我尝尝从视频底下的推荐列表里一路看过去，不知不觉就不知通向何处；而此前使用知乎时，关注列表已不再重要，我永恒的在首页下滑，点击那些具有冲击力的标题——甚至常常我都不知道自己点击的是什么。这太恐怖了，当我猛然意识到自己在做什么时，常常有悔恨和畏——海德格尔意义上的畏——爬上我的脊背。

RSS则用一种决绝的方式打破了这种恐怖的“症状”。订阅——坚定的唯一的订阅，让我来决定我应该看什么，这实在太过伟大，赋予人决定自己的生活方式的武器——给人一种崇高的自由。前所未有的“民主”的武器，在前所未有的生活方式中浮现。

# 一些RSS技巧

尽管RSS这样的伟大，但它仍然，正如一切伟大的事物那样，总是小众而不太便捷的，想真正使用RSS作为一种完整的互联网生活形式，总还需要一点点技巧。

1. 订阅源

   譬如我的网站，是提供了订阅源的，但并不是每一个网站都会提供订阅源，更不用说如Bilibili那样的平台了。但幸而有那么一个项目：[RSSHub](https://github.com/DIYgod/RSSHub)，提供了一种将各种各样奇怪的内容生成订阅源的手段，为各种不提供RSS源的网站生成适配RSS地址。你还可以使用插件[RSSHub-Radar](https://github.com/DIYgod/RSSHub-Radar)来在浏览器中抓取各种网站。

   > RSSHub is an open source, easy to use, and extensible RSS feed generator. It's capable of generating RSS feeds from pretty much everything.

   但遗憾的是，因为某些原因，RSSHub在国内无法访问，但我们还能搭建属于自己的RSSHub。[点击此处学习📖](https://zhuanlan.zhihu.com/p/395100455)

2. 邮箱推送

   一种这样的订阅方式，可能并不特别方便查阅，至少在还没适应时是这样的。但许多RSS订阅网站都支持邮箱推送，还有一些专门实现RSS邮箱推送服务的网站，比如[Rriefcake](https://app.briefcake.com)。使用它们就可以很轻松的在邮箱中订阅你的内容。

3. 习惯转移

   必要承认的一个事实是：其实我们也并不习惯使用RSS系统，毕竟我们早就在这个信息流中被驯化成了一种惯性生物，而且我们也常常不能脱离社交性信息流，否则我们就会成为所谓“脱节”的人。但是我们可以转移一部分精力到RSS上，比如每天开辟一段时间——就像你为邮件每天开辟的时间那样——专门查看你的RSS系统，这可以是每天吃早饭时，也可以是每天睡前。慢慢地，相信你会喜欢上这种订阅模式带给你的高效与专注。

# RSS何去何从

RSS诞生至今已26年左右，但却好似从未掀起过什么热潮，而在未来，也很难相信它会成为一种潮流。这是容易理解的，正如本文开头所写的那样，大多数人其实对这样的生活方式并不感冒，从邮件在中国的逐渐消亡就可见一斑。但它这样默默的运行着，我并不认为它会在终有一日消失，成为一种过去的产物，因为总有一些人，在奋力地尝试精彩地活着，掌握自己的生活，而RSS，作为一种“武器”，会永恒地发挥它的作用，RSSHub的贡献者高达几百位就是最好的例证。

本文的最后，我想引用穿山甲专访的《写到世界充满爱：专访 RSSHub 作者 DIYgod》中的一段来结尾：

> **问：说起来，你其实是将微博的信息流推送的形式，借助于自己的编程能力，转化为 RSS 的被动拉取的形态。那对于 RSS 和 现在的信息流应用，你有什么看法么？**
>
> DIYgod：信息流应用基本都有自己的一套推荐算法，受益于此，可以获得更轻松愉快的阅读体验；但另一方面来看，用户丧失了内容选择的主动权，看到的不一定是自己真正想看的，稍不注意也会消耗自己大量的时间，阅读效率更低。RSS 可以选择自己真正想看的内容，阅读效率更高，但这也导致使用门槛比信息流应用高了很多。信息流应用的另一个问题是它无法集中地收取信息，时不时地打开微博、Twitter、YouTube、哔哩哔哩，去翻看我关注的人有没有更新，实在是一件痛苦的事。最后是 RSS 可以做到没有遗漏地收取信息，而信息流应用很容易遗漏。
>
> **问：说起来集中在一个地方收取信息，你怎么看曾经的“即刻”应用，即刻应用也可以关注特定的人、微博之类的，在一个地方查看所有的信息。**
>
> DIYgod：我非常喜欢“即刻”，在“即刻”倒闭之前也一直在使用它，早期很像一个 RSS 阅读器，甚至真的可以订阅 RSS，但后来这些功能越来越淡化直至去掉了，取而代之的都是 UGC 内容了。


