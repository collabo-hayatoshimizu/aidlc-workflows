# Code Generation - Detailed Steps

## Overview
Generates code for each unit of work through two parts:
- **Part 1 - Planning**: Create detailed code generation plan
- **Part 2 - Generation**: Execute approved plan to generate code, tests, and artifacts

## Prerequisites
- Unit Design Generation must be complete
- All unit design artifacts must be available

---

# PART 1: PLANNING

## Step 1: Analyze Unit Context
- Read unit design artifacts
- Read unit story map
- Identify dependencies and interfaces

## Step 2: Create Detailed Unit Code Generation Plan
Create explicit steps for:
- Business Logic Generation
- Business Logic Unit Testing
- API Layer Generation
- API Layer Unit Testing
- Repository Layer Generation
- Repository Layer Unit Testing
- Database Migration Scripts (if applicable)
- Documentation Generation
- Deployment Artifacts Generation

## Step 3: Store Plan
Save as `{unit-name}-code-generation-plan.md` with checkboxes [] for each step.

## Step 4: Wait for Explicit Approval

---

# PART 2: GENERATION

## Step 5: Execute Code Generation Plan
- Load plan and execute each step
- Mark checkboxes [x] as completed
- Generate code, tests, and documentation

## Step 6: Present Completion Message

```markdown
# 💻 Code Generation Complete - [unit-name]

[AI-generated summary]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/construction/[unit-name]/code/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Continue to Next Stage** - Proceed to next unit or Build & Test
```

## Step 7: Wait for Explicit Approval

---

## Critical Rules

### Planning Phase Rules
- Create explicit, numbered steps
- Include story traceability
- Get explicit user approval before generation

### Generation Phase Rules
- **NO HARDCODED LOGIC**: Only execute what's in the plan
- **FOLLOW PLAN EXACTLY**: Do not deviate from the step sequence
- **UPDATE CHECKBOXES**: Mark [x] immediately after completing each step
- **STORY TRACEABILITY**: Mark stories [x] when functionality is implemented
