# nıu Communications Platform

**Deutsch** | [English](README.md)

**Offene Kommunikationsinfrastruktur. Gebaut, um sie selbst zu besitzen.**

Die **nıu Communications Platform** – kurz **nıu.cp** – ist eine offene Kommunikationsplattform für Teams, die zuverlässige Sprachkommunikation benötigen – zunächst mit einem klaren Fokus auf **Live-Produktion, Broadcast, Veranstaltungen und kleine Produktionsteams**.

Das Projekt verbindet dedizierte Kommunikationshardware mit offenen Standards, selbst betreibbarer Infrastruktur und optional betriebenen Diensten.

Unser Ziel ist kein weiteres geschlossenes Intercom-System.

Wir wollen eine Plattform bauen, die man **kaufen, verstehen, verändern, reparieren, selbst betreiben und weiterentwickeln** kann.

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
- Mumble/Murmur als offene native Sprachbasis
- SIP als vorgesehene Interoperabilitätsschicht
- offene Software, dokumentierte Schnittstellen und offene Hardware
- lokale und vollständig selbst betriebene Infrastruktur
- optional komfortabel betriebene Cloud-Infrastruktur
- keine technische Abhängigkeit von einer Hersteller-Cloud
- reparierbare, verständlich dokumentierte Hardware
- ein durch den Endnutzer austauschbarer Akku
- ein optionaler sekundärer Sub-GHz-/LoRa-Resilience-Pfad für kleine Status- und Steuerinformationen, unabhängig vom primären IP-Audioweg

Der Ausgangspunkt ist ein Gerät, das sich wie ein klassisches Beltpack benutzen lässt – technisch darunter aber Teil einer offenen IP-Kommunikationsplattform ist.

## Was nıu.cp besonders machen soll

nıu.cp soll nicht einfach ein Mumble-Client in einem eigenen Gehäuse werden. Die Plattform wird als vollständiges Produkt- und Systemkonzept entwickelt:

- **Mumble-native, SIP-interoperabel.** Der Echtzeit-Sprachpfad baut auf Mumble/Murmur auf; SIP soll dort angebunden werden, wo Interoperabilität mit bestehenden Kommunikationssystemen sinnvoll ist.
- **IP für Sprache, zusätzlicher Resilience-Pfad für kleine kritische Informationen.** Ein sekundärer Sub-GHz-Funkpfad wird für Presence, Status, Call-/Alarm-Signalisierung, Tally und Recovery-Nachrichten untersucht. Ein lokaler Direct-LoRa-Star zwischen Beltpacks und Base ist derzeit der stärkste Protokollkandidat. Dieser Pfad ist ausdrücklich **kein zweiter Audio-Transport** und noch keine endgültige Architekturentscheidung.
- **Compute ist austauschbar, Produktidentität bleibt auf dem Carrier.** Rechenmodul, Betriebssystem und Runtime sollen ersetzt oder weiterentwickelt werden können, ohne die physische Geräteidentität unnötig daran zu binden.
- **Austauschbarer Akku statt versiegeltem Verschleißteil.** Der Endnutzer soll den Battery Pack selbst wechseln können; Zellschutz und BMS bleiben Aufgabe eines serienreifen Herstellerpacks.
- **Cloud-Komfort ohne Cloud-Zwang.** Bare, Base und Cloud nutzen soweit sinnvoll dieselben Geräte- und Protokollgrundlagen.
- **Offenheit umfasst Diagnose und Reparatur.** Offizielle nıu-Trust-Roots bleiben geschützt, während Hardware, Software, Diagnose und Reparatur soweit rechtlich und technisch möglich nachvollziehbar bleiben.

## Offenheit, die beim Verstehen nicht aufhört

Die Plattform soll nicht nur offen sein, damit man theoretisch in Quellcode, Schaltpläne oder Schnittstellen schauen kann.

Unser Anspruch geht weiter:

**Open Source → Open Hardware → Open Diagnostics → Open Repair Documentation → Open Understanding**

Ein nıu.cp-Gerät soll nicht nur benutzbar, reparierbar und veränderbar sein. Ein neugieriger Besitzer soll auch eine echte Chance haben, **zu verstehen, wie es funktioniert**.

Das bedeutet: Technische Dokumentation soll – soweit sinnvoll und rechtlich möglich – nicht bei Source Code, Schaltplänen und Reparaturanleitungen enden. Sie soll zusätzlich erklären:

- Was macht ein Teilsystem?
- Warum existiert es?
- Wie arbeitet es mit anderen Teilen des Geräts zusammen?
- Warum wurde diese Architektur gewählt?
- Welches konkrete Problem löst oder verhindert ein bestimmtes Bauteil?

Dabei unterscheiden wir bewusst zwei Ebenen:

**Engineering & Repair Reference** richtet sich an Entwickler, professionelle Reparaturbetriebe und erfahrene Maker. Dort gehören Schaltpläne, BOMs, Pinouts, Messpunkte, Diagnoseverfahren, Testabläufe und Reparaturinformationen hin.

**Inside nıu.cp** soll technisch interessierte Nutzer, Maker, Lernende und Quereinsteiger schrittweise vom Produktverständnis bis zur tatsächlichen technischen Umsetzung führen.

Die didaktische Reihenfolge lautet:

**Produktnutzen → Architekturverständnis → Engineering-Detail**

Technische Begriffe werden dabei nicht vermieden, sondern erklärt.

> **Open Hardware bedeutet nicht nur: Du darfst hineinsehen. Open Understanding bedeutet: Wir helfen Dir zu verstehen, was Du dort siehst.**

Unser Ziel ist ein Produkt, das **hohen Bedienkomfort mit echter technischer Eigentümerschaft und Entwicklerfreiheit** verbindet.

## Ein Gerät. Drei Betriebsmodelle.

Die Plattform soll nicht vorschreiben, wo ihre Kommunikationsinfrastruktur betrieben werden muss.

### Bare

Das Gerät verbindet sich mit einer vorhandenen oder selbst betriebenen kompatiblen Server-Infrastruktur.

**Hardware kaufen. Server selbst betreiben. Fertig.**

Kein nıu-Server und kein Cloud-Abonnement sind erforderlich.

### Base

**nıu Base** ergänzt die Geräte um eine lokale, vorkonfigurierte Kommunikationsinstanz.

Die gesamte Sprachkommunikation kann innerhalb des eigenen Netzwerks stattfinden – auch unabhängig vom Internet. Perspektivisch kann Base außerdem lokale Infrastruktur für zusätzliche Gerätefunktionen wie den sekundären Resilience-/Control-Pfad bereitstellen.

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

Hier entsteht auch das erste **nıu.cp Beltpack** der Plattform.

### Operations

Die gleiche technische Grundlage kann später für operative Teams interessant sein, die unkomplizierte, dedizierte Gruppenkommunikation über IP-Netze benötigen.

Die Anforderungen und Benutzeroberfläche können sich dabei deutlich von Production unterscheiden – die Plattform darunter muss es nicht.

### Love

**nıu Love** untersucht einen bewusst anderen Anwendungsfall: eine extrem einfache, physische Kommunikationsverbindung zwischen wenigen Menschen.

Love ist keine bloße Variante des Production-Beltpacks, sondern eine eigenständige Produktidee auf derselben offenen Kommunikationsplattform.

## Warum Mumble?

Die Plattform baut nicht unnötig einen eigenen Voice-Stack.

Als native Kommunikationsgrundlage verwenden wir **Mumble/Murmur** und entwickeln darum herum die Komponenten, die aus einem allgemeinen VoIP-System eine dedizierte Kommunikationsplattform machen. **SIP ist als Interoperabilitätsschicht vorgesehen, nicht als Ersatz für das native Mumble-Modell.**

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

Offizielle nıu-Geräte, Firmware und Dienste verwenden von nıu kontrollierte kryptographische Vertrauensanker. Andere Betreiber können dieselbe offene Implementierung mit eigenen Schlüsseln und eigener Infrastruktur einsetzen.

Damit soll Offenheit möglich sein, ohne Herkunft und Authentizität offizieller Komponenten aufzugeben.

## Kein Cloud-Lock-in

Ein zentrales Architekturprinzip lautet:

> **The cloud is a service, not a dependency.**

Wer nıu Cloud nutzen möchte, soll eine möglichst einfache, betriebene Lösung erhalten.

Wer sie nicht nutzen möchte, soll die Plattform trotzdem vollständig sinnvoll einsetzen können.

Unsere Cloud muss deshalb durch **Komfort, Betrieb, Verfügbarkeit, Support und Integration** überzeugen – nicht dadurch, dass Geräte ohne sie künstlich eingeschränkt werden.

## Hardware, die ein Produkt werden soll

Das Projekt ist ausdrücklich nicht nur ein Softwareexperiment.

Das Beltpack wird mit Blick auf ein später tatsächlich produzierbares Gerät entwickelt. Der aktuelle physische Arbeitsstand untersucht einen **105 × 70 mm Core Body** mit seitlich teilversenktem, austauschbarem Battery Pack, großem PTT auf der Gegenseite und freier Rückseite für den Beltclip. Diese Geometrie ist noch kein Production Freeze, aber deutlich konkreter als ein abstraktes Konzept.

Zu den vorgesehenen bzw. untersuchten Eigenschaften gehören:

- dedizierte PTT-Bedienung
- internes Mikrofon und interner Lautsprecher
- separate MIC-/PHONES-Anschlüsse und TRRS-Headset
- USB Audio und perspektivisch Bluetooth Audio
- WLAN/IP-Kommunikation
- optionaler sekundärer Sub-GHz-/LoRa-Resilience-Pfad
- Display, physische VOL±/CH±/MENU/BACK-Bedienung und Statusanzeigen
- zwei USB-C-Schnittstellen für POWER und ACCESSORY; die mechanische Anordnung wird auch mit Blick auf eine mögliche Docking-Lösung entwickelt
- austauschbarer Battery Pack und Betrieb an ausreichender externer Versorgung
- robuste und wartbare Konstruktion
- sichere, vom Compute-Modul getrennte Geräteidentität
- automatisierbare Fertigung und End-of-Line-Tests
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
- **Prototype = measurement instrument.** Offene technische Fragen sollen am Prototyp reproduzierbar gemessen werden, statt nur theoretisch optimiert zu werden.

## Entwicklungsdokumentation

Die technischen Hintergründe, Architekturentscheidungen, Experimente und Validierungspläne werden bereits systematisch in separaten Repositories gepflegt.

Diese Repositories sind während der frühen Produktentwicklung **bewusst noch nicht öffentlich**. Die öffentliche Organisationsseite beschreibt daher den aktuellen Projektgedanken und die grundlegenden Prinzipien direkt, ohne auf nicht zugängliche Dokumente zu verweisen.

Mit zunehmender Reife sollen geeignete technische Dokumentation, Hardwaredesigns, Software und Entwicklungsressourcen schrittweise öffentlich zugänglich werden.

## Repository-Struktur

Die GitHub-Organisation soll die Plattform in klar getrennten Verantwortungsbereichen abbilden:

```text
nıu Communications Platform/
├── architecture        # Systemarchitektur, Spezifikationen und ADRs
├── beltpack            # Hardware und Device Software
├── base                # lokale/on-premise Plattform
├── cloud               # gehostete Plattform
├── factory-tools       # Fertigung, EOL und Provisioning-Werkzeuge
└── product-development # Fragen, Experimente und Erkenntnisse während der Entwicklung
```

Die Entwicklungs-Repositories sind derzeit privat und werden mit der praktischen Entwicklung der jeweiligen Komponenten weiter ausgebaut.

## Aktueller Status

🚧 **Aktive Architekturvalidierung und Prototypvorbereitung**

Der aktuelle Schwerpunkt liegt auf:

**Production → nıu.cp Beltpack → lokale Kommunikation → robuste Hardware → reproduzierbare Plattform**

Wesentliche Architekturentscheidungen sind bereits gefallen – darunter Carrier-basierte Geräteidentität, Mumble als natives Sprachprotokoll mit SIP-Interoperabilität, getrennte offene Trust Domains und der durch den Endnutzer austauschbare Battery Pack. Andere Punkte bleiben bewusst unter aktiver Validierung, insbesondere Compute-Auswahl, compute-unabhängige USB-Audio-Anbindung, Secondary Sub-GHz/LoRa, RF/Antennenverhalten, Battery-Dock, Mechanik und Serienfertigung.

Der derzeit stärkste mechanische Arbeitsstand nutzt einen 105 × 70 mm Core Body mit seitlichem Battery Pack. Für den zusätzlichen Resilience-Pfad wird ein lokaler Direct-LoRa-Star mit eigenständigem MCU/Radio als ernsthafter V1-Kandidat untersucht. Beides ist noch kein endgültiger Product Freeze.

Das Projekt wird bewusst nicht vollständig am Reißbrett eingefroren. Entscheidungen mit hohem Hardware-Lock-in-Risiko werden früh abgesichert; andere Fragen werden am Prototyp gemessen und anschließend entschieden.

Interfaces, Hardwaredesigns und Architekturentscheidungen können sich in dieser Phase noch deutlich verändern.

Technische Diskussion, konstruktive Kritik und spätere Beiträge aus der Community sind ausdrücklich willkommen.
