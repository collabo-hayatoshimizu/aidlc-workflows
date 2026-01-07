# Application Design - Detailed Steps

## Purpose
High-level component identification and service layer design.

Application Design focuses on:
- Identifying main functional components and their responsibilities
- Defining component interfaces (not detailed business logic)
- Designing service layer for orchestration
- Establishing component dependencies and communication patterns

**Note**: Detailed business logic design happens later in Functional Design (CONSTRUCTION phase)

## Prerequisites
- Context Assessment must be complete
- Requirements Assessment recommended
- Story Development recommended

## Step-by-Step Execution

### 1. Analyze Context
- Read requirements.md and stories.md
- Identify key business capabilities and functional areas

### 2. Create Application Design Plan
- Generate plan with checkboxes []
- Focus on components, responsibilities, methods, services

### 3. Include Mandatory Design Artifacts
- [ ] Generate components.md with component definitions
- [ ] Generate component-methods.md with method signatures
- [ ] Generate services.md with service definitions
- [ ] Generate component-dependency.md with relationships

### 4. Generate Context-Appropriate Questions
Use [Answer]: tag format. Categories:
- Component Identification
- Component Methods
- Service Layer Design
- Component Dependencies
- Design Patterns

### 5. Store and Execute Plan
- Save as `application-design-plan.md`
- Collect answers, analyze for ambiguities
- Generate design artifacts

### 6. Present Completion Message

```markdown
# 🏗️ Application Design Complete

[AI-generated summary of design artifacts]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/inception/application-design/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Approve & Continue** - Proceed to next stage
```

### 7. Wait for Explicit Approval
