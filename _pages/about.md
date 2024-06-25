---
permalink: /
title: "Academic Pages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

我是一名来自北京农学院[School of BUA](https://www.bua.edu.cn/),的四年级本科生，我的专业是智能科学与大数据技术。我的研究兴趣包括计算机视觉、计算机图形学、机器学习和计算摄影。

你可以在这里找到我的简历：杨智童的简历[my Curriculum_Vitae](../assets/Curriculum_Vitae.pdf)。

[Email](202120751231@bua.edu.cn) / [Github](https://github.com/yztsw1) / [Wechat](../images/WeCat.jpg) / 

一个数据驱动的个人网站
======
与许多其他基于Jekyll的GitHub页面模板一样，Academic Pages使您可以将网站的内容与其形式分离。您网站的内容和元数据位于结构化markdown文件中，而其他各种文件构成了主题，指定了如何将这些内容转换为HTML页面。您将这些各种markdown（.md）、YAML（.yml）、HTML和CSS文件保存在一个公共GitHub仓库中。每次您提交并将更新推送到仓库时，GitHub Pages服务都会根据这些文件创建静态HTML页面，这些页面托管在GitHub的服务器上，免费提供。

通过这种方式，可以实现动态内容管理系统（如Wordpress）的许多功能，使用的计算资源仅为后者的几分之一，且对黑客攻击和DDoS攻击的脆弱性要小得多。您还可以随心所欲地修改主题，而不必触及网站内容。如果您在Jekyll/HTML/CSS中破坏了某些内容且无法修复，您描述演讲、出版物等的markdown文件是安全的。您可以回滚更改，甚至删除仓库并重新开始——只要确保保存markdown文件！最后，您还可以编写脚本处理网站上的结构化数据，例如，这个脚本分析关于演讲的页面元数据，以显示您每次演讲的位置地图。

开始使用
======
如果您还没有GitHub帐户，请注册一个并确认您的电子邮件（必需！）
点击右上角的“fork”按钮，复制这个仓库。
进入仓库的设置（从“Code”开始的标签中最后一个项目，应在“Unwatch”下方）。将仓库重命名为"[your GitHub username].github.io"，这也将是您网站的URL。
设置全站配置并创建内容和元数据（见下文——还可以查看这一系列差异，显示了为用户"getorg-testacct"设置示例站点时更改了哪些文件）
将任何文件（如PDF、.zip文件等）上传到files/目录。它们将出现在https://[your GitHub username].github.io/files/example.pdf。
通过进入仓库设置，在“GitHub pages”部分检查状态

全站配置
------
网站的主要配置文件位于基本目录中的_config.yml，该文件定义了侧边栏和其他全站功能的内容。您需要将默认变量替换为关于您自己和您的网站GitHub仓库的变量。顶部菜单的配置文件位于_data/navigation.yml。例如，如果您没有作品集或博客文章，您可以删除navigation.yml文件中的这些项目，以从标题中移除它们。

创建内容和元数据
------
对于网站内容，每种类型的内容都有一个markdown文件，这些文件存储在诸如_publications、_talks、_posts、_teaching或_pages的目录中。例如，每次演讲都是一个存储在_talks目录中的markdown文件。在每个markdown文件的顶部是关于演讲的结构化数据，YAML格式，主题将解析这些数据以实现许多很酷的功能。关于演讲的相同结构化数据用于生成Talks页面上的演讲列表，每个特定演讲的单独页面，CV页面的演讲部分，以及您演讲过的地方的地图（如果您运行这个python文件或Jupyter笔记本，它根据_talks目录的内容创建地图的HTML）。


**Markdown生成器**

我还创建了一组Jupyter笔记本，它们将包含有关演讲或演示的结构化数据的CSV转换为个别markdown文件，这些文件将针对Academic Pages模板进行适当格式化。该目录中的示例CSV是我用来创建自己的个人网站stuartgeiger.com的。我通常的工作流程是，我保持一个关于我的出版物和演讲的电子表格，然后运行这些笔记本中的代码以生成markdown文件，然后提交并将它们推送到GitHub仓库。

如何编辑您网站的GitHub仓库
------
许多人使用git客户端在本地计算机上创建文件，然后将它们推送到GitHub的服务

