# Web 应用部署指南
**TODO**

本指南将帮助您将 AI 生成的 Web 应用部署到生产环境。

## 前置要求

- 完成的 Web 应用
- 版本控制设置
- 生产环境凭证
- 域名（可选）

## 部署选项

### 1. Vercel（推荐用于 Next.js）

```bash
# 安装 Vercel CLI
npm install -g vercel

# 登录 Vercel
vercel login

# 部署
vercel
```

### 2. Netlify

```bash
# 安装 Netlify CLI
npm install -g netlify-cli

# 登录 Netlify
netlify login

# 部署
netlify deploy
```

### 3. AWS Amplify

```bash
# 安装 AWS Amplify CLI
npm install -g @aws-amplify/cli

# 配置 AWS
amplify configure

# 初始化 Amplify
amplify init

# 部署
amplify push
```

## 部署流程

1. **构建准备**
   ```bash
   # 安装依赖
   npm install

   # 构建项目
   npm run build
   ```

2. **环境设置**
   - 创建 `.env.production`
   - 配置环境变量
   - 设置密钥

3. **数据库迁移**
   - 备份开发数据库
   - 运行迁移
   - 验证数据完整性

4. **SSL 配置**
   - 获取 SSL 证书
   - 配置 DNS 设置
   - 设置重定向

## 持续部署

### GitHub Actions

```yaml
name: Deploy
on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to Vercel
        uses: amondnet/vercel-action@v20
```

### GitLab CI

```yaml
deploy:
  stage: deploy
  script:
    - npm install
    - npm run build
    - npx vercel --prod
```

## 部署后检查

### 1. 验证
- 测试所有主要功能
- 检查性能指标
- 验证 SSL 证书
- 测试表单提交

### 2. 监控
- 设置错误跟踪
- 配置分析工具
- 监控性能
- 设置告警

### 3. 备份
- 数据库备份
- 代码备份
- 配置备份
- 记录恢复程序

## 常见问题

### 1. 构建失败
- 检查依赖
- 验证环境变量
- 查看构建日志
- 先在本地测试

### 2. 性能问题
- 启用缓存
- 优化图片
- 配置 CDN
- 检查打包大小

### 3. 安全问题
- 检查权限
- 检查 SSL 设置
- 审计依赖
- 测试安全头部

## 回滚程序

1. **快速回滚**
   ```bash
   # Vercel
   vercel rollback

   # Netlify
   netlify rollback

   # AWS Amplify
   amplify rollback
   ```

2. **手动回滚**
   - 恢复数据库备份
   - 部署前一个版本
   - 更新 DNS（如需要）
   - 验证功能

## 最佳实践

1. **零停机部署**
   - 使用预发布环境
   - 实施蓝绿部署
   - 配置健康检查

2. **安全性**
   - 启用 HTTPS
   - 配置 CSP 头部
   - 设置 WAF
   - 定期安全审计

3. **监控**
   - 设置日志
   - 配置监控
   - 启用告警
   - 定期备份

## 相关资源

- [移动应用发布](./deploy-mobile.md)
- [小程序发布](./deploy-miniprogram.md)
- [自定义模板](./custom-templates.md)
