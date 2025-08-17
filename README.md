========================================================
                          neoCTL
========================================================

A modern orchestration and management platform for virtual infrastructure.
Automate provisioning, configuration, and monitoring of VMs across multiple
hypervisors (Proxmox, KVM, VyOS) with DNS and storage integration.

Website: https://neoctl.shivamsancc.com
Author: Shivam Sancc
Year: 2025
License: MIT

--------------------------------------------------------
Features
--------------------------------------------------------
✔ Multi-Hypervisor Support: Manage VMs across Proxmox, KVM, VyOS nodes.
✔ Automated Orchestration: Simplify VM lifecycle operations.
✔ DNS Management: Cloudflare & PowerDNS integration.
✔ Storage Management: MinIO & NFS support.
✔ Monitoring & Logging: Centralized logging & infrastructure monitoring.
✔ API & CLI Ready: Fully scriptable for automation workflows.

--------------------------------------------------------
Architecture
--------------------------------------------------------
User Request → neoCTL API → Orchestrator → Hypervisor Providers (Proxmox, KVM, VyOS)
                                      ↓
                             Storage / DNS / Networking

Layers:
- Controller: Handles API requests & routes to services.
- Service: Core logic for VM, storage, networking, DNS.
- Providers: Hypervisor & service integrations.
- Core Utilities: Logging, validation, error handling.

--------------------------------------------------------
Installation
--------------------------------------------------------
Prerequisites:
- Go >= 1.21
- Git
- Access to Proxmox, KVM, VyOS servers
- Optional: Docker (for local development)

Steps:

1. Clone the repository:
   git clone https://github.com/neoctl/neoctl-server.git
   cd neoctl-server

2. Initialize Go modules:
   go mod tidy

3. Build the server:
   go build -o neoctl cmd/server/main.go

4. Run the server:
   ./neoctl

--------------------------------------------------------
Directory Structure
--------------------------------------------------------
neoctl-server/
|
├─ cmd/server/           # Entry point
├─ internal/
│  ├─ config/            # Configuration
│  ├─ database/          # DB & migrations
│  ├─ models/            # Data models
│  ├─ providers/         # Hypervisor/service implementations
│  ├─ services/          # Core business logic
│  ├─ controllers/       # API controllers
│  ├─ router/            # API routing
│  └─ core/              # Utilities: errors, logger, validator
├─ pkg/                  # Public packages
├─ scripts/              # Deployment & migration scripts
├─ configs/              # YAML config files
├─ docs/                 # Documentation
└─ docker/               # Dockerfiles & docker-compose

--------------------------------------------------------
Contributing
--------------------------------------------------------
Contributions are welcome! Please fork and submit pull requests.

1. Fork the repo
2. Create a branch (git checkout -b feature/YourFeature)
3. Commit changes (git commit -m 'Add new feature')
4. Push branch (git push origin feature/YourFeature)
5. Open a Pull Request

--------------------------------------------------------
License
--------------------------------------------------------
MIT License © 2025 Shivam Sancc

--------------------------------------------------------
Contact
--------------------------------------------------------
GitHub Issues: https://github.com/neoctl/neoctl-server/issues
Website: https://neoctl.shivamsancc.com
