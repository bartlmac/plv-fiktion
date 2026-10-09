# Unsere Prüfgates

<nav class="kopf"><a href="../">← Startseite</a><a href="./">← Bestandsmigrationen</a></nav>

Jede Stufe einer Bestandsübernahme endet in einem Gate. Der Name
sagt, wer entscheidet und worüber: **P** ist eine Prüfung durch das
Programm — deterministisch, sie blockiert bei Rot, kein Mensch ist
beteiligt; **A** ist eine Abnahme durch einen Menschen — das Gate
erzeugt die Vorlage und hält den signierten Entscheid-Snapshot.
Der Buchstabe danach nennt den Gegenstand: **Q** Quellen und
Ontologie, **K** Rechenkern, **B** Bestand, **M** die Migration als
Ganzes. Die Nummer ist die Reihenfolge innerhalb des Gegenstands;
ein abgeschaltetes Gate hinterlässt eine Lücke, es rückt nichts nach.

Die Stufen: **1** Quellen werden zur Faktenbasis, **2** die
Faktenbasis wird zur Spezifikation und Parametrierung des
Rechenkerns, **3** Abnahme — Rechenkern, Bestand und die drei
aktuariellen Tests, zuletzt das Migrationscontrolling A-M4, das die
Belege aller vorangehenden Gates bindet.
Die Spalte Vorgänger nennt nur, was das Gate tatsächlich verlangt;
im Tarif-Scope weniger als im Bestands-Scope.

Die Tabelle stammt aus dem Gate-Register unseres Systems, nicht aus
einer Abschrift.

| Gate | Art | Stufe | Was geprüft bzw. abgenommen wird | Hinterlässt | Vorgänger (Tarif / Bestand) |
| --- | --- | ---: | --- | --- | --- |
| <span id="P-Q1"></span>**P-Q1** `quellfragment` | Prüfung durch das Programm | 1 | Ein geliefertes Quellwerk (Tarifrechner, Tarifbeschreibung) wird deterministisch vorverdichtet — nichts wird umgeschrieben oder ergänzt, derselbe Lauf ergibt dieselben Bytes — und die Extraktion geprüft: Manifest gültig, Eingaben nicht leer, Altstände entfernt. Dabei misst das Gate, ob die Quelle Sollwerte für die spätere Nachrechnung mitbringt (Erwartungswert-Abdeckung full, sparse, none). Das Fragment selbst deutet danach ein Modell; die Prüfung P-Q3 fängt die Deutung. | Extraktionsmanifest mit Prüfsummen und Erwartungswert-Abdeckung | — |
| <span id="P-Q2"></span>**P-Q2** `zusammenfuehrung` | Prüfung durch das Programm | 1 | Die Fragmente aller Quellen werden zu einer Faktenbasis zusammengeführt; widersprechen sich zwei Quellen, entsteht eine Diskrepanz — sie wird festgehalten, nicht aufgelöst. | Faktenbasis (A-Box) mit Diskrepanzen | — |
| <span id="P-Q3"></span>**P-Q3** `fachliche-pruefung` | Prüfung durch das Programm | 1 | Die Faktenbasis wird gegen den fachlichen Vertrag, das Eingangsregister und den Pflichtumfang geprüft; offene Diskrepanzen blockieren. | Ledger P-Q3 | — |
| <span id="A-Q1"></span>**A-Q1** `quellenabnahme` | Abnahme durch einen Menschen | 2 | Ein Mensch nimmt die aus den Quellen abgeleitete Fachspezifikation ab — einschließlich der Entscheide zu jeder Diskrepanz und der Abdeckung des Pflichtumfangs. | signierter Entscheid-Snapshot | — |
| <span id="A-M6"></span>**A-M6** `fallauftrag` | Abnahme durch einen Menschen | 1 | Der Vorstand beauftragt den Fall: wer ihn führt, was migriert wird, wer unter welchem Mandat zeichnet und auf welchem abgenommenen Stand des Zielsystems. Jede weitere Abnahme des Falls setzt den angenommenen Auftrag voraus. | Fallauftrag, Entscheid-Snapshot | — |
| <span id="A-O1"></span>**A-O1** `tbox-aenderung` | Abnahme durch einen Menschen | 2 | Ein Mensch nimmt den Stand der Ontologie ab — des Vertrags, auf den sich Quellen, Spezifikation und Rechenwerk beziehen. Einmal außerhalb jedes Falls (Erstabnahme), danach im Fall nur, was sich durch ihn ändert; sonst verweist der Fall auf die geltende Abnahme. | Entscheid-Snapshot oder Verweis auf die geltende Abnahme | — |
| <span id="A-T1"></span>**A-T1** `tarifwerk` | Abnahme durch einen Menschen | 2 | Ein Mensch nimmt das Tarifwerk ab — Tarifpläne und Parametrierung der eigenen Tarifgenerationen —, mit jedem geänderten Feld neben seinem alten Wert. | Änderungsbeleg des Tarifwerks, Entscheid-Snapshot | — |
| <span id="P-K1"></span>**P-K1** `generations-golden-master` | Prüfung durch das Programm | 3 | Der aus der Spezifikation parametrierte Rechenkern wird gegen die Erwartungswerte des Quellrechners gerechnet; je Generation entsteht ein inhaltsadressierter Beleg mit Faktenbasis- und Systemstand. | Golden-Master-Beleg je Generation | — |
| <span id="P-B1"></span>**P-B1** `bestandspruefung` | Prüfung durch das Programm | 3 | Der Bestand wird gegen seinen Vertrag geprüft: Stamm, Historie, Ledger und Scheiben passen zusammen, jede Buchung trägt ihren Betrag aus dem Rechenkern; im Tagesbetrieb die nächtliche Wache. | Ledger P-B1 | — |
| <span id="A-M1"></span>**A-M1** `stichtagstest` | Abnahme durch einen Menschen | 3 | Aktuarielle Abnahme am Stichtag: Test je Vertrag am eigenen Verankerungszeitpunkt auf einer belegten Stichprobe. | Testergebnis, Bericht, Entscheid-Snapshot | — |
| <span id="A-M2"></span>**A-M2** `verlaufstest` | Abnahme durch einen Menschen | 3 | Aktuarielle Abnahme des Verlaufs: die Deckungsrückstellung ueber die Laufzeit gegen die Referenz. | Testergebnis, Bericht, Entscheid-Snapshot | — |
| <span id="A-M3"></span>**A-M3** `geschaeftsvorfalltest` | Abnahme durch einen Menschen | 3 | Aktuarielle Abnahme der Geschäftsvorfälle: jeder Vorfall an der Änderung des Deckungskapitals, als Vollerhebung. | Testergebnis, Bericht, Entscheid-Snapshot | — |
| <span id="A-M4"></span>**A-M4** `migrationscontrolling` | Abnahme durch einen Menschen | 3 | Abschlussabnahme der Migration: bindet die Pflichtbelege aller vorangehenden Gates und prueft sie erneut auf demselben Eingangs-, Faktenbasis-, System- und Stichtagsstand. | Abnahmebericht, Entscheid-Snapshot mit Artefakt-Hashes | P-Q3, A-Q1, A-M1, P-K1, A-K2, A-O1, A-T1 / P-Q3, A-Q1, A-M1, A-M2, A-M3, P-K1, A-K2, A-O1, A-T1, P-B1 |
| <span id="A-K2"></span>**A-K2** `kernaenderung` | Abnahme durch einen Menschen | 3 | Ein Mensch nimmt den Stand des Rechenkerns ab, auf dem ein Fall rechnet — mit jeder Änderung seit der letzten Abnahme, je Modul. Der Regressionsbeleg sagt, was die Änderung für den laufenden Bestand bedeutet; solange sein Werkzeug fehlt, steht er als benannte Ausnahme im Beleg, nie als Urteil. | Änderungsbeleg des Kerns, Regressionsbeleg, Entscheid-Snapshot | — |
| <span id="A-M5"></span>**A-M5** `fallabbruch` | Abnahme durch einen Menschen | 3 | Das entschiedene Ende eines Falls ohne Abnahme: Die Programmleitung des Falls hält fest, warum er abgebrochen wird. Ein Fall endet mit der Migrationsabnahme oder mit diesem Entscheid, nicht im Sande. | Abbruchbeleg, Entscheid-Snapshot | — |
| <span id="A-B1"></span>**A-B1** `auslieferung` | Abnahme durch einen Menschen | 4 | Der Betrieb nimmt ab, dass ein Stand nach außen sichtbar wird. Die erste Abnahme der laufenden Linie statt eines Falls: Der Bestand wird täglich geführt, ob eine Migration läuft oder nicht. | signierter Entscheid-Snapshot | — |
| <span id="A-B2"></span>**A-B2** `zugangsabnahme` | Abnahme durch einen Menschen | 4 | Der Betrieb nimmt den Zugang eines abgenommenen Bestands in die geführte Ablage ab: Eine Zugangsprobe fährt auf einer Kopie der Ablage zwei Läufe, mit und ohne den Eingang, und vergleicht, was der Zugang bewirkt, mit dem, was abgenommen wurde — vor der Registrierung, nicht erst am ersten Monatsabschluss. | Zugangsprobe, Entscheid-Snapshot | — |
| <span id="A-B3"></span>**A-B3** `anfangsbestand` | Abnahme durch einen Menschen | 4 | Der Betrieb nimmt den Bestand ab, den eine neu aufgesetzte Ablage nach ihrem ersten Lauf führt — einmal, außerhalb jedes Falls. | Beleg des Anfangsbestands, Entscheid-Snapshot | — |

Wie die Gates in einem Fall gelaufen sind, zeigt die Seite der
jeweiligen Übernahme unter [Bestandsmigrationen](./): je Station
der Lauf, der zählt, und im Verzeichnis der Belege alle Prüfläufe
und Entscheide.
<div class="fuss-fiktion">Fiktives Unternehmen — <a href="../hinter-den-kulissen/">Hinter den Kulissen</a></div>
