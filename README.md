# 板栗CRM (Banli CRM)

酒店客控管理系统销售团队的客户全生命周期管理平台

## 环境要求

- Node.js 18+
- PostgreSQL 15
- 内存: 6G RAM recommended
- Platform: fnOS (Docker Compose)
- Protocol: HTTP (no SSL required)

## MVP 功能模块

### 第一阶段
1. 员工账户管理 - 添加、编辑、禁用/启用
2. 客户信息管理 - 录入、查重、标签
3. 客户跟进记录 - 录入、附件、提醒
4. 基础权限管理 - RBAC角色权限

### 第二阶段（后续迭代）
5. 商机阶段管理 - Pipeline可视化
6. 产品与报价 - 自定义产品库
7. 合同签约 - 在线编辑、分享签约
8. 数据统计看板

## 技术栈

### 后端
- Node.js 18 + Express
- PostgreSQL 15 Alpine
- Sequelize ORM
- JWT 认证

### 前端
- Vue 3 + Vite
- Element Plus
- Pinia + Vue Router

### 部署
- Docker Compose
- Ports: 8080 (frontend), 3321 (backend API)

## 快速开始

```bash
# 克隆项目
git clone https://github.com/quanmingxin/yixiugege.git

# 进入项目目录
cd yixiugege

# 配置环境变量
cp .env.example .env

# 启动服务
docker-compose up -d

# 访问系统
# 前端: http://localhost:8080
# 后端: http://localhost:3321/api
```

## 默认管理员账号

首次启动后，系统会自动创建默认管理员账号：
- 用户名: admin
- 密码: 见启动日志或配置文件

⚠️ **请在首次登录后立即修改密码！**

## 项目结构

```
banli-crm/
├── backend/          # 后端代码
│   ├── src/
│   ├── uploads/
│   └── Dockerfile
├── frontend/         # 前端代码
│   ├── src/
│   └── Dockerfile
├── docker-compose.yml
└── .env.example
```

## 开发进度

- [x] 项目初始化
- [ ] 数据库设计
- [ ] 员工管理模块
- [ ] 客户管理模块
- [ ] 跟进记录模块
- [ ] 权限系统
- [ ] Docker部署配置
- [ ] 功能测试

## License

MIT