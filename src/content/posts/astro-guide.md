---
title: 'Astro 博客搭建指南'
description: '从零开始，一步步搭建一个基于 Astro 的个人博客。'
date: 2026-07-08
tags: ['Astro', '教程', 'GitHub Pages']
category: '技术'
---

## 为什么选择 Astro？

Astro 是一个现代化的静态站点生成器，它的核心理念是 **"Zero JS by default"**（默认零 JavaScript）。

这意味着你的博客页面在浏览器中加载时，不会携带任何不必要的 JavaScript，从而实现极致的加载速度。

## 技术栈总览

| 技术 | 用途 |
|------|------|
| Astro | 静态站点生成 |
| MDX | 增强型 Markdown |
| Pagefind | 全文搜索 |
| Giscus | 评论系统 |
| GitHub Pages | 部署托管 |

## 核心特性

### 1. 内容集合

Astro 的内容集合功能让你可以像管理数据库一样管理 Markdown 文件：

- ✅ 类型安全的 frontmatter 校验
- ✅ 自动生成的 TypeScript 类型
- ✅ 灵活的查询和过滤 API

### 2. 岛屿架构

Astro 的"岛屿架构"允许你在静态页面中嵌入交互式组件：

```astro
---
// 页面大部分是静态 HTML
---
<StaticHeader />
<!-- 只有需要交互的部分才加载 JS -->
<SearchBox client:load />
<StaticFooter />
```

### 3. 零配置部署

只需推送代码到 GitHub，GitHub Actions 会自动构建并部署到 GitHub Pages。

## 写作工作流

1. 在 `src/content/posts/` 下创建 `.md` 文件
2. 填写 frontmatter（标题、日期、标签、分类）
3. 用 Markdown 编写内容
4. 推送到 GitHub，自动部署

## 小结

Astro 是目前搭建个人博客的最佳选择之一。它既有现代框架的灵活性，又有静态站点的极致性能。希望这篇指南对你有所帮助！
