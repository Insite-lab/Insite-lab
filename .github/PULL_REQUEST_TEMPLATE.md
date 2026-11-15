---
name: "\U0001F4DD Pull Request"
description: Submit a pull request
title: "[PR]: "
labels: [""]
body:
  - type: markdown
    attributes:
      value: |
        Thanks for submitting a pull request!

  - type: textarea
    id: description
    attributes:
      label: Description
      description: Describe your changes in detail
    validations:
      required: true

  - type: textarea
    id: related-issue
    attributes:
      label: Related Issue
      description: Link to the issue this PR addresses
      placeholder: "Fixes #(issue)"
    validations:
      required: false

  - type: textarea
    id: motivation
    attributes:
      label: Motivation and Context
      description: Why is this change required? What problem does it solve?
    validations:
      required: false

  - type: textarea
    id: changes
    attributes:
      label: Changes Made
      description: List the changes you made
      value: |
        - [ ] Change 1
        - [ ] Change 2
        - [ ] Change 3
    validations:
      required: true

  - type: textarea
    id: testing
    attributes:
      label: Testing
      description: Describe the tests you ran to verify your changes
    validations:
      required: true

  - type: checkboxes
    id: checklist
    attributes:
      label: Checklist
      options:
        - label: My code follows the style guidelines of this project
          required: true
        - label: I have performed a self-review of my own code
          required: true
        - label: I have commented my code, particularly in hard-to-understand areas
          required: true
        - label: I have made corresponding changes to the documentation
          required: true
        - label: My changes generate no new warnings
          required: true
        - label: I have added tests that prove my fix is effective or that my feature works
          required: true
        - label: New and existing unit tests pass locally with my changes
          required: true

  - type: dropdown
    id: type
    attributes:
      label: Type of Change
      options:
        - Bug fix (non-breaking change that fixes an issue)
        - New feature (non-breaking change that adds functionality)
        - Breaking change (fix or feature that would cause existing functionality to change)
        - Documentation update
        - Refactoring (no functional changes)
    validations:
      required: true
