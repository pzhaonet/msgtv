
--- 
title: "现代统计图形之极乐净土"
subtitle: "Modern Statistical Graphics with Tidyverse"
author: "谢益辉，黄湘云，赵鹏，张列弛"
date: "2019-08-28"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, MSG-packages.bib, Modern-Stat-Graphics.bib]
biblio-style: apalike
link-citations: yes
classoption: "UTF8,oneside"
description: "现代统计图形之极乐净土书稿"
geometry: margin=1.18in
colorlinks: yes
github-repo: pzhaonet/msgtv
url: 'https\://pzhaonet.github.io/msgtv/'
---



 

# 版权声明 {#copyright .unnumbered}

本书电子版采用 Creative Commons（简称CC）许可证“署名 --- 非商业性使用 --- 相同方式共享 2.5 中国大陆”，该许可证的全文可以从<http://creativecommons.org/licenses/by-nc-sa/2.5/cn/>获得；一份普通人可以理解的法律文本概要可以从<http://creativecommons.org/licenses/by-nc-sa/2.5/cn/legalcode>获得。

<a href="http://creativecommons.org/licenses/by-nc-sa/2.5/cn/" target="_blank"><img src="images/cc-by-nc-sa.svg" width="30%" style="display: block; margin: auto;" /></a>

作者采用CC许可证的考虑：

本书是在《现代统计图形》第一版基础上修改而来的，而此书采取的是 CC 许可证，所以别无选择。


\BeginKnitrBlock{flushright}<p class="flushright">赵鹏</p>\EndKnitrBlock{flushright}

# 第一版欢迎 {#welcome1 .unnumbered}

## 版权声明 {#copyright1 .unnumbered}

本书电子版采用Creative Commons（简称CC）许可证“署名 --- 非商业性使用 --- 相同方式共享 2.5 中国大陆”，该许可证的全文可以从<http://creativecommons.org/licenses/by-nc-sa/2.5/cn/>获得；一份普通人可以理解的法律文本概要可以从<http://creativecommons.org/licenses/by-nc-sa/2.5/cn/legalcode>获得。

<a href="http://creativecommons.org/licenses/by-nc-sa/2.5/cn/" target="_blank"><img src="images/cc-by-nc-sa.svg" width="30%" style="display: block; margin: auto;" /></a>

本CC许可证赋予读者复制、发行、展览、表演、放映、广播或通过信息网络传播本作品以及创作演绎作品的自由，而无需向原作者征求许可或支付任何费用；本许可证与出版社版权独立，因此复制、传播或演绎本作品也无须征求出版社许可。您需要遵循的条件是：

- 声明原作者的署名（Attribution）：不得将本作品归为自己的劳动
- 不得将本作品用于商业目的（Noncommercial）
- 基于本作品的演绎作品须遵守同样许可证发布（Share Alike）

作者采用CC许可证的考虑主要有三点：

- 让读者能免费、自由获得本书，节省经济支出；在有网络和电子文档的时代，我们应该充分利用这些工具的优势，如传播快捷、读者交流反馈方便（以便提高书籍质量）等
- 版权的本来意义不在于控制所有权，它只不过是为了对原创者的一种署名激励；如果版权的存在妨碍了知识的传播，那么本人认为版权就没有太大的意义；CC许可证中的“非商业”和“同样许可证”限制条款在书籍出版14年后会自动取消，即读者可以用于商业目的或更改至其它许可证；CC许可证规定的14年似乎是很长的时间，但读者须知：通常的版权只有在原作者去世后50年才会被取消！换句话说，版权告诉我们一个很深刻的哲理：长寿是很重要的
- 自由软件用户往往有某种痴狂的特征，而这种痴狂往往来源于自由软件的分享精神；R语言让本人受益颇多，这本书可视作是对它的一种回馈；既然R语言是自由的，那么本书也将尽量“自由”

尽管CC许可证没有限制作品的传播方式，但本作者不愿看到本书被任何人以论坛附件的方式发布在任何论坛（尤其是某某经济论坛），原因是本书稿尚未成熟，或许有诸多不完善之处甚至严重错误，作者在不断更新中，若要传播本书稿给他人，请仅仅给出本书的原始链接<https://bookdown.org/xiangyun/msg/>，否则作者对传播过程中的错误概不负责。


## 捐赠说明 {#donate .unnumbered}

如果本书对您有任何帮助，您不妨考虑为“统计之都”网站（自愿）捐赠：<https://cosx.org/donate/>，捐赠所得将用于推广统计学和自由统计软件。捐赠之后请及时告知网站管理人员：[admin@cos.name](mailto:admin@cos.name)。


## 致谢 {#acknowledgement .unnumbered}

本书写作过程中收到了不少读者反馈，在此一并致谢。感谢魏太云、Dazhi Jiang和郑冰对本书文字的校对和建议；感谢赵彦云老师对本书书名和写作风格的建议；感谢李皞对写lattice系统和rgl包的提议；感谢李丰的“彩蛋”建议；感谢王晓伟、李承文、FreemanZY、agri521、annidy、Zhanwu
Dai耗费眼神帮我挑选了本书第一例彩蛋（图\@ref(fig:point-random)）；感谢殷腾飞增加动态图形系统GGobi的建议；感谢方莹提供第\@ref(chap:data)章的一些数据指引；本书部分小节的初稿内容来自一些朋友：王晓伟提供了lattice一节的初稿，邱怡轩提供grid和rgl两节的初稿，魏太云提供了《统计词话》的初稿，肖楠提供了RgoogleMaps一节的初稿。

最后，我要感谢我的父母和亲人们在2008年以来每个长假给我提供绝佳的写作环境，让我心无旁骛地写书；感谢吴喜之老师将R这套工具引入中国人民大学统计学院的课堂，以及王星老师在统计计算和非参数统计课堂上对R的介绍，没有他们的努力，我也许不会踏进R的大门；感谢我的硕士导师赵彦云老师在我的本硕学习期间给我的各种指导；感谢“统计之都”网站的会员们在[COS论坛](https://d.cosx.org/)上S-Plus
\& R版块和我的交流，他们的问题也使我意识到了图形知识的需求；感谢周筠老师和卢鸫翔编辑以及出版团队；感谢本书写作期间所有给我提供过帮助的人们。

\BeginKnitrBlock{flushright}<p class="flushright">谢益辉  </p>\EndKnitrBlock{flushright}


