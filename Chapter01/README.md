# Kapitel 01 

## Entscheidung für Linux 
Moore's Law: Gordon Moore, Mitbegründer von Interl, beobachtete 1965, dass sich die Dichte der Komponenten auf einem Chip etwa alle zwei Jahre verdoppelt. 

Ein **System on Chip**, oder **Soc**, ist ein hochintegrierter Chip, der einen oder mehrere **Prozessorkerne** enthält und Schnittstellen zu Hauptspeicher, Massenspeicher und Peripheriegeräten vieler Art besitzt. 

Einige Vorteile von Linux: 
+ Es unterstützt Standardschnittstellen und -protokolle wie USB, WI-FI, Bluetooth und viele Speichermedien.
+ Es unterstützt viele Prozessorarchitekturen wie Arm, MIPS, x86 und PowerPC.
+ Linux ist Open Source --> flexibel 
+ Linux hat eine aktive Community --> Up to date und unterstützt aktuelle Hardware, Protokolle und Standards

## Wann man sich nicht für Linux entscheiden sollte
"Linux funktioniert dort gut, wo das zu lösende Problem die Komplexität rechtfertigt." 
- Benötigt mehr Ressourcen als Echtzeit-Betriebssysteme wie VxWorks oder QNX
- Erforderliches Skillset 
- Benötigt das Produkt eine behördliche Zulassung? 

## Treffen der Akteure
- Die Open Source Community U-Boot, BusyBox, Buildroot, Yocto Projekt und viele weitere Projekte unter dem Dach von GNU.
- Die CPU-Architekten: 
    - ARM/Linaro (ARM Cortex-A)
    - Intel (x86 und x86_64)
    - SiFive (RISC-V)
    - IBM (PowerPC)
- SoC-Anbieter: Broadcom, Intel, Microchip, NXP, Qualcomm, TI und viele andere. Sie passen den Kernel und die Toolchain der CPU-Architekturen an ihre Produkte an.
- Board Vendors und OEMs: Sie bauen spezifische Produkte auf Basis der Referenzboards der SoC-Anbieter. So entstehen Produkte wie Set-Top-Boxen, Kameras oder universelle Entwicklungsboards wie die von Advantexh und Kontron oder die billigeren wie BeagleBoard, Raspberry.
- **Commercial Linux Vendors**: von Firmen wie Siemens, Timesys und Wind River, die kommerzielle Linux-Distributionen anbieten, die eine strenge behördliche Überprüfung und Validierung in verschiedenen Branchen durchlaufen haben. 

## Moving through the project life cycle. 

Die folgenden Phasen sind nicht notwendigerweise sequentiell und können sich überschneiden. 
- **Board bring-up** --> Entwicklungsumgebung und funktionsfähige Plattform für die nächste Phase aufbauen (Elemente von Embedded Linux)
- Systemarchitektur und Designentscheidungen: In Bezug auf Speichermedien für Daten und Programme, Trennung von Kernel-Device-Treibern und Applikationen, wie initialisiere ich das System? 
- Embedded Applikationen schreiben: Entwicklung, Einsatz von Python-Applikationen, Speicherverwaltung in einer ressourcenbeschränkten Umgebung etc.
- **Debugging and Performance Improvement**: beschreibt, wie man den Code sowohl in den Applikationen als auch im Kernel verfolgen, profilieren und debuggen kann. 

## Die vier Elemente von Embedded Linux 
- Toolchain**: Der Compiler und andere Werkzeuge, um Code für das Zielgerät zu erzeugen. 
- **Bootloader**: Das Programm, das das Board initialisiert und den Linux-Kernel lädt. 
- Kernel**: Der Kern des Systems, der die Systemressourcen verwaltet und mit der Hardware interagiert.
- **Root-Dateisystem**: Enthält die Bibliotheken und Programme, die ausgeführt werden, nachdem der Kernel seine Initialisierungen abgeschlossen hat. 

**Die folgenden zwei Werkzeuge können den gesamten Prozess automatisieren: Buildroot und das Yocto-Projekt**.

## Navigation Open Source

### Lizenzen 
Open-Source-Lizenzen bieten die Freiheit, den Quellcode zu erhalten, zu verändern und weiterzugeben. Sie fallen in die folgenden Kategorien: 
- **Copyleft-Lizenzen wie die GNU General Public License (GPL)**: Quellcode erhalten, verändern und in nichtkommerzielle Produkte integrieren ist erlaubt. Im Falle der Integration muss der Quellcode zur Verfügung gestellt werden.  
- **Lesser General Public License (LGPL)**: funktioniert wie die GPL mit dem Unterschied, dass das Verlinken aus kommerziellen Produkten erlaubt ist. 
- **Lizenzen wie die BSD- und MIT-Lizenzen**: Sie erlauben die Weiterverwendung des Quellcodes auch in kommerziellen Produkten unter der Bedingung, dass die Lizenz erhalten bleibt. 

Die neue GPL v3 und LGPL v3 weisen einige Unterschiede auf.

## Auswahl von Hardware für Embedded Linux
