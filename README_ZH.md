# KS 子域名注册系统

源码尚未发布，当前仍在进行初始版本的测试！请耐心等待首次发布！

![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg) ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge) ![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

一个高端、安全、功能完善的子域名分发注册系统。系统由现代的 React 前端与强大的 Node.js 后端构成，已完全容器化，便于部署。

## 项目概述

本项目分为两个主要部分：

- **[前端（Client）](./client/README.md)**：使用 React、Vite、Tailwind CSS 与 shadcn/ui 构建。提供现代化、响应式的界面，用于域名查询、注册与管理。
- **[后端（Server）](./server/README.md)**：基于 Node.js、Express、Sequelize 与 MySQL。负责业务逻辑、用户认证、DNS 集成（Cloudflare/PowerDNS）及数据库操作。

详细开发说明请参考各自的 README 文件。

## 功能特性

- **域名注册**：
    - 支持标准子域名（字母数字）与 `ip6.arpa`（十六进制）格式。
    - 实时检查本地数据库与上游提供商的可用性。
    - 可配置最小子域名长度与禁用词列表。
    - 可选的人工审批流程。
- **DNS 管理**：
    - 为已注册子域名管理 `NS` 记录。
    - 支持 **Cloudflare API Token** 与 **PowerDNS API** 集成。
    - 在域名删除或停用时自动清理 DNS 记录。
- **域名健康情报**：对所有注册域名进行实时安全分析（集成 VirusTotal），并提供公共报告页面。
- **安全**：
    - **认证**：Google OAuth、GitHub 登录、OAuth 2.0 与邮箱/密码登录。
    - **双重认证 2FA**：支持基于时间的一次性密码（TOTP）。
    - **限流**：严格限制认证接口（20 次/15 分钟）与 API（300 次/15 分钟）。
    - **保护机制**：敏感操作使用 hCaptcha，启用 Helmet 安全头与严格 CORS 策略。
    - **访问控制**：基于角色的权限控制（管理员/用户）。
    - **验证**：可选的 Mailjet 邮箱验证功能。
- **管理面板**：
    - **用户管理**：查看用户、封禁/解封、管理角色。
    - **域名管理**：暂停/启用域名、查看 DNS 信息、强制删除。
    - **系统设置**：配置站点名称、认证提供商、禁用词列表与 API 密钥。
- **多语言支持**：内置 i18n（英文/中文）。
- **高度可定制**：支持运行时配置，便于白标化部署。

---

# MIT 许可证 (MIT)
=====================

版权 © `2025` `KevvTheGoat`

特此授予获得本软件及相关文档文件（“软件”）副本的任何人免费使用本软件的权限，包括但不限于使用、复制、修改、合并、发布、分发、再许可及/或销售软件副本的权利；以及允许软件提供给的人员这样做，但须符合以下条件：

上述版权声明和本许可声明应包含在软件的所有副本或主要部分中。

本软件按“原样”提供，不附带任何形式的担保，无论是明示或暗示的，包括但不限于适销性、特定用途适用性及非侵权的担保。在任何情况下，作者或版权持有人均不对因软件或软件使用或其他交易中的使用或无法使用而产生的任何索赔、损害或其他责任负责，无论是在合同、侵权行为或其他方面。

