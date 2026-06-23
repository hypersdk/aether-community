---
> 🚀 **Trial v0.30.0 is live!** The latest release is available for trial today — [get started in 5 minutes →](#try-v030-in-5-minutes)

# Aether — Community

> **Universal runtime portability — one YAML spec deploys across Podman, Kubernetes, KubeVirt, and Metal3.**

![Version](https://img.shields.io/badge/version-v0.30.0-blue) ![Discussions](https://img.shields.io/github/discussions/hypersdk/aether-community) ![Issues](https://img.shields.io/github/issues/hypersdk/aether-community) ![License](https://img.shields.io/badge/license-Proprietary-red)

Public issue tracker and community feedback space for **Aether** by [Zyvor AI Labs](https://zyvor.dev).
The source code is maintained in a private repository. This repo is for bug reports, feature requests, UX feedback, and community discussion.

---

## What's new in v0.30

- Blue-green migration GA — zero-downtime runtime migration with automatic rollback on failure
- 4 new runtime adapters: Podman Quadlets, k3s, Talos, and bare-metal systemd units
- Drift auto-heal — detect and reconcile config drift automatically across all runtimes
- Terraform provider v0.30 — manage workload placement as infrastructure code
- Intent engine v2 — runtime scoring now includes GPU availability and network topology

---

## Why Aether

| Problem | Aether answer |
|---------|--------------|
| Same app has four completely different deploy paths | One YAML spec validated and deployed to any runtime |
| Runtime migrations are manual, risky, and slow | 16 migration paths with blue-green, rolling, and instant strategies |
| Teams guess which runtime fits the workload | Intent engine scores runtimes by cost, latency, and reliability |
| Config drift across runtimes goes unnoticed | Drift detection loop + auto-reconciliation on every runtime |
| Ops needs a single pane across runtime types | k9s-level web UI with SSE, command palette, and log viewer |

---

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│  Clients     React Web UI · Interactive TUI · Rust CLI       │
├──────────────────────────────────────────────────────────────┤
│  Control     Intent Engine · Migration Engine · Policy Gate  │
├──────────────────────────────────────────────────────────────┤
│  Runtimes    Podman · Kubernetes · KubeVirt · Metal3         │
└──────────────────────────────────────────────────────────────┘
```

---

## Try v0.30 in 5 minutes

```bash
# Binary
curl -fsSL https://releases.hypersdk.dev/aether/install.sh | AETHER_VERSION=0.30.0 bash

aether init
aether run --spec examples/workloads/simple-web.yaml
aether list --output wide

# Helm (Kubernetes)
helm repo add hypersdk https://charts.hypersdk.dev
helm install aether hypersdk/aether --version 0.30.0 \
  -n aether-system --create-namespace
```

**Requirements:** One or more runtimes: Podman 4+, Kubernetes 1.28+, KubeVirt, or Metal3

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, screenshots or logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Report →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**
Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code, internal configs, or architecture details
- API tokens, license keys, or credentials
- Private logs with sensitive data
- Security vulnerabilities — email security@zyvor.dev instead

---

## Join the community

⭐ [Star this repo](https://github.com/hypersdk/aether-community) · 💬 [Open a Discussion](https://github.com/hypersdk/aether-community/discussions) · 🐛 [Report a Bug](../../issues/new?template=bug_report.yml) · 📧 [hello@zyvor.dev](mailto:hello@zyvor.dev)

Maintained by [Zyvor AI Labs](https://zyvor.dev)
