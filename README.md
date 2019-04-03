Tic Tac Tiptoi
==============

Dies ist ein kleines Demo-Projekt für Tiptoi-Basteleien mit dem [tttool]: Ein
Tic-Tac-Toe-Spiel.

[tttool]: http://tttool.entropia.de/

In der Datei `tic-tac-tiptoi.yaml` wird die Logik des Spieles definiert: Für
jedes der neun Felder speichern wir in einem Register (z.B. `$OL` für das Feld
oben links), ob es leer ist (`$OL == 0`), ob hier ein Kreuz ist (`$OL == 1`)
oder ein Kreis (`$OL == 2`). Das Register `$turn` gibt an welcher Spieler dran
ist. Und um schnell erkennen zu können, wenn das Feld voll ist, zählen wir in
`$set` mit, wie viele Felder voll sind.

Mit dieser Übersicht sollte sich der restliche Code ergeben.

Das Programm erlaubt dass man schummelt: Tippt ein Spieler schnell auf mehrere
Felder, bevor das Ende von `win_check` erreicht ist, so kann er mehrere Felder
füllen. Das kann man lösen indem man `$turn` schon in `feldOL`… neu setzt, aber
das macht das Programm großer.
