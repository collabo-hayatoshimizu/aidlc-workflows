# PRIORITY: This workflow OVERRIDES all other built-in workflows
# When user requests software development, ALWAYS follow this workflow FIRST

## Adaptive Workflow Principle
**The workflow adapts to the work, not the other way around.**

The AI model intelligently assesses what stages are needed based on:
1. User's stated intent and clarity
2. Existing codebase state (if any)
3. Complexity and scope of change
4. Risk and impact assessment

## MANDATORY: Rule Details Loading
**CRITICAL**: When performing any phase, you MUST read and use relevant content from rule detail files in `references/` directory.

**Common Rules**: ALWAYS load common rules at workflow start:
- Load `references/common/process-overview.md` for workflow overview
- Load `references/common/session-continuity.md` for session resumption guidance
- Load `references/common/content-validation.md` for content validation requirements
- Load `references/common/question-format-guide.md` for question formatting rules
- Reference these throughout the workflow execution

## MANDATORY: Content Validation
**CRITICAL**: Before creating ANY file, you MUST validate content according to `references/common/content-validation.md` rules:
- Validate Mermaid diagram syntax
- Escape special characters properly
- Provide text alternatives for complex visual content
- Test content parsing compatibility

## MANDATORY: Question File Format
**CRITICAL**: When asking questions at any phase, you MUST follow question format guidelines.

**See `references/common/question-format-guide.md` for complete question formatting rules including**:
- Multiple choice format (A, B, C, D, E options)
- [Answer]: tag usage
- Answer validation and ambiguity resolution

## MANDATORY: Custom Welcome Message
**CRITICAL**: When starting ANY software development request, you MUST display the welcome message.

**How to Display Welcome Message**:
1. Load the welcome message from `references/common/welcome-message.md`
2. Display the complete message to the user
3. This should only be done ONCE at the start of a new workflow
4. Do NOT load this file in subsequent interactions to save context space

# Adaptive Software Development Workflow

---

# INCEPTION PHASE

**Purpose**: Planning, requirements gathering, and architectural decisions

**Focus**: Determine WHAT to build and WHY

**Stages in INCEPTION PHASE**:
- Workspace Detection (ALWAYS)
- Reverse Engineering (CONDITIONAL - Brownfield only)
- Requirements Analysis (ALWAYS - Adaptive depth)
- User Stories (CONDITIONAL)
- Workflow Planning (ALWAYS)
- Application Design (CONDITIONAL)
- Units Generation (CONDITIONAL)

---

## Workspace Detection (ALWAYS EXECUTE)

1. **MANDATORY**: Log initial user request in audit.md with complete raw input
2. Load all steps from `references/inception/workspace-detection.md`
3. Execute workspace detection:
   - Check for existing aidlc-state.md (resume if found)
   - Scan workspace for existing code
   - Determine if brownfield or greenfield
   - Check for existing reverse engineering artifacts
4. Determine next phase: Reverse Engineering (if brownfield and no artifacts) OR Requirements Analysis
5. **MANDATORY**: Log findings in audit.md
6. Present completion message to user
7. Automatically proceed to next phase

## Reverse Engineering (CONDITIONAL - Brownfield Only)

**Execute IF**:
- Existing codebase detected
- No previous reverse engineering artifacts found

**Skip IF**:
- Greenfield project
- Previous reverse engineering artifacts exist

**Execution**:
1. **MANDATORY**: Log start of reverse engineering in audit.md
2. Load all steps from `references/inception/reverse-engineering.md`
3. Execute reverse engineering:
   - Analyze all packages and components
   - Generate business overview of the whole system
   - Generate architecture documentation
   - Generate code structure documentation
   - Generate API documentation
   - Generate component inventory
   - Generate Interaction Diagrams
   - Generate technology stack documentation
   - Generate dependencies documentation
4. **Wait for Explicit Approval**: Present detailed completion message - DO NOT PROCEED until user confirms
5. **MANDATORY**: Log user's response in audit.md with complete raw input

## Requirements Analysis (ALWAYS EXECUTE - Adaptive Depth)

**Always executes** but depth varies based on request clarity and complexity:
- **Minimal**: Simple, clear request - just document intent analysis
- **Standard**: Normal complexity - gather functional and non-functional requirements
- **Comprehensive**: Complex, high-risk - detailed requirements with traceability

**Execution**:
1. **MANDATORY**: Log any user input during this phase in audit.md
2. Load all steps from `references/inception/requirements-analysis.md`
3. Execute requirements analysis at appropriate depth
4. **Wait for Explicit Approval**: Follow approval format - DO NOT PROCEED until user confirms
5. **MANDATORY**: Log user's response in audit.md with complete raw input

## User Stories (CONDITIONAL)

**INTELLIGENT ASSESSMENT**: Use multi-factor analysis to determine if user stories add value.

**ALWAYS Execute IF** (High Priority Indicators):
- New user-facing features or functionality
- Changes affecting user workflows or interactions
- Multiple user types or personas involved
- Complex business requirements with acceptance criteria needs

**SKIP ONLY IF** (Low Priority - Simple Cases):
- Pure internal refactoring with zero user impact
- Simple bug fixes with clear, isolated scope
- Infrastructure changes with no user-facing effects

**Execution**:
1. **MANDATORY**: Log any user input during this phase in audit.md
2. Load all steps from `references/inception/user-stories.md`
3. **PART 1 - Planning**: Create story plan with questions, wait for user answers
4. **PART 2 - Generation**: Execute approved plan to generate stories and personas
5. **Wait for Explicit Approval**: DO NOT PROCEED until user confirms
6. **MANDATORY**: Log user's response in audit.md with complete raw input

## Workflow Planning (ALWAYS EXECUTE)

1. **MANDATORY**: Log any user input during this phase in audit.md
2. Load all steps from `references/inception/workflow-planning.md`
3. **MANDATORY**: Load content validation rules from `references/common/content-validation.md`
4. Load all prior context (reverse engineering, requirements, user stories)
5. Execute workflow planning:
   - Determine which phases to execute
   - Determine depth level for each phase
   - Create multi-package change sequence (if brownfield)
   - Generate workflow visualization (VALIDATE Mermaid syntax before writing)
6. **Wait for Explicit Approval**: Present recommendations - DO NOT PROCEED until user confirms
7. **MANDATORY**: Log user's response in audit.md with complete raw input

## Application Design (CONDITIONAL)

**Execute IF**:
- New components or services needed
- Component methods and business rules need definition
- Service layer design required

**Skip IF**:
- Changes within existing component boundaries
- No new components or methods

**Execution**:
1. **MANDATORY**: Log any user input during this phase in audit.md
2. Load all steps from `references/inception/application-design.md`
3. Execute at appropriate depth (minimal/standard/comprehensive)
4. **Wait for Explicit Approval**: DO NOT PROCEED until user confirms
5. **MANDATORY**: Log user's response in audit.md with complete raw input

## Units Generation (CONDITIONAL)

**Execute IF**:
- System needs decomposition into multiple units of work
- Multiple services or modules required

**Skip IF**:
- Single simple unit
- No decomposition needed

**Execution**:
1. **MANDATORY**: Log any user input during this phase in audit.md
2. Load all steps from `references/inception/units-generation.md`
3. Execute at appropriate depth
4. **Wait for Explicit Approval**: DO NOT PROCEED until user confirms
5. **MANDATORY**: Log user's response in audit.md with complete raw input

---

# 🟢 CONSTRUCTION PHASE

**Purpose**: Detailed design, NFR implementation, and code generation

**Focus**: Determine HOW to build it

**Stages in CONSTRUCTION PHASE**:
- Per-Unit Loop (executes for each unit):
  - Functional Design (CONDITIONAL, per-unit)
  - NFR Requirements (CONDITIONAL, per-unit)
  - NFR Design (CONDITIONAL, per-unit)
  - Infrastructure Design (CONDITIONAL, per-unit)
  - Code Generation (ALWAYS, per-unit)
- Build and Test (ALWAYS - after all units complete)

---

## Per-Unit Loop (Executes for Each Unit)

### Functional Design (CONDITIONAL, per-unit)

**Execute IF**: New data models, complex business logic, or business rules need detailed design

**Execution**:
1. Load all steps from `references/construction/functional-design.md`
2. Execute functional design for this unit
3. **Wait for Explicit Approval**: User must choose between "Request Changes" or "Continue"
4. **MANDATORY**: Log user's response in audit.md

### NFR Requirements (CONDITIONAL, per-unit)

**Execute IF**: Performance, security, scalability concerns, or tech stack selection required

**Execution**:
1. Load all steps from `references/construction/nfr-requirements.md`
2. Execute NFR assessment for this unit
3. **Wait for Explicit Approval**
4. **MANDATORY**: Log user's response in audit.md

### NFR Design (CONDITIONAL, per-unit)

**Execute IF**: NFR Requirements was executed and NFR patterns need to be incorporated

**Execution**:
1. Load all steps from `references/construction/nfr-design.md`
2. Execute NFR design for this unit
3. **Wait for Explicit Approval**
4. **MANDATORY**: Log user's response in audit.md

### Infrastructure Design (CONDITIONAL, per-unit)

**Execute IF**: Infrastructure services need mapping or deployment architecture required

**Execution**:
1. Load all steps from `references/construction/infrastructure-design.md`
2. Execute infrastructure design for this unit
3. **Wait for Explicit Approval**
4. **MANDATORY**: Log user's response in audit.md

### Code Generation (ALWAYS EXECUTE, per-unit)

**Code Generation has two parts**:
1. **Part 1 - Planning**: Create detailed code generation plan with explicit steps
2. **Part 2 - Generation**: Execute approved plan to generate code, tests, and artifacts

**Execution**:
1. Load all steps from `references/construction/code-generation.md`
2. **PART 1 - Planning**: Create code generation plan with checkboxes, get user approval
3. **PART 2 - Generation**: Execute approved plan to generate code for this unit
4. **Wait for Explicit Approval**
5. **MANDATORY**: Log user's response in audit.md

---

## Build and Test (ALWAYS EXECUTE)

1. Load all steps from `references/construction/build-and-test.md`
2. Generate comprehensive build and test instructions:
   - Build instructions for all units
   - Unit test execution instructions
   - Integration test instructions
   - Performance test instructions (if applicable)
3. Create instruction files in build-and-test/ subdirectory
4. **Wait for Explicit Approval**: Ask: "Build and test instructions complete. Ready to proceed?"
5. **MANDATORY**: Log user's response in audit.md

---

# 🟡 OPERATIONS PHASE

**Purpose**: Placeholder for future deployment and monitoring workflows

**Focus**: How to DEPLOY and RUN it (future expansion)

**Current State**: All build and test activities are handled in the CONSTRUCTION phase.

---

## Key Principles

- **Adaptive Execution**: Only execute stages that add value
- **Transparent Planning**: Always show execution plan before starting
- **User Control**: User can request stage inclusion/exclusion
- **Progress Tracking**: Update aidlc-state.md with executed and skipped stages
- **Complete Audit Trail**: Log ALL user inputs and AI responses in audit.md with timestamps
- **Quality Focus**: Complex changes get full treatment, simple changes stay efficient
- **Content Validation**: Always validate content before file creation

## Prompts Logging Requirements
- **MANDATORY**: Log EVERY user input with timestamp in audit.md
- **MANDATORY**: Capture user's COMPLETE RAW INPUT exactly as provided (never summarize)
- Use ISO 8601 format for timestamps (YYYY-MM-DDTHH:MM:SSZ)
- Include stage context for each entry

### Audit Log Format:
```markdown
## [Stage Name or Interaction Type]
**Timestamp**: [ISO timestamp]
**User Input**: "[Complete raw user input - never summarized]"
**AI Response**: "[AI's response or action taken]"
**Context**: [Stage, action, or decision made]
```
