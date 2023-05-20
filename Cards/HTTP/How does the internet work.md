---
title: How does the internet work
date created: 2023-04-20
date modified: 2023-04-20
---

### 一个简单的网络

当两台计算机需要通信时，你必须将它们连接起来，要么是物理连接（通常用以太网电缆），要么是无线连接（例如用Wi-Fi或蓝牙系统）。所有现代计算机都可以维持其中任何一种连接。

注意：在本文的其余部分，我们将只谈论物理电缆，但无线网络的工作原理是一样的。

![Two computers linked together](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-1.png)

这样的网络不限于两台电脑。你可以随心所欲地连接任意多的计算机。但它很快就会变得复杂。如果你想连接，比如说，十台电脑，你需要45根电缆，每台电脑有九个插头

![Ten computers all together](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-2.png)

为了解决这个问题，网络上的每台计算机都与一台特殊的微型计算机相连，这台计算机被称为路由器。这个路由器只有一项工作：就像火车站的信号员一样，它确保从特定计算机发出的信息到达正确的目的地计算机。要向计算机B发送消息，计算机A必须将消息发送给路由器，而路由器则将消息转发给计算机B，并确保消息不会被送到计算机C。

一旦我们在系统中加入了路由器，我们由10台计算机组成的网络只需要10根电缆：每台计算机一个插头，路由器有10个插头。

![Ten computers with a router](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-3.png)

### 一个网络的网络

到目前为止还不错。但是，连接数百、数千、数十亿台计算机的情况呢？当然，一个单一的路由器不可能扩展到那么远，但是，如果你仔细阅读，我们说过，路由器是一台和其他计算机一样的计算机，那么是什么让我们不把两个路由器连接在一起呢？没有什么，所以我们就这么做吧。

![Two routers linked together](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-4.png)

通过将计算机连接到路由器，然后再将路由器连接到路由器，我们就能够无限地扩展。

![Routers linked to routers](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-5.png)

这样的网络非常接近于我们所说的互联网，但我们缺少一些东西。我们为我们自己的目的建立了那个网络。还有其他的网络：你的朋友，你的邻居，任何人都可以拥有自己的计算机网络。但是，在你的房子和世界其他地方之间设置电缆其实是不可能的，那么你如何处理这个问题？好吧，已经有电缆与你的房子相连了，例如，电力和电话。电话基础设施已经将你的房子与世界上的任何人连接起来，所以它是我们所需要的完美电线。为了将我们的网络连接到电话基础设施，我们需要一个特殊的设备，称为调制解调器。这个调制解调器将来自我们网络的信息转化为电话基础设施可以管理的信息，反之亦然。

![A router linked to a modem](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-6.png)

因此，我们已经连接到了电话基础设施。下一步是将信息从我们的网络发送至我们想要到达的网络。为了做到这一点，我们将把我们的网络连接到互联网服务提供商（ISP）。ISP是一家管理一些特殊路由器的公司，这些路由器都连接在一起，也可以访问其他ISP的路由器。因此，来自我们网络的信息通过ISP网络的网络被传送到目的地网络。互联网就是由这整个网络基础设施组成的。

![Full Internet stack](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-7.png)

### 寻找计算机

如果你想向一台计算机发送消息，你必须指定哪一台。因此，任何连接到网络的计算机都有一个唯一的地址来识别它，称为 "IP地址"（其中IP代表互联网协议）。这是一个由四个数字组成的地址，用点分开，例如：192.168.2.10。

这对计算机来说完全没有问题，但我们人类很难记住这种地址。为了使事情变得更容易，我们可以用一个人类可读的名字（称为域名）来别名一个IP地址。例如（在撰写本文时，IP地址可能会发生变化），google.com是在IP地址142.250.190.78之上使用的域名。因此，使用域名是我们在互联网上接触计算机的最简单方法。

![Show how a domain name can alias an IP address](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/dns-ip.png)

### 互联网和网络

你可能注意到，当我们用网络浏览器浏览网页时，我们通常使用域名来到达一个网站。这是否意味着互联网和网络是同一回事？并非如此简单。正如我们所看到的，互联网是一个技术基础设施，它允许数十亿台计算机全部连接在一起。在这些计算机中，一些计算机（称为网络服务器）可以向网络浏览器发送可理解的信息。互联网是一种基础设施，而网络则是建立在基础设施之上的一种服务。值得注意的是，还有其他一些建立在互联网之上的服务，如电子邮件和IRC。


## 参考文献

[How does the internet work?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work)