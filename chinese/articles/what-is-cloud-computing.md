> -  原文地址：[What is Cloud Computing?Introduction to the Cloud for Beginners](https://www.freecodecamp.org/news/what-is-cloud-computing/)
> -  原文作者: [Zubair Idris Aweda](https://www.freecodecamp.org/news/author/zubair-idris-aweda/)
> -  译者: JunoWei
> -  校对者: 


# 云计算是什么？针对初学者的云概念介绍


  ![What is Cloud Computing? Introduction to the Cloud for Beginners](https://www.freecodecamp.org/news/content/images/size/w2000/2022/05/cloud-sky.jpeg)


随着数字化领域和科技的不断发展，云计算仍然是一个重要议题，值得开发人员学习。你可能会在岗位招聘中遇到关于“云”的相关需求，可能会在对话中听到关于“云”的相关讨论，可能会在云服务商发布的广告中看到关于“云”的相关宣传，现在你对“云”充满好奇，想要知道更多。在这篇文章中，我会将复杂的概念分成简单易懂的小模块，让你更加容易理解“云”。

这是本文中涉及的主要内容：
-   [云计算出现前的世界](#the-world-before-cloud-computing)
-   [云计算是什么?](#what-is-cloud-computing)
-   [云服务供应商](#cloud-service-providers)
-   [云服务类型](#different-cloud-services)
-   [云计算助力解决的难题](#challenges-that-cloud-computing-helps-solve)
-   [云计算是如何帮助我们的?](#how-can-cloud-computing-help-you)
-   [云计算部署模式](#cloud-deployment-models)


让我们从学习云计算的基础内容开始，然后你可以在云计算这个持续发展的领域深入学习。
<h2 id="the-world-before-cloud-computing">云计算出现前的世界</h2>


了解云计算尝试解决的问题，可以帮助你理解云计算的历史发展，并感激云计算给世界科技带来的便携，这样才能更好地全方位理解云计算。“云”出现以前，部署网络服务曾是一个昂贵的过程。为了部署一套网络应用程序，首先需要采购符合存储要求的服务器，然后找到合适的空间存放，搭建好服务器后才能使用服务器托管应用程序。除了服务器的购置费，为了维持服务器不间断运行并持续在线，后续还会有很多额外支出，譬如电费和流量费用。同时还有安全问题，需要避免服务器遭到恶意破坏和盗取信息。除此之外，大多数的开发人员都不是精通服务器的专家，所以要么培养开发人员做系统管理者，要么招聘系统管理的专职人员，负责搭建配置服务器保证应用程序的稳定运行。而安装部署一套新的应用程序，重复整个过程并产生新的费用。扩展是指购买更多的服务器（或者是购买更好地服务器替换已有的服务器），配置符合现有配置的环境，然后将应用程序部署在新的服务器上。“云”时代之前，扩展应用程序并没有很方便，如果一开始控制成本，没有购入足够多的服务器或者是招聘足够多的系统工程师，最终可能导致算力不充足而需要扩展。这些都是云计算出现以前我们面对的问题，或许你现在困惑“云计算是怎么解决这些问题”，请看下文讲解。

<h2 id="what-is-cloud-computing">云计算是什么？</h2>
 
> **云计算**是一种按需提供的计算系统资源，例如数据存储（云存储）、算力等，且不需要用户直接主动管理。
> 云计算通过资源共享获取一致性，采用按使用量付费的模式，协助降低固定资产费用，同时可能需要用户支付超出预期的营业费用。 – [维基百科](https://en.wikipedia.org/wiki/Cloud_computing)


想象一下，云计算和在网吧中使用电脑类似。网吧中准备好了电脑，当你走进网吧时，只需要支付期望使用时间对应的费用，然后在这个时间段内就可以随便使用电脑。而云计算呢，你不需要购入、运维服务器，也不用承担运行成本，你也不用担心软件问题或者这些服务器缺少特定的软件，因为这些都由云服务供应商负责。云计算体验感最佳的地方就在于，你只需要付费订购需要使用的服务器以及服务时间段。进一步而言，当部署一套网络应用程序时，不用考虑很多事情，只用找到一个云服务供应商，选择符合程序要求的服务器，选择操作系统，然后就可以部署应用了。用简单易懂的话解释，云计算就是让别人来管理你的计算需求。当需要上线网站、手机 APP 或其他类似应用时，不再需要购置实体的服务器进行部署，只要使用他人已经准备好的服务器，上传代码文件即可。这和租房子类似，而现在做的就是在另外一台电脑中租用了计算空间。

<h2 id="cloud-service-providers">云服务供应商</h2>

云服务供应商是指提供云服务的公司。这些公司通常有很多服务器和系统工程师，会提供全流程服务，用户无需担心类似服务器成本和运行费用等问题，他们会给用户提供一个用于连接服务器的用户界面，当用户需要时使用即可。目前最受欢迎的云服务供应商是谷歌云、亚马逊（AWS）和微软（Azure），这些公司提供的服务都比较类似，但是定价模式、特点等各有不同。

以下是这些公司的提供内容的简介：

### 谷歌

谷歌提供基础架构即服务 IaaS（Compute Engine），容器即服务 CaaS（Kubernetes Engine）以及平台即服务 PaaS（App Engine）等服务，同时提供数据存储服务，如 Cloud Storage, Cloud SQL 以及 Bigtable 等产品。

### 亚马逊

亚马逊是第一家提供云服务的公司，提供基础架构即服务 IaaS（Elastic Compute, EC2），容器即服务 CaaS（Elastic Kubernetes Service, EKS）以及平台即服务 PaaS（Elastic Beanstalk）等产品，同时提供数据存储服务，如 Amazon S3、 DynamoDb 等产品。

### 微软

微软提供基础架构即服务 IaaS（Virtual Machine），容器即服务 CaaS（Kubernetes Service, AKS）以及平台即服务 PaaS（App Service）等产品，同时提供数据存储服务，如 Cosmos DB 等产品。

云服务供应商通常为了资源利用最大化会让用户共享服务器，但用户无需知道这方面的内容，也不用担心。接下来我们讲解一下以上提到的一些云服务类型，以便于更好理解这些云服务内容。

<h2 id="different-cloud-services">云服务类型</h2>

云服务供应商可以提供很多云服务类型，以下是最常见的服务类型：

### SaaS（软件即服务）
![saas-778x445](https://www.freecodecamp.org/news/content/images/2022/05/saas-778x445.jpeg)

[Geek Super](https://www.google.com/url?sa=i&url=https%3A%2F%2Fgeeksuper.com%2Fadvantages-of-saas-platforms-for-online-courses%2F&psig=AOvVaw0J54lC0WsxXAoS0L2czE27&ust=1652833369985000&source=images&cd=vfe&ved=0CA0QjhxqFwoTCIDvwOio5fcCFQAAAAAdAAAAABAO)


这项服务是指用户直接使用一些软件应用，不用关心源代码、托管环境或者开发细节等事情。只是使用软件，并且相信软件会被持续管理与升级。

### 平台即服务（PaaS）

这项服务是指用户只需专注应用的开发，其他的事项都已经准备好了（如硬件、计算环境和需要的软件）

### 基础架构即服务（IaaS）

这项服务是所有云服务中最复杂的类型，用户对订购的服务拥有最大的自主权，可以按照用户自己的想法适配和修改，但用户没有服务器的所属权。云服务供应商为用户提供所需的基础架构，用户负责搭建计算环境，安装运行应用程序所需的软件。这个方式与购买硬件非常类似，唯一的区别是用户租用并且虚拟拥有（没有实物）。

<h2 id="challenges-that-cloud-computing-helps-solve">云计算助力解决的难题</h2>

云计算可以避免每次开发新的应用时就需要购置并现场搭建物理服务器，最大的优势就是可以帮助公司降低成本，包括服务器费用和搭建配置服务器的人工费。扩展服务器因为需要有大量的搭建和配置工作，所以通常都不是简单的事情。譬如，一个应用程序需要更多的存储空间，一般情况下可以通过给现有服务器外置一个数据存储来解决，但这种方法往往有局限性。这时就会想到购置一个配置更好的服务器或者再购置一个服务器，无论是哪种方法，旧服务器上安装的与应用运行相关的所有软件，都需要在新的服务器上再安装一遍，并且还有把应用的文件转移到新服务器等操作。通常情况下，这些服务器资源也不会被应用程序充分利用。从商业角度出发，这是一种损失。这个问题最初的解决方案是虚拟化，在服务器中安装虚拟环境，并在虚拟环境中安装应用运行需要的所有软件，应用就可以在虚拟环境中运行起来了。这个方案虽然实现了资源最大化利用，但并不完美。

<h2 id="how-can-cloud-computing-help-you">云计算有什么好处?</h2>

云计算有很多好处，一些突出优势如下：
-   相比于建立一个完整的数据中心，付费订购更加划算，只需要计划好需要使用的配置。

-   云服务供应商负责扩展和运维服务器。

-   搭建方便，开发人员只需要专注于代码编写，所有的服务器搭建配置都能通过云服务供应商提供的用户界面操作完成，可以缩短开发时间，应用程序交付速度也更快。

-   可访问性，云服务供应商一般在全球有多个数据中心，确保应用的使用者可以快速地连接到服务器。

-   数据安全，因为数据不再存储在物理服务器上，所以更不容易被恶意攻击或者盗取数据信息。

<h2 id="cloud-deployment-models">云计算部署模式</h2>

云计算部署模式决定了数据（以及应用）存储位置和用户与服务器交互方式。
### 公有云


公有云的所有事项都由云服务供应商负责，这是最受欢迎的模式。选择使用公有云，就不需要关心服务器的运维，并且有高可靠性和无限扩展的可能性，但通常也意味着需要和他人共享服务器。这也是最便宜的模式，公司一般会采用按使用量付费的方式（所以无需过早提前支付）。但这个模式有一个潜在弊端，因为所有事项由云服务供应商负责，意味着用户几乎没有服务器的控制权。
### 私有云


私有云模式与传统托管应用程序的方式类似，需要有自己的数据中心，只有用户自己可以使用服务器，意味着用户拥有服务器的最高控制权限。不同的是，用户可以给服务器的使用者——通常是用户公司的开发人员，提供一个私有的服务界面。用户仍然需要管理这些物理服务器，需要自行负责运维和扩展。这个模式让用户可以自行控制并且尽可能地搭建安全性环境，所以比公有云更安全。如果基于合规要求必须保证数据不会被泄露，这种模式就最符合要求。不过这种模式是高额成本的模式，虽然现在有了固定价格模型，但服务器和硬件依然很昂贵，同时还需要额外费用招人运维，而且扩展也需要每次购置新的设备。
### 混合云

![What-is-Hybrid-Cloud](https://www.freecodecamp.org/news/content/images/2022/05/What-is-Hybrid-Cloud.jpeg)

混合云 | [W3Codemasters](https://www.google.com/url?sa=i&url=https%3A%2F%2Fw3codemasters.in%2Fwhat-is-hybrid-cloud-benefits-of-a-unified-hybrid-cloud-platform%2F&psig=AOvVaw3ekfLv5gwNG2kjXGoFfWA4&ust=1652833178148000&source=images&cd=vfe&ved=0CA0QjhxqFwoTCPj5qKKp5fcCFQAAAAAdAAAAABAI)


混合云是将公有云和私有云混合起来的模式，更具有灵活性。在使用公有云的同时，也可以按需搭建私有云。服务器用于遵守监管规则，云服务供应商则可以使访问更方便。当机构需要模式转换时，这种模式是最佳的选择，在转移过渡期间依然能够被使用维持商业运行。举个例子，应用程序托管在公有云上，再连接安装在安全的私有云上的数据库。这个模式因为需要一些自有服务器，所以定价比公有云更贵；而且因为数据和应用分散分布于多个服务器，比公有云也更为复杂。
### 如何选择部署模式


基于用户的特殊需求决定使用公有云、私有云还是混合云。

-   公有云定价合理获取便利

-   私有云提供更可靠的安全性和更高的控制权

-   混合云更加灵活，是介于公有云与私有云之间的方式


一些重要因素，如安全需求、合规要求、可扩展性、IT 架构中对控制权限的要求等，最终决定部署模式
## **总结**


学习了基础知识后，你现在可以开始深入学习云计算了。如果你有任何问题或者相关建议，请联系并转述给我。你可以通过[LinkedIn](https://www.linkedin.com/in/idris-aweda-zubair-5433121a3/)、[Twitter](https://twitter.com/AwedaIdris)、[Github](https://github.com/Zubs)阅读更多我的文章或者关注我的工作，快速方便并且是免费的！

---

![Zubair Idris Aweda](https://www.freecodecamp.org/news/content/images/size/w60/2023/02/IMG_6413-2.jpg)

[Zubair Idris Aweda](/news/author/zubair-idris-aweda/)
在计算机软件领域有多年软件工程经验，精通 PHP、JavaScript 和其他 web 开发工具。

