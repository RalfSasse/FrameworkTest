# FrameworkTest
WiX-Skript zur Prüfung, ob auf dem Zielrechner .NET Framework 4.8 und .NET Core 3.1.15 vorhanden sind.

Die Prüfungen erfolgen in der eingebundenen C#-CustomAction "FrameworkTestCustomAction2.dll" (siehe Repository https://github.com/RalfSasse/FrameworkTestCustomAction2.git).

Der neueste Stand enthält ListView- und VolumeCostList-Elemente.

ListView-Elemente sind in WiX keine Tabellen - sie enthalten keine Kopfzeilen und pro Zeile nur ein Icon und einen Text. Das Icon lässt sich nicht abhängig vom Inhalt der Variablen auswählen (einzelne ListItem-Elemente können keine Conditions enthalten). Außerdem wird die Reihenfolge der ListItem-Elemente ignoriert (im Dialogfenster steht DOTNETCOREVERSION oberhalb von DOTNETFRAMEWORKVERSION).

VolumeCostList-Elemente funktionieren so, wie ListView-Elemente in C# funktionieren: Sie haben mehrere Spalten und eine Kopfzeile. Leider funktionieren sie in WiX aber nur für Angaben zur Speicherkapazität auf Festplatten und lassen sich nicht zweckentfremden. Fehlen Spalten wie "VolumeCostAvailable" oder "VolumeCostRequired", gibt es eine Fehlermeldung vom Compiler. Eigene Spalten-Definitionen wie "MeineSpalte" werden ignoriert.

Den Ansatz mit CustomTable habe ich seit gestern nicht weiter verfolgt.
