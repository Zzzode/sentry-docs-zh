# Sentry 文档完整指南

## 📋 项目概述

Sentry是一个**代码级可观察性平台**，为开发者提供全面的错误监控、性能追踪和用户体验分析解决方案。该平台支持100多个平台和框架，涵盖30多种编程语言，帮助团队快速识别、调试和解决应用程序中的问题。

---

## 🗂️ 文档结构地图 (与实际目录一一对应)

### 📁 1. 账户管理 (`/account/`)

#### 1.1 🔑 认证令牌管理 (`/account/auth-tokens/`)

- **功能**: API访问令牌创建、管理和安全配置
- **文件**: `index.mdx`, `img/` 目录包含截图指南

#### 1.2 ⚙️ 用户设置 (`/account/user-settings/`)

- **功能**: 个人资料、通知偏好、安全设置
- **文件**: `index.mdx`, `img/` 目录包含界面截图

---

### 📁 2. API 文档 (`/api/`)

#### 2.1 🔐 认证与权限 (`/api/auth.mdx`)

- **功能**: API认证方式、令牌管理、权限说明

#### 2.2 📖 API 使用指南 (`/api/guides/`)

- **create-auth-token.mdx**: 创建认证令牌完整教程
- **teams-tutorial.mdx**: 团队管理API使用示例
- **img/**: 相关截图和图表

#### 2.3 📊 核心API功能

- **auth.mdx**: 认证机制详解
- **pagination.mdx**: 分页查询参数和使用方法
- **permissions.mdx**: 权限系统和访问控制
- **ratelimits.mdx**: 速率限制规则和最佳实践
- **requests.mdx**: API请求格式和响应结构

---

### 📁 3. CLI 工具 (`/cli/`)

#### 3.1 🚀 安装与配置

- **installation.mdx**: 多平台安装指南 (npm, brew, 直接下载)
- **configuration.mdx**: 配置文件设置和环境变量

#### 3.2 🔧 核心功能模块

- **crons.mdx**: 定时任务监控配置和管理
- **dif.mdx**: 调试信息文件(Debug Information Files)管理
- **releases.mdx**: 版本发布管理和源映射上传
- **send-event.mdx**: 手动事件发送和测试
- **index.mdx**: CLI工具总览和快速开始

---

### 📁 4. 核心概念 (`/concepts/`)

#### 4.1 📊 数据管理 (`/concepts/data-management/`)

- **event-grouping/**: 事件分组算法和配置
- **filtering/**: 数据过滤规则和配置
- **data-forwarding/**: 数据转发和第三方集成
- **size-limits.mdx**: 数据大小限制和配额管理

#### 4.2 🔍 搜索与查询 (`/concepts/search/`)

- **searchable-properties/**: 可搜索属性完整列表
- **saved-searches.mdx**: 保存搜索条件和分享
- **index.mdx**: 搜索语法和使用技巧

#### 4.3 🔄 迁移指南 (`/concepts/migration/`)

- **index.mdx**: 版本迁移和升级路径
- **img/**: 迁移过程截图

#### 4.4 📡 开放协议 (`/concepts/otlp/`)

- **index.mdx**: OpenTelemetry协议(OTLP)集成

#### 4.5 📖 关键术语 (`/concepts/key-terms/`)

- **dsn-explainer.mdx**: DSN(数据源名称)详解
- **environments/**: 环境概念和最佳实践
- **sample-rates/**: 采样率配置和影响
- **tracing/**: 分布式追踪核心概念
- **key-terms.mdx**: Sentry术语词汇表

---

### 📁 5. 平台支持 (`/platforms/`)

#### 5.1 📱 移动端平台

- **android/**: Android完整集成指南
  - configuration/, data-management/, enhance-errors/
  - enriching-events/, features/, integrations/
  - logs/, profiling/, tracing/, usage/
- **apple/**: iOS/macOS/watchOS/tvOS支持
  - common/, guides/, index.mdx
- **react-native/**: React Native跨平台
- **unity/**: Unity游戏引擎集成
- **unreal/**: Unreal Engine集成

#### 5.2 💻 后端平台

- **python/**: Python完整支持
  - crons/, logs/, tracing/, usage/
- **java/**: Java和JVM语言
  - common/, guides/, usage.mdx
- **go/**: Go语言SDK
  - common/, guides/, legacy-sdk/
- **php/**: PHP集成方案
  - common/, guides/, legacy-sdk/
- **ruby/**: Ruby和Rails
- **rust/**: Rust语言支持
- **elixir/**: Elixir和Phoenix框架

#### 5.3 🌐 前端平台

- **javascript/**: JavaScript浏览器支持
- **dart/**: Dart和Flutter框架
- **dotnet/**: .NET平台支持

#### 5.4 🎮 游戏和特殊平台

- **godot/**: Godot引擎集成
- **native/**: 原生C/C++应用
- **nintendo-switch/**: 任天堂Switch
- **playstation/**: PlayStation平台
- **xbox/**: Xbox平台支持

---

### 📁 6. 产品功能 (`/product/`)

#### 6.1 🐛 问题管理 (`/product/issues/`)

- **index.mdx**: 错误监控和问题追踪核心功能
- **img/**: 界面截图和功能演示

#### 6.2 📊 数据分析 (`/product/explore/`)

- **index.mdx**: 数据探索和分析平台
- **logs/**: 日志分析和查询
- **profiling/**: 性能分析工具

#### 6.3 🚀 发布管理 (`/product/releases/`)

- **index.mdx**: 版本发布和部署监控
- **health/**: 发布健康状况监控
- **setup/**: 发布集成配置
- **usage/**: 发布版本使用指南

#### 6.4 🔔 警报系统 (`/product/alerts/`)

- **index.mdx**: 智能警报和通知系统
- **img/**: 警报配置界面截图

#### 6.5 📱 用户体验 (`/product/explore/session-replay/`)

- 用户会话重放和体验分析

#### 6.6 📈 性能洞察 (`/product/insights/`)

- **index.mdx**: 应用性能监控总览
- **ai/**: AI代理性能监控
- **backend/**: 后端服务性能
- **frontend/**: 前端性能分析
- **mobile/**: 移动端性能优化

#### 6.7 ⏰ 定时任务 (`/product/crons/`)

- **index.mdx**: 定时任务监控和警报
- **img/**: 配置界面和监控图表

#### 6.8 📊 统计报告 (`/product/stats/`)

- **index.mdx**: 组织级别使用统计
- **img/**: 统计图表和报告示例

#### 6.9 🎯 项目设置 (`/product/projects/`)

- **index.mdx**: 项目创建和管理

#### 6.10 🔍 仪表板 (`/product/dashboards/`)

- 自定义监控仪表板创建和管理

#### 6.11 🛡️ 代码覆盖率 (`/product/codecov/`)

- **index.mdx**: 代码覆盖率集成
- **set-up.mdx**: 配置和设置指南
- **img/**: 覆盖率报告界面

#### 6.12 🤖 AI功能 (`/product/ai-in-sentry/`)

- **seer/**: AI驱动的错误分析和修复建议

#### 6.13 🔧 工具栏 (`/product/sentry-toolbar/`)

- 开发工具栏和调试助手

#### 6.14 🆙 上线监控 (`/product/uptime-monitoring/`)

- URL可用性监控和警报

#### 6.15 👥 用户反馈 (`/product/user-feedback/`)

- 应用内用户反馈收集和分析

---

### 📁 7. 组织管理 (`/organization/`)

#### 7.1 🔐 身份验证 (`/organization/authentication/`)

- **index.mdx**: 认证方式总览
- **sso/**: 单点登录(SSO)配置
- **two-factor-authentication/**: 双因素认证设置

#### 7.2 🔗 集成中心 (`/organization/integrations/`)

- **index.mdx**: 第三方集成总览
- **source-code-mgmt/**: 源代码管理集成 (GitHub, GitLab等)
- **issue-tracking/**: 问题跟踪系统集成 (Jira, Linear等)
- **notification-incidents/**: 通知和事件管理
- **deployment/**: 部署平台集成
- **cloud-monitoring/**: 云监控服务
- **compliance/**: 合规性工具集成
- **data-visualization/**: 数据可视化平台
- **feature-flag/**: 功能开关服务集成
- **session-replay/**: 会话重放工具
- **debugging/**: 调试工具集成
- **integration-platform/**: 自定义集成平台
- **troubleshooting.mdx**: 集成问题排查

#### 7.3 👥 成员管理 (`/organization/membership/`)

- **index.mdx**: 团队和用户管理
- **img/**: 管理界面截图

#### 7.4 ⚙️ 高级功能

- **dynamic-sampling/**: 动态采样配置
- **early-adopter-features/**: 早期采用者功能
- **data-storage-location/**: 数据存储地理位置
- **getting-started/**: 管理员快速入门指南

---

### 📁 8. 定价与配额 (`/pricing/`)

#### 8.1 💰 定价方案 (`/pricing/index.mdx`)

- 免费、团队、商业、企业方案对比

#### 8.2 📊 配额管理 (`/pricing/quotas/`)

- **index.mdx**: 数据配额和使用监控
- **img/**: 配额管理界面截图

#### 8.3 💳 历史定价 (`/pricing/legacy-pricing.mdx`)

- 旧版本定价方案说明

---

### 📁 9. 贡献指南 (`/contributing/`)

#### 9.1 🎯 方法论 (`/contributing/approach/`)

- **index.mdx**: 文档贡献总体方法
- **product-docs/**: 产品文档编写规范
- **sdk-docs/**: SDK文档编写指南

#### 9.2 📄 页面规范 (`/contributing/pages/`)

- **index.mdx**: 页面创建和编辑规范
- **frontmatter.mdx**: 页面元数据配置
- **images.mdx**: 图片使用规范
- **components.mdx**: 自定义组件开发
- **charts-diagrams.mdx**: 图表和流程图规范
- **banners.mdx**: 通知横幅使用
- **redirects.mdx**: 页面重定向配置
- **search.mdx**: 搜索优化建议
- **variables.mdx**: 变量和占位符使用

#### 9.3 🔧 环境配置 (`/contributing/environment.mdx`)

- 本地开发环境搭建指南

#### 9.4 🔗 链接规范 (`/contributing/linking.mdx`)

- 内部和外部链接最佳实践

#### 9.5 📱 平台文档 (`/contributing/platforms/`)

- **index.mdx**: 平台文档维护指南
- **platform-icons/**: 平台图标规范
- **versioning.mdx**: 版本管理和发布流程

---

### 📁 10. 安全与合规 (`/security-legal-pii/`)

#### 10.1 🔒 数据安全

- **传输加密**: TLS 1.3端到端加密
- **存储加密**: AES-256静态数据加密
- **密钥管理**: 企业级密钥管理服务
- **访问控制**: 基于角色的细粒度权限(RBAC)

#### 10.2 📋 合规认证

- **SOC2 Type II**: 安全控制审计认证
- **ISO 27001**: 信息安全管理体系
- **GDPR**: 欧盟通用数据保护条例合规
- **HIPAA**: 医疗行业数据保护标准
- **CCPA**: 加州消费者隐私法案

#### 10.3 🛡️ 隐私保护

- **数据匿名化**: 自动PII(个人身份信息)脱敏
- **数据保留**: 可配置的数据保留策略
- **审计日志**: 完整的操作和数据访问记录
- **地理合规**: 支持数据本地化存储要求

---

## 🗺️ 快速导航

### 🚀 新手入门路径

1. **选择平台**: `/platforms/[your-platform]/`
2. **基本配置**: `/platforms/[your-platform]/configuration/`
3. **错误监控**: `/product/issues/`
4. **性能监控**: `/product/insights/`
5. **警报设置**: `/product/alerts/`

### 🔧 开发者工具

- **CLI工具**: `/cli/` - 命令行管理和调试
- **REST API**: `/api/` - 程序化访问
- **搜索语法**: `/concepts/search/` - 高级查询

### 👥 团队管理

- **组织设置**: `/organization/`
- **成员管理**: `/organization/membership/`
- **集成配置**: `/organization/integrations/`

### 💰 成本控制

- **定价方案**: `/pricing/`
- **配额管理**: `/pricing/quotas/`
- **使用统计**: `/product/stats/`

---

## 📞 支持与资源

- **文档贡献**: `/contributing/` - 如何改进本文档
- **社区支持**: 通过GitHub Issues反馈问题
- **官方支持**: sentry.io官方支持渠道

> **注意**: 本文档结构与 `/docs/` 目录完全对应，每个文件和目录都有实际对应关系。如发现不一致，请参考实际目录结构。
