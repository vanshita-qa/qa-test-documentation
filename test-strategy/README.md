# QA Test Strategy

## Objective

This document defines the testing approach used to evaluate web applications across functional, integration, regression, exploratory, API and end-to-end workflows.

## Testing Approach

Testing is based on:

- Business requirements
- User workflows
- Risk assessment
- Functional behaviour
- Integration points
- Negative scenarios
- Boundary conditions
- Role and permission models
- Data consistency

## Test Levels

### Functional Testing

Validate that individual features behave according to requirements and acceptance criteria.

### Integration Testing

Validate interactions between modules, services, APIs and dependent workflows.

### End-to-End Testing

Validate complete business journeys from the initial user action through the final expected outcome.

### Regression Testing

Validate existing functionality after feature changes, defect fixes or releases.

### Exploratory Testing

Use structured exploratory sessions to identify unexpected behaviour, edge cases and workflow risks that may not be covered by predefined test cases.

## Test Design Techniques

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing
- State Transition Testing
- Error Guessing
- Risk-Based Testing
- Negative Testing

## Defect Management

Defects are documented with:

- Clear title
- Environment
- Preconditions
- Reproducible steps
- Expected result
- Actual result
- Severity
- Priority
- Reproducibility
- Business impact
- Supporting evidence

## Exit Criteria

Testing can be considered complete when:

- Planned critical scenarios have been executed.
- Critical and high-severity defects have been resolved or formally accepted.
- Regression testing has been completed for impacted areas.
- Known risks have been documented.
- Test results have been communicated to relevant stakeholders.
