# WP-UserAgent Revived

基于 [WP-UserAgent](https://www.kyleabaker.com/goodies/coding/wp-useragent/) 
（原作者：Kyle Baker）的进一步优化版本。

> ⚠️ 本项目为非官方 fork，原插件自 2020 年起停止维护。

## 主要改动

1. **现代扁平化图标**：替换了原插件中所有拟物风格的浏览器/系统图标
2. **Windows 11 识别**：通过三层 UA 改写架构实现 Win11 正确识别
   - 主题层：Chromium API 判断，将 UA 改写为 `Win NT 11`
   - 插件层：识别 `Win NT 11` 并显示 Win11 图标
   - 子插件层：页面展示时把 `Win NT 11` 修正回 `Windows NT 10.0`
3. **百科链接本地化**：将系统/浏览器介绍页由维基百科替换为百度百科
4. **部分代码使用 AI 编写**

## 安装方法

1. 下载本仓库的 `wp-useragent/` 目录
2. 上传到 `/wp-content/plugins/` 并激活
3. 如需 Win11 识别，额外安装 `zbook-win11-patch/` 子插件
4. 将 `theme-functions.php` 中的代码添加到你的主题 `functions.php`

## 许可证

- 代码：GPL-3.0（继承自原 WP-UserAgent）
- 原作者：Kyle Baker
- 图标许可证详见 ICON-LICENSE.md

## 图标来源

本插件 img/ 目录下的浏览器与系统图标来自：
- **oba.by 的 WP-UserAgent 增强版 v16.06.99**
  - 项目地址：https://cnb.cool/oba.by/wp-useragent
  - 博客文章：https://oba.by?p=400/
  - 原作者：obaby (https://oba.by)
  - 基于 kyleabaker 原版 WP-UserAgent (GPLv3)

图标随原插件分发，许可证继承原项目的 GPLv3。
若图标原作者对此有异议，可联系本仓库维护者进行替换或移除。

## 致谢

- 原插件作者 Kyle Baker 及其优秀的 WP-UserAgent
- 现代化图标的整理者oba.by
