# FrameworkTest
WiX-Skript zur Prüfung, ob auf dem Zielrechner .NET Framework 4.8 und .NET Core 3.1.15 vorhanden sind.

Die Prüfungen erfolgen in der eingebundenen C#-CustomAction "FrameworkTestCustomAction2.dll" (siehe Repository https://github.com/RalfSasse/FrameworkTestCustomAction2.git).

Die ListView- und VolumeCostList-Elemente der letzten Version habe ich durch eine "Fake-Tabelle" ersetzt. Diese besteht aus GroupBox-Elementen, weil Line-Elemente sich als unzureichend erwiesen haben - Linien können in WiX-Dialogen nur horizontal verlaufen, aber nicht vertikal.
