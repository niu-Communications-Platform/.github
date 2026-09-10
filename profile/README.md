# nıu Communications Platform

[Deutsch](README.de.md) | **English**

**Open communication infrastructure. Built to be owned.**

The **nıu Communications Platform** – short **nıu.cp** – is an open communication platform for teams that need reliable voice communication – initially with a clear focus on **live production, broadcast, events and small production teams**.

The project combines dedicated communication hardware with open standards, self-hosted infrastructure and optional managed services.

Our goal is not to build another closed intercom system.

We want to build a platform that can be **bought, understood, modified, repaired, self-hosted and further developed**.

> **Dedicated hardware. Open infrastructure. Your network. Your choice.**

The **[German version](README.de.md) is the canonical source** for the project's description and principles. This English version is maintained as a translation for collaboration, exchange and an international community. In case of discrepancies, the German version prevails.

---

## The idea

Professional intercom systems work extremely well – but they are often expensive, proprietary and tightly coupled to a vendor ecosystem.

Software-based communication systems, on the other hand, are flexible and affordable, but often rely on smartphones, computers or improvised hardware in practical use.

The nıu Communications Platform aims to combine the strengths of both approaches:

- dedicated, robust communication hardware
- physical push-to-talk controls
- communication over standard IP and Wi-Fi networks
- Mumble/Murmur as the open native voice foundation
- SIP as a planned interoperability layer
- open software, documented interfaces and open hardware
- local and fully self-hosted infrastructure
- optional managed cloud infrastructure
- no technical dependency on a vendor cloud
- repairable, understandable hardware documentation
- an end-user-replaceable battery
- an optional secondary Sub-GHz/LoRa resilience path for small status and control messages independent of the primary IP audio path

The starting point is a device that feels like a traditional intercom beltpack while being part of an open IP communication platform underneath.

## What should make nıu.cp different

nıu.cp is not intended to become just a Mumble client in a custom enclosure. The platform is being developed as a complete product and system concept:

- **Mumble-native, SIP-interoperable.** The real-time voice path builds on Mumble/Murmur; SIP is intended where interoperability with existing communication systems is useful.
- **IP for voice, an additional resilience path for small critical information.** A secondary Sub-GHz radio path is being investigated for presence, status, call/alarm signalling, tally and recovery messages. A local Direct-LoRa star between beltpacks and Base is currently the strongest protocol candidate. This path is explicitly **not a second audio transport** and is not yet a final architecture decision.
- **Replaceable compute, persistent carrier identity.** Compute modules, operating systems and runtime software should be replaceable or evolvable without unnecessarily tying the physical device identity to them.
- **Replaceable battery instead of a sealed wear part.** The end user should be able to exchange the battery pack; cell protection and BMS remain the responsibility of a production-ready supplier pack.
- **Cloud convenience without cloud dependency.** Bare, Base and Cloud should share the same device and protocol foundations wherever practical.
- **Openness includes diagnostics and repair.** Official nıu trust roots remain protected while hardware, software, diagnostics and repair remain understandable wherever legally and technically possible.

## Openness that does not stop at access

The platform should not only be open in the sense that source code, schematics or interfaces can theoretically be inspected.

Our ambition goes further:

**Open Source → Open Hardware → Open Diagnostics → Open Repair Documentation → Open Understanding**

A nıu.cp device should not only be usable, repairable and modifiable. A curious owner should have a real opportunity to **understand how it works**.

That means technical documentation should, wherever practical and legally possible, not stop at source code, schematics and repair instructions. It should also explain:

- What does a subsystem do?
- Why does it exist?
- How does it interact with other parts of the device?
- Why was this architecture chosen?
- What concrete problem does a particular component solve or prevent?

We deliberately distinguish between two documentation layers:

**Engineering & Repair Reference** is aimed at developers, professional repair shops and experienced makers. This is where schematics, BOMs, pinouts, test points, diagnostic procedures, test processes and repair information belong.

**Inside nıu.cp** is intended to guide technically curious users, makers, learners and career changers from product-level understanding towards the actual engineering implementation.

The didactic sequence is:

**Product purpose → architectural understanding → engineering detail**

Technical terms are not avoided; they are explained.

> **Open Hardware does not only mean: you may look inside. Open Understanding means: we help you understand what you see.**

Our goal is a product that combines **polished everyday usability with genuine technical ownership and developer freedom**.

## One device. Three deployment models.

The platform should not dictate where its communication infrastructure has to run.

### Bare

The device connects to an existing or self-hosted compatible server infrastructure.

**Buy the hardware. Run your own server. Done.**

No nıu server or cloud subscription is required.

### Base

**nıu Base** provides the devices with a local, preconfigured communication instance.

Voice communication can remain entirely within the local network and continue to operate independently of an Internet connection. In the future, Base may also provide local infrastructure for additional device capabilities such as the secondary resilience/control path.

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

The first **nıu.cp beltpack** is being developed for this environment.

### Operations

The same technical foundation may later serve operational teams that need straightforward, dedicated group communication over IP networks.

Their requirements and user experience may look very different from Production – while sharing the same platform underneath.

### Love

**nıu Love** explores a deliberately different use case: an extremely simple physical communication link between a small number of people.

Love is not merely another Production beltpack configuration. It represents a separate product concept built on the same open communication platform.

## Why Mumble?

We do not intend to reinvent a voice stack where a mature open solution already exists.

The platform uses **Mumble/Murmur** as its native communication foundation and builds the components around it that turn a general-purpose VoIP system into a dedicated communication platform. **SIP is planned as an interoperability layer, not as a replacement for the native Mumble model.**

```text
┌────────────────────────────────────────┐
│            nıu Applications            │
│     Production · Operations · Love     │
├────────────────────────────────────────┤
│          nıu Device Platform           │
│   UI · PTT · Audio · Provisioning      │
├────────────────────────────────────────┤
│        Communication / Interop          │
│       Mumble / Murmur · SIP bridge      │
├────────────────────────────────────────┤
│           Standard IP Networks         │
│          Wi-Fi · LAN · Internet        │
└────────────────────────────────────────┘
          ║
          ║ optional independent
          ║ low-bandwidth resilience/control
          ▼
      Sub-GHz / LoRa candidate
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

Official nıu hardware, firmware and services use cryptographic trust roots controlled by nıu. Independent operators can use the same open implementation with their own keys, infrastructure and trust roots.

This allows the platform to remain open without sacrificing the authenticity of official components.

## No cloud lock-in

One of the core architectural principles is:

> **The cloud is a service, not a dependency.**

Users who want nıu Cloud should receive a convenient managed solution.

Users who do not want it should still be able to operate the platform meaningfully and independently.

The managed service therefore has to compete through **convenience, operation, availability, support and integration** – not by artificially restricting hardware outside the cloud.

## Hardware designed to become a product

This project is explicitly more than a software experiment.

The beltpack is being developed with an actual manufacturable product in mind. The current physical working model explores a **105 × 70 mm Core Body** with a side-mounted partially recessed replaceable battery pack, large PTT on the opposite side and a free rear surface for the belt clip. This geometry is not yet a production freeze, but it is substantially more concrete than an abstract concept.

Planned or actively investigated capabilities include:

- dedicated PTT controls
- internal microphone and speaker
- separate MIC/PHONES connectors and TRRS headset support
- USB Audio and planned Bluetooth Audio
- Wi-Fi/IP communication
- optional secondary Sub-GHz/LoRa resilience path
- display, physical VOL±/CH±/MENU/BACK controls and status indication
- two USB-C interfaces for POWER and ACCESSORY; mechanical placement is also being developed with a possible docking solution in mind
- replaceable battery pack and operation from sufficient external power
- robust and serviceable construction
- secure device identity separated from the compute module
- scalable manufacturing and automated end-of-line testing
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
- **Prototype = measurement instrument.** Open engineering questions should be measured reproducibly on prototypes rather than optimized only in theory.

## Development documentation

Technical background, architecture decisions, experiments and validation plans are already maintained systematically in separate repositories.

During the early product-development phase, these repositories are **intentionally still private**. The public organization profile therefore describes the current project idea and core principles directly, without linking to documents that external visitors cannot access.

As the project matures, suitable technical documentation, hardware designs, software and development resources are intended to become public step by step.

## Repository structure

The GitHub organization is intended to represent the platform through clearly separated areas of responsibility:

```text
nıu Communications Platform/
├── architecture        # system architecture, specifications and ADRs
├── beltpack            # hardware and device software
├── base                # local/on-premises platform
├── cloud               # hosted platform
├── factory-tools       # manufacturing, EOL and provisioning tools
└── product-development # questions, experiments and findings during development
```

The development repositories are currently private and will evolve as practical development of the respective components continues.

## Current status

🚧 **Active architecture validation and prototype preparation**

Our present focus is:

**Production → nıu.cp Beltpack → local communication → robust hardware → reproducible platform**

Several important architecture decisions are already established, including carrier-based device identity, Mumble as the native voice protocol with SIP interoperability, separated open trust domains and the end-user-replaceable battery pack. Other points deliberately remain under active validation, especially compute selection, compute-independent USB-audio integration, Secondary Sub-GHz/LoRa, RF/antenna behaviour, the battery dock, mechanics and series manufacturing.

The current strongest mechanical working model uses a 105 × 70 mm Core Body with a side-mounted battery pack. For the additional resilience path, a local Direct-LoRa star using an independent MCU/radio is being investigated as a serious V1 candidate. Neither is a final product freeze yet.

The project is deliberately not being completely frozen on the drawing board. Decisions with high hardware lock-in risk are validated early; other questions will be measured on prototypes and decided based on practical results.

Interfaces, hardware designs and architectural decisions may change significantly during this phase.

Technical discussion, constructive criticism and future contributions from the community are explicitly welcome.
