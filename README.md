# neoCTL

<p align="center">
  <img src="https://img.shields.io/badge/Go-1.21+-00ADD8?style=for-the-badge&logo=go" alt="Go Version">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version">
</p>

<p align="center">
  <strong>A modern orchestration and management platform for virtual infrastructure</strong>
</p>

<p align="center">
  Automate provisioning, configuration, and monitoring of VMs across multiple hypervisors (Proxmox, KVM, VyOS) with integrated DNS and storage support.
</p>

<p align="center">
  <a href="https://neoctl.shivamsancc.com">🌐 Website</a> •
  <a href="#installation">📦 Installation</a> •
  <a href="#documentation">📚 Documentation</a> •
  <a href="#contributing">🤝 Contributing</a>
</p>

---

## ✨ Features

* 🔧 **Multi-Hypervisor Support** - Manage VMs across Proxmox, KVM, and VyOS nodes
* ⚡ **Automated Orchestration** - Simplify VM lifecycle operations
* 🌐 **DNS Management** - Cloudflare & PowerDNS integration
* 💾 **Storage Management** - MinIO & NFS support
* 📊 **Monitoring & Logging** - Centralized logging & infrastructure monitoring
* 🚀 **API & CLI Ready** - Fully scriptable for automation workflows

## 🏗️ Architecture

User Request → neoCTL API → Orchestrator → Hypervisor Providers (Proxmox, KVM, VyOS)
↓
Storage / DNS / Networking

### System Layers

| Layer              | Description                                 |
| ------------------ | ------------------------------------------- |
| **Controller**     | Handles API requests & routes to services   |
| **Service**        | Core logic for VM, storage, networking, DNS |
| **Providers**      | Hypervisor & service integrations           |
| **Core Utilities** | Logging, validation, error handling         |

## 📋 Requirements

* Go >= 1.21
* Git
* Access to Proxmox, KVM, VyOS servers
* Docker (optional, for local development)

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/neoctl/neoctl-server.git
cd neoctl-server

# Initialize Go modules
go mod tidy

# Build the server
go build -o neoctl cmd/server/main.go

# Run the server
./neoctl
```

## 📁 Directory Structure

```
neoctl-server/
├── cmd/server/           # Entry point
├── internal/
│   ├── config/           # Configuration
│   ├── database/         # DB & migrations
│   ├── models/           # Data models
│   ├── providers/        # Hypervisor/service implementations
│   ├── services/         # Core business logic
│   ├── controllers/      # API controllers
│   ├── router/           # API routing
│   └── core/             # Utilities: errors, logger, validator
├── pkg/                  # Public packages
├── scripts/              # Deployment & migration scripts
├── configs/              # YAML config files
├── docs/                 # Documentation
└── docker/               # Dockerfiles & docker-compose
```

## 📚 Documentation

For detailed documentation, visit: [https://neoctl.shivamsancc.com](https://neoctl.shivamsancc.com)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/YourFeature`)
3. **Commit** your changes (`git commit -m 'Add new feature'`)
4. **Push** to the branch (`git push origin feature/YourFeature`)
5. **Open** a Pull Request

## 📄 License

MIT License © 2025 Shivam Sancc

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

* 🐛 **Issues**: [GitHub Issues](https://github.com/neoctl/neoctl-server/issues)
* 🌐 **Website**: [https://neoctl.shivamsancc.com](https://neoctl.shivamsancc.com)
* 👨‍💻 **Author**: Shivam Sancc

---

<p align="center">
  <strong>Built for modern infrastructure teams who demand simplicity without sacrificing power.</strong>
</p>

<p align="center">
  Made with ❤️ by <a href="https://github.com/shivamsancc">Shivam Sancc</a>
</p>
