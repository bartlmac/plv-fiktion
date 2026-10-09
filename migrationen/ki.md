# Künstliche Intelligenz in unseren Migrationen

<nav class="kopf"><a href="../">← Startseite</a></nav>

Unsere Bestandsübernahmen werden von KI-Agenten vorbereitet. Sie lesen
die gelieferten Unterlagen, rechnen nach und legen vor. Urteilen tun
sie nicht: Das tun Prüfstrecken, die deterministisch laufen. Und
zeichnen tun sie erst recht nicht: Das tun Menschen, je Abnahme die
zuständige Rolle.

Diese Seite sagt, was die Agenten bei uns dürfen, und zeigt an der
Übernahme Baldrian, wie es aussieht.

## Was ein Agent darf und was nicht {#was-agenten-duerfen}

Der Unterschied zwischen Vorschlag und Urteil ist bei uns keine
Hausregel, sondern in der Bauart festgelegt: Ein Agent kann einen Lauf
ablehnen, aber keinen freigeben. Eine Freigabe braucht einen Schlüssel,
und Schlüssel haben Menschen. Wer gezeichnet hat, wird nicht behauptet,
sondern aus dem Schlüssel bestimmt, und jeder Entscheid-Snapshot trägt
Rolle und Schlüsselklasse. Ob je eine Agentenrolle einen Entscheid
trägt, ist an den Snapshots gemessen, nicht behauptet — die Antwort
muss nein lauten.

## Wer legt vor, wer zeichnet {#rollen}

Das KI-Werkzeug arbeitet mit Agentenrollen, versioniert mit Aufgabe,
Fähigkeiten und Werkzeugliste; die Liste unten ist aus den Definitionen
erhoben, nicht abgeschrieben. Jeder Agentenrolle steht eine menschliche
Rolle des Unternehmens gegenüber, die zeichnet — mit demselben Namen,
damit die Paarung ablesbar ist. Den Auftrag eines Falls zeichnet der
Vorstand; ihm steht kein Agent gegenüber. Danach: welche Fähigkeiten eine
Rolle hat (das sagt ihre Definition), womit das System die Unterlagen
liest, und welche Rolle welches Gate zeichnet — für die Gates der
Übernahme Baldrian sagt es der jeweilige Entscheid-Snapshot selbst.

<div class="rollen"><table class="agenten"><thead><tr><th>Agentenrolle</th><th>legt vor</th><th>Menschliche Rolle, die zeichnet</th></tr></thead><tbody><tr><td><b>Aktuariat</b><small>agent/aktuariat</small></td><td>bereitet alles vor, was das Aktuariat des aufnehmenden Unternehmens zeichnen muss: Feldabbildung, die drei aktuariellen Abnahmen, die Vorlage des Migrationscontrollings, die Fortführung des Bestands nach der Übernahme.</td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td></tr><tr><td><b>Architektur</b><small>agent/architektur</small></td><td>hält die Migration in der vorgeschriebenen Architektur: Schichten, Determinismus, Gate- und Ledger-Verträge, Beweiskette aus Prüfsummen, Snapshots und Manifesten, Sicherheitsgrenzen. Bereitet Architekturentscheide vor.</td><td><b>IT-Verantwortung</b><small>mensch/architektur</small></td></tr><tr><td><b>Betrieb</b><small>agent/betrieb</small></td><td>bereitet vor, was die Betriebsverantwortung für den Bestand zeichnen muss, den sie jeden Tag führt: die Zugangsprobe und die Vorlage der Zugangsabnahme A-B2, das Stands-Paket für die Auslieferung A-B1 und den Nachweis des Anfangsbestands eines neu eingerichteten Bestands für A-B3.</td><td><b>Betriebsverantwortung</b><small>mensch/betrieb</small></td></tr><tr><td><b>Programmleitung</b><small>agent/programmleitung</small></td><td>führt einen Migrationsfall von Anfang bis Ende, steuert die anderen Rollen durch die Stufen und hält an jedem menschlichen Gate an: Sie übergibt Entscheidungsvorlagen.</td><td><b>Programmleitung</b><small>mensch/programmleitung</small></td></tr><tr><td><b>Rechenkern</b><small>agent/rechenkern</small></td><td>die Entwicklungsrolle im Zielsystem: setzt beschlossene Änderungen am Rechenkern und Tarifparametrierungen um und hält Referenzwerte, Regressionstests und Dokumentation intakt.</td><td><b>Rechenkern-Verantwortung</b><small>mensch/rechenkern</small></td></tr></tbody></table><p class="quelle">Die Paarung steckt im Namen: Die Agentenrolle und die menschliche Rolle tragen dieselbe Kennung, nur die Ebene davor ist eine andere — <code>agent/rechenkern</code> legt vor, <code>mensch/rechenkern</code> zeichnet. Ohne Agenten-Gegenstück im Werkzeug: Vorstand (<code>mensch/vorstand</code>), Aktuar des abgebenden Hauses (<code>mensch/quell-aktuar</code>).</p><h3 id="faehigkeiten">Fähigkeiten</h3><p>11 versionierte Fähigkeiten; welche Rolle welche hat, sagt ihre Definition.</p><table class="faehigkeiten"><thead><tr><th>Fähigkeit</th><th>Rolle</th><th>was sie tut</th></tr></thead><tbody><tr><td><code>aktuartest-durchfuehren</code></td><td>Aktuariat</td><td>fährt die drei aktuariellen Abnahmen A-M1 bis A-M3 und bereitet je Abnahme die Entscheidungsvorlage auf</td></tr><tr><td><code>author-rechner-toolbox-gate</code></td><td>Architektur</td><td>entwirft den Vertrag eines neuen Prüfkommandos: eine Ausgabe, feste Rückgabewerte, ein Ledger-Eintrag</td></tr><tr><td><code>bereite-fachkonflikt-auf</code></td><td>Aktuariat</td><td>bereitet einen Widerspruch zwischen Unterlagen zur menschlichen Entscheidung auf: beide Lesarten, Auswirkung, Empfehlung</td></tr><tr><td><code>dokumentiere-system</code></td><td>Architektur, Rechenkern</td><td>hält die Dokumentation nach den Regeln des Systems nach: erzeugt schlägt handgeschrieben</td></tr><tr><td><code>entwickle-im-zielsystem</code></td><td>Architektur, Rechenkern</td><td>der Rahmen jeder Änderung am Zielsystem: Schichten, Determinismus, Test-Pflicht</td></tr><tr><td><code>extrahiere-quellfragment</code></td><td>Aktuariat</td><td>liest eine gelieferte Quelle (Tarifbeschreibung, Tarifrechner) in ein Quellfragment; was nicht belegt ist, bleibt offen statt geraten</td></tr><tr><td><code>integriere-migrationsinkrement</code></td><td>Architektur, Rechenkern</td><td>bringt Änderungen während eines laufenden Falls in kleinen, geprüften Schritten ein</td></tr><tr><td><code>migrationsfall-durchfuehren</code></td><td>Programmleitung</td><td>führt einen Fall durch die drei Stufen und hält an jedem menschlichen Gate an</td></tr><tr><td><code>pruefe-migrationscontrolling</code></td><td>Aktuariat</td><td>fährt das Controlling über zwei Stichtage und bereitet die Vorlage für A-M4 auf</td></tr><tr><td><code>teste-adversarial</code></td><td>Architektur, Rechenkern</td><td>prüft einen fertigen Block gegen den Strich: Befunde finden, widerlegen, als Regressionstest festhalten</td></tr><tr><td><code>transformiere-quellbestand</code></td><td>Aktuariat</td><td>schlägt die Abbildung des gelieferten Bestandsabzugs auf unser Datenmodell vor; jede Unklarheit wird ein offener Konflikt</td></tr></tbody></table><h3 id="werkzeuge">Werkzeuge</h3><p>Was eine Agentenrolle bedienen darf, legt ihre Definition fest — Aktuariat: lesen, suchen, Kommandos ausführen, schreiben, ändern; Architektur: lesen, suchen, Kommandos ausführen, schreiben, ändern; Betrieb: lesen, suchen, Kommandos ausführen, schreiben, ändern; Programmleitung: lesen, suchen, Kommandos ausführen, schreiben, ändern; Rechenkern: alle Werkzeuge. Womit das System die gelieferten Unterlagen liest, ist keine Frage der Rolle, sondern der Laufzeit: Dieselben Bibliotheken, gepinnt im <a href="../it/techstack.html">Techstack</a>, stehen jeder Rolle zur Verfügung.</p><table class="werkzeuge"><thead><tr><th>Bibliothek</th><th>eingesetzt für</th><th>verwendet in</th></tr></thead><tbody><tr><td><code>openpyxl</code><small>3.1.5</small></td><td>liest die gelieferten Excel-Tarifrechner (Zellen, Formeln, Namen)</td><td>1 Modul (<code>quellen/extract/openpyxl_backend</code>)</td></tr><tr><td><code>oletools</code><small>0.60.2</small></td><td>liest die VBA-Makros der Tarifrechner, ohne Excel</td><td>1 Modul (<code>quellen/extract/openpyxl_backend</code>)</td></tr><tr><td><code>pandas</code><small>2.3.3</small></td><td>hält Bestände, Journale und Abschlüsse als Tabellen</td><td>28 Modulen (<code>bestand/abschluss</code>, <code>bestand/auswertung</code>, …)</td></tr><tr><td><code>pyarrow</code><small>25.0.1</small></td><td>schreibt und liest die festgeschriebenen Abschlüsse (Parquet)</td><td>1 Modul (<code>bestand/parquet_io</code>)</td></tr><tr><td><code>matplotlib</code><small>3.11.1</small></td><td>zeichnet die Grafiken der Bestandsberichte</td><td>1 Modul (<code>bestand/report</code>)</td></tr><tr><td><code>pydantic</code><small>2.13.4</small></td><td>prüft die Form jeder Aussage der Faktenbasis</td><td>6 Modulen (<code>ontologie/aussage</code>, <code>ontologie/befuellung</code>, …)</td></tr><tr><td><code>pypdf</code><small>6.19.0</small></td><td>liest die gelieferten Tarifbeschreibungen und Mitteilungen (PDF)</td><td>1 Modul (<code>quellen/tarifplan_staging</code>)</td></tr></tbody></table><h3 id="gates-und-rollen">Wer welches Gate zeichnet</h3><table class="zeichnung"><thead><tr><th>Gate</th><th>zeichnet</th><th>in dieser Übernahme</th></tr></thead><tbody><tr><td><code>A-Q1</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-M1</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-M2</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-M3</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-M4</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-M5</code></td><td><b>Programmleitung</b><small>mensch/programmleitung</small></td><td><span class="platzhalter">kein Gegenstand dieser Übernahme</span></td></tr><tr><td><code>A-M6</code></td><td><b>Vorstand</b><small>mensch/vorstand</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/vorstand</code></td></tr><tr><td><code>A-O1</code></td><td><b>IT-Verantwortung</b><small>mensch/architektur</small></td><td><span class="platzhalter">kein Gegenstand dieser Übernahme</span></td></tr><tr><td><code>A-K2</code></td><td><b>Rechenkern-Verantwortung</b><small>mensch/rechenkern</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/rechenkern</code></td></tr><tr><td><code>A-T1</code></td><td><b>Verantwortlicher Aktuar</b><small>mensch/aktuariat</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/aktuariat</code></td></tr><tr><td><code>A-B1</code></td><td><b>Betriebsverantwortung</b><small>mensch/betrieb</small></td><td><b>angenommen</b> am 08.10.2026 durch <code>mensch/betrieb</code></td></tr><tr><td><code>A-B2</code></td><td><b>Betriebsverantwortung</b><small>mensch/betrieb</small></td><td><b>angenommen</b> am 02.10.2026 durch <code>mensch/betrieb</code></td></tr><tr><td><code>A-B3</code></td><td><b>Betriebsverantwortung</b><small>mensch/betrieb</small></td><td><span class="platzhalter">kein Gegenstand dieser Übernahme</span></td></tr></tbody></table><p class="pointe"><b>10 geltende Entscheide in diesem Fall, jeder von einer menschlichen Rolle, keiner mit der Schlüsselklasse agent</b> — gemessen an den Snapshots, nicht behauptet.</p></div>

Wo die Rollen im Ablauf stehen, zeigt [Der Prozess in dreizehn Stationen](./#prozess).

## Wie ein Gate heißt {#kennung}

Eine Bestandsübernahme durchläuft bei uns Stationen, und an den meisten
sitzt ein Gate. Sein Name ist eine Kennung aus vier Teilen:

<div class="kennung-zerlegung">
<span class="teil"><b>P</b><small>1</small></span><span class="trenner">-</span><span class="teil"><b>Q</b><small>2</small></span><span class="teil"><b>3</b><small>3</small></span><span class="trenner">.</span><span class="teil"><b>fachliche-pruefung</b><small>4</small></span>
</div>
<ol class="kennung-legende">
<li><b>Art</b>, wer entscheidet: P Prüfung durch das Programm · A Abnahme durch einen Menschen</li>
<li><b>Gegenstand</b>: Q Quellen · K Rechenkern · B Bestand · M Migration als Ganzes</li>
<li><b>Nummer</b>, laufend innerhalb des Gegenstands</li>
<li><b>Fachliche Kennung</b>, so steht sie im Ledger</li>
</ol>

Vor dem Bindestrich steht, wer entscheidet: **P** für eine Prüfung durch
das Programm, deterministisch, sie blockiert bei Rot; **A** für eine
Abnahme durch einen Menschen, der entscheidet und zeichnet, das Gate
erzeugt die Vorlage und hält den signierten Entscheid. Dahinter der
Gegenstand: **Q** Quellen, **K** Rechenkern, **B** Bestand, **M** die
Migration als Ganzes. Die Ziffer nummeriert innerhalb des Gegenstands.

Das Kontrastpaar macht die erste Stelle sofort verständlich: P-Q3 prüft
die Quellen maschinell, A-Q1 nimmt sie ab, gleicher Gegenstand, andere
Art, dort entscheidet und zeichnet ein Mensch. Die Nummern haben Lücken,
und das ist gewollt: Ein abgeschaltetes Gate hinterlässt eine Lücke, es
rückt nichts nach, sonst entstünde genau die Verwechslung, die diese
Ordnung abschaffen soll. Deshalb gibt es A-M1 und A-M4, und A-M2 und
A-M3 dazwischen sind eigene Gates.

## An einer gefahrenen Übernahme {#beispiel}

Wie das bei der Übernahme Baldrian aussieht — an jeder
Station das Gate, was es prüft, was es hinterlässt und was der Lauf dort
ergab —, zeigt [Die Übernahme Baldrian](baldrian/): eine Seite, von der
Lieferung bis zum Zugang in die Bücher, mit den Zahlen und Belegen jeder
Station.

## Feststellungen des Aktuariats {#feststellungen}

Die Feststellungen zu den gelieferten Unterlagen und die Entscheidung zu
jeder Diskrepanz stehen auf der Seite der Übernahme an der Station
[Quellen abnehmen](baldrian/#der-widerspruch), mit beiden Lesarten und
dem Dossier, das der Agent dafür vorgelegt hat; was sich durch die
Übernahme an Rechenkern und Tarifwerk geändert hat, unter [Was sich am
System änderte](baldrian/#umbau).

Zurück zum Verfahren: [Bestandsmigrationen](./).

<div class="fuss-fiktion">Fiktives Unternehmen — <a href="../hinter-den-kulissen/">Hinter den Kulissen</a></div>
