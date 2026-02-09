# Cluster API (CAPI) Hands-on Lab: From Management to Workload
This repository documents my practical experience setting up a Kubernetes multi-cluster environment using Cluster API. The goal was to understand the lifecycle of a workload cluster and how the management cluster orchestrates infrastructure via providers.

Technical Stack
- Management Cluster: kind (Kubernetes in Docker)
- Infrastructure Provider: CAPD (Cluster API Provider Docker)
- Bootstrap Provider: Kubeadm
- Orchestration Tool: clusterctl

Key Achievements & Troubleshooting
- Initialized Management Cluster: Successfully transformed a local kind cluster into a CAPI Management Plane.
- Feature Gate Debugging: Enabled the ClusterTopology feature gate within the management cluster to support modern Cluster object structures.
- Workload Provisioning: Created a "Vanilla" Kubernetes workload cluster using Docker containers as nodes.
- Node Readiness: Diagnosed and resolved node NotReady states by verifying CNI requirements and control plane initialization.

What I Learned
- Through this lab, I gained a deep understanding of how CAPI handles the reconciliation loop. This experience is directly applicable to CAPA, as I now understand how the management plane uses image metadata (AMIs in AWS vs. Docker Images in CAPD) to build healthy workload nodes.
