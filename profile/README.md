# nıu Communications Platform

[Deutsch](README.de.md) | **English**

**Open communication infrastructure. Built to be owned.**

The **nıu Communications Platform** is an open communication platform for teams that need reliable voice communication – initially with a clear focus on **live production, broadcast, events and small production teams**.

The project combines dedicated communication hardware with open standards, self-hosted infrastructure and optional managed services.

Our goal is not to build another closed intercom system.

We want to build a platform that can be **bought, understood, modified, self-hosted and further developed**.

> **Dedicated hardware. Open infrastructure. Your network. Your choice.**

The **German version is the canonical source** for the project's description and principles. This English version is maintained as a translation for collaboration, exchange and an international community. In case of discrepancies, the German version prevails.

---

## The idea

Professional intercom systems work extremely well – but they are often expensive, proprietary and tightly coupled to a vendor ecosystem.

Software-based communication systems, on the other hand, are flexible and affordable, but often rely on smartphones, computers or improvised hardware in practical use.

The nıu Communications Platform aims to combine the strengths of both approaches:

- dedicated, robust communication hardware
- physical push-to-talk controls
- communication over standard IP and Wi-Fi networks
- open software and documented interfaces
- local and fully self-hosted infrastructure
- optional managed cloud infrastructure
- no technical dependency on a vendor cloud

The starting point is a device that feels like a traditional intercom beltpack while being part of an open IP communication platform underneath.

## One device. Three deployment models.

The platform should not dictate where its communication infrastructure has to run.

### Bare

The device connects to an existing or self-hosted compatible server infrastructure.

**Buy the hardware. Run your own server. Done.**

No nıu server or cloud subscription is required.

### Base

**nıu Base** provides the devices with a local, preconfigured communication instance.

Communication can remain entirely within the local network and continue to operate independently of an Internet connection.

Base combines the control of self-hosting with the convenience of an appliance.

### Cloud

**nıu Cloud** provides the required communication infrastructure as a managed service operated by us.

Devices can be deployed without operating a dedicated server and can communicate across the Internet.

Cloud is the most convenient deployment model – but **it is not a requirement for using the platform**.

## One platform, multiple products

The underlying technology is intentionally designed to support more than one use case.

### Production

Our first focus.

**nıu Production** targets small and medium-sized teams working in:

- live production
- streaming
- broadcast
- events
- theatre
- film and video production
- mobile production environments

The first nıu beltpack is being developed for this environment.

### Operations

The same technical foundation may later serve operational teams that need straightforward, dedicated group communication over IP networks.

Their requirements and user experience may look very different from Production – while sharing the same platform underneath.

### Love

**nıu Love** explores a deliberately different use case: an extremely simple physical communication link between a small number of people.

Love is not merely another Production beltpack configuration. It represents a separate product concept built on the same open communication platform.

## Why Mumble?

We do not intend to reinvent a voice stack where a mature open solution already exists.

The platform uses **Mumble/Murmur** as its communication foundation and builds the components around it that turn a general-purpose VoIP system into a dedicated communication platform:

```text
┌─────────────────────────────────────┐
│          nıu Applications           │
│ Production · Operations · Love      │
├─────────────────────────────────────┤
│        nıu Device Platform          │
│ UI · PTT · Audio · Provisioning     │
├─────────────────────────────────────┤
│       Communication Layer           │
│          Mumble / Murmur            │
├─────────────────────────────────────┤
│        Standard IP Networks         │
│       Wi-Fi · LAN · Internet        │
└─────────────────────────────────────┘
```

There is no reason to reinvent the wheel where a proven open protocol already exists.

Development can therefore focus on hardware, user interaction, provisioning, management, integration and reliable operation.

## Open source by architecture

Open source is not intended to be an afterthought or merely the publication of selected software components.

The platform is designed to be **reproducible and independently operable**.

This is intended to include:

- hardware and PCB designs
- device software
- Base/server components
- provisioning and management
- documented protocols and APIs
- reproducible build and deployment processes

A third party should be able to build a compatible system using its own infrastructure and its own **trust domain**.

Our principle is:

**Open source means implementation freedom – not inheriting the nıu identity or nıu trust.**

Official nıu hardware, firmware and services use cryptographic trust roots controlled by nıu. Independent operators can use the same open source implementation with their own keys, infrastructure and trust roots.

This allows the platform to remain open without sacrificing the authenticity of official components.

## No cloud lock-in

One of the core architectural principles is:

> **The cloud is a service, not a dependency.**

Users who want nıu Cloud should receive a convenient managed solution.

Users who do not want it should still be able to operate the platform meaningfully and independently.

The managed service therefore has to compete through **convenience, operation, availability, support and integration** – not by artificially restricting hardware outside the cloud.

## Hardware designed to become a product

This project is explicitly more than a software experiment.

The beltpack is being developed with an actual manufacturable product in mind:

- dedicated PTT controls
- integrated audio
- external headset and audio-device connectivity
- Wi-Fi/IP communication
- display and status indication
- battery operation and continuous powered operation
- robust and serviceable construction
- scalable manufacturing and automated end-of-line testing
- provisioning and secure device identity
- OTA updates, recovery and diagnostics
- regulatory compliance and certification

Even early hardware decisions are therefore evaluated against whether the device can eventually be manufactured reproducibly at scale rather than assembled successfully once on a workbench.

## Architectural principles

Several principles already guide development:

- **Complexity on the inside, simplicity on the outside.** The device should remain easy to use even when a capable platform operates underneath.
- **Capability ≠ Feature.** The technical platform may expose more capability than the normal user interface needs to show.
- **Hardware creates possibilities; software decides later which of them are used.** Expensive hardware lock-ins should be avoided early.
- **Identity lives on the carrier. Configuration belongs to deployment. Runtime state belongs to the compute module.** Replaceable components should not unnecessarily define device identity.
- **Reality beats configuration.** The system should distinguish between desired state and the hardware or connectivity actually available.
- **Open source means implementation freedom, not inherited trust.** Independent builds and independent trust domains are intentional parts of the architecture.

The technical background and decisions are documented in the [`architecture`](https://github.com/niu-Communications-Platform/architecture) repository.

## Repository structure

The GitHub organization is intended to represent the platform through clearly separated areas of responsibility:

```text
nıu Communications Platform/
├── architecture       # system architecture, specifications and ADRs
├── beltpack           # hardware and device software
├── base               # local/on-premises platform
├── cloud              # hosted platform
└── factory-tools      # manufacturing, EOL and provisioning tools
```

Not all repositories exist yet. They will be created as practical development of the respective components begins.

## Current status

🚧 **Early development / architecture and prototyping**

Our present focus is:

**Production → Beltpack → local communication → robust hardware → reproducible platform**

Early prototypes and existing open-source components are being used to validate the architecture, hardware and interaction model in real-world environments.

The project is deliberately not being completely frozen on the drawing board. Before the first hardware prototype, the main focus is on decisions that could create expensive hardware lock-ins later. Other questions will be measured on the prototype and decided based on practical results.

Interfaces, hardware designs and architectural decisions may change significantly during this phase.

Technical discussion, constructive criticism and future contributions from the community are explicitly welcome.
