# Aether — Community

> **Universal runtime portability — deploy once, move workloads across Podman, K8s, KubeVirt, Metal3**

Public issue tracker and community feedback space for **Aether** by [Zyvor AI Labs](https://zyvor.dev).

The source code is maintained in a private repository. This repo is for:
- Bug reports
- Feature requests
- UX feedback
- Documentation gaps
- Questions and discussion

---

## Key features

- One YAML spec deploys to Podman, Kubernetes, KubeVirt, or Metal3
- 16 migration paths with immediate, blue-green, and rolling strategies
- Intent engine scores runtimes by cost, latency, and reliability
- Drift detection and auto-reconciliation
- 19-page React dashboard + interactive TUI
- Terraform provider

---

## Installation

Aether runs as a standalone binary or as a Kubernetes deployment.

**Binary:**
```bash
curl -fsSL https://releases.hypersdk.dev/aether/install.sh | bash

aether init
aether run --spec examples/workloads/simple-web.yaml
aether list --output wide
```

**Helm (Kubernetes):**
```bash
helm repo add hypersdk https://charts.hypersdk.dev
helm install aether hypersdk/aether -n aether-system --create-namespace
```

**Packages:** .deb and .rpm packages available on the releases page.

**Requirements:** One or more of: Podman, Kubernetes 1.28+, KubeVirt, Metal3

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, and screenshots/logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Feedback →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**

Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code or internal configuration
- API tokens, license keys, or credentials  
- Private logs with sensitive data
- Security vulnerabilities (email security@zyvor.dev)

---

Maintained by [Zyvor AI Labs](https://zyvor.dev)
