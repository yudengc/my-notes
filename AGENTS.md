# AGENTS.md

This file provides guidance to AI coding agents when working with code in this repository.

## 项目概述

这是一个基于 **Docsify + GitHub Pages** 的个人笔记站点，使用纯 Markdown 编写，无构建步骤。内容覆盖 Java、AI、大数据、架构等技术栈的学习笔记和实战记录。

- 站点标题：邓钰个人笔记
- GitHub 仓库：yudengc/my-notes
- 部署方式：GitHub Pages（通过 `.nojekyll` 禁用 Jekyll）

## 本地预览

```bash
# 安装 docsify-cli
npm i -g docsify-cli

# 启动本地服务（默认 http://localhost:3000）
docsify serve .
```

## 目录结构与约定

- `index.html` — Docsify 入口配置，包含插件（搜索、分页、emoji、图片缩放、KaTeX 数学公式、代码复制）
- `_sidebar.md` — 全局侧边栏导航，**新增笔记文件后必须在此添加对应链接**
- `template.md` — 新笔记模板，包含标准章节：背景/问题 → 核心原理 → 代码实战 → 踩坑 & 解决 → 总结 & 延伸
- 内容按主题分目录：`java/`、`ai/`、`notes/`、`tricks/`、`life/`、`智能问数/`、`绩效自评/` 等

## 写笔记的约定

1. 新笔记参考 `template.md` 的结构编写
2. 文件使用中文命名或英文短横线命名（如 `virtual-threads-deep-dive.md`）
3. 新建文件后必须在 `_sidebar.md` 中添加导航条目，否则页面上无法访问
4. 代码块使用 Prism 语法高亮，支持 `bash`、`python`、`java` 等语言
