# KS-Subdomain-Registrar

![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg) ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge) ![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

A premium, secure, and fully-featured domain registrar application designed for distributing subdomains. It features a modern React frontend and a robust Node.js backend, fully containerized for easy deployment.

## Project Overview

This project is divided into two main components:

- **[Frontend (Client)](./client/README.md)**: Built with React, Vite, Tailwind CSS, and shadcn/ui. It provides a responsive and intuitive user interface for domain search, registration, and management.
- **[Backend (Server)](./server/README.md)**: Built with Node.js, Express, Sequelize, and MySQL. It handles business logic, authentication, DNS integration (Cloudflare/PowerDNS), and database operations.

Please refer to the respective README files for detailed development instructions for each component.

## Features

- **Domain Registration**:
    - Support for standard subdomains (alphanumeric) and `ip6.arpa` (hexadecimal).
    - Real-time availability checks against local DB and upstream providers.
    - Configurable minimum subdomain length and banned keywords list.
    - Optional manual approval flow for new registrations.
- **DNS Management**:
    - Manage `NS` records for registered subdomains.
    - Integration with **Cloudflare** (via API Token) and **PowerDNS** (via API).
    - Automatic cleanup of DNS records upon domain deletion or suspension.
- **Domain Health Intelligence**: Real-time security analysis of all registered domains (VirusTotal integration) with a public reporting page.
- **Security**:
    - **Authentication**: Google OAuth, GitHub Login, OAuth 2.0 Integration and standard email/password.
    - **2FA**: Time-based One-Time Password (TOTP) support.
    - **Rate Limiting**: Strict limits on Auth (20 req/15m) and API (300 req/15m) endpoints.
    - **Protection**: hCaptcha on sensitive actions, Helmet headers, and strict CORS policies.
    - **Access Control**: Role-Based Access Control (RBAC) for Admin and User roles.
    - **Verification**: Optional Email Verification via Mailjet.
- **Admin Panel**:
    - **User Management**: View users, toggle bans, and manage roles.
    - **Domain Management**: Suspend/Activate domains, view DNS details, and force-delete.
    - **System Settings**: Configure site name, auth providers, banned keywords, and API keys.
- **Multi-lingual**: Built-in i18n support (English/Chinese).
- **Customizable**: Runtime configuration for easy white-labeling and deployment.
