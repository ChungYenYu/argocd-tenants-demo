# argocd-tenants-demo

> GitOps source for [`20260527-argocd-appset-flagger`](https://github.com/ChungYenYu/20260527-argocd-appset-flagger) lab.

Each `tenants/<id>/` is a self-contained Helm chart deploying:
- podinfo Deployment + Service
- Flagger Canary (progressive 10→25→50%, success-rate ≥ 99%)

ArgoCD ApplicationSet watches `tenants/*` — add a new dir → new tenant auto-onboarded in ≤60 s.
