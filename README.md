# HuXinxin0226 · 个人博客

这是一个用 Jekyll + GitHub Pages 搭建的纯静态个人博客，不需要 Node.js、npm 或 React。
写 Markdown 文章，提交到 `main` 分支，GitHub Actions 会自动构建并发布到 GitHub Pages。

## 技术说明

- 构建发生在 GitHub Actions 上（`Build and deploy Jekyll site` workflow），本地无需安装 Ruby、Jekyll、Node.js 或 npm。
- 文章写在 `_posts/`，文件名格式为 `YYYY-MM-DD-title.md`，开头保留 Front Matter（`layout: post`、`title`、`date`、`excerpt`、`tags`）。
- 首页内容与项目卡片在 `index.html` 中修改；关于页在 `about.md`；配色与排版在 `assets/style.css`。
- 个人信息（站名、简介、时区）在 `_config.yml`。

## 写一篇新文章

在 `_posts/` 中复制示例文章，文件名使用：

```text
YYYY-MM-DD-title.md
```

文章开头保留 Front Matter：

```yaml
---
layout: post
title: 文章标题
date: 2026-10-10
excerpt: 一句话摘要
tags:
  - 学习
---
```

第二个 `---` 之后直接写 Markdown 正文：标题、段落、列表、链接、代码块都可以使用。

## 发布流程

1. 修改或新增 `_posts/*.md`。
2. 修改首页内容时编辑 `index.html`；关于页编辑 `about.md`；配色编辑 `assets/style.css`。
3. `git add`、`git commit`、`git push` 到 `main`。
4. GitHub Actions 自动运行 Jekyll，将 Markdown 编译成 HTML 并发布到 GitHub Pages。

## 第一次启用 Pages

把仓库推送到 GitHub 后，在仓库中打开：

```text
Settings → Pages → Source → GitHub Actions
```

之后每次推送到 `main`，workflow 都会重新生成网站。

博客地址：https://HuXinxin0226.github.io
