# Förderbandsteuerung (Conveyor Belt)

Studienprojekt im Masterstudiengang Mechatronik  
Schwerpunkt Embedded Systems

## Projektbeschreibung

Dieses Projekt entstand im Rahmen des Moduls **Embedded Systems** des Masterstudiengangs Mechatronik an der Fachhochschule Vorarlberg.

Ziel war die Entwicklung einer verteilten Förderbandsteuerung in C++. Mehrere Controller kommunizieren über TCP/IP miteinander und geben Transportaufträge bzw. Pakete entlang einer simulierten Förderstrecke weiter.

Ein Auftrag wird dabei von einem Controller übernommen, bestätigt und anschließend an den nächsten Controller weitergereicht. Die Steuerungslogik basiert auf Zustandsmaschinen und einer ereignisgesteuerten Architektur.

Das Projekt diente insbesondere dazu, Konzepte der Embedded-Softwareentwicklung, Kommunikation zwischen Steuerungseinheiten sowie die Strukturierung komplexerer Anwendungen in C++ zu erlernen.

---

## Funktionen

- Kommunikation zwischen mehreren Steuerungseinheiten über TCP/IP
- Weitergabe von Paketen bzw. Transportaufträgen zwischen den Controllern
- Quittierung und Bestätigung empfangener Aufträge
- Zustandsbasierte Ablaufsteuerung
- Bedienoberfläche zur Überwachung und Steuerung
- Modularer Softwareaufbau in C++

---

## Softwarearchitektur

Die Anwendung ist in mehrere funktionale Module unterteilt.

### Steuerung

| Modul | Aufgabe |
|---------|---------|
| SysControl | Zentrale Ablaufsteuerung |
| MotorControl | Steuerung des Förderbandabschnitts |
| DisplayControl | Anzeige und Benutzeroberfläche |
| KeyboardHandler | Verarbeitung von Benutzereingaben |

### Kommunikation

| Modul | Aufgabe |
|---------|---------|
| TCPHandler_UI | Kommunikation mit der Benutzeroberfläche |
| TCPHandler_Chain | Kommunikation zwischen den Förderbandsegmenten |

### Zustandsverwaltung

Die Systemlogik basiert auf Zustandsmaschinen.

Definiert werden die Zustände unter anderem durch:

- `SysState.h`
- `MotorState.h`
- `OpMode.h`

Dadurch wird das Verhalten der einzelnen Förderbandabschnitte klar strukturiert und einfach erweiterbar.

---

## Projektstruktur

```text
.
├── SysControl.*
├── MotorControl.*
├── DisplayControl.*
├── KeyboardHandler.*
├── TCPHandler_UI.*
├── TCPHandler_Chain.*
├── Command.h
├── SysState.h
├── MotorState.h
└── OpMode.h
```

---

## Verwendete Technologien

- C++
- TCP/IP Kommunikation
- Zustandsmaschinen (State Machines)
- Ereignisgesteuerte Programmierung
- Objektorientierte Softwareentwicklung

---

## Lernziele

Im Rahmen des Projekts wurden insbesondere folgende Themen behandelt:

- Entwurf modularer Embedded-Software
- Netzwerkkommunikation zwischen Steuerungseinheiten
- Implementierung von Zustandsautomaten
- Softwarearchitektur für eingebettete Systeme
- Objektorientierte Entwicklung in C++

---

## Hinweis

Dieses Repository enthält den Quellcode eines Studienprojekts. Die Implementierung entstand zu Lernzwecken im Rahmen des Masterstudiengangs Mechatronik und dient als Beispiel für die Entwicklung verteilter Embedded-Anwendungen in C++.

## Autor

**Markus Gerstenberg**  
M.Sc. Mechatronik
