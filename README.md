# AgentShield 2040 — Your AI. Your Rules.

A product prototype for the Flipkart Associate Product Manager case competition. Core message: **Your AI suggests. You decide.**

In 2040, personal AI agents shop, pay bills and manage calendars. AgentShield is a governance layer that lets a user monitor, understand, restrict and override those agents.

## Open it
Double-click `index.html`. No server, install, internet connection, CDN or external API is needed (HTML5 + CSS3 + vanilla JavaScript only).

## Features
- **Command Center** — animated stats, autonomy gauge, agent cards (click for permissions), activity timeline, attention alert with Review / Reject.
- **Activity Monitor** — 12 records, status chips, search, agent and date filters, decision-report modal with Approve / Reject, and a "Simulate a new AI action" panel to test rules.
- **Autonomy Control** — Observer / Assisted / Autonomous modes (scores 20 / 64 / 88), spending-limit slider with validation, approval rules, Save button.
- **Privacy Vault** — six data categories with live toggles; disabled categories block simulated actions that need them.
- **Risk Intelligence** — demonstration risk gauge, risk breakdown, SVG trend chart, recommendations that navigate to the relevant screen.
- **Emergency Control** — confirmed suspend and restore flow; the event is logged and previous permissions are preserved.
- **Settings** — reset all data or reset only the guided demo.

The autonomy score measures how much authority is delegated to AI, not how safe it is.

## Guided demonstration
Click **▶ Experience AgentShield in Action** on the Command Center:
1. ShopMate AI attempts an ₹8,999 purchase.
2. AgentShield runs an animated policy check against your current limit and rules.
3. The purchase is paused: human approval required.
4. The decision is explained: reasoning, data used, sponsorship disclosure (simulated), policy.
5. You approve or reject.
6. Status, timeline and counters update everywhere.
7. "Your AI suggested. You decided."

**Reset Demo** restores only the demo transaction to Pending; privacy and autonomy settings are untouched. If you raise the limit above ₹8,999 (or a rule blocks the purchase), the demo shows the corresponding outcome instead.

## Persistence
Mode, limit, rules, permissions, activity and emergency state are saved in `localStorage` under `agentshield2040`. Corrupted or missing data falls back to defaults.

## Important: security is simulated
All agents, transactions, security events and risk scores are simulated. No payments are made, no financial accounts are connected, and the prototype cannot stop any real external AI agent. A production system would need external integrations and enforceable authorization mechanisms.

## Files
`index.html` (structure) · `style.css` (design system) · `script.js` (state, policy engine, demo, persistence)
