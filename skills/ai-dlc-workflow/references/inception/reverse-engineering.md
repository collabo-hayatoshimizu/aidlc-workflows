# Reverse Engineering

**Purpose**: Analyze existing codebase and generate comprehensive design artifacts

**Execute when**: Brownfield project detected (existing code found in workspace)

**Skip when**: Greenfield project (no existing code)

## Step 1: Multi-Package Discovery

### 1.1 Scan Workspace
- All packages (not just mentioned ones)
- Package relationships via config files
- Package types: Application, CDK/Infrastructure, Models, Clients, Tests

### 1.2 Understand the Business Context
- The core business that the system is implementing overall
- The business overview of every package
- List of Business Transactions implemented in the system

### 1.3 Infrastructure Discovery
- CDK packages, Terraform, CloudFormation
- Deployment scripts

### 1.4 Build System Discovery
- Build systems: Maven, Gradle, npm
- Build dependencies between packages

### 1.5 Service Architecture Discovery
- Lambda functions, Container services
- API definitions, Data stores

## Step 2: Generate Documentation

Create these artifacts in `aidlc-docs/inception/reverse-engineering/`:

- **business-overview.md**: Business context, transactions, dictionary
- **architecture.md**: System overview, component descriptions, data flow
- **code-structure.md**: Build system, key classes, design patterns
- **api-documentation.md**: REST APIs, internal APIs, data models
- **component-inventory.md**: Application, infrastructure, shared, test packages
- **technology-stack.md**: Languages, frameworks, infrastructure, tools
- **dependencies.md**: Internal and external dependencies
- **code-quality-assessment.md**: Test coverage, code quality indicators

## Step 3: Present Completion Message

```markdown
# 🔍 Reverse Engineering Complete

[AI-generated summary of key findings]

> **📋 REVIEW REQUIRED:**  
> Please examine the artifacts at: `aidlc-docs/inception/reverse-engineering/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications if required
> ✅ **Approve & Continue** - Proceed to **Requirements Analysis**
```

## Step 4: Wait for User Approval

- **MANDATORY**: Do not proceed until user explicitly approves
- **MANDATORY**: Log user's response in audit.md
