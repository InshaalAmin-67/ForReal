# Security policy

## Report a vulnerability privately

Use [GitHub's private vulnerability reporting form](https://github.com/InshaalAmin-67/ForReal/security/advisories/new). Do not disclose an exploitable issue or actual credentials in a public issue or pull request.

Include the affected commit, a minimal reproduction using fictional data, the observed behavior, and the expected impact. For instruction-related issues, include the input that caused the assistant to cross a trust or permission boundary. Never send real tokens, passwords, or sensitive conversation content as a demonstration.

Security fixes target the current `main` branch. Older commits and third-party forks may not contain those fixes.

## What this project trusts

The official source is [InshaalAmin-67/ForReal](https://github.com/InshaalAmin-67/ForReal). Forks and proposed changes are separate, unreviewed sources until the maintainer accepts them.

ForReal contains instructions and UI metadata. It does not need credentials, an installer script, executable dependencies, or a service of its own. The host assistant supplies any tools and enforces its own permissions. The skill's wording is not a sandbox or a guarantee against prompt injection.

Market pages, search results, attachments, issue text, and pull request descriptions are evidence to inspect, not instructions to obey. Research must not cause the assistant to disclose secrets, run unrelated commands, install software, or send private information elsewhere.

## Repository safeguards

- `main` requires pull requests, resolved review conversations, and a linear commit history. These restrictions also apply to administrators.
- Force pushes and branch deletion are blocked on `main`.
- GitHub Actions is disabled. Proposed workflows cannot run in this repository while it remains disabled.
- Secret scanning and push protection are enabled. They supplement review and do not detect every possible sensitive value.
- The wiki and repository projects are disabled; public issues and pull requests remain available.
- `CODEOWNERS` identifies the maintainer for review routing. The repository has one maintainer, so a second person's approval is not mandatory. Contributors do not receive write access by opening a pull request.

Repository settings are managed on GitHub; these files do not enforce settings on a fork. Repository protections also do not prevent an owner or a compromised administrator account from changing those settings.

## Installing and updating

Review `SKILL.md`, `agents/openai.yaml`, and the complete diff before accepting an update. Prefer a reviewed commit for reproducible installs. Do not execute commands supplied by unknown contributors or automatically install from their forks.

Maintainers should protect their GitHub account with two-factor authentication, keep recovery codes securely, and grant tokens or apps only the access they need. Account security is separate from repository settings.
