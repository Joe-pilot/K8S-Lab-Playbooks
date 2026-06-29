# K8S Lab Playbooks

AWX-friendly Ansible automation repository for a Kubernetes lab.

Execution order:
1. playbooks/01-node-setup.yml
2. playbooks/02-cluster-init.yml
3. playbooks/03-join-control-plane.yml
4. playbooks/04-join-workers.yml
5. playbooks/05-labels-taints.yml
6. playbooks/06-os-patching.yml

AWX objects:
- Inventory: Kubernetes Lab
- Credential: K8S Lab SSH
- Project: K8S Lab Playbooks
- Branch: main

Important:
- `05-labels-taints.yml` runs on `k8s-cp-01`, not localhost.
- Join playbooks require AWX Surveys.
