# Workflow Planning

**Purpose**: Determine which phases to execute and create comprehensive execution plan

**Always Execute**: This phase always runs after understanding requirements and scope

## Step 1: Load All Prior Context

- Reverse Engineering artifacts (if brownfield)
- Requirements Analysis artifacts
- User Stories (if executed)

## Step 2: Detailed Scope and Impact Analysis

### Change Impact Assessment
1. **User-facing changes**: Does this affect user experience?
2. **Structural changes**: Does this change system architecture?
3. **Data model changes**: Does this affect database schemas?
4. **API changes**: Does this affect interfaces or contracts?
5. **NFR impact**: Does this affect performance, security, or scalability?

### Risk Assessment
- **Low**: Isolated change, easy rollback
- **Medium**: Multiple components, moderate rollback
- **High**: System-wide impact, complex rollback
- **Critical**: Production-critical, difficult rollback

## Step 3: Phase Determination

### Application Design - Execute IF:
- New components or services needed
- Component methods and business rules need definition
- Service layer design required

### Units Generation - Execute IF:
- System needs decomposition into multiple units
- Multiple services or modules required

### NFR Implementation - Execute IF:
- Performance, security, scalability requirements
- Monitoring/observability needed

## Step 4: Generate Workflow Visualization

Create Mermaid flowchart showing all phases with EXECUTE or SKIP status.

## Step 5: Create Execution Plan Document

Create `aidlc-docs/inception/plans/execution-plan.md` with:
- Detailed analysis summary
- Workflow visualization
- Phases to execute with rationale
- Estimated timeline
- Success criteria

## Step 6: Present Plan to User

```markdown
# 📋 Workflow Planning Complete

**Recommended Execution Plan**:

🔵 **INCEPTION PHASE:**
[List stages with rationale]

🟢 **CONSTRUCTION PHASE:**
[List stages with rationale]

**Estimated Timeline**: [Duration]

> **📋 REVIEW REQUIRED:**  
> Please examine: `aidlc-docs/inception/plans/execution-plan.md`

> **🚀 WHAT'S NEXT?**
>
> 🔧 **Request Changes** - Ask for modifications
> 📝 **Add Skipped Stages** - Include stages currently marked as SKIP
> ✅ **Approve & Continue** - Proceed to next stage
```

## Step 7: Handle User Response

- **If approved**: Proceed to next stage
- **If changes requested**: Update plan and re-confirm
