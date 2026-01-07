# Functional Design

## Purpose
Detailed business logic design per unit.

Functional Design focuses on:
- Detailed business logic and algorithms for the unit
- Domain models with entities and relationships
- Detailed business rules, validation logic, and constraints
- Technology-agnostic design (no infrastructure concerns)

## Prerequisites
- Units Generation must be complete
- Unit of work artifacts must be available

## Steps to Execute

### Step 1: Analyze Unit Context
- Read unit definition from unit-of-work.md
- Read assigned stories from unit-of-work-story-map.md
- Understand unit responsibilities and boundaries

### Step 2: Create Functional Design Plan
Generate plan with checkboxes [] focusing on business logic, domain models, business rules.

### Step 3: Generate Context-Appropriate Questions
Use [Answer]: tag format. Categories to consider:
- Business Logic Modeling
- Domain Model
- Business Rules
- Data Flow
- Integration Points
- Error Handling
- Business Scenarios

### Step 4: Store Plan and Collect Answers
- Save as `{unit-name}-functional-design-plan.md`
- Analyze answers for ambiguities
- Create follow-up questions if needed

### Step 5: Generate Functional Design Artifacts
- `business-logic-model.md`
- `business-rules.md`
- `domain-entities.md`

### Step 6: Present Completion Message

```markdown
# 🔧 Functional Design Complete - [unit-name]

[AI-generated summary]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/construction/[unit-name]/functional-design/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Continue to Next Stage** - Proceed to next stage
```

### Step 7: Wait for Explicit Approval
