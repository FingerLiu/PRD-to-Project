# Windsurfrules 配置说明

Windsurfrules 是一个指导 AI 进行项目开发的配置系统。它定义了项目结构、编码标准和协作模式。

## 核心概念

### 1. 项目结构规则

```yaml
DOCUMENTATION_RULES:
  markdown_files:
    - README.md: "项目文档"
    - CONTRIBUTING.md: "贡献指南"
  resource_directories:
    - docs/: "文档目录"
    - assets/: "静态资源"
```

### 2. 代码风格指南

```yaml
CODE_STYLE:
  language_specific:
    javascript:
      format: "prettier"
      rules:
        semi: true
        singleQuote: true
    python:
      format: "black"
      line_length: 88
```

### 3. AI 协作设置

```yaml
AI_COLLABORATION:
  context_files:
    - .github/
    - docs/AI_GUIDELINES.md
  memory_files:
    - .memories/
    - .context/
  review_guidelines:
    - "检查安全最佳实践"
    - "确保代码文档完整"
```

## 配置部分

### 1. 安全和敏感信息

```yaml
IGNORE_PATTERNS:
  - "**/.env*"
  - "**/secrets/*"
  - "**/credentials.json"
```

### 2. 版本控制

```yaml
VERSION_CONTROL:
  changelog:
    format: "Keep a Changelog"
    files:
      - CHANGELOG.md
  release_notes:
    directory: "releases/"
```

### 3. 质量保证

```yaml
QUALITY_RULES:
  - "所有 Markdown 文件必须有适当的标题"
  - "图片必须经过优化"
  - "代码示例必须包含注释"
```

## 最佳实践

1. **从简单开始**
   - 从基本规则开始
   - 根据需要增加复杂度
   - 专注于基本模式

2. **保持一致性**
   - 使用一致的命名
   - 遵循既定模式
   - 记录例外情况

3. **定期更新**
   - 定期审查规则
   - 根据反馈更新
   - 保持文档最新

## 模板示例

1. [基础 Web 项目](../templates/basic-web-rules.md)
2. [全栈应用](../templates/fullstack-rules.md)
3. [移动端开发](../templates/mobile-rules.md)

## 常用配置

### Web 项目配置

```yaml
NEXTJS_PROJECT:
  directory: "website/"
  structure:
    - app/: "App Router 目录"
    - components/: "可复用组件"
    - lib/: "工具函数"
```

### 移动端项目配置

```yaml
MOBILE_PROJECT:
  directory: "mobile/"
  structure:
    - src/: "源代码"
    - assets/: "资源文件"
    - tests/: "测试文件"
```

## 相关概念

- [PRD 结构](./prd-structure.md)
- [AI 协作](./ai-collaboration.md)
- [自定义模板](../how-to/custom-templates.md)
