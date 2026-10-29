<p align="center">
  <img src="assets/yyc3-family.png" alt="YYC³ Family" width="720">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/YYC3-Family-00d4ff?style=flat-square" alt="YYC3 Family">
  <img src="https://img.shields.io/github/license/YYC-Cube/YYC3-AI-Growth-Guardian-System?style=flat-square" alt="License">
  <img src="https://img.shields.io/github/last-commit/YYC-Cube/YYC3-AI-Growth-Guardian-System?style=flat-square" alt="Last Commit">
</p>

# YYC³ 智能插拔式移动AI系统

<div align="center">

![YYC³ Logo](https://img.shields.io/badge/YYC³-智能插拔式移动AI系统-blue?style=for-the-badge)
![Version](https://img.shields.io/badge/version-1.0.0-green?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![Bun](https://img.shields.io/badge/runtime-Bun-black?style=for-the-badge)

**Intelligent Pluggable Mobile AI System**

基于事件驱动+目标驱动混合架构的智能插拔式移动AI系统，支持动态工具注册、知识库管理、多模态AI交互和微服务部署。

[快速开始](#快速开始) • [功能特性](#功能特性) • [系统架构](#系统架构) • [API文档](#api文档) • [部署指南](#部署指南)

</div>

## 📋 目录

- [项目概述](#项目概述)
- [功能特性](#功能特性)
- [系统架构](#系统架构)
- [技术栈](#技术栈)
- [快速开始](#快速开始)
- [开发指南](#开发指南)
- [部署指南](#部署指南)
- [API文档](#api文档)
- [配置说明](#配置说明)
- [监控与运维](#监控与运维)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

## 🎯 项目概述

YYC³智能插拔式移动AI系统是一个现代化的、可扩展的AI服务平台，采用微服务架构和容器化部署，提供：

- **智能拖拽AI组件** - 支持React DnD的可拖拽AI助手
- **事件驱动核心引擎** - 混合事件驱动和目标驱动架构
- **动态工具生态** - 自动工具发现与注册系统
- **RAG知识库** - 向量存储和检索增强生成
- **多模态交互** - 文本、语音、图像、文件全支持
- **微服务架构** - 完整的服务编排和API网关
- **实时学习系统** - 三层学习架构（行为、策略、知识）

## ✨ 功能特性

### 🤖 智能AI助手

- **拖拽式界面** - 基于React DnD的智能组件
- **多视图切换** - 对话、工具、洞察多模式
- **位置优化** - 自动最佳位置计算
- **实时任务监控** - 动态任务状态跟踪

### 🧠 核心系统引擎

- **AgenticCore** - 事件驱动+目标驱动混合架构
- **ServiceOrchestrator** - 微服务编排与协调
- **GoalManagementSystem** - 目标生命周期管理
- **MetaLearningSystem** - 三层智能学习架构

### 🛠️ 工具与知识系统

- **ToolManager** - 动态工具发现与注册
- **KnowledgeManager** - RAG知识库管理
- **APIGateway** - 统一API网关与负载均衡
- **向量数据库** - 高效相似度搜索

### 🎨 多模态交互

- **文本对话** - 智能回复与上下文理解
- **语音识别** - 实时语音转文字
- **图像处理** - 视觉内容理解与分析
- **文件上传** - 多格式文件智能处理

### 🏗️ 基础设施

- **容器化部署** - Docker + Docker Compose
- **微服务架构** - 服务发现与健康检查
- **实时通信** - WebSocket双向通信
- **监控告警** - Prometheus + Grafana + Jaeger

## 🏗️ 系统架构

```mermaid
graph TB
    subgraph "前端层"
        A[智能AI组件] --> B[React应用]
        B --> C[拖拽界面]
    end

    subgraph "API网关层"
        D[API Gateway] --> E[负载均衡]
        D --> F[认证授权]
        D --> G[限流熔断]
    end

    subgraph "服务层"
        H[AgenticCore] --> I[事件处理]
        J[ToolManager] --> K[工具注册]
        L[KnowledgeManager] --> M[RAG检索]
        N[GoalManager] --> O[目标管理]
        P[MetaLearning] --> Q[学习系统]
    end

    subgraph "数据层"
        R[PostgreSQL] --> S[关系数据]
        T[Redis] --> U[缓存会话]
        V[Elasticsearch] --> W[搜索索引]
        X[VectorDB] --> Y[向量存储]
    end

    A --> D
    D --> H
    D --> J
    D --> L
    D --> N
    D --> P

    H --> R
    J --> T
    L --> V
    L --> X
    N --> R
    P --> R
```

### 核心组件

| 组件 | 功能 | 状态 |
|------|------|------|
| **AgenticCore** | 事件驱动核心引擎 | ✅ 完成 |
| **ServiceOrchestrator** | 服务编排管理 | ✅ 完成 |
| **ToolManager** | 工具注册发现 | ✅ 完成 |
| **KnowledgeManager** | RAG知识库 | ✅ 完成 |
| **APIGateway** | 统一API网关 | ✅ 完成 |
| **IntelligentWidget** | 智能拖拽组件 | ✅ 完成 |
| **EnhancedAIGirl** | 增强AI助手 | ✅ 完成 |

## 🛠️ 技术栈

### 前端技术

- **React 19.2.3** - 用户界面框架
- **Next.js 14.2.35** - React应用框架
- **TypeScript 5** - 类型安全的JavaScript
- **TailwindCSS 4.1.9** - 原子化CSS框架
- **Radix UI** - 无样式组件库（包含完整的UI组件集合）
- **Framer Motion 12.23.25** - 动画库
- **React DnD 16.0.1** - 拖拽功能库
- **React Beautiful DnD 13.1.1** - 拖拽功能库
- **Lucide React 0.454.0** - 图标库
- **React Icons 5.5.0** - 图标库
- **React Hook Form 7.60.0** - 表单处理
- **Zod 3.25.76** - 数据验证
- **TanStack React Query 5.56.2** - 数据获取和状态管理
- **Redux Toolkit 2.11.2** - 状态管理
- **Redux Persist 6.0.0** - 状态持久化
- **SWR** - 数据获取库
- **next-intl 4.6.1** - 国际化支持
- **next-themes 0.4.6** - 主题管理
- **date-fns 4.1.0** - 日期处理
- **React Dropzone 14.3.8** - 文件上传
- **React Toastify 11.0.5** - 通知提示
- **Sonner 1.7.4** - 通知组件
- **Recharts 2.15.4** - 图表库
- **Embla Carousel 8.5.1** - 轮播组件
- **React Day Picker 9.8.0** - 日期选择器
- **Vaul 1.1.2** - 抽屉组件
- **React Resizable Panels 2.1.7** - 可调整面板

### 后端技术

- **Bun 1.1.38** - 高性能JavaScript运行时
- **Node.js >= 18.0.0** - 服务端JavaScript
- **Hono 4.6.3** - 轻量级Web框架
- **@hono/node-server 1.19.7** - Hono Node.js服务器适配器
- **Socket.io 4.8.0** - 实时通信
- **Socket.io Client 4.8.0** - Socket.io客户端
- **WS 8.18.0** - WebSocket库
- **PostgreSQL (pg 8.13.0)** - 关系型数据库
- **Redis (ioredis 5.4.1)** - 内存数据库
- **Redis (redis 4.7.0)** - Redis客户端
- **SQLite (sqlite3 5.1.7)** - 轻量级数据库
- **SQL.js 1.12.0** - 纯JavaScript SQLite实现
- **JWT (jsonwebtoken 9.0.2)** - JSON Web Token认证

### AI/ML技术

- **OpenAI API 4.67.1** - GPT模型集成
- **AI SDK 5.0.115** - Vercel AI SDK
- **@ai-sdk/openai 1.0.2** - OpenAI AI SDK
- **TensorFlow.js 4.22.0** - 机器学习库
- **@tensorflow-models/universal-sentence-encoder 1.3.3** - 通用句子编码器
- **RAG架构** - 检索增强生成

### 开发工具

- **ESLint 9.0.0** - 代码检查
- **Prettier 3.3.2** - 代码格式化
- **Biome 1.9.4** - 代码格式化和检查工具
- **TypeScript ESLint 8.0.0** - TypeScript代码检查
- **Testing Library** - React测试库
  - @testing-library/react 16.3.0
  - @testing-library/jest-dom 6.9.1
  - @testing-library/user-event 14.6.1
  - @testing-library/dom 10.4.1
- **Jest** - 测试框架
- **jsdom 27.3.0** - DOM模拟
- **PostCSS 8.5** - CSS处理
- **Autoprefixer 10.4.20** - CSS自动前缀

### 基础设施

- **Docker** - 容器化技术
- **Docker Compose** - 容器编排
- **Nginx** - 反向代理
- **Vercel Analytics** - 分析和监控
- **Vercel Speed Insights** - 性能监控

## 🚀 快速开始

### 环境要求

- **Bun** >= 1.0.0
- **Node.js** >= 18.0.0
- **Docker** >= 20.0.0
- **Docker Compose** >= 2.0.0

### 一键部署

```bash
# 克隆项目
git clone https://github.com/yyc3/xy-ai.git
cd yyc3-xy-ai

# 配置环境变量
cp .env.example .env.local
# 编辑 .env.local 填入必要的配置

# 一键部署
chmod +x deploy.sh
./deploy.sh deploy
```

### 开发环境启动

```bash
# 安装依赖
bun install

# 启动开发服务器（Next.js应用）
bun run dev:next

# 启动主服务（Bun服务）
bun run dev

# 启动特定服务
bun run orchestrator  # 服务编排
bun run gateway       # API网关
bun run agentic       # Agentic核心
```

### 访问地址

- **主应用**: <http://localhost:1228> (Next.js应用，项目专用端口)
- **API网关**: <http://localhost:1229> (项目专用端口)
- **Nginx代理**: <http://localhost>

## 📖 开发指南

### 项目结构

```
yyc3-xy-ai/
├── .github/            # GitHub Actions工作流配置
├── .trae/              # Trae IDE配置和规则
│   └── rules/          # 项目规则文档
├── __mocks__/          # 模拟数据
├── __tests__/          # 测试文件
├── analytics/          # 分析和监控模块
│   └── dashboard/      # 监控仪表板
├── app/                # Next.js应用目录
│   ├── (auth)/         # 认证相关页面
│   ├── (main)/         # 主应用页面
│   ├── api/            # API路由
│   ├── layout.tsx      # 根布局
│   └── page.tsx        # 首页
├── assets/             # 静态资源
├── backend/            # 后端服务
│   ├── services/       # 后端服务模块
│   └── package.json    # 后端依赖
├── components/         # React组件
│   ├── ai-widget/      # 智能AI组件
│   ├── ai-xiaoyu/      # 小语AI助手
│   ├── ui/             # UI基础组件
│   └── ...             # 其他业务组件
├── config/             # 配置文件
├── core/               # 核心引擎
│   ├── agents/         # AI代理
│   ├── knowledge/      # 知识库管理
│   ├── learning/       # 学习系统
│   ├── orchestrator/   # 服务编排
│   ├── prediction/     # 预测服务
│   └── tools/          # 工具管理
├── docs/               # 文档目录
│   ├── 00-文档索引.md  # 文档总索引
│   ├── 01-TECH_STACK.md # 技术栈文档
│   ├── 01-项目架构规范.md # 架构规范
│   ├── 02-API接口文档.md # API文档
│   ├── 03-组件开发规范.md # 组件规范
│   ├── 04-CODE_STYLE.md # 代码风格
│   ├── 05-项目架构总览.md # 架构总览
│   ├── YYC3-XY-设计类/ # 设计文档
│   ├── YYC3-XY-开发类/ # 开发文档
│   ├── YYC3-XY-管理类/ # 管理文档
│   └── ...             # 其他文档
├── hooks/              # React Hooks
├── lib/                # 工具库
├── public/             # 公共静态资源
├── scripts/            # 脚本文件
├── styles/             # 样式文件
├── types/              # TypeScript类型定义
├── utils/              # 工具函数
├── .env.docker         # Docker环境变量
├── .env.example        # 环境变量示例
├── .gitignore          # Git忽略文件
├── .prettierrc         # Prettier配置
├── .yarnrc.yml         # Yarn配置
├── Dockerfile          # Docker配置
├── deploy.sh           # 部署脚本
├── docker-compose.yml  # Docker Compose配置
├── next.config.ts      # Next.js配置
├── package.json        # 项目依赖
├── tsconfig.json       # TypeScript配置
└── README.md           # 项目说明
```

### 文档索引

项目文档按照以下结构组织：

#### 核心文档
- [文档索引](docs/00-文档索引.md) - 完整的文档索引和管理规范
- [技术栈文档](docs/01-TECH_STACK.md) - 项目技术栈详细说明
- [项目架构规范](docs/01-项目架构规范.md) - 系统架构设计规范
- [API接口文档](docs/02-API接口文档.md) - API接口详细说明
- [组件开发规范](docs/03-组件开发规范.md) - 组件开发指南
- [代码风格规范](docs/04-CODE_STYLE.md) - 代码风格和格式规范
- [项目架构总览](docs/05-项目架构总览.md) - 整体架构概览

#### 设计文档 (YYC3-XY-设计类/)
- 角色信息管理器技术文档
- AI智能浮窗系统设计
- AI智能插拔式核心机制
- 0-3成长守护白皮书
- 0-3阶段深度设计与开发方案

#### 开发文档 (YYC3-XY-开发类/)
- 开发指南和最佳实践
- 测试规范和流程
- 部署指南
- 故障排除指南

#### 管理文档 (YYC3-XY-管理类/)
- 项目管理规范
- 团队协作指南
- 版本发布流程
- 质量保证标准

#### AI闭环式文库
- AI智能浮窗系统
- AI智能移动可插拔
- AI浮窗可拖拽智呼系统
- AI浮窗系统设计
- Music音乐系统
- OPEN-API文档

详细文档请参考 [docs/00-文档索引.md](docs/00-文档索引.md)

### 开发工作流

1. **功能开发**

   ```bash
   # 创建功能分支
   git checkout -b feature/new-feature

   # 开发和测试
   bun run dev:next
   bun test
   ```

2. **代码质量**

   ```bash
   # 类型检查
   bun run type-check

   # 代码检查
   bun run lint

   # 代码格式化
   bun run format
   ```

3. **构建部署**

   ```bash
   # 构建Next.js应用
   bun run build:next

   # 构建主服务
   bun run build

   # 部署
   ./deploy.sh deploy
   ```

### 组件开发

#### 创建新的AI工具

```typescript
// core/tools/example-tool.ts
import { Tool, ToolResult } from '@/types/tools';

export class ExampleTool implements Tool {
  id = 'example-tool';
  name = '示例工具';
  description = '这是一个示例工具';
  version = '1.0.0';

  async execute(input: any): Promise<ToolResult> {
    // 工具执行逻辑
    return {
      success: true,
      data: '处理结果',
      metadata: {}
    };
  }

  async validate(input: any): Promise<boolean> {
    // 输入验证逻辑
    return true;
  }
}
```

#### 注册工具

```typescript
// core/tools/ToolManager.ts
import { ExampleTool } from './example-tool';

const toolManager = new ToolManager();
await toolManager.registerTool(new ExampleTool());
```

## 📦 部署指南

### 生产环境部署

1. **服务器要求**
   - CPU: 4核心以上
   - 内存: 8GB以上
   - 存储: 100GB以上
   - 网络: 100Mbps以上

2. **部署步骤**

   ```bash
   # 克隆代码
   git clone https://github.com/yyc3/xy-ai.git
   cd yyc3-xy-ai

   # 配置环境变量
   cp .env.example .env.local
   # 编辑配置文件

   # 部署服务
   ./deploy.sh deploy
   ```

3. **SSL配置**

   ```bash
   # 将SSL证书放置到配置目录
   mkdir -p config/nginx/ssl
   cp your-cert.pem config/nginx/ssl/cert.pem
   cp your-key.pem config/nginx/ssl/key.pem
   ```

### 监控配置

系统集成了完整的监控方案：

- **Vercel Analytics** - 应用分析和用户行为追踪
- **Vercel Speed Insights** - 性能监控和优化建议

访问监控面板：

- Vercel Analytics: 通过Vercel Dashboard访问
- Vercel Speed Insights: 通过Vercel Dashboard访问

## 📚 API文档

### 核心API端点

#### 健康检查

```http
GET /api/health
```

#### AI对话

```http
POST /api/ai/chat
Content-Type: application/json

{
  "message": "用户消息",
  "context": "对话上下文",
  "mode": "chat|voice|image"
}
```

#### 工具调用

```http
POST /api/tools/{toolId}/execute
Content-Type: application/json

{
  "input": "工具输入参数",
  "options": {}
}
```

#### 知识检索

```http
POST /api/knowledge/search
Content-Type: application/json

{
  "query": "搜索查询",
  "limit": 10,
  "threshold": 0.7
}
```

### WebSocket事件

#### 连接建立

```javascript
const socket = io('ws://localhost:1229');

// 监听AI回复
socket.on('ai-response', (data) => {
  console.log('AI回复:', data.message);
});

// 发送用户消息
socket.emit('user-message', {
  message: '用户输入',
  timestamp: Date.now()
});
```

## ⚙️ 配置说明

### 环境变量配置

主要配置项说明：

```bash
# 系统基础配置
NODE_ENV=development
PORT=1229

# AI服务配置
OPENAI_API_KEY=your-openai-api-key
ANTHROPIC_API_KEY=your-anthropic-api-key

# 数据库配置
DATABASE_URL=postgresql://user:pass@localhost:5432/yyc3_ai
REDIS_URL=redis://localhost:6379

# 向量数据库
VECTOR_DB_URL=http://localhost:6333
VECTOR_DIMENSION=1536
```

完整配置参考 `.env.example` 文件。

### 服务配置

各服务的详细配置：

- **API网关**: 负载均衡、限流、认证
- **数据库**: PostgreSQL连接池、Redis集群
- **监控**: Prometheus指标、Grafana仪表板
- **日志**: 结构化日志、集中收集

## 📊 监控与运维

### 关键指标

- **系统性能**: CPU、内存、磁盘、网络
- **应用指标**: 请求量、响应时间、错误率
- **业务指标**: AI调用次数、工具使用率
- **数据库**: 连接数、查询性能、缓存命中率

### 告警规则

系统预设了以下告警规则：

- 服务不可用
- 响应时间过长
- 错误率过高
- 资源使用率过高
- 数据库连接异常

### 日志管理

日志级别和输出配置：

```typescript
// 日志配置示例
const logger = winston.createLogger({
  level: process.env.LOG_LEVEL || 'info',
  format: winston.format.combine(
    winston.format.timestamp(),
    winston.format.json()
  ),
  transports: [
    new winston.transports.File({ filename: 'logs/error.log', level: 'error' }),
    new winston.transports.File({ filename: 'logs/combined.log' }),
    new winston.transports.Console()
  ]
});
```

## 🤝 贡献指南

我们欢迎所有形式的贡献！

### 贡献方式

1. **报告问题** - 提交Issue报告bug或提出建议
2. **功能开发** - Fork项目并提交Pull Request
3. **文档改进** - 完善文档和示例
4. **测试覆盖** - 增加单元测试和集成测试

### 开发流程

1. Fork项目到个人仓库
2. 创建功能分支: `git checkout -b feature/amazing-feature`
3. 提交更改: `git commit -m 'Add amazing feature'`
4. 推送分支: `git push origin feature/amazing-feature`
5. 提交Pull Request

### 代码规范

- 使用TypeScript进行类型安全开发
- 遵循ESLint和Prettier配置
- 编写单元测试覆盖新功能
- 添加适当的注释和文档

## 📄 许可证

本项目基于 [MIT许可证](LICENSE) 开源。

## 🙏 致谢

感谢以下开源项目的支持：

- [React](https://reactjs.org/) - 用户界面框架
- [Bun](https://bun.sh/) - 高性能JavaScript运行时
- [Docker](https://www.docker.com/) - 容器化技术
- [OpenAI](https://openai.com/) - AI模型服务
- [PostgreSQL](https://www.postgresql.org/) - 关系型数据库

## 📞 联系我们

- **项目主页**: <https://github.com/yyc3/yyc3-xy-ai>
- **问题反馈**: <https://github.com/yyc3/yyc3-xy-ai/issues>
- **邮箱**: <admin@0379.email>
- **官网**: <https://yyc3.ai>

---

<div align="center">

**⭐ 如果这个项目对您有帮助，请给我们一个Star！**

Made with ❤️ by YYC³ Team

</div>
