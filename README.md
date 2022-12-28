---
title: 我的博客网页教程
comments: true
date: 2019-07-11 
categories: 博客教程
---
![image](https://user-images.githubusercontent.com/36963108/163677071-34bca585-7dcc-4c32-8644-98b5cfed4ce8.png)

[hexo官网](https://hexo.io/themes/)

[我的博客官网](http://coomatrix.com//categories/)

[我的博客主题仓库](https://github.com/KangChou/my-theme-hiero)

[当前博客hiero主题教程](http://coomatrix.com/2020/07/07/hieroCN/)

[我最初开始搭建博客的详细教程](https://mp.weixin.qq.com/s/oGHMts-xo2RQiusp9yifDA)

下面开始介绍博客搭建中的一些常用环节

### 配置环境

安装Node（必须）安装Git（必须）

### 正式安装Hexo

为了不跳坑╮(╯▽╰)╭，请先建好你要放博客的目录，进到目录中再进行以下操作如我的：cd ~/Blog

#### 1、安装Hexo

```text
sudo npm install hexo-cli -g
```

#### 2、初始化Hexo

```text
hexo init + 需要初始化的目录
```

这里建议init与你github仓库一样的名字[http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io)

<!-- more -->

#### 3、安装依赖

进入初始化后的目录：cd [http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io)安装Hexo依赖

```text
npm install
```

#### 4、生成静态页面

```text
hexo generate # 简写 hexo g
```

本地预览其实不需要执行这部也行

#### 5、启动本地服务

```text
hexo server # 简写 hexo s 调试加参数：--debug
```

#### 6、测试

浏览器输入： [http://localhost:4000](https://link.zhihu.com/?target=http%3A//localhost%3A4000/) 若能正常显示网页切没有任何报错，恭喜你！到此Hexo的安装就完成了

### Next 安装

在本地博客目录[http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io)下操作

#### 1、安装 Next 主题

```text
git clone https://github.com/iissnan/hexo-theme-next themes/next
```

#### 2、使用 Next 主题

**首先，**复制一份打开本地博客目录下的 **_config.yml** 文件，命名为 **_config_bak.yml**，做为备份，以防改错**然后，**使用文本编辑器打开本地博客目录下的 **_config.yml** 文件，搜索，定位 theme 键值，将 theme 的值修改为 **next**

```text
theme: next //刚刚安装的主题名称
```

**注意：**Hexo配置文件中所有的配置项冒号与值之间都要有一个空格，不然配置不会生效重启本地服务，访问 [http://localhost:4000](https://link.zhihu.com/?target=http%3A//localhost%3A4000/) 就能看到 Next 主题默认界面了

#### 3、配置

由于配置项比较多，直接注释，放出配置文件

**站点配置文件**

```python
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/
## 设置项的键值之间一定要有空格

# Site
title: luosv`s blog # 网站标题
subtitle: 副标题起个啥呢 # 网站副标题
description: About Life, Books and Code. # 网站描述 主要用于SEO
author: luosv # 作者名字 用于主题显示文章的作者
language: zh-Hans # 网站使用的语言
timezone: # 网站时区 Hexo 默认使用您电脑的时区

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
## 如果您的网站存放在子目录中，例如 http://yoursite.com/blog，则请将您的 url 设为 http://yoursite.com/blog 并把 root 设为 /blog/
## 这项暂时不需要配置，绑定域名后，要创建 sitemap.xml 时再配置该项
url: http://yoursite.com # 网址
root: / # 网站根目录
permalink: :year/:month/:day/:title/ # 文章的永久链接格式
permalink_defaults: # 永久链接中各部分的默认值

# Directory
# 目录，如果您刚刚开始接触Hexo，通常没有必要修改这一部分的值
source_dir: source # 资源文件夹，这个文件夹用来存放内容
public_dir: public # 公共文件夹，这个文件夹用于存放生成的站点文件
tag_dir: tags # 标签文件夹
archive_dir: archives # 归档文件夹
category_dir: categories # 分类文件夹
code_dir: downloads/code # Include code 文件夹
i18n_dir: :lang # 国际化（i18n）文件夹
skip_render: # 跳过指定文件的渲染，您可使用 glob 表达式来匹配路径

# Writing
# 文章布局、写作格式的定义，不建议修改
new_post_name: :title.md # File name of new posts 新文章的文件名称
default_layout: post # 预设布局
titlecase: false # Transform title into titlecase 把标题转换为 title case
external_link: true # Open external links in new tab 在新标签中打开链接
filename_case: 0 # 把文件名称转换为 (1) 小写或 (2) 大写
render_drafts: false # 显示草稿
post_asset_folder: false # 启动 Asset 文件夹
relative_link: false # 把链接改为与根目录的相对位址
future: true # 显示未来的文章
highlight: # 代码块的设置
  enable: true
  line_number: true
  auto_detect: false
  tab_replace:

# Category & Tag
default_category: uncategorized # 默认分类
category_map: # 分类别名
tag_map: # 标签别名

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
## Hexo 使用 Moment.js 来解析和显示时间
date_format: YYYY-MM-DD # 日期格式
time_format: HH:mm:ss # 时间格式

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10 # 每页显示的文章量 (0 = 关闭分页功能)
pagination_dir: page # 分页目录

# Search
search:
  path: search.xml
  field: post
  format: html
  limit: 10000

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: next # 当前主题名称，值为false时禁用主题

# Deployment
## Docs: https://hexo.io/docs/deployment.html
## 部署部分的设置
deploy:
  type: git # 使用 Git 提交
  repository: https://github.com/xxx/xxx.github.io.git # 存放博客的仓库地址
  
```

**主题配置文件**

```text
# ---------------------------------------------------------------
# Site Information Settings
# ---------------------------------------------------------------
# 设置项的键值之间一定要有空格

# Put your favicon.ico into `hexo-site/source/` directory.
favicon: /favicon.ico

# Set default keywords (Use a comma to separate)
# 设置关键字
keywords: "Life, Books, Code"

# Set rss to false to disable feed link.
# Leave rss as empty to use site's feed link.
# Set rss to specific value if you have burned your feed already.
rss:

# Specify the date when the site was setup
# 设置博客开始时间
since: 2017

# icon between year and author @Footer
authoricon: heart

# Footer `powered-by` and `theme-info` copyright
copyright: true


# Canonical, set a canonical link tag in your hexo, you could use it for your SEO of blog.
# See: https://support.google.com/webmasters/answer/139066
# Tips: Before you open this tag, remember set up your URL in hexo _config.yml ( ex. url: http://yourdomain.com )
canonical: true

# Change headers hierarchy on site-subtitle (will be main site description) and on all post/pages titles for better SEO-optimization.
seo: false

# ---------------------------------------------------------------
# Menu Settings 设置菜单
# ---------------------------------------------------------------

# When running the site in a subdirectory (e.g. domain.tld/blog), remove the leading slash (/archives -> archives)
# 此处可以修改显示顺序，调换下面的配置项即可
menu:
  home: / # 主页
  categories: /categories # 分类页
  archives: /archives # 归档页
  tags: /tags # 标签页
  about: /about # 关于页面
  #sitemap: /sitemap.xml
  #commonweal: /404.html # 公益404


# Enable/Disable menu icons.
# 设定菜单项的图标
# Icon Mapping:
#   Map a menu item to a specific FontAwesome icon name.
#   Key is the name of menu item and value is the name of FontAwesome icon. Key is case-senstive.
#   When an question mask icon presenting up means that the item has no mapping icon.
menu_icons:
  enable: true
  #KeyMapsToMenuItemKey: NameOfTheIconFromFontAwesome
  home: home
  about: user
  categories: th
  schedule: calendar
  tags: tags
  archives: archive
  sitemap: sitemap
  commonweal: heartbeat




# ---------------------------------------------------------------
# Scheme Settings 设置风格
# ---------------------------------------------------------------

# Schemes
#scheme: Muse # 默认 Scheme，这是 NexT 最初的版本，黑白主调，大量留白
#scheme: Mist # Muse 的紧凑版本，整洁有序的单栏外观
scheme: Pisces # 双栏 Scheme，小家碧玉似的清新


# ---------------------------------------------------------------
# Font Settings
# - Find fonts on Google Fonts (https://www.google.com/fonts)
# - All fonts set here will have the following styles:
#     light, light italic, normal, normal italic, bold, bold italic
# - Be aware that setting too much fonts will cause site running slowly
# - Introduce in 5.0.1
# ---------------------------------------------------------------
font:
  enable: true

  # Uri of fonts host. E.g. //fonts.googleapis.com (Default)
  host:

  # Global font settings used on <body> element.
  global:
    # external: true will load this font family from host.
    external: true
    family: Lato

  # Font settings for Headlines (h1, h2, h3, h4, h5, h6)
  # Fallback to `global` font settings.
  headings:
    external: true
    family:

  # Font settings for posts
  # Fallback to `global` font settings.
  posts:
    external: true
    family:

  # Font settings for Logo
  # Fallback to `global` font settings.
  # The `size` option use `px` as unit
  logo:
    external: true
    family:
    size:

  # Font settings for <code> and code blocks.
  codes:
    external: true
    family:
    size:




# ---------------------------------------------------------------
# Sidebar Settings 设置侧栏
# ---------------------------------------------------------------


# Social Links
# 侧栏社交链接
# Key is the link label showing to end users.
# Value is the target link (E.g. GitHub: https://github.com/iissnan)
social:
  GitHub: https://github.com/luosv
  简书: http://www.jianshu.com/u/1b1a17e2c18b
  Weibo: http://weibo.com/5394586088/profile?topnav=1&wvr=6
  LOFTER: http://luosv.lofter.com/


# Social Links Icons
# 链接的图标
# Icon Mapping:
#   Map a menu item to a specific FontAwesome icon name.
#   Key is the name of the item and value is the name of FontAwesome icon. Key is case-senstive.
#   When an globe mask icon presenting up means that the item has no mapping icon.
social_icons:
  enable: true
  # Icon Mappings.
  # KeyMapsToSocialItemKey: NameOfTheIconFromFontAwesome
  GitHub: github
  Twitter: twitter
  Weibo: weibo
  简书: book
  LOFTER: camera


# Sidebar Avatar
# 设置头像
# in theme directory(source/images): /images/avatar.jpg
# in site  directory(source/uploads): /uploads/avatar.jpg
avatar: /uploads/images/avatar.jpg


# Table Of Contents in the Sidebar
toc:
  enable: true

  # Automatically add list number to toc.
  number: true


# Creative Commons 4.0 International License.
# http://creativecommons.org/
# Available: by | by-nc | by-nc-nd | by-nc-sa | by-nd | by-sa | zero
#creative_commons: by-nc-sa
#creative_commons:


sidebar:
  # Sidebar Position, available value: left | right
  position: left # 靠左放置
  #position: right # 靠右放置

  # Sidebar Display, available value:
  # 设置侧栏显示的时机
  #  - post    expand on posts automatically. Default.
  #  - always  expand for all pages automatically
  #  - hide    expand only when click on the sidebar toggle icon.
  #  - remove  Totally remove sidebar including sidebar toggle.
  display: post #  默认行为，在文章页面（拥有目录列表）时显示
  #display: always # 在所有页面中都显示
  #display: hide # 在所有页面中都隐藏（可以手动展开）
  #display: remove # 完全移除

  # Sidebar offset from top menubar in pixels.
  offset: 12
  offset_float: 0

  # Back to top in sidebar
  b2t: false

  # Scroll percent label in b2t button
  scrollpercent: false


# Blog rolls
# 友情链接
#links_title: Links
#links_layout: block
#links_layout: inline
links:



# ---------------------------------------------------------------
# 其它配置
# ---------------------------------------------------------------

# 打赏配置
# 打赏说明文本
reward_comment: 坚持原创技术分享，您的支持将鼓励我继续创作！
# 微信收款二维码
wechatpay: /uploads/images/wechat-reward-image.jpg
# 支付宝收款二维码
alipay: /uploads/images/alipay-reward-image.jpg


# 网站logo设置
# 没效果，报错，后面想办法解决
# favicon: /favicon.ico




# ---------------------------------------------------------------
# Post Settings
# ---------------------------------------------------------------

# Automatically scroll page to section which is under <!-- more --> mark.
scroll_to_more: true

# Automatically excerpt description in homepage as preamble text.
excerpt_description: true

# Automatically Excerpt. Not recommend.
# Please use <!-- more --> in the post to control excerpt accurately.
auto_excerpt:
  enable: false # 设置是否显示阅读全文，文章较多的话，有必要设置为 true
  length: 150

# Post meta display settings
post_meta:
  item_text: true
  created_at: true
  updated_at: false
  categories: true

# Post wordcount display settings
# Dependencies: https://github.com/willin/hexo-wordcount
post_wordcount:
  item_text: true
  wordcount: false
  min2read: false

# Wechat Subscriber
#wechat_subscriber:
  #enabled: true
  #qcode: /path/to/your/wechatqcode ex. /uploads/wechat-qcode.jpg
  #description: ex. subscribe to my blog by scanning my public wechat account

# Declare license on posts
post_copyright:
  enable: false
  license: CC BY-NC-SA 3.0
  license_url: https://creativecommons.org/licenses/by-nc-sa/3.0/



# ---------------------------------------------------------------
# Misc Theme Settings
# ---------------------------------------------------------------

# Custom Logo.
# !!Only available for Default Scheme currently.
# Options:
#   enabled: [true/false] - Replace with specific image
#   image: url-of-image   - Images's url
custom_logo:
  enabled: false
  image:


# Code Highlight theme
# 代码高亮主题
# Available value:
#    normal | night | night eighties | night blue | night bright
# https://github.com/chriskempson/tomorrow-theme
highlight_theme: normal


# ---------------------------------------------------------------
# Third Party Services Settings
# ---------------------------------------------------------------

# MathJax Support
mathjax:
  enable: false
  per_page: false
  cdn: //cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML


# Swiftype Search API Key
#swiftype_key:

# Baidu Analytics ID
#baidu_analytics:

# Duoshuo ShortName
#duoshuo_shortname:

# Disqus
#disqus_shortname:

# Hypercomments
#hypercomments_id:

# Gentie productKey
#gentie_productKey:

# changyan
changyan:
  enable: false
  appid:
  appkey:

# Support for youyan comments system.
# You can get your uid from http://www.uyan.cc
#youyan_uid: your uid

# Support for LiveRe comments system.
# You can get your uid from https://livere.com/insight/myCode (General web site)
#livere_uid: your uid

# Baidu Share
# Available value:
#    button | slide
# Warning: Baidu Share does not support https.
#baidushare:
##  type: button

# Share
#jiathis:
# Warning: JiaThis does not support https.
#add_this_id:

# Share
#duoshuo_share: true

# Google Webmaster tools verification setting
# See: https://www.google.com/webmasters/
#google_site_verification:

# Google Analytics
#google_analytics:

# Yandex Webmaster tools verification setting
# See: https://webmaster.yandex.ru/
#yandex_site_verification:

# CNZZ count
#cnzz_siteid:

# Application Insights
# See https://azure.microsoft.com/en-us/services/application-insights/
# application_insights:

# 一些第三方服务设置，这里只提一下”多说“，其他的请参考官方介绍
# Make duoshuo show UA
# user_id must NOT be null when admin_enable is true!
# you can visit http://dev.duoshuo.com get duoshuo user id.
duoshuo_info:
  ua_enable: true
  admin_enable: true
  user_id: 0 # **这里不要动，千万别动**
  admin_nickname: Author


# Facebook SDK Support.
# https://github.com/iissnan/hexo-theme-next/pull/410
facebook_sdk:
  enable: false
  app_id:       #<app_id>
  fb_admin:     #<user_id>
  like_button:  #true
  webmaster:    #true

# Facebook comments plugin
# This plugin depends on Facebook SDK.
# If facebook_sdk.enable is false, Facebook comments plugin is unavailable.
facebook_comments_plugin:
  enable: false
  num_of_posts: 10  # min posts num is 1
  width: 100%       # default width is 550px
  scheme: light     # default scheme is light (light or dark)

# VKontakte API Support.
# To get your AppID visit https://vk.com/editapp?act=create
vkontakte_api:
  enable: false
  app_id:       #<app_id>
  like:         true
  comments:     true
  num_of_posts: 10


# Show number of visitors to each article.
# You can visit https://leancloud.cn get AppID and AppKey.
leancloud_visitors:
  enable: true
  app_id: 3CJD75sRcSicWe9kgRSIlGrS-gzGzoHsz
  app_key: huqzr6iJ2YXBINGz7oaWmy3x

# Show PV/UV of the website/page with busuanzi.
# Get more information on http://ibruce.info/2015/04/04/busuanzi/
busuanzi_count:
  # count values only if the other configs are false
  enable: false
  # custom uv span for the whole site
  site_uv: true
  site_uv_header: <i class="fa fa-user"></i>
  site_uv_footer:
  # custom pv span for the whole site
  site_pv: true
  site_pv_header: <i class="fa fa-eye"></i>
  site_pv_footer:
  # custom pv span for one page only
  page_pv: true
  page_pv_header: <i class="fa fa-file-o"></i>
  page_pv_footer:


# Tencent analytics ID
# tencent_analytics:

# Tencent MTA ID
# tencent_mta:


# Enable baidu push so that the blog will push the url to baidu automatically which is very helpful for SEO
baidu_push: false

# Google Calendar
# Share your recent schedule to others via calendar page
#
# API Documentation:
# https://developers.google.com/google-apps/calendar/v3/reference/events/list
calendar:
  enable: false
  calendar_id: <required>
  api_key: <required>
  orderBy: startTime
  offsetMax: 24
  offsetMin: 4
  timeZone:
  showDeleted: false
  singleEvents: true
  maxResults: 250

# Algolia Search
algolia_search:
  enable: false
  hits:
    per_page: 10
  labels:
    input_placeholder: Search for Posts
    hits_empty: "We didn't find any results for the search: ${query}"
    hits_stats: "${hits} results found in ${time} ms"


# Local search 本地搜索
local_search:
  enable: true

# External URL with BASE64 encrypt & decrypt
# Usage: {% exturl text url "title" %}
# Alias: {% extlink text url "title" %}
exturl: false


#! ---------------------------------------------------------------
#! DO NOT EDIT THE FOLLOWING SETTINGS
#! UNLESS YOU KNOW WHAT YOU ARE DOING
#! ---------------------------------------------------------------

# Motion
use_motion: true

# Fancybox
fancybox: true

# Canvas-nest
canvas_nest: false

# Script Vendors.
# Set a CDN address for the vendor you want to customize.
# For example
#    jquery: https://ajax.googleapis.com/ajax/libs/jquery/2.2.0/jquery.min.js
# Be aware that you should use the same version as internal ones to avoid potential problems.
# Please use the https protocol of CDN files when you enable https on your site.
vendors:
  # Internal path prefix. Please do not edit it.
  _internal: lib

  # Internal version: 2.1.3
  jquery:

  # Internal version: 2.1.5
  # See: http://fancyapps.com/fancybox/
  fancybox:
  fancybox_css:

  # Internal version: 1.0.6
  # See: https://github.com/ftlabs/fastclick
  fastclick:

  # Internal version: 1.9.7
  # See: https://github.com/tuupola/jquery_lazyload
  lazyload:

  # Internal version: 1.2.1
  # See: http://VelocityJS.org
  velocity:

  # Internal version: 1.2.1
  # See: http://VelocityJS.org
  velocity_ui:

  # Internal version: 0.7.9
  # See: https://faisalman.github.io/ua-parser-js/
  ua_parser:

  # Internal version: 4.6.2
  # See: http://fontawesome.io/
  fontawesome:

  # Internal version: 1
  # https://www.algolia.com
  algolia_instant_js:
  algolia_instant_css:

  # Internal version: 1.0.0
  # https://github.com/hustcc/canvas-nest.js
  canvas_nest:



# Assets
css: css
js: js
images: images

# Theme version
version: 5.1.0

```

### 基础配置

#### 1、创建分类页面

1. 打开命令行，定位到 [http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io) 目录
2. 新建一个页面，命名为 categories

   ```text
   hexo new page categories
   ```
3. 根据提示找到新建的 index.md 文件，编辑 title 即分类页的标题

#### 2、创建标签云页面

1. 打开命令行，定位到 [http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io) 目录
2. 新建一个页面，命名为 tags

   ```text
   hexo new page tags
   ```
3. 根据提示找到新建的 index.md 文件，编辑 title 即标签页的标题

#### 3、配置模板

在站点根目录的 scaffolds 目录下的 post.md 文件，打开编辑

```text
title: {{ title }} # 文章标题
date: {{ date }} # 日期
categories: # 分类
tags: # 标签
```

原只有 title 和 date，添加你创建的分类 categories 和标签 tags

#### 4、写博客与发布

经过上述步骤，本地博客和主题设置已经完成，那么接下来就是写博客了。

博客文件需要存放到 [http://xxxx.github.io/source/_posts](https://link.zhihu.com/?target=http%3A//xxxx.github.io/source/_posts) 文件夹中，在该文件夹下面你可以按照你的博客分类建立一系列的文件夹来管理博客原文件

**1、用 Markdown 写文章**

不管用什么编辑 Markdown 文件，最后生成的 md 文件放到 [http://xxxx.github.io/source/_posts](https://link.zhihu.com/?target=http%3A//xxxx.github.io/source/_posts) 文件夹或其子文件夹中即可，如：

```text
---
title: Hexo+Next配置Blog # 这是标题
categories:  # 这里写的分类会自动汇集到 categories 页面上，分类可以多级
- 哎折腾 # 一级分类
- 技术流 # 二级分类 
tags:   # 这里写的标签会自动汇集到 tags 页面上
- Hexo # 可配置多个标签，注意格式
- Blog
---

## This is my first blog!
```

> **文字居中（写博客时）**
>
> 在你博客文章中需要居中处加上下面这段代码即可，中间的文字改成你所需要的文字
>
> ```text
> <blockquote class="blockquote-center">
> 不忘初心，这里可以写多行文字
> </blockquote>
> ```

**注意：**分类和标签是自动维护的，关键是的文章要按照规定的格式写，如上格式，可以参考

**说明：**Next 主题会自动生成目录，这也省了不少事。

**2、在本地运行测试**

打开命令行定位到 [http://xxxx.github.io](https://link.zhihu.com/?target=http%3A//xxxx.github.io) 目录，输入命令：

```text
hexo s # 这是简写 == hexo server # 启动服务预览
```

**3、在浏览器查看效果**

在浏览器中输入 [http://localhost:4000](https://link.zhihu.com/?target=http%3A//localhost%3A4000/) 访问本地博客，看看效果吧

**4、安装自动部署发布工具**

这里用到了 [hexo-deployer-git](https://link.zhihu.com/?target=https%3A//github.com/hexojs/hexo-deployer-git)，使用如下命令安装：

```text
npm install hexo-deployer-git --save
```

**5、发布到 GitHubPages**

确认在本地上显示无误之后，就可以将 md 转为 静态网页文件，然后发布到 GitHubPages 上去了

```text
hexo clean #清除缓存 网页正常情况下可以忽略此条命令
hexo g #生成静态网页
hexo d #开始部署

也可以一次性执行
hexo clean && hexo g && hexo d
```

如果是第一次部署，终端会提示要求输入用户名和密码。等命令执行完之后，过几分钟打开 [woot!](https://link.zhihu.com/?target=http%3A//xxx.github.io/) 即可看到你的个人博客了。以后要发布新文章，执行上述命令即可

### Hexo 常用命令

**Hexo 安装升级**

```text
npm install hexo -g #安装  
npm update hexo -g #升级  
hexo init #初始化
```

**常用简写**

```text
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo p == hexo publish
hexo g == hexo generate#生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy#部署
```

**启动本地服务**

```text
hexo server #Hexo #会监视文件变动并自动更新，您无须重启服务器。
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP
```

**监视文件变动**

```text
hexo generate #使用 Hexo 生成静态文件快速而且简单
hexo generate --watch #监视文件变动
hexo clean #清除缓存 网页正常情况下可以忽略此条命令
```

**部署**

```text
#两个命令的作用是相同的
hexo generate --deploy
hexo deploy --generate
hexo deploy -g
hexo server -g
```

**草稿**

```text
# 新建草稿
hexo new draft <title>
# 发布草稿为post
hexo publish draft <title>
```

**模板**

```text
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #将.deploy目录部署到GitHub
hexo new [layout] <title>
hexo new photo "My Gallery"
hexo new "Hello World" --lang tw
```

**写作时间**

```text
变量    描述
:title    标题
:year    建立的年份（4 位数）
:month    建立的月份（2 位数）
:i_month    建立的月份（去掉开头的零）
:day    建立的日期（2 位数）
:i_day    建立的日期（去掉开头的零）
```

### 个性化配置

上面完成的博客样子看起来太普通了，下面做些个性化的增强配置

#### 圆形头像

现在很多网站都流行圆形头像，但 NexT 主题默认还不支持，当然我们可以很方便地添加圆形头像效果，将以下代码覆盖主题目录下 source/css/_common/components/sidebar/sidebar-author.styl 文件内容

```text
.site-author-image {
  display: block;
  margin: 0 auto;
  padding: $site-author-image-padding;
  max-width: $site-author-image-width;
  height: $site-author-image-height;
  border: $site-author-image-border-width solid $site-author-image-border-color;

  /* 头像圆形 */
  border-radius: 80px;
  -webkit-border-radius: 80px;
  -moz-border-radius: 80px;
  box-shadow: inset 0 -1px 0 #333sf;

  /* 设置循环动画 [animation: (play)动画名称 (2s)动画播放时长单位秒或微秒 (ase-out)动画播放的速度曲线为以低速结束 
    (1s)等待1秒然后开始动画 (1)动画播放次数(infinite为循环播放) ]*/
  -webkit-animation: play 2s ease-out 1s 1;
  -moz-animation: play 2s ease-out 1s 1;
  animation: play 2s ease-out 1s 1; 

  /* 鼠标经过头像旋转360度 */
  -webkit-transition: -webkit-transform 1.5s ease-out;
  -moz-transition: -moz-transform 1.5s ease-out;
  transition: transform 1.5s ease-out;
}

img:hover {
  /* 鼠标经过停止头像旋转 
  -webkit-animation-play-state:paused;
  animation-play-state:paused;*/

  /* 鼠标经过头像旋转360度 */
  -webkit-transform: rotateZ(360deg);
  -moz-transform: rotateZ(360deg);
  transform: rotateZ(360deg);
}

/* Z 轴旋转动画 */
@-webkit-keyframes play {
  0% {
    -webkit-transform: rotateZ(0deg);
  }
  100% {
    -webkit-transform: rotateZ(-360deg);
  }
}
@-moz-keyframes play {
  0% {
    -moz-transform: rotateZ(0deg);
  }
  100% {
    -moz-transform: rotateZ(-360deg);
  }
}
@keyframes play {
  0% {
    transform: rotateZ(0deg);
  }
  100% {
    transform: rotateZ(-360deg);
  }
}

.site-author-name {
  margin: $site-author-name-margin;
  text-align: $site-author-name-align;
  color: $site-author-name-color;
  font-weight: $site-author-name-weight;
}

.site-description {
  margin-top: $site-description-margin-top;
  text-align: $site-description-align;
  font-size: $site-description-font-size;
  color: $site-description-color;
}

```

#### 腾讯公益404页面

腾讯公益404页面，寻找丢失儿童，让大家一起关注此项公益事业！效果如 [http://www.ixirong.com/404.html](https://link.zhihu.com/?target=http%3A//www.ixirong.com/404.html)

使用方法，新建 404.html 页面，放到主题的 source 目录下，内容如下：

```text
<!DOCTYPE HTML>
<html>
<head>
  <meta http-equiv="content-type" content="text/html;charset=utf-8;"/>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="robots" content="all" />
  <meta name="robots" content="index,follow"/>
</head>
<body>

<script type="text/javascript" src="http://www.qq.com/404/search_children.js"
        charset="utf-8" homePageUrl="your site url "
        homePageName="回到我的主页">
</script>

</body>
</html>
```

#### 为博客加上GitHub丝带

如果是 Next 主题（其他主题也差不多），添加 GitHub 丝带：在 themes\next\layout\_layout.swig 中加入相关代码，记得修改自己的链接

相关代码你可以在 GitHub 官方网站 [GitHub Ribbons](https://link.zhihu.com/?target=https%3A//github.com/blog/273-github-ribbons) 上进行选择

#### 加入作者版权信息

我们可以为博客文章加入作者版权信息。例如本文地址：[http://www......./](https://link.zhihu.com/?target=http%3A//www......./) 转载请注明出处，谢谢！等等。对Next主题而言，先找到/themes/next/layout/_macro/post.swig，再找到其中的微信订阅部分，如下所示：

```text
<div>
  {% if not is_index %}
    {% include 'wechat-subscriber.swig' %}
  {% endif %}
</div>
```

然后直接在其上面添加如下代码段：

```text
<div align="center">
  {% if not is_index %}
    <div class="copyright">
    <p><span>
    <b>本文地址：</b><a href="{{ url_for(page.path) }}" title="{{ page.title }}">{{ page.permalink }}</a><br /><b>转载请注明出处，谢谢！</b>
    </span></p>
    </div>
  {% endif %}
</div>
```

当然，在上面这段代码，你可以进行一些个性化编写，可以展示你自己个性化的版权信息

#### 为博客加入动态背景

首先找到\themes\next\layout\_layout.swig，在末尾前加上下面一句:（这里提供两种样式，当然你也可以自由更改）

**默认灰色线条**

```text
<script type="text/javascript" src="/js/src/particle.js"></script>
```

**浅蓝色线条**

```text
<script type="text/javascript" src="/js/src/particle.js" count="50" zindex="-2" opacity="1" color="0,104,183"></script>
```

然后在themes\source\js\src下新建文件particle.js写上以下代码:

```text
!function(){function n(n,e,t){return n.getAttribute(e)||t}function e(n){return document.getElementsByTagName(n)}function t(){var t=e("script"),o=t.length,i=t[o-1];return{l:o,z:n(i,"zIndex",-1),o:n(i,"opacity",.5),c:n(i,"color","0,0,0"),n:n(i,"count",99)}}function o(){c=u.width=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,a=u.height=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight}function i(){l.clearRect(0,0,c,a);var n,e,t,o,u,d,x=[w].concat(y);y.forEach(function(i){for(i.x+=i.xa,i.y+=i.ya,i.xa*=i.x>c||i.x<0?-1:1,i.ya*=i.y>a||i.y<0?-1:1,l.fillRect(i.x-.5,i.y-.5,1,1),e=0;e<x.length;e++)n=x[e],i!==n&&null!==n.x&&null!==n.y&&(o=i.x-n.x,u=i.y-n.y,d=o*o+u*u,d<n.max&&(n===w&&d>=n.max/2&&(i.x-=.03*o,i.y-=.03*u),t=(n.max-d)/n.max,l.beginPath(),l.lineWidth=t/2,l.strokeStyle="rgba("+m.c+","+(t+.2)+")",l.moveTo(i.x,i.y),l.lineTo(n.x,n.y),l.stroke()));x.splice(x.indexOf(i),1)}),r(i)}var c,a,u=document.createElement("canvas"),m=t(),d="c_n"+m.l,l=u.getContext("2d"),r=window.requestAnimationFrame||window.webkitRequestAnimationFrame||window.mozRequestAnimationFrame||window.oRequestAnimationFrame||window.msRequestAnimationFrame||function(n){window.setTimeout(n,1e3/45)},x=Math.random,w={x:null,y:null,max:2e4};u.id=d,u.style.cssText="position:fixed;top:0;left:0;z-index:"+m.z+";opacity:"+m.o,e("body")[0].appendChild(u),o(),window.onresize=o,window.onmousemove=function(n){n=n||window.event,w.x=n.clientX,w.y=n.clientY},window.onmouseout=function(){w.x=null,w.y=null};for(var y=[],s=0;m.n>s;s++){var f=x()*c,h=x()*a,g=2*x()-1,p=2*x()-1;y.push({x:f,y:h,xa:g,ya:p,max:6e3})}setTimeout(function(){i()},100)}();
```

#### 为博客加入鼠标点击显示红心

鼠标点击小红心在\themes\next\source\js\src文件目录下添加love.js文件。内容为：

```text
!function(e,t,a){function n(){c(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"),o(),r()}function r(){for(var e=0;e<d.length;e++)d[e].alpha<=0?(t.body.removeChild(d[e].el),d.splice(e,1)):(d[e].y--,d[e].scale+=.004,d[e].alpha-=.013,d[e].el.style.cssText="left:"+d[e].x+"px;top:"+d[e].y+"px;opacity:"+d[e].alpha+";transform:scale("+d[e].scale+","+d[e].scale+") rotate(45deg);background:"+d[e].color+";z-index:99999");requestAnimationFrame(r)}function o(){var t="function"==typeof e.onclick&&e.onclick;e.onclick=function(e){t&&t(),i(e)}}function i(e){var a=t.createElement("div");a.className="heart",d.push({el:a,x:e.clientX-5,y:e.clientY-5,scale:1,alpha:1,color:s()}),t.body.appendChild(a)}function c(e){var a=t.createElement("style");a.type="text/css";try{a.appendChild(t.createTextNode(e))}catch(t){a.styleSheet.cssText=e}t.getElementsByTagName("head")[0].appendChild(a)}function s(){return"rgb("+~~(255*Math.random())+","+~~(255*Math.random())+","+~~(255*Math.random())+")"}var d=[];e.requestAnimationFrame=function(){return e.requestAnimationFrame||e.webkitRequestAnimationFrame||e.mozRequestAnimationFrame||e.oRequestAnimationFrame||e.msRequestAnimationFrame||function(e){setTimeout(e,1e3/60)}}(),n()}(window,document);
```

找到\themes\next\layout\_layout.swing文件，在文件的后面，`</body>`之前 添加以下代码：

```text
<!-- 小红心 -->
<script type="text/javascript" src="/js/src/love.js"></script>
```

#### 添加Local Search功能

安装 hexo插件在你的站点文件夹中，用shell等运行下面这行代码：

```text
npm install hexo-generator-searchdb --save
```

**编辑站点配置文件**

添加以下字段：

```text
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

**启用本地搜索**

编辑主题配置文件启用本地搜索

```text
# Local search
local_search:
  enable: true
```

#### 修改字体大小

打开\themes\next\source\css\ _variables\base.styl文件，将$font-size-base改成16px，如下所示：

```text
$font-size-base           = 16px    # 我觉得还是默认的14比较合适
```

#### 不蒜子统计

找到\themes\next\layout\_partials\footer.swig文件，加入下面不蒜子统计代码：

```text
  |  本页点击 <span id="busuanzi_value_page_pv"></span> 次
  |  本站总点击 <span id="busuanzi_value_site_pv"></span> 次
  |  您是第 <span id="busuanzi_value_site_uv"></span> 位访客
<script async src="https://dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js">
</script>
```

#### 在标题下添加【阅读量】等

现在要添加的阅读量统计也依赖下面这段代码

```text
<script async src="https://dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js">
</script>
```

打开/themes/next/layout/_macro/post.swig，找到标签`<div class="post-meta"></div>`，在该标签内部合适的位置（如time和categories之间或categories后面）添加：

```text
{% if not is_index %}
  <span id="busuanzi_container_page_pv">  |  阅读量 <span id="busuanzi_value_page_pv"></span> 次</span>
{% endif %}
```

#### 将阅读量改为热度（更个性）

还可以继续修改，看到好多人的博客不是阅读次数（阅读量），而是热度 188 ℃，那么可以继续这样修改，首先在Next主题的/themes/next/languages/zh-Hans文件中查找”阅读次数“这几个字，可以看到，在post中的visitors被定义为“阅读次数”，把这里的“阅读次数”改为“热度”。

那么怎么在页面中显示呢。打开Next主题文件夹中layout/_macro/post.swig，在这个文件里加上摄氏度的标志，在`<span class="leancloud-visitors-count">`下面增加一行`<span>`℃即可

#### 修改标题下分类等的样式

在Next主题中，我用的是LeanCloud数据统计，默认样式是在统计数据前有个小眼睛，我感觉不好看，想把它去掉，那么打开/themes/next/layout/_macro/post.swig，找到标签`<i class="fa fa-eye"></i>`，去掉下面这段代码即可：

```text
<span class="post-meta-item-icon">
  <i class="fa fa-eye"></i>
</span>
```

#### 设置动态title

在 \themes\next\source\js\src 目录下新建 dytitle.js 。添加以下内容：

```text
<!--崩溃欺骗-->
var OriginTitile = document.title;
 var titleTime;
 document.addEventListener('visibilitychange', function () {
     if (document.hidden) {
         $('[rel="icon"]').attr('href', "/img/TEP.ico");
         document.title = ' 页面崩溃啦 ~ | cwyaml！';
         clearTimeout(titleTime);
     }
     else {
         $('[rel="icon"]').attr('href', "/favicon.ico");
         document.title = ' 噫又好了~ ' + OriginTitile;
         titleTime = setTimeout(function () {
             document.title = OriginTitile;
         }, 2000);
     }
 });
```

更改 \themes\next\layout\_layout.swig 。在 </body 之前添加：

```text
<!--卖萌-->
<script type="text/javascript" src="/js/src/dytitle.js"></script>
```

#### 首页分割线

在 \themes\next\source\css\_custom\custom.styl 文件中添加以下代码，可以修改博客首页中每篇文章的分割线长度，我设置为了100%长度

```text
//index页面中每篇文章相隔的那条线
.posts-expand {
  .post-eof {
    display: block;
    margin: $post-eof-margin-top auto $post-eof-margin-bottom;
    width: 100%;
    height: 3px;
    background: $grey-light;
    text-align: center;
  }
}
```

#### 字体、颜色等设置

在\themes\next\source\css\_variables\custom.styl 文件中添加以下代码。具体功能我已经做了注释

```text
// 标题，修改成你期望的字体族
$font-family-headings = Georgia, sans
// 修改成你期望的字体族
$font-family-base = "Microsoft YaHei", Verdana, sans-serif
// 代码字体
$code-font-family = "Input Mono", "PT Mono", Consolas, Monaco, Menlo, monospace
// 正文字体的大小
$font-size-base = 16px
// 代码字体的大小
$code-font-size = 14px
// 代码块颜色
$code-foreground = #dd0055
// Background color for <body>
$body-bg-color = #e7e5dc  //theme mist use #fdfdfd
// text-color
$text-color = #353535

```

[鸣谢文献](https://www.jianshu.com/p/e8e5addbbcfd)




.sidebar {
  margin-left: -100%;
  right: auto;
  bottom: auto;

  // Do NOT delete this line
  // or Affix (position: fixed) will not work in Google Chrome.
  -webkit-transform: none;
}

    欢迎关注我的公众号

![img](https://pic2.zhimg.com/80/v2-73a30c3faecaef3337cbba516a9a66ed_720w.jpg)
