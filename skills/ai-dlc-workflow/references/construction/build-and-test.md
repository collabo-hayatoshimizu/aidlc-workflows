# Build and Test

**Purpose**: Build all units and execute comprehensive testing strategy

## Prerequisites
- Code Generation must be complete for all units
- All code artifacts must be generated

## Step 1: Analyze Testing Requirements

Determine appropriate testing strategy:
- **Unit tests**: Already generated per unit
- **Integration tests**: Test interactions between units/services
- **Performance tests**: Load, stress, and scalability testing
- **End-to-end tests**: Complete user workflows
- **Contract tests**: API contract validation
- **Security tests**: Vulnerability scanning

## Step 2: Generate Build Instructions

Create `build-instructions.md` with:
- Prerequisites (build tool, dependencies, environment variables)
- Build steps (install dependencies, configure environment, build all units)
- Troubleshooting guide

## Step 3: Generate Unit Test Execution Instructions

Create `unit-test-instructions.md` with:
- Commands to run all unit tests
- Expected results and coverage
- How to fix failing tests

## Step 4: Generate Integration Test Instructions

Create `integration-test-instructions.md` with:
- Test scenarios for unit interactions
- Setup and cleanup procedures
- Commands to run integration tests

## Step 5: Generate Performance Test Instructions (If Applicable)

Create `performance-test-instructions.md` with:
- Performance requirements
- Test environment setup
- Load and stress test commands
- How to analyze results

## Step 6: Generate Additional Test Instructions (As Needed)

- Contract tests for microservices
- Security tests
- End-to-end tests

## Step 7: Generate Test Summary

Create `build-and-test-summary.md` with:
- Build status
- Test execution summary (unit, integration, performance)
- Overall status
- Next steps

## Step 8: Present Results

```markdown
# 🔨 Build and Test Complete!

**Build Status**: [Success/Failed]

**Test Results**:
✅ Unit Tests: [X] passed
✅ Integration Tests: [X] scenarios passed
✅ Performance Tests: [Status]

**Generated Files**:
- build-instructions.md
- unit-test-instructions.md
- integration-test-instructions.md
- performance-test-instructions.md
- build-and-test-summary.md

**Ready to proceed to Operations stage?**
```

## Step 9: Wait for Explicit Approval
