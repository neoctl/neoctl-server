# neoCTL

> \[!CAUTION]
> neoCTL is currently in active development. Some features may be unstable or subject to change.
> Please test thoroughly in non-production environments before deploying to production.

<a href="https://neoctl.shivamsancc.com">![neoctl.shivamsancc.com](https://img.shields.io/badge/site-neoctl.shivamsancc.com-00A1FF?style=flat-square)</a> <a href="https://neoctl.shivamsancc.com/docs/">![Docs](https://img.shields.io/badge/docs-00A1FF?style=flat-square)</a> <a target="_blank" href="https://discord.gg/neoctl"><img src="https://dcbadge.limes.pink/api/server/neoctl?style=flat" alt="discord community" /></a>
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
![GitHub Sponsor](https://img.shields.io/github/sponsors/shivamsancc?label=Sponsors\&logo=GitHub)

### What is neoCTL?

neoCTL is an open-source, modern orchestration and management platform for virtual infrastructure. Built for scalability and efficiency, it automates provisioning, configuration, and monitoring of VMs across multiple hypervisors (Proxmox, KVM, VyOS) with integrated DNS and storage support. It delivers simplified infrastructure management while maintaining enterprise-grade reliability.

<!-- ## Get started

### Setting up neoCTL with Docker

The easiest way to get started with neoCTL is using [Docker](https://www.docker.com/) by running the following command.

```bash
$ docker run -p 8080:8080 neoctl/neoctl-server:latest
```

The above command will start the neoCTL server running locally on port `8080` and you can connect to it using the neoCTL CLI and SDKs.

> \[!NOTE]
> If you are looking to setup neoCTL for development or want to setup from source, refer to our [CONTRIBUTING.md](CONTRIBUTING.md) guide. -->

### Setting up from Source

```bash
$ git clone https://github.com/neoctl/neoctl-server.git
$ cd neoctl-server

$ go mod tidy

$ go build -o neoctl cmd/server/main.go

$ ./neoctl
```

## Setting up CLI

### Using cURL

The best way to connect to neoCTL is using the neoCTL CLI and you can install it by running the following command:

```bash
$ sudo su
$ curl -sL https://raw.githubusercontent.com/neoctl/neoctl-cli/main/install.sh | sh
```

If you are working on an unsupported OS (as per above script), you can always follow the installation instructions mentioned in the [neoctl/cli](https://github.com/neoctl/neoctl-cli) repository.

> \[!NOTE]
> If you are looking to setup neoCTL for development or want to setup from source, refer to our [CONTRIBUTING.md](CONTRIBUTING.md) guide.

## Want to contribute?

The Code Contribution Guidelines are published at [CONTRIBUTING.md](CONTRIBUTING.md); please read them before you start making any changes. This would allow us to have a consistent standard of coding practices and developer experience.

Contributors can join the [Discord Server](https://discord.gg/neoctl) for quick collaboration.

## Sponsors

We are incredibly grateful to our sponsors for their generous support, which makes the development of neoCTL possible.

<a href="https://www.coderabbit.ai/?utm_source=github&utm_medium=social&utm_campaign=sponsor&utm_term=dicedb">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://www.coderabbit.ai/images/logo-white.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://www.coderabbit.ai/images/logo-orange.svg">
    <img alt="CodeRabbit" src="https://www.coderabbit.ai/images/logo-orange.svg">
  </picture>
</a>

## Support and Sponsor Us

neoCTL is a project with a strong vision and [roadmap](https://neoctl.shivamsancc.com/roadmap/). If you like what we do and find neoCTL useful, please consider supporting and [sponsoring us on GitHub](https://github.com/sponsors/shivamsancc).

![GitHub Sponsor](https://img.shields.io/github/sponsors/shivamsancc?label=Sponsors\&logo=GitHub)

## Contributors

<a href="https://github.com/neoctl/neoctl-server/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=neoctl/neoctl-server"/>
</a>

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/shivamsancc">Shivam Sancc</a>
</p>
