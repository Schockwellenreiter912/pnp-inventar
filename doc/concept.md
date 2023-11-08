# Konzept
## Zusammenfassung

Die Website soll die Verwaltung von Rollenpsiel Inventar erleichtern und bestehende Spreadsheets ablösen.

## Anwendungsfälle
### Inventar für eine Gruppe einrichten

```mermaid
flowchart LR
A[Admin erzeugt neue Gruppe] -->|Input: Gruppenname| B[Neue Gruppe in DB anlegen]
```

### Simple Berechtigungen

```mermaid
flowchart LR
A[Admin öffnet Rechteverwaltung für Gruppe] --> B[Übersicht der bestehenden Berechtigungen]
B --> C{Aktionen}
C --> D[Admin nimmt Benutzer in Gruppe auf]
C --> E[Admin ändert Berechtigungen für Benutzer]
D --> E
```

Berechtigungen:
 - Admin
 - Gruppenverwalter
 - Benutzer

### Ausrüstungslisten für eine Gruppe hinterlegen

```mermaid
flowchart LR
A[Gruppenverwalter öffnet Ausrüstungslisten für Gruppe] --> B[Übersicht der hinterlegten Ausrüstungslisten]
B --> C{Aktionen}
C --> D[Neue Ausrüstungsliste hinterlegen]
D --> E[Drag&Drop Datei mit Ausrüstungsliste]
C --> F[Ausrüstungsliste bearbeiten]
C --> G[Ausrüstungsliste entfernen]
```

#### Ausrüstungsliste
 - Name
 - Gegenstände(Liste)
  - Name
  - Kategorie
  - Schlagworte
  - Preis

### Ausrüstungspakete für eine Gruppe hinterlegen

```mermaid
flowchart LR
A[Gruppenverwalter öffnet Ausrüstungslisten für Gruppe] --> B[Übersicht der hinterlegten Ausrüstungslisten]
B --> C{Aktionen}
C --> D[Neue Ausrüstungsliste hinterlegen]
D --> E[Drag&Drop Datei mit Ausrüstungsliste]
C --> F[Ausrüstungsliste bearbeiten]
C --> G[Ausrüstungsliste entfernen]
```

#### Ausrüstungspakete
 - Name
 - Aurüstungsliste
 - Gegenstände

### Gegenstände erhalten

```mermaid
flowchart LR
A[Benutzer öffnet Inventar für Gruppe] --> B[Übersicht des aktuellen Inventars]
B --> C{Aktionen}
C --> D[Mengen der Gegenstände anpassen]
C --> E[Details zu einem Gegenstand hinterlegen]
```

### Gegenstände einlagern

```mermaid
flowchart LR
A[Benutzer öffnet Inventar für Gruppe] --> B[Übersicht des aktuellen Inventars]
B --> C{Aktionen}
C --> D[Gegenstände dem Lager zuordnen]
```

### Gegenstände verteilen

```mermaid
flowchart LR
A[Benutzer öffnet Inventar für Gruppe] --> B[Übersicht des aktuellen Inventars]
B --> C{Aktionen}
C --> D[Gegenstände einem Charakter zuordnen]
```

### Gegenstände verkaufen

```mermaid
flowchart LR
A[Benutzer öffnet Inventar für Gruppe] --> B[Übersicht des aktuellen Inventars]
B --> C{Aktionen}
C --> D[Mengen von Gegenständen für Verkauf markieren]
D -->|Nach dem Verkauf, z.B. in einer Sitzung| E[Menge von verkauften Gegenständen reduzieren]
E --> F[Geld aus Verkäufen erhalten]
```
