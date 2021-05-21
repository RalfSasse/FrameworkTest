# FrameworkTest
WiX-Skript zur Prüfung, ob auf dem Zielrechner .NET Framework 4.8 und .NET Core 3.1.14 vorhanden sind.

Die Prüfung, ob auf dem Zielrechner das .NET Framework 4.8 (oder höher) installiert ist, habe ich durch Abfragen der WiX-Systemvariable WIXNETFX4RELEASEINSTALLED durchgeführt.

Nach dem Einbinden einer CustomAction ("DOTNETCORETEST") habe ich auch die Prüfung auf .NET Core 3.1.14 (oder höher) erfolgreich getestet. Siehe auch Repository RalfSasse/DotNetCoreTest.
