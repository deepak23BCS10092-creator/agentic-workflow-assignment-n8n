# Agentic Personal Productivity Assistant

## Overview

This project is an AI-powered productivity workflow built using n8n. The system helps users transform different types of information such as emails, study requirements, goals, and documents into structured, actionable outputs.

Instead of relying on a single AI prompt, the workflow uses multiple specialized AI agents, routing logic, validation checks, and automated notifications to create a complete productivity management system.

The workflow demonstrates agentic AI concepts including task decomposition, role-based agents, routing, structured outputs, validation, and human-in-the-loop approval.

---

## Problem

Students and professionals receive information from multiple sources including emails, assignments, documents, study materials, and personal goals.

Managing these inputs manually often leads to:

* Missed deadlines
* Poor task prioritization
* Unstructured study plans
* Forgotten goals
* Important documents not being converted into actionable tasks

This workflow automates the entire process from information intake to actionable output.

---

## Features

### AI Agents

* Input Classifier Agent
* Email Prioritizer Agent
* Study Planner Agent
* Goal Tracker Agent
* Document Action Extractor Agent

### Workflow Capabilities

* Intelligent content classification
* Dynamic routing based on content type
* Email prioritization
* Study schedule generation
* Goal tracking recommendations
* Action extraction from documents
* Structured JSON outputs
* Urgency detection
* Human approval for urgent items
* Google Sheets logging
* Email notifications

---

## Workflow Architecture

Content Intake Form
↓
Input Classifier
↓
Route by Type
├── Email Prioritizer
├── Study Planner
├── Goal Tracker
└── Document Action Extractor
↓
Merge Results
↓
Validate Schema
↓
Check Urgency
↓
Approval Workflow
↓
Google Sheets Logging
↓
Email Digest

---

## Technologies Used

* n8n
* OpenAI GPT Models
* Gmail Integration
* Google Sheets
* PDF Extraction
* Structured Output Parsers

---

## Agentic Concepts Demonstrated

* Task decomposition
* Agent specialization
* Structured outputs
* Workflow routing
* Deterministic validation
* Human-in-the-loop review
* Tool integration
* Error handling

---

## Sample Use Cases

### Email Prioritization

Classifies and prioritizes incoming emails based on urgency and importance.

### Study Planning

Generates personalized study schedules from academic inputs.

### Goal Tracking

Provides actionable recommendations aligned with user goals.

### Document-to-Action Workflow

Extracts tasks, deadlines, and action items from uploaded documents.

---

## Repository Contents

* workflow.json
* README.md
* problem-statement.md
* workflow-explanation.md
* screenshots/
* sample-input-output/

---

## Author

Developed as part of the Agentic Workflow Design and n8n Demo assignment.
