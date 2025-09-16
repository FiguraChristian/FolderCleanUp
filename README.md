# FolderCleanUp - Automatischer Datei-Organisator (Python & Tkinter)

Ein Desktop-Tool mit grafischer Benutzeroberfläche (GUI) zum automatischen Aufräumen und Sortieren von Dateien in einem beliebigen Ordner.

## Das Problem

Jeder kennt es: Der "Downloads"-Ordner oder der Desktop wird schnell unübersichtlich. Unzählige Dateien verschiedenster Typen sammeln sich an und die manuelle Sortierung in Unterordner ist eine mühsame und zeitaufwendige Aufgabe.

**Ausgangssituation:** Ein unstrukturierter Ordner mit einer Mischung aus Bildern, Dokumenten, Archiven und Installationsdateien.

<img width="1654" height="960" alt="Screenshot_before" src="https://github.com/user-attachments/assets/b1934ae2-09f5-4b89-8585-08ad6ad61ae7" />


## Die Lösung

Dieses Tool bietet eine einfache und schnelle Lösung. Mit nur zwei Klicks können Benutzer einen beliebigen Ordner auswählen und das Skript sortiert alle Dateien automatisch in logische Unterordner, basierend auf ihrer Dateiendung.

**Das Ergebnis:** Ein perfekt organisierter Ordner, in dem alle Dateien nach Kategorien wie "Bilder", "Dokumente" oder "Archive" geordnet sind.

<img width="1454" height="937" alt="Screenshot_after" src="https://github.com/user-attachments/assets/6af3e318-ee50-4191-b349-dce12d4b97e5" />


## Key Features

* **Grafische Benutzeroberfläche (GUI):** Dank der Integration von `Tkinter` ist das Tool auch für technisch nicht versierte Anwender einfach zu bedienen.
* **Flexible Konfiguration:** Die Zuordnung von Dateiendungen zu Zielordnern ist in einer separaten `config.py`-Datei ausgelagert. Dadurch kann die Sortierlogik einfach erweitert werden, ohne den Kern des Programms zu verändern.
* **Automatisches Logging:** Jede Dateiverschiebung wird in einer `log.csv`-Datei protokolliert. Dies schafft Transparenz und hilft bei der Nachverfolgung und Fehleranalyse.
* **Robuste Fehlerbehandlung:** Das Skript ist darauf ausgelegt, mit Fehlern (z.B. wenn eine Datei nicht verschoben werden kann) umzugehen, diese zu protokollieren und den Sortiervorgang für die restlichen Dateien fortzusetzen.

## Projektstruktur

Das Projekt ist modular aufgebaut, um eine gute Lesbarkeit und Wartbarkeit zu gewährleisten:

* `main.py`: Der Haupteinstiegspunkt, der die grafische Benutzeroberfläche startet.
* `gui.py`: Definiert das gesamte Erscheinungsbild und die Funktionalität der `Tkinter`-Benutzeroberfläche.
* `file_sorter.py`: Enthält die Kernlogik für den Sortierprozess, inklusive der Dateiverschiebung und des Loggings.
* `config.py`: Eine zentrale Konfigurationsdatei, die das Mapping der Dateiendungen zu den Zielordnern enthält.

## Verwendete Technologien
- **Python**
- **Tkinter** (für die grafische Benutzeroberfläche)
- **Pandas** (für die Erstellung und Verwaltung der CSV-Logdatei)
- **os** & **shutil** Module (für die Interaktion mit dem Dateisystem)
