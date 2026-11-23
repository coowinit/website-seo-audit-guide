# Website SEO Audit Guide

网站 SEO 排查与优化操作指南。面向 B2B 网站技术维护及 SEO 协同工作，以“检查 → 证据 → 判断 → 整改 → 验收”为主线。

## v1.1 功能

- 10 个章节、25 个操作检查项，涵盖访问、索引、Canonical、页面标题、性能、内容、链接与转化。
- 各检查项包含工具、操作步骤、合格判断、常见误判、整改方式和验收建议。
- 章节导航、全站搜索、优先级筛选、检查进度（浏览器 localStorage）、深浅主题、打印、响应式布局。
- Screaming Frog 实战专题新增 8 个检查项目与 3 张示例截图，涵盖 Dashboard、Canonical、H1/H2、JavaScript 渲染及证据导出。
- 纯静态 HTML/CSS/JavaScript 和 JSON，无数据库或打包工具。

## 本地预览

请使用本地 HTTP 服务器（直接双击 HTML 时，浏览器可能禁止 JSON 文件读取）：

```bash
cd website-seo-audit-guide
python -m http.server 8000
```

打开 http://localhost:8000/ 。也可使用 VS Code Live Server。

## GitHub Pages 发布

1. 项目已托管于公开仓库 `coowinit/website-seo-audit-guide`；后续更新提交至 `main`。
2. 在仓库 Settings → Pages → Build and deployment 中选择 Deploy from a branch。
3. 选择 `main` 分支和 `/ (root)`，保存。
4. 访问 `https://<你的用户名>.github.io/website-seo-audit-guide/`。

项目仓库：https://github.com/coowinit/website-seo-audit-guide/ 。页面右上角的 GitHub 图标已指向本仓库。

## 目录

```text
index.html
assets/css/style.css
assets/js/app.js
data/sections.json
data/checks.json
assets/images/screaming-frog/
docs/
README.md
```

## 维护规范

- `data/sections.json` 定义章节；`data/checks.json` 定义检查项目。
- `checks.json` 的 `id` 必须唯一且稳定，变更 ID 会让用户保存在本地的完成进度失效。
- 每一条检查项尽量保留：检查目标、操作、合格判断、误判提醒、整改和验收。
- 外部链接引用官方文档优先，定期复核；不把工具警告当成真实故障。
- 本项目的案例属于方法示例，不构成对具体网站当前情况的持续监控。

## 后续路线图

- v1.2：脱敏案例库、检查记录导出及 Word 报告模板。

## 示例截图与使用说明

- `assets/images/screaming-frog/` 中图片来源于实际排查时的工具截图，仅用于解释操作界面。公开仓库发布前应再次确认截图中域名、数据和第三方软件界面使用是否符合发布要求。
- 操作菜单与筛选名可能随 Screaming Frog 版本变化，以 [官方用户指南](https://www.screamingfrog.co.uk/seo-spider/user-guide/) 为准；JavaScript 渲染功能可能要求付费许可。
- 本地进度存于浏览器 localStorage，项目更新时不要修改已有检查项的 `id`。

## 许可

项目内容和代码供个人维护与内部学习使用。公开发布前请确认截图、客户域名及业务资料的披露权限。
