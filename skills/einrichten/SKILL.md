---
name: einrichten
description: Set up and check the Meyster connection after installing the plugin. Use right after installation, or when a Meyster tool fails because the connection is missing, switched off or not approved.
---

# Meyster einrichten

Help the member connect their Meyster account and confirm that it works.

## What the member needs

- A Meyster account at https://meyster.work.
- The company owner has switched on "KI-Apps verbinden (MCP)" under Firmeneinstellungen, Automatisierung. Without it every tool call is refused.
- On the first call, a Meyster consent page opens. The member signs in and approves the app there. Meyster marks the app as verified when it is Claude or ChatGPT.

## Steps

1. Call `get_current_time` to check that the connection answers.
2. Call `get_entity_details` with `entityType` "company" and tell the member which company is connected, by name.
3. If a call is refused because the connector is off, tell the member to ask the company owner to switch on "KI-Apps verbinden (MCP)", and link https://meyster.work/hilfe/ki-verbindungen.
4. If the member is not signed in, tell them the consent page opens on the next call, and to sign in with their Meyster login.
5. Close with three things they can try, in German:
   - "Erstelle ein Angebot für ..." to draft a quote.
   - "Zeig mir die offenen Rechnungen von diesem Monat."
   - "Zeig mir den Kunden ..." to see a customer card.

## Rules

- Never ask for the member's password in the chat. Sign in happens only on the Meyster page.
- The connection drafts and reads. Finalizing, numbering, sending and cancelling a document always happen in Meyster.
- The member can disconnect the app at any time in the Meyster company settings.
