# Mid-Workflow Changes and Phase Management

## Overview

Users may request changes to the execution plan or phase execution during the workflow. This document provides guidance on handling these requests safely and effectively.

## Types of Mid-Workflow Changes

### 1. Adding a Skipped Phase
**Handling**: Confirm request, check dependencies, update execution plan, execute phase, log change.

### 2. Skipping a Planned Phase
**Handling**: Confirm request, warn about impact, get explicit confirmation, update plan, log change.

### 3. Restarting Current Stage
**Handling**: Understand concern, offer modify vs restart options, archive existing work if restart, re-execute.

### 4. Restarting Previous Stage
**Handling**: Assess impact on dependent stages, warn user, archive affected artifacts, reset stages, re-execute.

### 5. Changing Stage Depth
**Handling**: Confirm request, update execution plan, adjust approach, update timeline estimates.

### 6. Pausing Workflow
**Handling**: Complete current step, update checkboxes, update state, log pause, provide resume instructions.

## General Guidelines for Handling Changes

### Before Making Changes
1. **Understand the Request**: Ask clarifying questions
2. **Assess Impact**: Identify all affected stages and artifacts
3. **Explain Consequences**: Communicate what will need to be redone
4. **Offer Alternatives**: Sometimes modification is better than restart
5. **Get Explicit Confirmation**: User must understand and accept the impact

### During Changes
1. **Archive Existing Work**: Always backup before making destructive changes
2. **Update All Tracking**: Keep state files and audit.md in sync
3. **Communicate Progress**: Keep user informed
4. **Validate Changes**: Ensure changes are consistent across all artifacts

### After Changes
1. **Verify Consistency**: Check that all artifacts are aligned
2. **Update Documentation**: Ensure all references are updated
3. **Log Completely**: Document full change history in audit.md
4. **Confirm with User**: Verify changes meet expectations
5. **Resume Workflow**: Continue with normal execution

## Best Practices

1. **Always Confirm**: Never make destructive changes without explicit user confirmation
2. **Explain Impact**: Users need to understand consequences before deciding
3. **Offer Options**: Sometimes there are multiple ways to handle a change
4. **Archive First**: Always backup before making destructive changes
5. **Update Everything**: Keep all tracking files in sync
6. **Log Thoroughly**: Document all changes for audit trail
7. **Be Flexible**: Workflow should adapt to user needs, not force rigid process
