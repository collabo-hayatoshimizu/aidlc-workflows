# Requirements Analysis (Adaptive)

**Assume the role** of a product owner

**Adaptive Phase**: Always executes. Detail level adapts to problem complexity.

## Prerequisites
- Workspace Detection must be complete
- Reverse Engineering must be complete (if brownfield)

## Execution Steps

### Step 1: Load Reverse Engineering Context (if available)

**IF brownfield project**: Load architecture, component-inventory, technology-stack artifacts.

### Step 2: Analyze User Request (Intent Analysis)

- **Request Clarity**: Clear, Vague, or Incomplete
- **Request Type**: New Feature, Bug Fix, Refactoring, Migration, etc.
- **Initial Scope**: Single File, Single Component, Multiple Components, System-wide
- **Initial Complexity**: Trivial, Simple, Moderate, Complex

### Step 3: Determine Requirements Depth

- **Minimal**: Clear and simple request
- **Standard**: Needs clarification, normal complexity
- **Comprehensive**: Complex project, high risk

### Step 4: Assess Current Requirements

Analyze whatever the user has provided and convert to markdown format.

### Step 5: Thorough Completeness Analysis

**MANDATORY**: Evaluate ALL of these areas:
- Functional Requirements
- Non-Functional Requirements
- User Scenarios
- Business Context
- Technical Context
- Quality Attributes

### Step 6: Generate Clarifying Questions

- **ALWAYS** create `requirement-verification-questions.md` unless exceptionally clear
- Use [Answer]: tag format
- Include "Other" option for custom responses
- Analyze ALL answers for ambiguities
- Create follow-up questions if needed

### Step 7: Generate Requirements Document

Create `aidlc-docs/inception/requirements/requirements.md` with:
- Intent analysis summary
- Functional and non-functional requirements
- User's answers incorporated

### Step 8: Present Completion Message

```markdown
# 🔍 Requirements Analysis Complete

[AI-generated summary of requirements]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/inception/requirements/requirements.md`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> 📝 **Add User Stories** - Include User Stories stage (if skipped)
> ✅ **Approve & Continue** - Proceed to next stage
```

### Step 9: Wait for Explicit Approval

- Do not proceed until user explicitly approves
- Log approval in audit.md
