# Infrastructure Design

## Prerequisites
- Functional Design must be complete for the unit
- NFR Design recommended (provides logical components to map)

## Overview
Map logical software components to actual infrastructure choices for deployment environments.

## Steps to Execute

### Step 1: Analyze Design Artifacts
- Read functional design artifacts
- Read NFR design artifacts (if exists)
- Identify logical components needing infrastructure

### Step 2: Create Infrastructure Design Plan
Generate plan with checkboxes [] focusing on mapping to actual services (AWS, Azure, GCP, on-premise).

### Step 3: Generate Context-Appropriate Questions
Use [Answer]: tag format. Categories:
- Deployment Environment
- Compute Infrastructure
- Storage Infrastructure
- Messaging Infrastructure
- Networking Infrastructure
- Monitoring Infrastructure
- Shared Infrastructure

### Step 4: Store Plan and Collect Answers
- Save as `{unit-name}-infrastructure-design-plan.md`
- Analyze answers for ambiguities

### Step 5: Generate Infrastructure Design Artifacts
- `infrastructure-design.md`
- `deployment-architecture.md`
- `shared-infrastructure.md` (if applicable)

### Step 6: Present Completion Message

```markdown
# 🏢 Infrastructure Design Complete - [unit-name]

[AI-generated summary]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/construction/[unit-name]/infrastructure-design/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Continue to Next Stage** - Proceed to **Code Generation**
```

### Step 7: Wait for Explicit Approval
