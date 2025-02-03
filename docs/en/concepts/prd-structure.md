# PRD Structure

A well-structured PRD (Product Requirements Document) is crucial for AI-driven development. This guide explains the key components of a PRD in our system.

## Core Components

### 1. Project Overview
```yaml
project:
  name: "My Project"
  type: "web|app|miniprogram"
  description: "A brief description of your project"
  version: "1.0.0"
```

### 2. Product Requirements

```yaml
product_requirements:
  user_stories:
    - as: "user type"
      i_want: "desired action"
      so_that: "expected outcome"
  
  features:
    - name: "Feature Name"
      priority: "high|medium|low"
      description: "Detailed feature description"
      acceptance_criteria:
        - "Criterion 1"
        - "Criterion 2"
```

### 3. Technical Requirements

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

### 4. Testing Requirements

```yaml
testing_requirements:
  unit_testing:
    coverage: "80%"
    framework: "jest"
  
  integration_testing:
    strategy: "end-to-end"
    tools: ["cypress"]
```

## Best Practices

1. **Be Specific**
   - Use precise requirements
   - Include measurable criteria
   - Define clear boundaries

2. **Stay Technology-Agnostic**
   - Focus on what needs to be done
   - Let AI suggest optimal technical solutions
   - Keep requirements flexible

3. **Include Examples**
   - Provide user flow examples
   - Include mockups or wireframes
   - Reference similar implementations

## Template Examples

We provide several PRD templates for different project types:

1. [Web Application Template](../templates/web-app-prd.md)
2. [Mobile App Template](../templates/mobile-app-prd.md)
3. [Mini Program Template](../templates/mini-program-prd.md)

## Common Pitfalls

1. **Over-specification**
   - Don't lock into specific implementations
   - Allow AI room for optimization

2. **Under-specification**
   - Don't be too vague
   - Include necessary business logic

3. **Inconsistent Requirements**
   - Ensure requirements don't conflict
   - Maintain consistent terminology

## Related Concepts

- [Windsurfrules Configuration](./windsurfrules.md)
- [AI Collaboration](./ai-collaboration.md)
- [Custom Templates](../how-to/custom-templates.md)
