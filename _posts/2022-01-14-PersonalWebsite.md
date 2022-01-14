---
layout:     post
title:      "个人网站搭建 Personal Website"
subtitle:   " 通过 GitHub Page 快速搭建个人网站"
date:       2022-01-14 10:00:00
author:     "Huang Wei"
header-img: "img/posts/2022-01-14-PersonalWebsite/bg.jpg"
catalog: true
ttags: 
    - Career
    - 生产力
    - Productivity
    - 第二大脑
    - Second Brain
---

## 方案

一开始准备自己装一套 [Typecho](https://typecho.org/) 或者 [Hexo](https://hexo.io/zh-cn/) 之类的轻量级开源框架来用，扫了一眼之前撸到的2台还没真正用起来Oracle Cloud VPS，
正在纠结这2个VPS不能快速重制系统，如果安装过程出现问题重来一遍有点费劲时。

[GitHub Pages](https://pages.github.com/) 从一堆方案中冒了出来：
- 首先它支持独立域名，要用于 [mrhuangtalk.com](https://mrhuangtalk.com) ，这是首要条件
- 其次支持 Markdown 格式，这正好和我用于搭建第二大脑的使用的Obsidian一致，这样码文效率会高不少。 everything is for Productivity , you know ~
- 数据方便导出带走。通过Github repository管理数据，不要太方便
- 另外搭建简单，有非常多的[模版(jekyllthemes)](http://jekyllthemes.org/)可用

## 简单流程

### 域名

之前一直用Godaddy，结果发现 namesilo 甚至直接从 cloudflare 买都比Godaddy便宜，大家买域名时可以多比较比较。

买完后随手把Nameservers换成cloudflare，这样使我所有的域名都可以在cloudflare统一管理，还能享受cloudflare各种免费服务

![image-20220114113254712](/img/posts/2022-01-14-PersonalWebsite/image-20220114113254712.png)

### 使用 Github Page

- 注册Github账号，如果你没有的话。
- Github Page使用 [用户名].github.io 作为给你使用的二级域名，如果你需要和你用户名不一样的域名，需要新建一个组织（Organizations），组织名称就是你想用的二级域名。一开始没注意，这里卡了我30分钟。

![image-20220114122031561](/img/posts/2022-01-14-PersonalWebsite/image-20220114122031561.png)

- 在新建组织下新建repository，名字是 MrHuangTalk.github.io。然后Setting 中 Page 里选中分支启用Page，在挑选github自带的几个主题，这样属于你的 https://mrhuangtalk.github.io 有GitHub二级域名的网站就建好了。

![image-20220114122442081](/img/posts/2022-01-14-PersonalWebsite/image-20220114122442081.png)

- 下面开始设置注册好的一级域名。首先设置你新买域名 DNS 的CNAME，A和AAAA records，CNAME内容为Github给的二级域名（MrHuangTalk.github.io），同时设置Github Page中Custom Domain为你的一级域名，这样域名和网站就都搞定了。
- 更详细步骤可参考 [Github 设置文档](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)

![image-20220114123845509](/img/posts/2022-01-14-PersonalWebsite/image-20220114123845509.png)

![image-20220114124319186](/img/posts/2022-01-14-PersonalWebsite/image-20220114124319186.png)

- 发布网站内容我是用GitHub Desktop和VS code进行。首先用GitHub Desktop把repository Clone到本地，在用VS code进行新建和更新（Typora、Obsidian等Markdown编辑器也可，主要我还需要修改一些主题内容，VS Code更通用），最后在用GitHub Desktop提交发布，和代码管理一样，你的文章就发步到了github，通过我们的一级域名就可以访问了。

![image-20220114130358808](/img/posts/2022-01-14-PersonalWebsite/image-20220114130358808.png)

### 更多主题

- 如果GitHub提供的主题你都不满意，还可以从[jekyllthemes](http://jekyllthemes.org/)免费挑选自己心仪的主题，下载下来替换之前Clone下来的内容，就可以使用更多的主题模版，丰富我们的个人主页
  
![image-20220114102740674](/img/posts/2022-01-14-PersonalWebsite/image-20220114102740674.png)

## 结尾

如果有疑问，我们可以在留言区交流。