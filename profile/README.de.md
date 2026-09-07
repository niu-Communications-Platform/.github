# nıu Communications Platform

**Deutsch** | [English](README.md)

**Offene Kommunikationsinfrastruktur. Gebaut, um sie selbst zu besitzen.**

Die **nıu Communications Platform** ist eine offene Kommunikationsplattform für Teams, die zuverlässige Sprachkommunikation benötigen – zunächst mit einem klaren Fokus auf **Live-Produktion, Broadcast, Veranstaltungen und kleine Produktionsteams**.

Das Projekt verbindet dedizierte Kommunikationshardware mit offenen Standards, selbst betreibbarer Infrastruktur und optional betriebenen Diensten.

Unser Ziel ist kein weiteres geschlossenes Intercom-System.

Wir wollen eine Plattform bauen, die man **kaufen, verstehen, verändern, selbst betreiben und weiterentwickeln** kann.

> **Dedicated hardware. Open infrastructure. Your network. Your choice.**

Die **deutsche Fassung ist die kanonische Quelle** für die Beschreibung und Grundsätze des Projekts. Die englische Fassung wird als gepflegte Übersetzung für Austausch, Zusammenarbeit und eine internationale Community geführt. Bei Abweichungen gilt die deutsche Fassung.

---

## Die Idee

Professionelle Intercom-Systeme funktionieren hervorragend – sind aber häufig teuer, proprietär und eng an das Ökosystem eines Herstellers gebunden.

Softwarebasierte Lösungen sind dagegen flexibel und günstig, setzen im praktischen Einsatz aber häufig Smartphones, Computer oder improvisierte Hardware voraus.

Die nıu Communications Platform versucht, diese beiden Welten zusammenzuführen:

- dedizierte, robuste Kommunikationshardware
- physische Push-to-Talk-Bedienung
- Kommunikation über Standard-IP-Netzwerke und WLAN
- offene Software und dokumentierte Schnittstellen
- lokale und vollständig selbst betriebene Infrastruktur
- optional komfortabel betriebene Cloud-Infrastruktur
- keine technische Abhängigkeit von einer Hersteller-Cloud

Der Ausgangspunkt ist ein Gerät, das sich wie ein klassisches Beltpack benutzen lässt – technisch darunter aber Teil einer offenen IP-Kommunikationsplattform ist.

## Ein Gerät. Drei Betriebsmodelle.

Die Plattform soll nicht vorschreiben, wo ihre Kommunikationsinfrastruktur betrieben werden muss.

### Bare

Das Gerät verbindet sich mit einer vorhandenen oder selbst betriebenen kompatiblen Server-Infrastruktur.

**Hardware kaufen. Server selbst betreiben. Fertig.**

Kein nıu-Server und kein Cloud-Abonnement sind erforderlich.

### Base

**nıu Base** ergänzt die Geräte um eine lokale, vorkonfigurierte Kommunikationsinstanz.

Die gesamte Kommunikation kann innerhalb des eigenen Netzwerks stattfinden – auch unabhängig vom Internet.

Damit verbindet Base die Kontrolle eines selbst betriebenen Systems mit dem Komfort einer Appliance.

### Cloud

**nıu Cloud** stellt die benötigte Kommunikationsinfrastruktur als von uns betriebenen Dienst bereit.

Geräte können damit ohne eigenen Server eingerichtet und über das Internet miteinander verbunden werden.

Cloud ist die komfortabelste Betriebsform – aber **keine Voraussetzung für die Nutzung der Plattform**.

## Eine Plattform, mehrere Produkte

Die technische Plattform ist bewusst nicht auf einen einzelnen Anwendungsfall beschränkt.

### Production

Der erste Schwerpunkt.

**nıu Production** richtet sich an kleine und mittlere Teams in:

- Live-Produktion
- Streaming
- Broadcast
- Veranstaltungstechnik
- Theater
- Film- und Videoproduktion
- mobilen Produktionsteams

Hier entsteht auch das erste Beltpack der Plattform.

### Operations

Die gleiche technische Grundlage kann später für operative Teams interessant sein, die unkomplizierte, dedizierte Gruppenkommunikation über IP-Netze benötigen.

Die Anforderungen und Benutzeroberfläche können sich dabei deutlich von Production unterscheiden – die Plattform darunter muss es nicht.

### Love

**nıu Love** untersucht einen bewusst anderen Anwendungsfall: eine extrem einfache, physische Kommunikationsverbindung zwischen wenigen Menschen.

Love ist keine bloße Variante des Production-Beltpacks, sondern eine eigenständige Produktidee auf derselben offenen Kommunikationsplattform.

## Warum Mumble?

Die Plattform baut nicht unnötig einen eigenen Voice-Stack.

Als Kommunikationsgrundlage verwenden wir **Mumble/Murmur** und entwickeln darum herum die Komponenten, die aus einem allgemeinen VoIP-System eine dedizierte Kommunikationsplattform machen:

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

Das Rad soll dort nicht neu erfunden werden, wo bereits ein bewährtes offenes Protokoll existiert.

Die Entwicklungsarbeit konzentriert sich stattdessen auf Hardware, Bedienung, Provisionierung, Management, Integration und zuverlässigen Betrieb.

## Open Source ist Teil der Architektur

Open Source verstehen wir nicht als nachträgliche Veröffentlichung einzelner Softwarekomponenten.

Die Plattform soll grundsätzlich **nachbaubar und unabhängig betreibbar** sein.

Dazu gehören perspektivisch:

- Hardware und PCB-Designs
- Device Software
- Base-/Server-Komponenten
- Provisioning und Management
- dokumentierte Protokolle und APIs
- reproduzierbare Build- und Deployment-Prozesse

Ein Dritter soll eine kompatible Plattform mit eigener Infrastruktur und eigener **Trust Domain** betreiben können.

Dabei gilt:

**Open Source bedeutet Implementierungsfreiheit – nicht die Übernahme der nıu-Identität oder nıu-Vertrauensstellung.**

Offizielle nıu-Geräte, Firmware und Dienste verwenden von nıu kontrollierte kryptographische Vertrauensanker. Andere Betreiber können denselben offenen Source Code mit eigenen Schlüsseln und eigener Infrastruktur einsetzen.

Damit soll Offenheit möglich sein, ohne Herkunft und Authentizität offizieller Komponenten aufzugeben.

## Kein Cloud-Lock-in

Ein zentrales Architekturprinzip lautet:

> **The cloud is a service, not a dependency.**

Wer nıu Cloud nutzen möchte, soll eine möglichst einfache, betriebene Lösung erhalten.

Wer sie nicht nutzen möchte, soll die Plattform trotzdem vollständig sinnvoll einsetzen können.

Unsere Cloud muss deshalb durch **Komfort, Betrieb, Verfügbarkeit, Support und Integration** überzeugen – nicht dadurch, dass Geräte ohne sie künstlich eingeschränkt werden.

## Hardware, die ein Produkt werden soll

Das Projekt ist ausdrücklich nicht nur ein Softwareexperiment.

Das Beltpack wird mit Blick auf ein später tatsächlich produzierbares Gerät entwickelt:

- dedizierte PTT-Bedienung
- integriertes Audio
- Anschluss externer Headsets und Audio-Geräte
- WLAN/IP-Kommunikation
- Display und Statusanzeigen
- Akkubetrieb und stationärer Dauerbetrieb
- robuste und wartbare Konstruktion
- automatisierbare Fertigung und End-of-Line-Tests
- Provisioning und sichere Geräteidentität
- OTA-Updates, Recovery und Diagnose
- regulatorische Konformität und Zertifizierung

Bereits frühe Hardwareentscheidungen werden deshalb daraufhin betrachtet, ob ein Gerät später nicht nur einmal am Labortisch, sondern reproduzierbar in größeren Stückzahlen gefertigt werden kann.

## Architekturprinzipien

Einige Grundsätze prägen die Entwicklung bereits heute:

- **Komplexität nach innen, Einfachheit nach außen.** Das Gerät soll sich einfach bedienen lassen, auch wenn darunter eine leistungsfähige Plattform arbeitet.
- **Capability ≠ Feature.** Die technische Plattform darf mehr können, als die normale Benutzeroberfläche zeigen muss.
- **Hardware schafft Möglichkeiten, Software entscheidet später, welche davon genutzt werden.** Teure Hardware-Lock-ins sollen früh vermieden werden.
- **Identity lives on the carrier. Configuration belongs to deployment. Runtime state belongs to the compute module.** Austauschbare Komponenten sollen nicht unnötig die Identität des Geräts bestimmen.
- **Reality beats configuration.** Das System soll zwischen gewünschtem Zustand und tatsächlich verfügbarer Hardware bzw. Verbindung unterscheiden.
- **Open source means implementation freedom, not inherited trust.** Eigene Builds und eigene Trust Domains sind ausdrücklich vorgesehen.

## Architektur-Dokumentation

Die technischen Hintergründe und Entscheidungen werden im [`architecture`](https://github.com/niu-Communications-Platform/architecture)-Repository dokumentiert. Deutsch ist dort die kanonische Sprache; die englischen Seiten werden als gepflegte Übersetzungen geführt.

- [Produktprinzipien](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/00-product/product-principles.md)
- [Systemarchitektur](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/10-system/system-architecture.md)
- [Audioarchitektur](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/40-audio/audio-architecture.md)
- [Netzwerkarchitektur](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/50-networking/network-architecture.md)
- [Identity- und Trust-Architektur](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/60-identity-security/identity-trust-architecture.md)
- [Provisioning, Ownership und Lifecycle](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/70-provisioning-lifecycle/provisioning-lifecycle.md)
- [Factory- und Fertigungsarchitektur](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/80-manufacturing/factory-architecture.md)
- [UX-/UI-Prinzipien](https://github.com/niu-Communications-Platform/architecture/blob/main/docs/de/90-ux-ui/ux-ui-principles.md)

[Vollständiger deutscher Dokumentationsindex](https://github.com/niu-Communications-Platform/architecture/tree/main/docs/de)

## Repository-Struktur

Die GitHub-Organisation soll die Plattform in klar getrennten Verantwortungsbereichen abbilden:

```text
nıu Communications Platform/
├── architecture       # Systemarchitektur, Spezifikationen und ADRs
├── beltpack           # Hardware und Device Software
├── base               # lokale/on-premise Plattform
├── cloud              # gehostete Plattform
└── factory-tools      # Fertigung, EOL und Provisioning-Werkzeuge
```

Nicht alle Repositories existieren bereits. Sie entstehen mit der praktischen Entwicklung der jeweiligen Komponenten.

## Aktueller Status

🚧 **Frühe Entwicklung / Architektur und Prototyping**

Der aktuelle Schwerpunkt liegt auf:

**Production → Beltpack → lokale Kommunikation → robuste Hardware → reproduzierbare Plattform**

Prototypen und bestehende Open-Source-Komponenten dienen zunächst dazu, Architektur, Hardware und Bedienkonzept praktisch zu validieren.

Das Projekt wird bewusst nicht vollständig am Reißbrett eingefroren. Vor dem ersten Hardware-Prototyp werden vor allem Entscheidungen abgesichert, die später teure Hardware-Lock-ins erzeugen würden. Andere Fragen werden am Prototyp gemessen und anschließend entschieden.

Interfaces, Hardwaredesigns und Architekturentscheidungen können sich in dieser Phase noch deutlich verändern.

Technische Diskussion, konstruktive Kritik und spätere Beiträge aus der Community sind ausdrücklich willkommen.
