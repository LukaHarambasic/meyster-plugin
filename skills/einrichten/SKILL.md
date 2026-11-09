---
name: einrichten
description: Die Verbindung zu Meyster nach der Installation einrichten und prüfen. Nutze den Skill direkt nach der Installation oder wenn ein Meyster-Werkzeug scheitert, weil die Verbindung fehlt, ausgeschaltet oder nicht bestätigt ist.
---

# Meyster einrichten

Hilf dem Nutzer, sein Meyster-Konto zu verbinden, und prüfe, dass die Verbindung funktioniert.

## Was der Nutzer braucht

- Ein Meyster-Konto unter https://meyster.work.
- Die Inhaberin oder der Inhaber des Betriebs hat unter Firmeneinstellungen, Automatisierung "KI-Apps verbinden (MCP)" eingeschaltet. Ohne diese Freigabe wird jeder Werkzeugaufruf abgelehnt.
- Beim ersten Aufruf öffnet sich eine Zustimmungsseite von Meyster. Dort meldet sich der Nutzer an und bestätigt die App. Meyster kennzeichnet die App als verifiziert, wenn es Claude oder ChatGPT ist.

## Schritte

1. Rufe `get_current_time` auf, um zu prüfen, dass die Verbindung antwortet.
2. Rufe `get_entity_details` mit `entityType` "company" auf und nenne dem Nutzer den Namen des verbundenen Betriebs.
3. Wird ein Aufruf abgelehnt, weil die Verbindung ausgeschaltet ist, bitte den Nutzer, die Inhaberin oder den Inhaber des Betriebs "KI-Apps verbinden (MCP)" einschalten zu lassen, und verlinke https://meyster.work/hilfe/ki-verbindungen.
4. Ist der Nutzer nicht angemeldet, sag ihm, dass sich die Zustimmungsseite beim nächsten Aufruf öffnet und er sich dort mit seinem Meyster-Zugang anmeldet.
5. Schließe mit drei Dingen, die er ausprobieren kann:
   - "Erstelle ein Angebot für ...", um ein Angebot zu entwerfen.
   - "Zeig mir die offenen Rechnungen von diesem Monat."
   - "Zeig mir den Kunden ...", um eine Kundenkarte zu sehen.

## Regeln

- Frag im Chat nie nach dem Passwort des Nutzers. Angemeldet wird nur auf der Seite von Meyster.
- Die Verbindung entwirft und liest. Fertigstellen, Nummerieren, Versenden und Stornieren eines Dokuments passieren immer in Meyster.
- Der Nutzer kann die App jederzeit in den Firmeneinstellungen von Meyster trennen.
