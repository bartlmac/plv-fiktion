# Techstack

<nav class="kopf"><a href="../">← Startseite</a><a href="./">← IT</a></nav>

Sprache, Bibliotheken und Versionen des Systems, wie sie
im Betrieb gepinnt sind.

Python >=3.11, keine
Laufzeit-Abhaengigkeit zu Office-Produkten oder zu
KI-Diensten: Der Rechenkern und alle Gates laufen ohne
Netz. Versionen exakt gepinnt:

| Laufzeit | Version |
|---|---|
| `openpyxl` | 3.1.5 |
| `oletools` | 0.60.2 |
| `pandas` | 2.3.3 |
| `pyarrow` | 25.0.1 |
| `matplotlib` | 3.11.1 |
| `pydantic` | 2.13.4 |
| `pypdf` | 6.19.0 |

| Entwicklung | Version |
|---|---|
| `pytest` | 9.0.3 |
| `hypothesis` | 6.155.5 |
| `pytest-xdist` | 3.6.1 |

Die KI-Agenten arbeiten AUSSERHALB dieser Laufzeit: Sie lesen
Lieferungen und schlagen vor; gerechnet und geurteilt wird
ausschliesslich im deterministischen Kern.

<div class="fuss-fiktion">Fiktives Unternehmen — <a href="../hinter-den-kulissen/">Hinter den Kulissen</a></div>
