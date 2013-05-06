Abkürzung: `FaSb: Fa=Folie Nummer a, Sb=Seite Nummer b`

Netzwerkarchitekturen
=====================

Begriffe
--------

- Grundmodell der Kommunikation
    - Grundkomponenten: Sender, Empfänger, Abstrakter Übetragungsabschnitt, Dienstzugangspunkte
- Dienst
    - Bündelung zusammengehöriger Funktionen
    - Dienstfunktionalität: unabhängige Nutzung von Teilkomponenten eines Dienstes
    - Dienstprimitiv: Einzelvorgänge einer Dienstfunktion
        - Request (Anfrage, Sender → Empfänger)
        - Indication (Benachrichtigung des Partners, Sender → Empfänger)
        - Response (Antwort, Sender ← Empfänger)
        - Confirmation (Benachrichtigung über Abschluss, Sender ← Empfänger)
    - Diensthierarchie: Dienst baut auf anderen Diensten auf
    - Dienstzugangspunkt: Schnittstelle zur Nutzung
- Weg-Zeit-Diagramm (F2S13)
- Richtung des Datenaustauschs
    - Simplex (Richtungsbetrieb): Fluss nur in eine Richtung (Radio, Fernseher, Sensor)
    - Halbduplex (Wechselbetrieb): Fluss abwechselnd in beide Richtungen (Wechselsprecher)
    - Vollduplex (Gegenbetrieb): Fluss gleichzeitig in beide Richtungen (Telefon, DSL)
- Dienstbewertung: Dienstqualität
    - Angemessenheit: Eigung des Dienstes für das Einsatzgebiet
    - Technische Leistung: Laufzeit, Antwortzeit, Datenrate
    - Zuverlässigkeit: Erkennen von und reagieren auf Störungen
        - Verlust, Duplizierung, Vertauschung, Verfälschung von Informationen
    - Sicherheit: Erkennen von und reagieren auf bewusste Eingriffe
        - Abhören, Modifizieren, Maskieren, Unterbrechen von Informationen/Dienstprimitiven
    - Kosten: Investitions- und Betriebskosten zur Erbringung des Dienstes
- Vereinfachtete geschichtete Architektur
    - Ende-zu-Ende-Übertragung
    - Gerät-zu-Gerät-Übertragung
    - Bit-Übertragung
- Protokoll
    - Regeln und Formate für Informationsaustausch
    - Innerhalb einer Schicht (horizontale Kommunikation)
- Horizontale Kommunikation
    - Zwischen Sendern und Empfängern
    - Kommunikation innerhalb der gleichen Schicht
- Vertikale Kommunikation
    - Kommunikation zwischen Schichten eines Systems
    - Zugriff auf nächsthöhere oder nächstniedrigere Schicht
- Datenkapselung
    - Kapselung der Daten in Kontrollinformation wie Header und Trailer
    - Kontrollinformationen werden vor Weitergabe in höhere Schicht entfernt
- Protocol Data Unit (PDU)
    - Beinhaltet Daten und Protokollkontrollinformation
- Service Data Unit (SDU)
    - Datenteil
    - Wird aus PDU extrahiert und an höhere Schicht weitergegeben

OSI-Modell
----------

- Schichten
    1. Bit-Übetragung (Physical Layer)
        - Reine Bitübertragung
        - Keine Pufferung, keine Zuverlässigkeit (Möglichkeit von Störungen)
    2. Sicherung (Data Link Layer)
        - Datenübetragung zwischen Geräten
        - Fehlererkennung und -behebung für Physical Layer
        - Gliederung eines Bitstroms in Dateneinheiten
        - Pufferung sowohl beim Sender als auch beim Empfänger
    3. Vermittlung (Network Layer)
        - Adressierung von Geräten
        - Wegewahl zwischen Ende-zu-Ende-Strecken
    4. Transport (Transport Layer)
        - Datenübetragung zwischen Anwendungen
        - Abstrahiert von Diensten aus Vermittlungsschicht
        - Fehlererkennung und -behebung
        - Pufferung
    5. Sitzung (Session Layer)
        - Bietet Nichtunterbrechbarkeit von Kommunikationsbeziehungen
        - Übergibt Anwungen die Kontrolle über den Datenaustausch (Sitzungsmanagement, Rücksetzvereinbarung...)
    6. Darstellung (Presentation Layer)
        - Einheitliche Darstellung von Daten (Syntax)
        - Erhalt der Semantik der Information
    7. Anwendung (Application Layer)
        - Austauch von Anwendungsabhängigen Daten
- 1-4 bilden Transportsystem
- 5-7 bilden Anwendungssystem

Internet-Modell
---------------

- Schichten
    1. Rechner-Netzanschluss (OSI 1-2)
    2. Vermittlung (OSI 3)
    3. Transport (OSI 4)
    4. Anwendung (OSI 5-7)

Physikalische Grundlagen
========================

???
