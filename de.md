# Data Dictionary Minimal Information Model - DDMIM
Medizinische Daten werden in unterschiedlichen Szenarien, in unterschiedlichem Umfang und in unterschiedlichen Formaten erhoben und verarbeitet. Um als Außenstehender einen ausreichenden Eindruck über diese Daten und deren Bedeutung zu erhalten, kann ein Data Dictionary oder auch Codebook hinzugezogen werden. Diese sind jedoch nicht immer vorhanden und wenn, dann oftmals nicht standardisiert, sowohl bezogen auf den Inhalt als auch die Struktur.

Ziel dieses Workshops ist die Erarbeitung eines Minimalen Informationsmodells für Data Dictionaries, d.h. einem Vokabular aus konsentierten Konzepten und Vorschlägen zur Obligation. Dazu sollen existierende Data Dictionaries untersucht und extrahierte Konzepte diskutiert werden. Gemeinsam mit relevanten Experten wie Medizinischen Dokumentaren, Medical Data Scientists, Medizininformatikern und Biometrikern wollen wir diskutieren, wie die Mindestanforderungen an ein solches Informationsmodell Data Dictionary lauten sollten. Auch Fragen des Aufwands der manuellen Erstellung solcher Data Dictionaries für die Forscher sind relevant.

Langfristig soll ein formales Modell unter Berücksichtigung existierender Standards und Systeme erstellt, in einer breiten Community konsentiert und mit relevanten Stakeholdern abgestimmt werden.



### Modul Kern:
Minimale Informationen, um ein Datenelement zu beschreiben.

| Attributname | Beschreibung | Kardinalität |
|--------------|-------------|----------------|
| Identifikator | Ein Identifikator des Datenelements, der in der Sammlung eindeutig ist. |  1..1 |
| Kurzbezeichnung | Ein aussagekräftiger Name für das Datenelement (wird häufig als Label verwendet). | 1..1 |
| Langbeschreibung | Eine ausführliche Beschreibung mit allen relevanten Informationen, die eine korrekte Interpretation, insbesondere für Dritte, ermöglichen. | 1..1 |


### Modul Datenqualität:
Minimale Informationen um die Datenqualitätsaspekte eines Datenelementes zu beschreiben.

| Attributname | Beschreibung | Kardinalität |
|--------------|-------------|----------------|
| Datentyp | Der Datentyp des Datenelement-Wertes, z.B. Numerisch, Text, Datum, ... |  1..1 |
| Wertebereich/ Format | Den Bereich der gültigen Werte für das Datenelement | 1..1 |
| Maßeinheit | Maßeinheit einer dem Wertebereich entsprechenden Ausprägung des Datenelementes, z.B. kg, cm; bestenfalls standardisiert, z.B. UCUM | 0..1 |



### Modul Terminologie:
Zur Vermeidung von Interpretationsfehlern und Vereinfachung von maschineller Verarbeitung ist die Annotation von  eindeutigen Codes hilfreich.

| Attributname | Beschreibung | Kardinalität |
|--------------|-------------|----------------|
| System, Code | Eine Liste von Codes, die die durch das Datenelement repräsentierte Information innerhalb eines Begriffssystems einordnen, unter Angabe des jeweils dazugehörigen Kodierungssystems (z.B. Terminologie wie Snomed CT, Klassifikation wie ICD-10) |  0..n |
