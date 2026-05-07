name: "Add Content to Project Management Process Docs"
description: "Request to add a README with summary and links to all docs in the project management documentation set."
title: "[Process Doc Update]: README, project management processes summary, and links to docs (OctoAcme Project Management Docs)"
labels: ["documentation", "process improvement"]
body:
  - type: dropdown
    id: process_doc
    attributes:
      label: "Which process document do you want to update? (If this is a new document, select '')"
      description: "Select the program management process document you want to add content to. If this is a new process doc, choose ''."
      options:
        - 
    validations:
      required: true

  - type: textarea
    id: content_summary
    attributes:
      label: "Summary of New Content"
      description: |
        Add a new README to the docs directory for OctoAcme Project Management that:
        - Provides a brief summary of the project's process approach
        - Includes a clickable list of links with one-line descriptions to each document in `docs/`.
      placeholder: "E.g., Add README with project management summary and document links."
    validations:
      required: true

  - type: textarea
    id: rationale
    attributes:
      label: "Why is this update needed?"
      description: "A README is needed to aid discoverability, organize reference materials, and onboard new team members by quickly surfacing available process docs and their purpose."
      placeholder: "E.g., Better docs navigation, new team onboarding, close structure gap."
    validations:
      required: true

  - type: textarea
    id: example_content
    attributes:
      label: "Suggested Content (optional)"
      description: |
        See below for exact README proposal (include summary + doc links).
      placeholder: |
        # OctoAcme Project Management Docs
        
        ## Summary
        The OctoAcme Project Management documentation provides standardized, repeatable workflows that cover the full project lifecycle: initiation, planning, execution, risk management, release, retrospectives, and roles. Principles include customer focus, iterative delivery, and clear accountability.
        
        ## Documents
        - [Project Management Overview](docs/octoacme-project-management-overview.md): How projects run, roles, principles, and core process structure
        - [Project Initiation Guide](docs/octoacme-project-initiation.md): How new projects are started, key deliverables, and decision gates
        - [Project Planning](docs/octoacme-project-planning.md): Planning, backlog, estimation, dependencies, and test planning
        - [Execution & Tracking](docs/octoacme-execution-and-tracking.md): Daily delivery, quality standards, metrics, and blockers
        - [Risk Management & Communication](docs/octoacme-risks-and-communication.md): Risk registers, stakeholder updates, and escalation
        - [Release & Deployment Guide](docs/octoacme-release-and-deployment.md): Release process, checklists, and rollback
        - [Retrospective & Continuous Improvement](docs/octoacme-retrospective-and-continuous-improvement.md): Capturing learnings and action items
        - [Roles & Personas](docs/octoacme-roles-and-personas.md): Project roles, responsibilities, and example communications
    
  - type: checkboxes
    id: acceptance_criteria
    attributes:
      label: "Acceptance Criteria"
      description: "Check all that apply:"
      options:
        - label: "Content aligns with existing process docs"
        - label: "Update improves clarity or closes a documented gap"
        - label: "Proposed content has been reviewed with stakeholders (if needed)"
