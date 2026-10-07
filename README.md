# Awesome-IoT-Fleet-Device-Management

## Top IoT Fleet & Device Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Over-the-Air Updates, Fleet Orchestration & Self-Hosted Device Management*  

**Last updated: October 2026**



This repository tracks notable **commercial IoT fleet management platforms** and **open-source projects** that provision, update, monitor, and secure connected device fleets at scale — from OTA software update engines to full device management platforms with remote access and telemetry.



**Examples** include AWS IoT Device Management, Particle Cloud, BalenaCloud, Memfault, Mender.io, Azure IoT Hub, Canonical Ubuntu Core, Tuya Smart, Esper, and Uptane (the category leaders).



**Open-source emphasis**: IoT fleet management is one of the strongest open-source domains. **Eclipse hawkBit** reached 1.0 in April 2026 after 84 contributors and nearly 4,000 commits, delivering production-ready OTA update infrastructure with multi-tenancy, staged rollouts, and mTLS security . **Mender** provides atomic A/B updates with automatic rollback and delta updates for embedded Linux . **NervesHub** is proven at 400,000+ devices per instance with signed OTA updates and remote console access . **Magistrala** (formerly Mainflux) offers a Go-based, cloud-native IoT framework with fine-grained access control . **NAOS** brings standardized remote management to ESP32 microcontrollers . **ThingsBoard** leads as the most popular open-source IoT platform with extensive data visualization and rule engine capabilities . This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AWS IoT Device Management](https://aws.amazon.com/iot-device-management/)**  

  **AWS's managed IoT fleet management** — onboard, organize, monitor, and remotely manage IoT devices at scale . **Fleet indexing, remote troubleshooting, and secure tunneling** . **Best for AWS-native IoT workloads** .



- **[Particle Cloud](https://www.particle.io/)**  

  **IoT platform for connected devices** — cellular and Wi-Fi modules with cloud connectivity, OTA updates, and device management . **Best for prototyping and production IoT** .



- **[BalenaCloud](https://www.balena.io/)**  

  **Container-based fleet management** — deploy and manage Docker containers across IoT devices . **OpenBalena** provides the open-source backend for self-hosting  . **Best for containerized IoT deployments** .



- **[Memfault](https://memfault.com/)**  

  **Embedded device observability** — monitor fleet health, diagnose crashes, and manage OTA updates . **Best for embedded engineering teams** .



- **[Mender.io](https://mender.io/)**  

  **Managed Mender** — end-to-end OTA software update manager with atomic updates and rollback . **Open-source server and client available for self-hosting**  . **Best for embedded Linux fleet management** .



- **[Azure IoT Hub](https://azure.microsoft.com/en-us/products/iot-hub/)**  

  **Microsoft's managed IoT platform** — device-to-cloud messaging, device management, and OTA updates . **Best for Azure-native IoT** .



- **[Canonical Ubuntu Core](https://ubuntu.com/core)**  

  **Ubuntu for IoT devices** — snap-based, transactional updates with full device management . **Best for Ubuntu-based IoT fleets** .



- **[Tuya Smart](https://www.tuya.com/)**  

  **IoT platform for smart devices** — device management, OTA updates, and app integration . **Best for consumer IoT** .



- **[Esper](https://esper.io/)**  

  **DevOps for dedicated devices** — remote debugging, OTA updates, and fleet management for Android and iOS devices . **Best for dedicated device fleets** .



- **[Uptane](https://uptane.org/)**  

  **Open-source security framework for automotive OTA updates** — designed to resist compromise of update servers . **Best for automotive and safety-critical OTA** .



## Open-Source GitHub Projects



### OTA Software Update Platforms



- **[Eclipse hawkBit](https://github.com/eclipse-hawkbit/hawkbit)**  

  **The open-source standard for IoT software updates, now production-ready at 1.0**, EPL 2.0 licensed with **84 contributors, 2,442 pull requests, and nearly 4,000 commits**  . **Domain-independent back-end framework for rolling out software updates** to constrained edge devices, powerful gateways, and everything in between . **Three integration APIs**: DDI (REST/HTTP) for direct device polling, DMF (AMQP/RabbitMQ) for gateway-managed devices, and Management REST API for orchestration . **Enterprise-grade operations**: multi-tenancy with tenant isolation, cascading rollout groups with success/error thresholds and emergency shutdown, approval workflows, and fine-grained RBAC  . **Security at every layer**: per-device tokens, gateway tokens, mTLS, OAuth 2.0/OIDC, and entity-level access control . **Deployment flexibility**: monolith or microservices with Spring Cloud . **Commercial validation**: Bosch IoT Rollouts and Kynetics Update Factory built on hawkBit  . **Best for production OTA update infrastructure** .



- **[Mender](https://github.com/mendersoftware/mender)**  

  **End-to-end open-source OTA software update manager for embedded Linux devices**, Apache-2.0 licensed . **Atomic A/B partition updates with automatic rollback** — writes new image to inactive partition, swaps on next boot; if update fails, rolls back automatically  . **Delta updates** minimize bandwidth by sending only binary diffs . **Code signing, compression, and phased rollouts** reduce risk . **Update Modules** enable flexible update types (single file, script, Docker container)  . **Pull-based architecture** — devices poll for updates, ideal for NAT'ed and cellular connections . **Proven in production**: gridX uses Mender for their gridBox IoT devices with Yocto builds  . **Best for atomic, reliable embedded Linux updates** .



- **[NervesHub](https://github.com/nerves-hub/nerves_hub_web)**  

  **Open-source platform for secure OTA firmware updates and fleet management of Nerves-based IoT devices**, Apache-2.0 licensed . **Proven at 400,000+ devices per instance**  . **Cryptographically signed firmware** — devices reject tampered or corrupted images . **Deployment groups** target devices by tag and version with configurable concurrency and failure thresholds . **Remote console** — connect to live IEx session or shell without VPN or physical access . **Fleet health monitoring** — track CPU, memory, load, and custom metrics . **Delta updates via xdelta3** for constrained connections . **Flexible authentication**: Shared Secret, X.509 mTLS, or NervesKey hardware-backed security . **Best for Nerves/Elixir IoT device fleets** .



- **[SWUpdate](https://github.com/sbabic/swupdate)**  

  **Linux embedded update agent**, GPL-2.0 licensed . **Supports multiple update strategies** — A/B, recovery, and delta updates . **Integrates with hawkBit via hara-ddiclient**  . **Best for embedded Linux OTA** .



- **[RAUC](https://github.com/rauc/rauc)**  

  **Safe and secure update framework for embedded Linux**, LGPL-2.1 licensed . **A/B updates with atomic switching and rollback** . **Integrates with hawkBit via rauc-hawkbit-updater** (C) or rauc-hawkbit (Python)  . **Best for embedded Linux OTA** .



### Full IoT Device Management Platforms



- **[ThingsBoard](https://github.com/thingsboard/thingsboard)**  

  **The most popular open-source IoT platform with 17,000+ GitHub stars**, Apache-2.0 licensed . **Device management, data collection, processing, and visualization**  . **Rule Engine for event-based workflows** — trigger actions on device data, alarms, and schedules . **Multi-tenancy with RBAC** — manage multiple organizations from one instance . **Supports MQTT, CoAP, HTTP, LwM2M, SNMP** with dashboards and device management  . **Security**: Two-Factor Authentication, OAuth 2.0, Access Tokens, X.509 Certificates, SSL, DTLS  . **Trade-offs**: Can be resource-heavy; Community edition lacks many Professional features  . **Best for comprehensive IoT platform with visualization** .



- **[Magistrala](https://github.com/absmach/magistrala)**  

  **Modern, Go-based, cloud-native IoT platform framework** (formerly Mainflux), Apache-2.0 licensed . **Small number of main concepts**: users, devices, channels, messages, policies — familiar to most engineers  . **Atom integration model** provides identity, authorization, and catalog with workspaces (tenants), entities, resources, and groups  . **Fine-grained access control** — define object-scoped roles like "reader on channel1"  . **Scales from simple prototypes to complex deployments** without rigid patterns . **Trade-offs**: No built-in dashboard (available via plugins); community support still catching up to Java-based platforms  . **Best for high-performance, cloud-native IoT core** .



- **[OpenRemote](https://github.com/openremote/openremote)**  

  **100% open-source IoT platform for smart environments**, AGPL-3.0 licensed . **Rich capabilities focused on support and management of smart environments**  . **Supports HTTP, SNMP, MQTT, Bluetooth, Serial, TCP, UDP, Z-wave, KNX, Velbus**  . **Data visualization, device management, Android/iOS push notifications** . **Keycloak with OAuth 2.0 and TLS/SSL** for security  . **Trade-offs**: Support must be paid; completely open source but commercial support tiers available  . **Best for smart building and environment management** .



### Microcontroller Fleet Management



- **[NAOS (Networked Artifacts Operating System)](https://github.com/256dpi/naos)**  

  **Open-source collection of protocols, libraries, and tools for building highly interactive smart devices with standardized remote management**, Apache-2.0 licensed  . **Primarily targets ESP32 family** — based on Espressif's ESP-IDF framework . **Out-of-the-box features**: configuration parameters, multi-dimensional metrics, file-system access, remote firmware update, device provisioning, sub-device relaying, password protection, coredump extraction, live log tailing  . **Connectivity layers**: WiFi, Ethernet, BLE, MQTT (with reverse-channel), mDNS discovery, HTTP/WS server and client, Serial, OSC, Relay  . **Tools**: `naos` CLI for project management, `naos-explorer` TUI/desktop app for inspection, `naos-fleet` CLI for fleet management  . **SDKs**: Go, TypeScript (NAOS.js), Swift (NAOSKit)  . **Best for ESP32 fleet management with standardized protocols** .



- **[Mongoose OS](https://github.com/cesanta/mongoose-os)**  

  **IoT firmware development framework with OTA and remote management**, Apache-2.0 (Community) licensed  . **Supported MCUs**: CC3220, CC3200, ESP32, ESP8266, STM32F4, STM32L4, STM32F7  . **Features**: OTA firmware updates with rollback, flash encryption, crypto chip support, ARM mbedTLS, device management dashboard  . **Built-in integration** for AWS IoT, Google IoT Core, Microsoft Azure, Adafruit IO, generic MQTT  . **Code in C or JavaScript** (embedded mJS engine)  . **Best for rapid IoT firmware development** .



### Additional Strong Open-Source Options



- **OpenBalena** — Open-source backend for Balena device fleet management (core API only; no UI)  . **Best for self-hosted Balena deployments** .

- **Balena Admin** — Community-maintained admin dashboard for OpenBalena  .

- **Pantavisor** — Lightweight LXC-based runtime for embedded Linux with atomic signed state revisions, kernel included as a container, ~1 MB footprint  . **Best for resource-constrained devices** .

- **Mender MCU** — Mender client for microcontrollers  .

- **Qbee.io** — Device agent for IoT device management platform  .



**Frameworks for building custom IoT fleet management solutions**: Combine **Eclipse hawkBit** for production-grade OTA update infrastructure with multi-tenancy and staged rollouts  . Use **Mender** for atomic embedded Linux updates with automatic rollback and delta updates  . Deploy **NervesHub** for Nerves/Elixir device fleets with signed firmware and remote console access  . Choose **ThingsBoard** for comprehensive IoT platform with dashboards and rule engine  . Integrate **Magistrala** for Go-based, cloud-native IoT core with fine-grained access control  . Use **NAOS** for ESP32 fleet management with standardized protocols  . Note that true enterprise IoT fleet management with managed infrastructure, global scale, and vendor-supported SLAs (AWS IoT, Particle, BalenaCloud) remains primarily commercial territory; open-source stacks provide strong OTA, device management, and fleet orchestration foundations that require integration for complete IoT fleet operations.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- IoT fleet management platforms handle device credentials and may control physical devices. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.

- **OTA updates are security-critical** — unsigned or unverified firmware updates are a major attack vector. Eclipse hawkBit, Mender, and NervesHub all provide cryptographic signing and verification  .

- **Atomic updates with rollback are essential** for devices in remote locations — Mender's A/B partition approach ensures devices never brick  .

- **License considerations**: hawkBit uses EPL 2.0, Mender uses Apache-2.0, NervesHub uses Apache-2.0, ThingsBoard uses Apache-2.0, Magistrala uses Apache-2.0, and NAOS uses Apache-2.0. Verify licensing against your use case before committing.

- The open-source ecosystem provides strong OTA, device management, and fleet orchestration foundations, but **managed infrastructure, global scale, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for IoT engineers, embedded developers, and organizations seeking IoT fleet management sovereignty.**  

Let's make IoT fleet and device management more open, transparent, and secure.
