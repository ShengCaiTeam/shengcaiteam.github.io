---
layout: post
title: "_config.yml 中的布局设置及其他内容"
tags:
  - jekyll
  - dactl
  - howto
hero: https://source.unsplash.com/collection/582860/
overlay: red
disqus: true
---

dactl 的所有配置都必须在`_config.yml`文件中设置。请继续阅读，了解您可以切换的所有功能，包括配置布局。
{: .lead}

我把 dactl 的 `_config.yml` 分成了两部分。第一部分应该由你自己配置，第二部分包含重要的 Jekyll 和构建设置，除非你知道自己在做什么，否则最好不要去管它。
<!–-break-–>

让我们逐行查看第一部分（可配置部分）中的每一行：

```yaml
# Base blog settings
blog:
  title: dactl
  description: >
    this should contain a proper description
  # Layout configuration
  logo_path: "assets/img/dactl.svg" # path to logo file
  search_path:# "yourgitusername.github.io"
    # needed for searchbox in archive page
  hero_layout: true # turn on hero layout for blog and posts
  hero_placeholder: "assets/img/generic_hero.jpg" # placeholder for hero
  excerpts: true # show excerpts instead of full post content on blog page
  inline_footnotes: true # enable/disable barefoot inline footnotes
  titles_only: false # titles only on main blog page

# Fonts
font: '"Rubik", -apple-system, BlinkMacSystemFont, "Helvetica Neue", sans-serif'
load_google_fonts: "Rubik:400,400italic,700,700italic"

# Author info
author:
  fullname: Your Name
  rss: true # generate RSS feed and show it's icon in header
  mail: your@email.com # change to your e-mail address
  twitter: twitter-user-name
  github: github-user-name
  youtube: youtube-user-name
  stackoverflow: stackoverflow-user-name
  disqus: dactl # your disqus site name
  google_analytics: # 'UA-XXXXXXXX-X'
  photo: "uploads/me2.png"
  photo2x: "uploads/me.png"

baseurl:
  "/dactl/" # the subpath of your site, e.g. /blog/, set to '' in case of hosting on GitHub pages
  # i.e. `http://<username>.github.io`
url: "" # the base hostname & protocol for your site
```

## Base blog settings

- `title` - 您博客的标题 `<title>` 标签，并在标题.
- `description` - 您博客的描述，显示在页脚中

## Layout settings

- `logo_path` - 用作徽标的 .svg 图像的路径
- `search_path` - 指向您博客的路径，DuckDuckGo 的搜索栏需要该路径才能在 Archive 页面找到。
- `hero_layout` - true / false - 打开或关闭主图像布局。关闭后，您无需在帖子的 YAML 前端提供图像和叠加层，并且布局会略有调整。
- `hero_placeholder` - 图像的路径，当没有为帖子设置英雄时，该图像将用作占位符，可选。
- `excerpts` - true 或 false - 打开或关闭文章摘录。设置为 "false "时，您将在博客页面上看到每篇文章的全文内容。
- `inline_footnotes` - true 或 false - 设置为 "false "时，将关闭 Barefoot.js 内嵌脚注。
- `titles_only` - true 或 false - 设置为 "true "时，Jekyll 将只生成包含文章标题的博客布局。当设置为 "true "时，"hero_layout "和 "excerpts "会被 "titles_only "覆盖。

## Fonts | 字体

- `font` - 主题排版使用的字体系列名称。
- `load_google_fonts` - 选择应加载的字体系列，由 [google fonts](https://fonts.google.com) 提供。要更改字体，您需要提供字体名称和变体--字体重量必须为 400 和 700。
  选择应加载的字体系列，由 [google fonts](https://fonts.google.com) 提供。要更改字体，您需要提供字体名称和变体--字体重量必须为 400 和 700。

## Author info | 作者信息

- `fullname` - 您的名字和姓氏或昵称，在整个博客中使用。
- `rss` - true or false - 打开或关闭 RSS 源。
- `mail` - 您的电子邮件地址。
- `twitter` - 你的推特用户名
- `github` - 您的 Github 用户名
- `youtube` - 您的 YouTube 用户名
- `stackoverflow` - 您的 Stackoverflow 用户名
- `disqus` - 您的 Disqus 站点名称。
- `photo` - 您的头像或照片，用于“关于”页面。
- `photo2x` - 与上述相同，但分辨率更高。

## Google Analytics （分析）

- `google_analytics` - 如果您想使用它，请在此处提供您的 Google Analytics ID。
- `baseurl` - 博客的子路径，例如 `/blog`，如果托管在 Github 页面上，则留空 - `yourusername.github.io
