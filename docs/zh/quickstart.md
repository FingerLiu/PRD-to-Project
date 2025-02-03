# 快速入门指南

本指南将帮助您在 10 分钟内创建第一个完全由 AI 驱动的、可迭代、可协作的项目。无论您是要构建 Web 应用、移动应用还是微信小程序，按照以下步骤即可快速开始。

## 前置要求

### 1. 安装 AI 驱动的 IDE

目前支持：
- [Windsurf IDE](https://windsurf.app)（推荐）

即将支持：
- Cursor
- Devin
- Mars Code

### 2. 选择 PRD 模板

访问我们的 [GitHub 模板仓库](https://github.com/PRD-to-Project/templates)，选择符合以下条件的模板：
- 项目类型（Web/App/小程序）
- 技术栈
- 项目规模

每个模板包含：
1. **结构化的 PRD 文件**
   - 产品需求
   - 技术规格
   - 测试要求
   - [了解更多 PRD 结构](../concepts/prd-structure.md)

2. **Windsurfrules 配置**
   - 项目设置规则
   - 代码风格指南
   - AI 协作设置
   - [了解更多 Windsurfrules](../concepts/windsurfrules.md)

使用模板：
1. 在 GitHub 仓库中导航到你选择的模板
2. 点击"Use this template"按钮
3. 为新仓库命名
4. 选择可见性（公开/私有）
5. 点击"Create repository from template"

## 开始使用

### 1. 在 Windsurf 中打开项目

1. 打开 Windsurf IDE
2. 点击`文件 > 从 Git 新建项目`
3. 输入你的 GitHub 仓库 URL
4. 点击`克隆并打开`

### 2. 开始开发

#### 背景说明
我们在 `.windsurfrules` 中为不同技术栈指定了完整的开发指引，包括：
- 开发工具
- 依赖管理
- 测试框架
- 部署工具

大模型会像对应技术栈的专业工程师一样，为您的项目选择最合适的工具和实践。

#### 开发 1.0 版本

1. 编辑模板中的 `PRD.md` 文件：
   - 填写实际需求
   - 定义功能和规格
   - 设置项目约束

2. 启动 AI 协作：
   - 在 Windsurf 中输入"开始开发"
   - AI 将自动：
     - 分析您的 PRD
     - 规划开发任务
     - 生成代码
     - 搭建项目结构

3. 审查和完善：
   - 检查生成的代码
   - 提供反馈
   - 请求修改

### 3. 调试和测试

1. 预览应用：
   ```
   输入"预览"命令：
   - 启动开发服务器
   - 打开预览窗口
   - 启用热重载
   ```

2. 运行测试：
   ```
   输入"测试"命令：
   - 运行单元测试
   - 检查代码覆盖率
   - 执行集成测试
   ```

3. 性能测试：
   ```
   输入"性能测试"命令：
   - 检查加载时间
   - 分析性能指标
   - 获取优化建议
   ```

### 4. 部署上线

1. 准备部署：
   ```
   输入"部署"命令：
   - 构建生产版本
   - 运行部署前检查
   - 生成部署资源
   ```

2. 查看部署指南：
   - [Web 应用部署](../how-to/deploy-web.md)
   - [移动应用发布](../how-to/deploy-mobile.md)
   - [小程序发布](../how-to/deploy-miniprogram.md)

### 5. 迭代和更新

开发新的大版本时：

1. 创建新的 PRD 文件：
   ```
   PRD-2.0.md
   PRD-3.0.md
   等
   ```

2. AI 将自动：
   - 检测新的 PRD 文件
   - 规划版本更新
   - 保持向后兼容
   - 更新 CHANGELOG.md

3. 版本管理：
   - 每个大版本使用独立的 PRD
   - 在 CHANGELOG.md 中记录变更
   - 自动更新依赖
   - 文档版本化

## 下一步

- [创建自定义模板](../how-to/custom-templates.md)
- [高级 PRD 编写](../how-to/advanced-prd.md)
- [AI 协作最佳实践](../concepts/ai-collaboration.md)

## 常见问题

- [故障排除指南](../how-to/troubleshooting.md)
- [常见问题解答](../how-to/faq.md)

## 需要帮助？

- [加入 Discord 社区](https://discord.gg/prd-to-project)
- [GitHub Issues](https://github.com/FingerLiu/PRD-to-Project/issues)
- [查看文档](https://prd-to-project.github.io/docs)
