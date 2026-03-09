name: Bug report
description: Report a real bug in repo content, links, templates, or project behavior.
title: "[Bug] "
labels:
  - bug
  - needs-triage
body:
  - type: markdown
    attributes:
      value: |
        Use this form for reproducible bugs.

        Good examples:
        - a broken link
        - a malformed template
        - a file that renders incorrectly
        - a content or structure bug in docs
        - a reproducible repo-level problem

  - type: input
    id: affected_area
    attributes:
      label: Affected area
      description: Which page, template, file, or repo surface is affected
      placeholder: e.g. README, ECOSYSTEM_MAP, recognition_update.yml, config.yml
    validations:
      required: true

  - type: textarea
    id: current_behavior
    attributes:
      label: Current behavior
      description: What is happening now
      placeholder: Describe the bug clearly
    validations:
      required: true

  - type: textarea
    id: expected_behavior
    attributes:
      label: Expected behavior
      description: What should happen instead
      placeholder: Describe the expected result
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: Steps to reproduce
      description: Give a short reproducible path
      placeholder: |
        1. Open ...
        2. Click ...
        3. See ...
    validations:
      required: true

  - type: textarea
    id: evidence
    attributes:
      label: Evidence
      description: Add screenshots, links, rendered output, or other useful context
      placeholder: Paste supporting details here
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: Checklist
      options:
        - label: I confirmed this is a bug, not a feature request or general question
          required: true
        - label: I included enough detail for someone else to reproduce or inspect the issue
          required: true
