# n8n Review Checklist

Use this when reviewing or debugging an n8n workflow.

## Business fit
- Is the workflow solving a real operational problem?
- Is n8n the right home for it?
- Should any part stay manual, human-approved, or agent-led instead?

## Trigger quality
- Is the trigger explicit and reliable?
- Can duplicate executions happen?
- Is idempotency needed?

## Inputs and outputs
- Are inputs normalized?
- Are required fields validated?
- Are outputs structured and routable?

## Branching
- Are branches easy to understand?
- Do branch names reflect business meaning?
- Are approval paths obvious?

## Error handling
- What happens when an API fails?
- What happens on timeout?
- Is retry behavior safe?
- Is a human alerted when intervention is needed?

## Approval logic
- Is major approval separated from minor approval?
- Can the workflow pause and resume cleanly?
- Are rejected items handled intentionally?

## Observability
- Can someone inspect current state quickly?
- Are logs or records written where future-you can find them?
- Is it obvious why a task failed?

## Maintainability
- Could another operator understand this workflow next week?
- Is there unnecessary duplication?
- Should a repeated subflow become its own reusable workflow?

## AI orchestration
- Are worker roles narrow and well-defined?
- Are prompts or briefs structured?
- Are outputs reviewed before automatic release?
- Is there a sane escalation path?

## Final judgment
Approve only if the workflow is:
- reliable enough to trust
- clear enough to maintain
- bounded enough to debug
- aligned enough to support the business without creating hidden risk
