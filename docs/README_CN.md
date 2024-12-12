# Astro Zen 博客

一个使用 Astro 构建的极简、响应式和 SEO 友好的博客模板。具有简洁的设计、暗色模式支持和基于 markdown 的内容管理。

在线演示: [Yujian's blog](https://blog.larryxue.dev/)

如果您觉得这个项目有帮助，请考虑给我点个star～ ⭐️。

## 特性

- 📝 支持 Markdown/MDX 内容创作
- 🎨 简洁的极简设计
- 🏷️ 基于标签的组织方式
- 🌓 暗色模式支持
- 🔍 SEO 优化
- 📱 完全响应式
- 🔗 社交媒体集成
- 📰 RSS 订阅支持
- ⚡ 优秀的性能

## 安装

1. 克隆仓库：

   ```bash
   git clone https://github.com/larry-xue/astro-zen-blog.git
   cd astro-zen-blog
   ```

2. 安装依赖：

   ```bash
   npm install
   ```

3. 启动开发服务器：

   ```bash
   npm run dev
   ```

## 配置

### 网站设置

1. 打开 `src/config.ts` 并自定义您的网站设置：

```typescript
export const siteConfig: SiteConfig = {
  site: "https://example.com/", // 您的网站 URL
  title: "您的博客",
  slogan: "探索世界与自我",
  description: "在这里写描述",
  social: {
    github: "https://github.com/username",
    linkedin: "https://www.linkedin.com/in/username",
    email: "your@email.com",
    rss: true,
  },
  homepage: {
    maxPosts: 5, // 显示的最大文章数量
    tags: [], // 仅显示包含这些标签的文章
    excludeTags: [], // 排除包含这些标签的文章
  }
};
```

### 首页文章过滤

如果您想要对首页文章进行更多自定义，可以通过更新 `src/utils/posts.ts` 中的 `filterPublishedPosts` 函数来自定义显示的文章。

### 主题

在 `tailwind.config.js` 中更新主要和次要颜色：

## 编写内容

1. 在 `src/content/blog/` 目录下创建新的博客文章
2. 使用以下前置元数据模板：

```markdown
---
title: "文章标题"
description: "文章简短描述"
date: YYYY-MM-DD
tags: ["标签1", "标签2"]
image: "封面图片 URL"
---

您的内容写在这里...
```

当然，你可以根据需要在 `src/content/config.ts` 中自定义元数据。

## 构建和部署

1. 构建您的网站：

   ```bash
   npm run build
   ```

2. 部署选项：

   - **Cloudflare Pages**: [部署到 Cloudflare Pages](https://developers.cloudflare.com/pages/framework-guides/deploy-an-astro-site/#deploy-with-cloudflare-pages)

## 项目结构

```
astro-zen-blog/
├── src/
│   ├── content/
│   │   └── blog/    # 博客文章
│   ├── layouts/     # 页面布局
│   ├── components/  # UI 组件
│   └── config.ts    # 网站配置
├── public/          # 静态资源
└── astro.config.mjs # Astro 配置
```

## 功能路线图

- [ ] 搜索功能
- [ ] 评论集成
- [ ] ...更多

## 贡献

欢迎贡献！您可以：

1. Fork 这个仓库
2. 创建您的功能分支
3. 提交一个拉取请求

## 许可证

该项目基于 MIT 许可证 - 查看 LICENSE 文件了解详情。
