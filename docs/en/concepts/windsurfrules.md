# Windsurfrules Configuration

Windsurfrules is a configuration system that guides AI in project development. It defines project structure, coding standards, and collaboration patterns.

## Core Concepts

### 1. Project Structure Rules

```yaml
DOCUMENTATION_RULES:
  markdown_files:
    - README.md: "Project documentation"
    - CONTRIBUTING.md: "Contribution guidelines"
  resource_directories:
    - docs/: "Documentation directory"
    - assets/: "Static assets"
```

### 2. Code Style Guidelines

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

### 3. AI Collaboration Settings

```yaml
AI_COLLABORATION:
  context_files:
    - .github/
    - docs/AI_GUIDELINES.md
  memory_files:
    - .memories/
    - .context/
  review_guidelines:
    - "Check for security best practices"
    - "Ensure code documentation"
```

## Configuration Sections

### 1. Security and Sensitive Information

```yaml
IGNORE_PATTERNS:
  - "**/.env*"
  - "**/secrets/*"
  - "**/credentials.json"
```

### 2. Version Control

```yaml
VERSION_CONTROL:
  changelog:
    format: "Keep a Changelog"
    files:
      - CHANGELOG.md
  release_notes:
    directory: "releases/"
```

### 3. Quality Assurance

```yaml
QUALITY_RULES:
  - "All Markdown files must have proper headers"
  - "Images must be optimized"
  - "Code examples must include comments"
```

## Best Practices

1. **Start Simple**
   - Begin with basic rules
   - Add complexity as needed
   - Focus on essential patterns

2. **Maintain Consistency**
   - Use consistent naming
   - Follow established patterns
   - Document exceptions

3. **Regular Updates**
   - Review rules periodically
   - Update based on feedback
   - Keep documentation current

## Template Examples

1. [Basic Web Project](../templates/basic-web-rules.md)
2. [Full Stack Application](../templates/fullstack-rules.md)
3. [Mobile Development](../templates/mobile-rules.md)

## Common Configurations

### For Web Projects

```yaml
NEXTJS_PROJECT:
  directory: "website/"
  structure:
    - app/: "App Router directory"
    - components/: "Reusable components"
    - lib/: "Utility functions"
```

### For Mobile Projects

```yaml
MOBILE_PROJECT:
  directory: "mobile/"
  structure:
    - src/: "Source code"
    - assets/: "Resources"
    - tests/: "Test files"
```

## Related Concepts

- [PRD Structure](./prd-structure.md)
- [AI Collaboration](./ai-collaboration.md)
- [Custom Templates](../how-to/custom-templates.md)
