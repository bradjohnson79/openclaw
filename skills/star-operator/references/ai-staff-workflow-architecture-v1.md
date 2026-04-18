# AI Staff Workflow Architecture v1

## Purpose

Create a practical operating architecture where:
- Brad acts as administrator
- Star acts as project manager and orchestration lead
- AI staff execute specialized work
- automation systems move tasks, data, approvals, and status updates across the stack

## Core hierarchy

### Brad
Owns:
- final authority
- major approvals
- strategic direction
- staffing decisions
- budget-impacting decisions

### Star
Owns:
- project intake
- task decomposition
- delegation
- worker review
- quality control
- approval triage
- final synthesis before Brad approval when required

### AI staff
Own:
- specialized execution
- first-pass outputs
- narrow-scope assignments
- escalation when blocked or unclear

## Automation backbone

### Recommended backbone
Use **n8n** as the primary workflow engine.

Use **Zapier** only when:
- a specific integration is faster there
- setup speed matters more than flexibility
- the workflow is simple enough that long-term control is less important

### Why n8n should be primary
- better for branching logic
- better for internal orchestration
- better for self-hosting and control
- better for multi-step AI staff systems
- better for cost control at scale

## Task flow

### 1. Intake
A task enters through one of these paths:
- direct instruction from Brad
- CRM/event trigger
- content calendar trigger
- lead-generation trigger
- social media workflow trigger
- ad workflow trigger
- website or funnel change request

The intake record should include:
- task name
- business goal
- priority
- source
- due date if any
- risk level
- required approval level

### 2. Triage by Star
Star decides:
- Is this strategic or operational?
- Is it major or minor?
- Can it be handled directly?
- Should it be delegated?
- Which worker should own the first pass?
- Does Brad need to approve before work begins?

### 3. Worker assignment
Star routes the task to the appropriate worker.

Examples:
- junior marketing specialist for research, first-pass promotion, and marketing support
- ads specialist for campaign structure, paid traffic ideas, and keyword/ad planning
- content worker for copy, scripts, captions, posts, and hook generation
- social worker for platform-specific adaptation and scheduling support
- builder or SEO worker for implementation and optimization
- QA worker for final review and defect finding

### 4. Execution
The worker returns:
- requested deliverable
- assumptions made
- blockers
- open questions
- recommendation if relevant

### 5. Review by Star
Star either:
- approves the work
- revises it
- sends it back for improvement
- routes it to another worker
- escalates it to Brad if it crosses the major-decision boundary

### 6. Approval path
#### Minor work
Star can approve and move forward.

#### Major work
Brad must approve before implementation or release.

Major includes:
- new idea implementation on a website
- new system integration
- staffing or authority changes
- significant budget or paid-spend changes
- meaningful strategic shifts

### 7. Deployment or release
Once approved, automation pushes the work to the next destination:
- publish queue
- CRM
- social scheduler
- ad platform workflow
- implementation queue
- archive/logging system

### 8. Reporting and memory
Each completed task should produce:
- status
- owner
- output link or artifact
- approval record
- lessons or notes if something should be reused later

## Automation responsibility split

### Star responsibilities
- decision making
- approval triage
- task decomposition
- delegation
- quality review
- escalation
- final synthesis

### Worker responsibilities
- execution within scope
- reporting blockers
- returning usable outputs in the required format

### n8n responsibilities
- workflow routing
- conditional branching
- queue control
- status updates
- notifications
- record creation
- approval-state tracking
- pushing work between systems

### Zapier responsibilities
- lightweight app integrations
- simple triggers
- fast connector-based workflows where deep logic is not required

## Recommended first operational lanes

### Lane 1: Lead generation
Use for:
- lead magnets
- funnel ideas
- landing page copy
- follow-up sequences
- promotion support

Flow:
Star -> junior marketing specialist -> content -> builder/SEO -> QA -> Star -> Brad if major

### Lane 2: Social media management
Use for:
- post planning
- content calendars
- captions
- repurposing
- platform adaptation for Facebook, TikTok, YouTube, and Instagram

Flow:
Star -> junior marketing specialist -> content -> social -> QA -> Star

### Lane 3: SEO and promotion
Use for:
- keyword opportunity research
- content optimization
- on-page changes
- promotional tie-ins

Flow:
Star -> junior marketing specialist -> builder/SEO -> QA -> Star -> Brad if major website change

### Lane 4: Ads strategy and promotion
Use for:
- Google Ads planning
- campaign structure
- ad creative variations
- testing plans

Flow:
Star -> ads specialist -> content -> QA -> Star -> Brad if budget or strategy impact is major

## Approval checkpoints

Brad approval required for:
- major website changes
- new system connections
- role/authority changes
- high-impact ad or budget changes
- meaningful shifts in strategic direction

Star approval sufficient for:
- drafts
- revisions
- routine operational decisions
- minor implementation steps
- worker reassignments

## Design principle

Keep workers narrow.
Keep Star central.
Keep Brad above major decisions.
Keep automation handling movement, not judgment.

## Immediate next build targets

1. Junior Marketing Specialist Role Spec
2. Task request template
3. Approval-state template
4. First n8n lane design for lead generation
5. First social media workflow lane
