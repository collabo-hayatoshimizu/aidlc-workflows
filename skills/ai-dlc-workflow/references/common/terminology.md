# AI-DLC Terminology Glossary

## Core Terminology

### Phase vs Stage

**Phase**: One of the three high-level lifecycle phases in AI-DLC
- 🔵 **INCEPTION PHASE** - Planning & Architecture (WHAT and WHY)
- 🟢 **CONSTRUCTION PHASE** - Design, Implementation & Test (HOW)
- 🟡 **OPERATIONS PHASE** - Deployment & Monitoring (future expansion)

**Stage**: An individual workflow activity within a phase
- Examples: Context Assessment stage, Requirements Assessment stage, Code Planning stage
- Each stage has specific prerequisites, steps, and outputs
- Stages can be ALWAYS-EXECUTE or CONDITIONAL

## Three-Phase Lifecycle

### INCEPTION PHASE
**Purpose**: Planning and architectural decisions  
**Focus**: Determine WHAT to build and WHY

**Stages**:
- Workspace Detection (ALWAYS)
- Reverse Engineering (CONDITIONAL - Brownfield only)
- Requirements Analysis (ALWAYS - Adaptive depth)
- User Stories (CONDITIONAL)
- Workflow Planning (ALWAYS)
- Application Design (CONDITIONAL)
- Units Generation (CONDITIONAL)

### CONSTRUCTION PHASE
**Purpose**: Detailed design and implementation  
**Focus**: Determine HOW to build it

**Stages**:
- Functional Design (CONDITIONAL, per-unit)
- NFR Requirements (CONDITIONAL, per-unit)
- NFR Design (CONDITIONAL, per-unit)
- Infrastructure Design (CONDITIONAL, per-unit)
- Code Planning (ALWAYS)
- Code Generation (ALWAYS)
- Build and Test (ALWAYS)

### OPERATIONS PHASE
**Purpose**: Deployment and operational readiness  
**Focus**: How to DEPLOY and RUN it

**Stages**:
- Operations (PLACEHOLDER)

## Architecture Terms

### Unit of Work
A logical grouping of user stories for development purposes.

### Service
An independently deployable component in a microservices architecture.

### Module
A logical grouping of functionality within a single service or monolith.

### Component
A reusable building block within a service or module.

## Stage Terminology

### Planning vs Generation
- **Planning**: Creating a plan with questions and checkboxes for execution
- **Generation**: Executing the plan to create artifacts

### Depth Levels
- **Minimal**: Quick, focused execution for simple changes
- **Standard**: Normal depth with standard artifacts for typical projects
- **Comprehensive**: Full depth with all artifacts for complex/high-risk projects

## Artifact Types

### Plans
Documents with checkboxes and questions that guide execution.
- Located in `aidlc-docs/plans/`

### Artifacts
Generated outputs from executing plans.
- Located in various `aidlc-docs/` subdirectories

### State Files
Files tracking workflow progress and status.
- `aidlc-state.md`: Overall workflow state
- `audit.md`: Complete audit trail of all interactions

## Common Abbreviations

- **AI-DLC**: AI-Driven Development Life Cycle
- **NFR**: Non-Functional Requirements
- **UOW**: Unit of Work
- **API**: Application Programming Interface
