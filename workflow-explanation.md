# Workflow Explanation

## Workflow Goal

The objective of this workflow is to automatically process different types of productivity-related content and generate actionable outputs using specialized AI agents.

---

## Step 1: Content Intake Form

The workflow begins with a form where the user submits content and selects its type.

Possible categories:

* Email
* Study
* Goal
* Document

This provides a structured entry point for the workflow.

---

## Step 2: Input Classifier Agent

### AI Component

The Input Classifier Agent analyzes the submitted content and determines its category.

Responsibilities:

* Understand user input
* Classify content
* Generate structured output
* Prepare routing information

Output Example:

```json
{
  "type": "email",
  "confidence": 0.95
}
```

---

## Step 3: Route by Type

### Deterministic Component

A routing node directs the content to the appropriate specialized agent.

Possible routes:

* Email Prioritizer
* Study Planner
* Goal Tracker
* Action Extractor

This ensures each content type is processed by a dedicated expert agent.

---

## Step 4A: Email Prioritizer Agent

### AI Component

Responsibilities:

* Analyze email content
* Determine urgency
* Determine importance
* Generate priority labels

Output Example:

```json
{
  "priority": "High",
  "reason": "Deadline within 24 hours"
}
```

---

## Step 4B: Study Planner Agent

### AI Component

Responsibilities:

* Analyze academic requirements
* Create study schedules
* Recommend task sequencing
* Allocate study time

Output Example:

```json
{
  "daily_plan": [
    "DSA Practice",
    "Machine Learning Revision"
  ]
}
```

---

## Step 4C: Goal Tracker Agent

### AI Component

Responsibilities:

* Review goals
* Evaluate progress
* Recommend next actions
* Generate milestone suggestions

Output Example:

```json
{
  "goal": "Placement Preparation",
  "next_action": "Complete 3 Leetcode problems"
}
```

---

## Step 4D: Document Action Extractor

### AI Component

Responsibilities:

* Extract tasks
* Detect deadlines
* Identify action items
* Summarize important information

This converts unstructured documents into actionable outputs.

---

## Step 5: Merge Results

### Deterministic Component

Results from all specialized agents are merged into a common structure for downstream processing.

---

## Step 6: Schema Validation

### Deterministic Component

The workflow validates that every agent output follows the expected JSON schema.

Checks include:

* Required fields present
* Valid structure
* Consistent formatting

This improves reliability and reduces processing errors.

---

## Step 7: Urgency Check

### Deterministic Component

Business rules evaluate urgency levels.

Examples:

* High priority tasks
* Immediate deadlines
* Critical actions

Urgent items trigger an approval workflow.

---

## Step 8: Approval Workflow

### Human-in-the-Loop Component

When high-priority content is detected, the system sends an approval request through Gmail.

This provides an additional verification layer before taking action.

---

## Step 9: Google Sheets Logging

### Deterministic Component

The workflow records processed items for auditing and tracking purposes.

Logged information includes:

* Content type
* Priority
* Timestamp
* Workflow outcome

---

## Step 10: Email Digest

### Deterministic + AI Component

The workflow sends a final summary email containing:

* Priority information
* Recommended actions
* Study plans
* Goal recommendations
* Extracted tasks

---

## AI vs Deterministic Logic

### AI Responsibilities

* Classification
* Prioritization
* Planning
* Goal analysis
* Task extraction

### Deterministic Responsibilities

* Routing
* Validation
* Approval triggering
* Logging
* Notifications

This separation follows agentic workflow design principles by using AI for reasoning tasks and deterministic logic for control and execution.

---

## Practical Value

The workflow reduces manual effort required to organize information and helps users convert incoming content into meaningful actions. By combining multiple specialized agents with deterministic control logic, the system creates a reliable and scalable productivity assistant.
