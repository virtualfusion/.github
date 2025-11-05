# Virtual Fusion Global Templates Repository

Welcome to the **Global Templates Repository** for Virtual Fusion.

This repository is the central source for shared **community health files** that apply to all other repositories in the Virtual Fusion organization. It includes templates for things like:

- Issue reports (bug reports, feature requests)
- Pull request descriptions
- Code of conduct or contributing guidelines
- Future shared configuration and workflow files

## Why does this repository exist?

Managing templates individually across many repositories can be repetitive and hard to maintain. By keeping our shared templates in this central repository, we get several benefits:

- A single source of truth for issue and pull request templates
- Consistency across all repositories within Virtual Fusion
- Quicker onboarding of new team members
- Ability to improve templates in one place and have those changes automatically apply across the organization

## How it works

GitHub supports using a repository named `.github` at the organization level to store default templates and common files. When this repository is public, all other repositories in the organization inherit these templates unless they override them locally.

This means:

- If a repo does not have its own issue or PR templates, it will use the ones defined here
- Updating a template in this repo updates it for every repo that relies on it

## Current Templates

The following templates are currently available in this repository:

- Bug Report Template
- Feature Request Template
- Technical Feature Implementation Template
- Pull Request Template

More templates will be added and improved over time.

## Contributing

To suggest changes or add new templates:

1. Create a branch and make your changes
2. Open a pull request with a clear description
3. Assign it to a reviewer from the Virtual Fusion team

All updates here will automatically reflect in other repositories that inherit from this template set.

## Requirements

- This repository must remain **public** to ensure proper inheritance
- Each consuming repository must not define its own version of the same template if it wants to inherit from this repo

---

With this setup, we aim to maintain consistent, high quality templates across all our projects and to continue improving our documentation practices.
