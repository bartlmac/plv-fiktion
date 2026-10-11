# Verzeichnis der Belege

<nav class="kopf"><a href="../../">← Startseite</a><a href="../">← Bestandsmigrationen</a><a href="./">← Die Übernahme</a></nav>


Jeder Bericht steht bei der Station der [Übernahme](./), an der er
entsteht. Hier stehen alle noch einmal beisammen, für den,
der einen bestimmten sucht.

| Bericht | Station |
|---|---|
| [Übernommener Bestand zum Stichtag](artefakte/abgeleitet/berichte/bestandsbericht-vor.html) | [Station 8 · Bestand prüfen](./#bestand-pruefen) |
| [A-M1 Stichtagstest](artefakte/abgeleitet/berichte/aktuartest.html) | [Station 9 · Stichtag prüfen](./#stichtag-pruefen) |
| [A-M2 Verlaufstest](artefakte/abgeleitet/berichte/aktuartest-A-M2.html) | [Station 10 · Verlauf prüfen](./#verlauf-pruefen) |
| [A-M3 Geschäftsvorfalltest](artefakte/abgeleitet/berichte/aktuartest-A-M3.html) | [Station 11 · Geschäftsvorfälle prüfen](./#geschaeftsvorfaelle-pruefen) |
| [A-M4 Migrationscontrolling](artefakte/abgeleitet/berichte/migrationsabnahme.html) | [Station 12 · Migrationscontrolling](./#migrationscontrolling) |

149 Dateien unter `artefakte/`. Welche Datei an welche Station gehört, ist aus der Belegkette des Falls erhoben — aus dem, was jedes Prüfprotokoll gelesen und geschrieben hat, und aus den Prüfsummen, die jeder Entscheid bindet:

* [Station 1 · Auftrag und Lieferung](./#die-lieferung) — 33 Dateien, dazu 1 nicht veröffentlicht
* [Station 2 · Quellen lesen](./#quellen-lesen) — 24 Dateien
* [Station 3 · Quellen zusammenführen](./#quellen-zusammenfuehren) — 3 Dateien
* [Station 4 · Faktenbasis prüfen](./#faktenbasis-pruefen) — 3 Dateien
* [Station 5 · Quellen abnehmen](./#der-widerspruch) — 5 Dateien
* [Station 6 · Bestand übersetzen](./#die-uebersetzung-der-daten) — 2 Dateien
* [Station 7 · Rechenkern gegen den Quellrechner](./#rechenkern-gegen-quellrechner) — 16 Dateien
* [Station 8 · Bestand prüfen](./#bestand-pruefen) — 19 Dateien
* [Station 9 · Stichtag prüfen](./#stichtag-pruefen) — 7 Dateien
* [Station 10 · Verlauf prüfen](./#verlauf-pruefen) — 7 Dateien
* [Station 11 · Geschäftsvorfälle prüfen](./#geschaeftsvorfaelle-pruefen) — 7 Dateien
* [Station 12 · Migrationscontrolling](./#migrationscontrolling) — 10 Dateien
* [Station 13 · Zugang in die Bücher](./#der-bestand) — 10 Dateien
* `lieferung` — Ansichten der gelieferten Dateien (22 Dateien)
* [`abgeleitet/aufwand.json`](artefakte/abgeleitet/aufwand.json) — gelesen von dieser Darstellung, keiner Station der Kette zugeordnet
* [`abgeleitet/schichten/verankerung_schichten.json`](artefakte/abgeleitet/schichten/verankerung_schichten.json) — gelesen von dieser Darstellung, keiner Station der Kette zugeordnet

## Bereinigt veröffentlicht {#bereinigt}

13 Dateien tragen im Fall Pfade des Rechners, auf dem der Lauf lief. Veröffentlicht sind sie mit benannten Platzhaltern — `<baum>` für den Arbeitsbaum, in dem der Fall liegt, `<schluesselverzeichnis>` für das Verzeichnis des Schlüsselmaterials, `<welt>` für die Laufzeitumgebung — und darum nicht bytegleich mit dem Original. Je Datei nennt das [Bereinigungsmanifest](artefakte/bereinigung.json) die Prüfsumme des Originals im Fall, die Entscheide, die dieses Original über seine Prüfsumme binden, die Prüfsumme der veröffentlichten Fassung und die Ersetzungen; 10 der 13 Originale bindet kein Entscheid. Alle übrigen Belege unter `artefakte/` sind bytegleich mit ihren Originalen im Fall; die Ansichten der Lieferung sind Ansichten — eine CSV als Vorschau ihrer ersten Zeilen, alles Übrige bytegleich.

| Datei | Original im Fall | gebunden von | veröffentlicht | ersetzt |
|---|---|---|---|---|
| [`abgeleitet/berichte/zugangsprobe.json`](artefakte/abgeleitet/berichte/zugangsprobe.json) | `073fb02dc438f99d…` | <span class="kennung">A-B2</span> | `0e4563e277b2cf0e…` | <span class="kennung">`<baum>` ×1</span> |
| [`abgeleitet/diagnostics/abnahmebericht.gate.json`](artefakte/abgeleitet/diagnostics/abnahmebericht.gate.json) | `acbee802ce9db2c4…` | <span class="kennung">A-B1</span>, <span class="kennung">A-B2</span>, <span class="kennung">A-M1</span>, <span class="kennung">A-M2</span>, <span class="kennung">A-M3</span>, <span class="kennung">A-M4</span>, <span class="kennung">A-Q1</span>, <span class="kennung">A-T1</span> | `9364cfcace72d654…` | <span class="kennung">`<baum>` ×1</span> |
| [`abgeleitet/diagnostics/gate_entscheid_ab1.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ab1.gate.json) | `4001ce3b8c4fb03b…` | keinem Entscheid | `bd852587ddbce529…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_ab2.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ab2.gate.json) | `9d246aeffd9a46e8…` | keinem Entscheid | `d52646d3eeaaee42…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_ak2.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ak2.gate.json) | `6effe2bd192f5eb2…` | keinem Entscheid | `5e0b9564d238b9fc…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_am1.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am1.gate.json) | `fa14e9b7e577eec6…` | keinem Entscheid | `0fa1d5efd713c62a…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_am2.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am2.gate.json) | `1748ca86e051385a…` | keinem Entscheid | `e9b0dcefcf015c24…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_am3.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am3.gate.json) | `4794d67c1a3b6971…` | keinem Entscheid | `576be8114694e687…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_am4.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am4.gate.json) | `5a6fec29ff5f4d7d…` | keinem Entscheid | `05aee8fece93ddac…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_am6.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am6.gate.json) | `0e9be969e382d28e…` | keinem Entscheid | `eb993498603ef106…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_aq1.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_aq1.gate.json) | `b8649b8d21ee736d…` | keinem Entscheid | `a853f700cbbcf833…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`abgeleitet/diagnostics/gate_entscheid_at1.gate.json`](artefakte/abgeleitet/diagnostics/gate_entscheid_at1.gate.json) | `d2e0b5d7902f2db8…` | keinem Entscheid | `b28b39d83e353583…` | <span class="kennung">`<baum>` ×3</span>, <span class="kennung">`<schluesselverzeichnis>` ×1</span>, <span class="kennung">`<welt>` ×2</span> |
| [`eingang.json`](artefakte/eingang.json) | `1cd21fb78c7a49c2…` | <span class="kennung">A-B1</span>, <span class="kennung">A-B2</span>, <span class="kennung">A-K2</span>, <span class="kennung">A-M1</span>, <span class="kennung">A-M2</span>, <span class="kennung">A-M3</span>, <span class="kennung">A-M4</span>, <span class="kennung">A-M6</span>, <span class="kennung">A-Q1</span>, <span class="kennung">A-T1</span> | `d9694050cea50062…` | <span class="kennung">`<baum>` ×12</span>, <span class="kennung">`<welt>` ×9</span> |

Nicht veröffentlicht: `entscheide/A-M6-fc3d42a8f0dff08385c0dfad9c64a664e522fb17228ff7dacc1a263a51a7965b.json` — ein überholter Entscheid-Snapshot mit einer vertraulichen Angabe; Prüfsumme der Datei `ae39704d90faf8ddf12c2edd3b69e5fca641f2726e8e5b90290d707995dce353`. Ein Snapshot wird nie bereinigt, weil eine Änderung seine Signatur und die Verweise der Folgeentscheide bräche.

Nicht auf dieser Seite: 132 Dateien des Falls, die keine Station trägt — Arbeitsunterlagen der Agenten (Protokolle, Messungen, Übergaben) und überholte Zwischenstände. Sie sind nicht Teil der Belegkette.

Außerhalb des Falls gelesen: `src/rechner_pipeline/kern/tafeln.xml` (P-K1) — eine Datei des Systemstands, nicht des Falls.

## Alle Prüfläufe und ihre Ledger {#wie-es-lief}

19 Prüfschritte, 42 Anläufe bis zum
Urteil. Die Seite der Übernahme nennt je Station den Lauf, der zählt; hier
stehen alle, auch die 10 Entscheid-Gates, die je
Entscheid-Runde ein eigenes Ledger schreiben.

| Prüfschritt | Anläufe | Urteil | Ledger |
|---|---:|---|---|
| P-Q1.quellfragment | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/extract.gate.json) |
| entscheid.A-M6 | 6 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am6.gate.json) |
| P-Q2.zusammenfuehrung | 4 | passed | [`json`](artefakte/abgeleitet/diagnostics/abox_merge.gate.json) |
| P-Q3.fachliche-pruefung | 6 | passed | [`json`](artefakte/abgeleitet/diagnostics/abox_validate.gate.json) |
| entscheid.A-K2 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ak2.gate.json) |
| P-K1.generations-golden-master | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/generation_golden.gate.json) |
| P-B1.bestandspruefung | 5 | passed | [`json`](artefakte/abgeleitet/diagnostics/bestand_validate.gate.json) |
| A-M4.migrationscontrolling | 3 | passed | [`json`](artefakte/abgeleitet/diagnostics/abnahmebericht.gate.json) |
| A-M1.stichtagstest | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/aktuartest.gate.json) |
| A-M2.verlaufstest | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/aktuartest-A-M2.gate.json) |
| A-M3.geschaeftsvorfalltest | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/aktuartest-A-M3.gate.json) |
| entscheid.A-Q1 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_aq1.gate.json) |
| entscheid.A-M1 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am1.gate.json) |
| entscheid.A-M2 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am2.gate.json) |
| entscheid.A-M3 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am3.gate.json) |
| entscheid.A-T1 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_at1.gate.json) |
| entscheid.A-M4 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_am4.gate.json) |
| entscheid.A-B2 | 1 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ab2.gate.json) |
| entscheid.A-B1 | 5 | passed | [`json`](artefakte/abgeleitet/diagnostics/gate_entscheid_ab1.gate.json) |

## Die Entscheid-Snapshots {#zeichnungen}

18 Entscheid-Snapshots liegen im Fall, 10 davon geltend —
je Gate einer; die übrigen sind Runden, die durch Korrekturen
überholt wurden und erhalten bleiben. Je Snapshot Gate,
Entscheid, Rolle und Prüfstand:
[Die Entscheid-Snapshots der Gates](entscheide.html).


<div class="fuss-fiktion">Fiktives Unternehmen — <a href="../../hinter-den-kulissen/">Hinter den Kulissen</a></div>

*Erzeugt am 2026-10-11 aus dem Systemstand `70e3934acd7d`.*

