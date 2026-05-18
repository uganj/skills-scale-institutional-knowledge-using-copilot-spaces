---
name: "Create README for OctoAcme Project Management Docs"
description: "Create a README file for the docs folder that provides an overview of OctoAcme project management processes and links to all documentation."
title: "[Process Doc Update]: Create README for OctoAcme Project Management Docs with links and process summary"
labels: ["documentation", "process improvement"]
body:
  - type: dropdown
    id: process_doc
    attributes:
      label: "Which process document do you want to update?"
      description: "This is a new document for the docs folder"
      options:
        - "<new document>"
    validations:
      required: true

  - type: textarea
    id: content_summary
    attributes:
      label: "Summary of New Content"
      description: "Briefly describe the new content or update you want to add."
      value: "Create a comprehensive README.md for the docs/ folder that serves as the central navigation hub for all OctoAcme project management processes. The README should provide a brief introduction to OctoAcme's project management approach, the principles that guide our work, and organized links to all process documentation."
    validations:
      required: true

  - type: textarea
    id: rationale
    attributes:
      label: "Why is this update needed?"
      description: "Explain the reason for this addition."
      value: "The docs/ folder currently lacks an entry point for new team members and stakeholders. A README will improve discoverability, provide context about OctoAcme's project management methodology, and serve as a centralized navigation hub for all process documentation. This addresses a key gap in onboarding and institutional knowledge sharing."
    validations:
      required: true

  - type: textarea
    id: example_content
    attributes:
      label: "Suggested Content"
      description: "Paste the proposed new text and structure for the README"
      value: "## OctoAcme Project Management Processes

### Overview
OctoAcme's project management approach is built on principles of customer-first delivery, iterative development, clear ownership, data-informed decisions, and psychological safety. This folder contains comprehensive guides for running projects at all stages of the lifecycle.

### Core Principles
- **Customer-first**: Prioritize customer value and usability
- **Iterative delivery**: Deliver small, testable increments
- **Clear ownership**: Each project has a named Project Manager (PM) and Product Lead
- **Data-informed decisions**: Measure impact and iterate based on evidence
- **Psychological safety**: Encourage feedback and learning

### Project Lifecycle
Our projects follow a structured lifecycle from initiation through close-out:

1. **Initiation** → Define business need and get stakeholder alignment
2. **Planning** → Break work into shippable increments and create detailed plans
3. **Execution** → Build, test, review, and iterate on deliverables
4. **Release** → Deploy to production and verify success
5. **Retrospective** → Capture learnings and identify improvements

### Documentation Guide

#### For All Team Members
- **[OctoAcme Project Management Overview](./octoacme-project-management-overview.md)** - Start here for a high-level introduction to our approach, roles, artifacts, and communication cadence

#### For Project Planning & Initiation
- **[Project Initiation Guide](./octoacme-project-initiation.md)** - Define initial steps to validate work, align stakeholders, and create lightweight plans
- **[Project Planning](./octoacme-project-planning.md)** - Turn approved initiatives into actionable plans and backlogs for delivery

#### For Day-to-Day Execution
- **[Execution & Tracking](./octoacme-execution-and-tracking.md)** - Guidance for managing execution, tracking progress toward milestones, and team rhythm
- **[Roles & Personas](./octoacme-roles-and-personas.md)** - Detailed descriptions of core roles (Developers, Product Managers, Project Managers) and their responsibilities

#### For Risk & Communication
- **[Risk Management & Communication](./octoacme-risks-and-communication.md)** - How to identify, manage, and communicate risks, dependencies, and stakeholder updates

#### For Release & Deployment
- **[Release & Deployment Guide](./octoacme-release-and-deployment.md)** - Standardized processes for releasing features to production, including checklists and rollback procedures

#### For Continuous Improvement
- **[Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)** - How to run effective retrospectives and convert learnings into actionable improvements

### Quick Reference

**Communication Cadence**
- Daily standups (15 min) - Focus on progress, blockers, dependencies
- Weekly PM + PdM sync - Alignment and prioritization
- Twice-weekly delivery standups - Team coordination
- Monthly stakeholder updates - High-level progress and risks
- Sprint end demo/retrospective - Showcase work and capture learnings

**Key Artifacts**
- Project Charter / One-pager
- Roadmap and Release Plan
- Sprint/Iteration Backlog
- Acceptance Criteria & Definition of Done
- Risk Register
- Retrospective notes and action items

**Common Checklists**
- [Project Initiation Checklist](./octoacme-project-initiation.md#initiation-checklist)
- [Planning Checklist](./octoacme-project-planning.md#planning-checklist)
- [Execution Checklist](./octoacme-execution-and-tracking.md#execution-checklist)
- [Deployment Checklist](./octoacme-release-and-deployment.md#deployment-checklist)

### Getting Started
1. Read the [OctoAcme Project Management Overview](./octoacme-project-management-overview.md) to understand our approach
2. Use the relevant guides for your project phase (Initiation → Planning → Execution → Release → Retrospective)
3. Reference role descriptions in [Roles & Personas](./octoacme-roles-and-personas.md) to understand team responsibilities
4. Check checklists at each phase to ensure nothing is missed

### Feedback & Improvements
Have ideas to improve our processes? See [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md) for how to contribute improvements, or open an issue using the [Process Doc Update template](./.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml)."

  - type: checkboxes
    id: acceptance_criteria
    attributes:
      label: "Acceptance Criteria"
      description: "Check all that apply"
      options:
        - label: "Content aligns with existing process docs"
        - label: "Update improves clarity or closes a documented gap"
        - label: "Proposed content has been reviewed with stakeholders (if needed)"
