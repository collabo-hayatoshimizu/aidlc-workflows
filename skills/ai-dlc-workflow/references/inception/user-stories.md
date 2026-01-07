# User Stories - Detailed Steps

## Purpose
Convert requirements into user-centered stories with acceptance criteria.

## Prerequisites
- Workspace Detection must be complete
- Requirements Analysis recommended

## Intelligent Assessment Guidelines

### High Priority Execution (ALWAYS Execute)
- New user-facing features
- User experience changes
- Multi-persona systems
- Customer-facing APIs
- Complex business logic
- Cross-team projects

### Skip Only For Simple Cases
- Pure refactoring with zero user impact
- Isolated bug fixes
- Infrastructure-only changes
- Developer tooling

---

# PART 1: PLANNING

## Step 1: Validate User Stories Need (MANDATORY)

Perform assessment and document in `user-stories-assessment.md`.

## Step 2: Create Story Plan

Generate comprehensive plan with checkboxes for story development.

## Step 3: Generate Context-Appropriate Questions

Use [Answer]: tag format. Categories to evaluate:
- User Personas
- Story Granularity
- Story Format
- Breakdown Approach
- Acceptance Criteria
- User Journeys
- Business Context

## Step 4: Include Mandatory Artifacts

- [ ] Generate stories.md with INVEST criteria
- [ ] Generate personas.md with user archetypes
- [ ] Include acceptance criteria for each story
- [ ] Map personas to relevant stories

## Step 5: Store Story Plan

Save as `aidlc-docs/inception/plans/story-generation-plan.md`

## Step 6: Collect and Analyze Answers

- Wait for ALL [Answer]: tags to be completed
- Analyze for ambiguities
- Create follow-up questions if needed

## Step 7: Wait for Explicit Approval of Plan

---

# PART 2: GENERATION

## Step 8: Execute Story Generation Plan

- Load plan and execute each step
- Mark checkboxes [x] as completed
- Generate stories.md and personas.md

## Step 9: Present Completion Message

```markdown
# 📚 User Stories Complete

[AI-generated summary of stories and personas]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/inception/user-stories/`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> ✅ **Approve & Continue** - Proceed to **Workflow Planning**
```

## Step 10: Wait for Explicit Approval

---

## Critical Rules

- **NO HARDCODED LOGIC**: Only execute what's in the plan
- **UPDATE CHECKBOXES**: Mark [x] immediately after completing each step
- **RESOLVE AMBIGUITIES**: Must resolve all vague answers before generation
