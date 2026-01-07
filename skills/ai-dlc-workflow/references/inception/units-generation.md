# Units Generation - Detailed Steps

## Overview
Decomposes the system into manageable units of work through two parts:
- **Part 1 - Planning**: Create decomposition plan with questions
- **Part 2 - Generation**: Execute approved plan to generate unit artifacts

**DEFINITION**: A unit of work is a logical grouping of stories for development purposes.

## Prerequisites
- Context Assessment must be complete
- Application Design phase REQUIRED

---

# PART 1: PLANNING

## Step 1: Create Unit of Work Plan
Generate plan with checkboxes [] for decomposing system into units.

## Step 2: Include Mandatory Unit Artifacts
- [ ] Generate unit-of-work.md with unit definitions
- [ ] Generate unit-of-work-dependency.md with dependency matrix
- [ ] Generate unit-of-work-story-map.md mapping stories to units

## Step 3: Generate Context-Appropriate Questions
Use [Answer]: tag format. Categories:
- Story Grouping
- Dependencies
- Team Alignment
- Technical Considerations
- Business Domain

## Step 4: Store Plan and Collect Answers
- Save as `unit-of-work-plan.md`
- Analyze answers for ambiguities
- Get explicit approval

---

# PART 2: GENERATION

## Step 5: Execute Unit of Work Plan
- Load plan and execute each step
- Mark checkboxes [x] as completed
- Generate all unit artifacts

## Step 6: Present Completion Message

```markdown
# 🔧 Units Generation Complete

[AI-generated summary of units]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/inception/application-design/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Approve & Continue** - Proceed to **CONSTRUCTION PHASE**
```

## Step 7: Wait for Explicit Approval

---

## Critical Rules

- **NO HARDCODED LOGIC**: Only execute what's in the plan
- **UPDATE CHECKBOXES**: Mark [x] immediately after completing each step
- **VERIFY COMPLETION**: Ensure all unit artifacts are complete
