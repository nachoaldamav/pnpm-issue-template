---
name: Bug Report
description: Create a bug report for the pnpm core
labels: ['template: bug']
body:
  - type: markdown
    attributes:
      value: |
        *Note:* If you leave out sections, the issue might be moved to the ["Help" section](https://github.com/pnpm/pnpm/discussions/categories/help).
        Feature requests should be opened as [discussions](https://github.com/pnpm/pnpm/discussions/new?category=ideas).
  - type: checkboxes
    attributes:
      label: Verify latest release
      description: 'Please run `pnpm install pnpm@latest` to try the latest version of pnpm. Some issues may already be fixed in the latest release, so please verify that your issue reproduces before opening a new issue.'
      options:
        - label: I verified that the issue exists in the latest pnpm release
          required: true
  - type: textarea
    attributes:
      label: Provide environment information
      description: Please run `pnpm env info` in the root directory of your project and paste the results.
      render: bash
    validations:
      required: true
  - type: dropdown
    attributes:
      label: Which area(s) of pnpm are affected? (leave empty if unsure)
      multiple: true
      options:
        - 'Resolver'
        - 'CLI'
        - 'Hooks'
        - 'Lockfile'
        - 'Store'
        - 'Package manager compatibility'
        - 'Operating System (Windows, MacOS, Linux)'
  - type: input
    attributes:
      label: Link to the code that reproduces this issue or a replay of the bug
      description: |
        A link to a GitHub repository minimal reproduction. If a minimal reproduction can't be created please share a replay of the bug which doesn't require sharing a private repo.
    validations:
      required: true
  - type: textarea
    attributes:
      label: To Reproduce
      description: Steps to reproduce the behavior, please provide a clear description of how to reproduce the issue, based on the linked minimal reproduction. Screenshots can be provided in the issue body below. If using code blocks, make sure that [syntax highlighting is correct](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting) and double check that the rendered preview is not broken.
    validations:
      required: true
  - type: textarea
    attributes:
      label: Describe the Bug
      description: A clear and concise description of what the bug is.
    validations:
      required: true
  - type: textarea
    attributes:
      label: Expected Behavior
      description: A clear and concise description of what you expected to happen.
    validations:
      required: true
  - type: markdown
    attributes:
      value: Before posting the issue go through the steps you've written down to make sure the steps provided are detailed and clear.
  - type: markdown
    attributes:
      value: Contributors should be able to follow the steps provided in order to reproduce the bug.
  - type: markdown
    attributes:
      value: These steps are used to add integration tests to ensure the same issue does not happen again. Thanks in advance!
  - type: input
    attributes:
      label: Which Node.js version are you using? (if relevant)
      description: 'Please specify the exact version. For example: 14.18.1'
  - type: input
    attributes:
      label: How are you using pnpm? (if relevant)
      description: 'For example: Workspace, Standalone installation'