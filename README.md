# Container Ship of Theseus

Kubernetes conformance testing via GitHub Actions.

## What

Runs [Sonobuoy](https://sonobuoy.io/) certified-conformance tests against a [kind](https://kind.sigs.k8s.io/) cluster on every push and PR.

## Workflow

- **Cluster**: kind v0.26.0, node image `kindest/node:v1.36.0`
- **Conformance**: Sonobuoy v0.57.3, `certified-conformance` mode
- **Timeout**: 120 minutes
- **Artifacts**: Results archive retained for 30 days

Triggered on push to `main`, PRs targeting `main`, or manually via `workflow_dispatch`.
