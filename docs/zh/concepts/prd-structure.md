# PRD 结构说明

在 AI 驱动的开发中，一个结构良好的 PRD（产品需求文档）至关重要。本指南将解释我们系统中 PRD 的关键组成部分。

## 核心组件

### 1. 项目概述
```yaml
project:
  name: "我的项目"
  type: "web|app|miniprogram"
  description: "项目简要描述"
  version: "1.0.0"
```

### 2. 产品需求

```yaml
product_requirements:
  user_stories:
    - as: "用户类型"
      i_want: "期望操作"
      so_that: "预期结果"
  
  features:
    - name: "功能名称"
      priority: "high|medium|low"
      description: "详细功能描述"
      acceptance_criteria:
        - "验收标准1"
        - "验收标准2"
```

### 3. 技术需求

```yaml
technical_requirements:
  architecture:
    type: "monolithic|microservices|serverless"
    stack:
      frontend: ["react", "tailwind"]
      backend: ["node", "express"]
      database: ["postgresql"]
  
  constraints:
    performance:
      load_time: "< 3s"
      concurrent_users: 1000
    security:
      authentication: "required"
      data_encryption: "required"
```

### 4. 测试需求

```yaml
testing_requirements:
  unit_testing:
    coverage: "80%"
    framework: "jest"
  
  integration_testing:
    strategy: "end-to-end"
    tools: ["cypress"]
```

## 最佳实践

1. **保持具体**
   - 使用精确的需求描述
   - 包含可衡量的标准
   - 定义清晰的边界

2. **保持技术中立**
   - 关注需要完成的目标
   - 让 AI 推荐最优技术方案
   - 保持需求的灵活性

3. **包含示例**
   - 提供用户流程示例
   - 包含原型或线框图
   - 引用类似实现

## 模板示例

我们为不同类型的项目提供了多个 PRD 模板：

1. [Web 应用模板](../templates/web-app-prd.md)
2. [移动应用模板](../templates/mobile-app-prd.md)
3. [小程序模板](../templates/mini-program-prd.md)

## 常见陷阱

1. **过度规范**
   - 不要锁定具体实现
   - 给 AI 优化的空间

2. **规范不足**
   - 避免过于模糊
   - 包含必要的业务逻辑

3. **需求不一致**
   - 确保需求之间不冲突
   - 保持术语的一致性

## 相关概念

- [Windsurfrules 配置](./windsurfrules.md)
- [AI 协作](./ai-collaboration.md)
- [自定义模板](../how-to/custom-templates.md)
