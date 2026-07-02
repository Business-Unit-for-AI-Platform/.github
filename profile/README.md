# Business-Unit-for-AI-Platform

AI-Platform business unit organization.

## Standard Repositories

- [`requirements`](https://github.com/Business-Unit-for-AI-Platform/requirements): product/business requirements, scope, workflows, acceptance criteria, and open questions.
- [`platform-roadmap`](https://github.com/Business-Unit-for-AI-Platform/platform-roadmap): roadmap, module planning, release sequencing, and productization strategy.
- [`knowledge-base`](https://github.com/Business-Unit-for-AI-Platform/knowledge-base): reusable knowledge for customer scenarios, AI tools, prompts/agents, models/providers, delivery playbooks, productization, and stable decisions.
- [`deploy`](https://github.com/Business-Unit-for-AI-Platform/deploy): deployment orchestration, domains, CI/CD release notes, environment mapping, and operations docs.
- [`.github`](https://github.com/Business-Unit-for-AI-Platform/.github): organization profile and repository map.

## Repository Map

Current repositories should keep this split:

- Business application repositories own source code, tests, builds, and development docs.
- `requirements` owns durable product/business requirements.
- `platform-roadmap` owns roadmap, version planning, and productization sequencing.
- `knowledge-base` owns reusable knowledge, customer scenarios, tool methods, prompt/agent/model lessons, delivery playbooks, and stable decisions.
- `deploy` owns deployment and operations workflows.
- `.github` owns organization-level profile and repository map.

## Governance

- Keep development and deployment separate.
- Use GitHub Actions/CI for deployment workflows; store credentials in GitHub Actions secrets.
- Do not commit tokens, passwords, SSH keys, customer private data, or server credentials.
