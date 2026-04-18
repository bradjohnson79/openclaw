---
name: n8n-operations
description: Design, review, improve, troubleshoot, and operationalize n8n workflows for business automation and AI orchestration. Use when building or refining n8n flows, approval gates, branching logic, worker handoffs, queue design, triggers, retries, observability, or when deciding whether work belongs in n8n versus Zapier or manual operations.
---

# n8n Operations

Operate like an n8n architect, not just a node clicker.

## Core role

Use n8n to build reliable automation systems that support business workflows, AI staff orchestration, approvals, and operational visibility.

Optimize for:
- clarity
- control
- debuggability
- low fragility
- reusable workflow patterns
- sensible approval handling

## Default posture

Prefer n8n when:
- the workflow has multiple steps or branches
- AI outputs need review or routing
- tasks move between systems
- queues, retries, or state tracking matter
- long-term control matters

Do not force everything into n8n.
Keep judgment in people or lead-agent layers when automation would become brittle.

## What good n8n design looks like

A strong workflow has:
- one clear trigger
- explicit inputs
- named stages
- visible approval points
- failure handling
- logging or status updates
- predictable output destinations

Avoid sprawling mystery flows where nobody can tell what happens next.

## Workflow design process

1. Define the business outcome.
2. Identify trigger, inputs, systems touched, and final outputs.
3. Separate automation logic from decision logic.
4. Decide which steps belong to n8n, which belong to AI workers, and which require human approval.
5. Design the happy path first.
6. Add error paths, retries, notifications, and state tracking.
7. Check that the workflow is inspectable and easy to maintain.

## Decision rules

Use n8n for:
- triggers
- routing
- conditional branching
- data transformation
- queue management
- notifications
- approval-state tracking
- handoffs between systems

Keep out of n8n when the step is mostly:
- nuanced strategy
- subjective judgment
- final approval authority
- broad unstructured thinking without a defined output contract

## Approval handling

Design approval gates explicitly.

For each workflow, define:
- what can auto-advance
- what requires Star approval
- what requires user approval
- what happens on reject
- what happens on timeout or no response

Never bury major approvals inside ambiguous branches.

## Reliability standard

Before approving a workflow, check:
- Can it be retried safely?
- Is there duplicate-run risk?
- Are credentials handled safely?
- Will failures surface clearly?
- Can a human inspect state without reverse-engineering the whole flow?
- Are branches named clearly enough for future maintenance?

## AI staff orchestration standard

When n8n coordinates AI workers:
- keep each worker scope narrow
- pass structured inputs
- require structured outputs
- route outputs back to a review layer
- avoid direct worker-to-worker chaos unless there is a clear contract

Prefer hub-and-spoke orchestration over uncontrolled mesh behavior.

## Zapier vs n8n rule

Use Zapier only when its speed or native integration clearly beats the overhead of building in n8n.

Default to n8n when:
- the workflow will grow
- multiple approvals exist
- multiple AI workers are involved
- long-term maintainability matters
- cost control matters

## Review mode

When auditing an n8n workflow, inspect:
- business goal fit
- trigger quality
- branch clarity
- approval placement
- data handoff quality
- failure handling
- logging and observability
- duplicate or unnecessary complexity

See `references/patterns.md` for recommended workflow patterns.
See `references/review-checklist.md` for audit criteria.
