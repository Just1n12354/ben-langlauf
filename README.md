# Ben-Langlauf — sechs Stunden unbeaufsichtigt

Ein lokal laufender KI-Agent bekam eine Liste offener Programmieraufgaben und
sechs Stunden Zeit. Kein Mensch hat eingegriffen. Jede Aufgabe gilt erst als
gelöst, wenn ein unabhängiger Testlauf sie bestätigt — nicht, wenn der Agent
das behauptet.

**→ [Alle 376 Aufgaben ansehen](https://just1n12354.github.io/ben-langlauf/)**
**→ [Als PDF, 87 Seiten](https://just1n12354.github.io/ben-langlauf/ben-6-stunden.pdf)**

| | |
|---|---:|
| gelöste Aufgaben | 376 |
| Fehlschläge | 0 |
| Zeilen Code | 5 341 |
| davon in den 68 einzeln geschriebenen | 1 644 |
| Median je Aufgabe | 52 s |
| manipulierte Tests | 0 |

## Was das ist

Ein Prüfstand aus Modulen, die nichts tun ausser einen Fehler zu werfen, und je
einem Test dazu. Der Test ist die Spezifikation und für den Agenten tabu. Pro
Aufgabe startet ein frischer Agentendurchgang; danach führt der Rahmen den
Abnahmebefehl **noch einmal selbst** aus. Nur dieser zweite, unabhängige Lauf
entscheidet.

## Was das nicht ist

Kleine, klar umrissene Aufgaben: eine Datei, eine Funktion, ein Test der genau
sagt, was richtig ist. Das ist etwas anderes als Arbeit in einem gewachsenen
System mit unklaren Anforderungen. 308 der 376 Aufgaben sind Varianten aus fünf
Familien — der Lauf belegt Ausdauer, die Bandbreite belegt eher der Teil mit den
68 verschiedenen Aufgaben.

Ein späterer Lauf über zwölf Stunden ist durchgefallen: der Agent schrieb eine
Endlosschleife und bemerkte sie auch im zweiten Anlauf nicht. Und ein Teil der
gefundenen Fehler lag am Prüfstand, nicht am Agenten. Wer Agenten misst, misst
zuerst sein eigenes Messgerät.

## Aufbau

Modell `Qwen3.8-27B`, lokal auf einer NVIDIA GB10. Agentenrahmen: Hermes.
Keine Cloud, keine API.
