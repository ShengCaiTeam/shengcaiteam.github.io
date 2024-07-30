---
layout: post
title: "欢迎来到 jekyll"
date: 2024-07-30 11:30:29 +0700
categories: jekyll update
---

从 Jekyll 的帮助信息中，我们可以看到几个有用的子命令和选项。让我们来解释一些常用的命令及其用法：

### 创建新站点

你已经创建了一个新站点，可以使用以下命令：

```shell
jekyll new myblog
```

### 构建站点

构建站点会将所有的源文件转换为静态文件并存储在 `_site` 目录中：

```shell
jekyll build
```

### 运行服务器

本地运行 Jekyll 服务器以预览你的站点：

```shell
jekyll serve
```

### 使用额外选项

你可以指定源目录和目标目录：

```shell
jekyll build --source your_source_directory --destination your_destination_directory
jekyll serve --source your_source_directory --destination your_destination_directory
```

例如，如果你想将站点构建到 `./dist` 目录中，可以这样做：

```shell
jekyll build --destination ./dist
jekyll serve --destination ./dist
```

### 运行命令

以下是一些常用命令的示例：

1. **构建站点**：

   ```shell
   jekyll build
   ```

2. **运行服务器**：

   ```shell
   jekyll serve
   ```

3. **指定目标目录**：
   ```shell
   jekyll build --destination ./dist
   jekyll serve --destination ./dist
   ```

请尝试这些命令，并确保在项目的根目录中运行它们。如果遇到任何问题，请提供详细的错误信息。
