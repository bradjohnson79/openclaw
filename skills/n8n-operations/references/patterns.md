# n8n Patterns

## 1. Intake and triage pattern

Use when tasks arrive from forms, CRMs, chat systems, webhooks, or scheduled events.

Pattern:
1. Trigger
2. Normalize input
3. Assign task ID
4. Classify priority and type
5. Route to Star or the appropriate queue
6. Record status

Use this for:
- lead intake
- content requests
- support escalations
- internal ops requests

## 2. Approval gate pattern

Use when a workflow crosses a business risk boundary.

Pattern:
1. Build candidate output
2. Store artifact or payload
3. Send approval request
4. Wait for response
5. Branch on approve, reject, or timeout
6. Record decision

Use explicit states:
- pending_approval
- approved
- rejected
- expired

## 3. AI worker handoff pattern

Use when a lead agent or automation layer sends work to a specialized worker.

Pattern:
1. Create structured brief
2. Dispatch to worker
3. Receive structured result
4. Validate result format
5. Route to review layer
6. Update task state

Do not skip result validation.

## 4. Retry and alert pattern

Use when downstream systems can fail or rate-limit.

Pattern:
1. Attempt step
2. If transient failure, retry with backoff
3. If repeated failure, alert operator
4. Preserve task state for manual recovery

Do not silently swallow repeated failures.

## 5. Publish queue pattern

Use when outputs should not go live immediately.

Pattern:
1. Prepare publish artifact
2. Send to review queue
3. Require approval if needed
4. Publish through connector
5. Record timestamp, destination, and payload summary

Good for:
- social posts
- outbound messages
- CMS publishing
- ad launches

## 6. Multi-lane business pattern

Use when several workflow types coexist under one operating model.

Recommended lanes:
- lead generation
- content production
- social media
- SEO changes
- ad planning and launches
- admin and outreach

Keep each lane modular.
Do not cram every lane into one giant workflow.

## 7. Human override pattern

Use when an operator needs to step in.

Pattern:
1. Detect blocker or edge case
2. Pause task
3. Notify operator with context
4. Resume, reroute, or cancel based on response
5. Log override decision

This pattern is essential for complex AI-assisted operations.
