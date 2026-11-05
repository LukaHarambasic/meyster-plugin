---
name: meyster
description: "Arbeit in Meyster, der Software für Handwerksbetriebe: Angebote und Rechnungen als Entwürfe, Kunden, Projekte, Katalog, Materialpreise und Fragen zur Bedienung. Use whenever the user mentions Meyster, or a quote (Angebot), invoice (Rechnung), customer (Kunde) or project (Projekt) of their trade business."
---

# Meyster

Meyster ist die Software des Handwerksbetriebs, für den der Nutzer arbeitet. Der Connector `meyster` gibt Dir ihre Werkzeuge. Sie handeln als der Nutzer, mit genau den Rechten seiner Rolle in Meyster.

Damit Du so arbeitest wie der Assistent in Meyster selbst:

1. Liegen Dir die Server-Anweisungen von Meyster nicht vor, lädst Du zuerst mit dem Werkzeug `load_skill` den Skill `meyster-basics`. Er enthält die Regeln des Assistenten, die Beschreibung des Betriebs und dessen eigene Regeln.
2. Vor jeder Aufgabe lädst Du mit `load_skill` den passenden Skill und befolgst ihn:
- `meyster-basics`: die Grundregeln von Meyster, die Beschreibung und die eigenen Regeln des Betriebs. Lade sie zuerst, wenn Dir die Server-Anweisungen von Meyster nicht vorliegen.
- `draft-workflow`: vor einem neuen Angebot oder einer neuen Rechnung: Struktur planen, Katalog nutzen, Mengen berechnen, Entwurf anlegen und übergeben.
- `document-edit`: vor einer Änderung an einem bestehenden Angebot oder einer bestehenden Rechnung: IDs, Kundenwechsel, Sperrregeln, Prüfungsschritt.
- `creation-guidance`: vor dem Anlegen eines Kunden oder Projekts: Pflichtfelder, Typerkennung, Duplikate.
- `help-center`: bei Fragen zur Bedienung von Meyster, zu Regeln, Einstellungen, Begriffen und rechtlichen Hintergründen.
3. Jedes Werkzeug sagt in seiner Beschreibung, wann und wie Du es nutzt.

Fertigstellen, Nummerieren, Versenden und Stornieren macht der Nutzer immer selbst in Meyster. Ein Entwurf liefert einen reviewUrl: diesen Link gibst Du ihm.
