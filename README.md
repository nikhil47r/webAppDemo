
- Dockerfile contained root user (fixed)
- Image scan showed 2 high CVEs (patched dependencies)
- Secrets were hardcoded (moved to K8s secrets)


- Used Alpine image + multi-stage Docker build
- Semgrep + Trivy integrated in GitHub Actions
- Only push images if passing security gates
- Secrets are loaded from Kubernetes Secrets
- IaC scanned using tfsec


- Enable runtime protection with Falco
- Apply Network Policies to isolate workloads
- Use signed images (Cosign)
- Add Pod Security Policies or OPA/Gatekeeper
