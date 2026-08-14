# AI Systems Blueprint — Patel Heaters & Control Pvt. Ltd.

| | |
|---|---|
| **Prepared for** | Mitesh Patel, Director |
| **Business** | Industrial electrical heaters, RTD/thermocouples, control panels, ovens, blowers, sealing machines + electrical accessories trading — B2B, domestic & export |
| **Current stack** | Odoo ERP (Community) + Tally (billing) + ChatGPT (partial) + WhatsApp/Email |
| **Prepared by** | BuildOur AI |
| **Sources** | Systems Brief (submitted 01.08.2026) + audit call of 06.08.2026 (Zoom auto-transcript largely garbled on the Hindi discussion; legible portions covered onboarding logistics — a re-listen of the audio is recommended to recover the rest) |

---

## Executive Summary

Mitesh's brief describes a business that wins on repeat trust — roughly 70% regular customers, most re-ordering the same items — but runs on verbal follow-up: Mitesh personally present in every department, reminding people of tasks, digging out old specifications for repeat orders, and chasing payments. The stated vision is one window from inquiry to dispatch, where a customer, dealer, or supplier sees their own view and gets answers without a phone call into the factory.

This blueprint recommends eight systems in three phases. Phase 1 attacks the two leaks Mitesh called out as daily and uncountable: repeat-order lookups that delay dispatch by 2–3 days, and quotations that wait on manual technical calculation. A data-foundation track runs alongside, because the brief is honest about the gap: today only 2% of BOMs, 0% of drawings, and 40% of stock live in Odoo — and every automation below depends on that data existing. The target is the system running before the pre-winter heater season.

---

## 1. Current State: How Work Happens Today, and Where It Hurts

### 1.1 Inquiry and quoting
95% of inquiries arrive by email and WhatsApp; they're registered manually in Odoo. For repeat items, the team quotes from memory and confirms on WhatsApp or email. For new requirements, a product manager discusses specs, gets a drawing prepared, then quotes. Orders are noted in a register.

**Pain:** For repeat orders — the bulk of the business — the team spends too much time checking old specifications and past drawings. This happens almost every week and delays dispatch by two to three days, sometimes costing the follow-up order from that customer. Quotation pricing is calculated by hand every time.

### 1.2 Order-to-production handover
Once approved, the order is planned into production and accounts is informed — all manually.

**Pain:** "Taking too much time to take into process" — delivery delays start before production even begins. There is no system view of what stage an order is at, so answering a customer's status question means walking the floor.

### 1.3 Quality control and documentation
QC handles routine testing well, but when a customer requires detailed or advanced QC documentation, mistakes happen or a senior person must be physically present.

**Pain:** Non-standard QC documentation is a recurring weekly failure point. QC report creation is on Mitesh's "never want to manually do again" list.

### 1.4 Support and information access
Support staff can't answer customers directly — they relay questions to other departments because the ERP doesn't hold the information (drawings, BOMs, process status) and training is thin.

**Pain:** Every customer question becomes an internal relay race. This is why Mitesh pictures "1 window, 1 person or AI" answering inquiry-to-dispatch status.

### 1.5 Finance
Payment follow-up runs on reminders from Mitesh; purchase invoice entry is delayed.

**Pain:** Daily leak. Purchase bill entry and payment follow-ups are both on the "never again" list.

### 1.6 People, reporting, and accountability
No reporting system exists; responsibilities aren't written down. Mitesh must be 100% present in every department, reminding people of tasks verbally. Six senior people (Mitesh, Preet, Manan, Shyam, Anand, Tannu) each carry two jobs — supervisors also handle customer follow-ups, which slip by a day or two when production gets busy. The marketing hire has no reporting structure at all.

**Pain:** This is the reason Mitesh bought the program — his words: "people has no accountability and don't know their responsibilities... 100% has to be present in each and every department."

### 1.7 Data foundation (the honest picture)
In Odoo today: 100% billing and ledger, 95% quotes — but 20% customer database, 40% stock, 2% BOM, 0% drawings, 0% manufacturing process. Tally runs billing in parallel; Mitesh would consolidate to one system if old data transfers cleanly.

**Pain:** The automations Mitesh wants (instant repeat quotes, stock visibility, status answers) read from exactly the data that isn't in the system yet.

---

## 2. Recommended AI Systems

### System 1 — Repeat-Order Memory
**What it does:** For any regular customer inquiry, instantly retrieves their full history — past specs, drawings, prices, delivery times — and drafts the confirmation. For unchanged repeat orders from regular customers, it can confirm on its own (a decision Mitesh explicitly delegated to AI in the brief).
**Solves:** The #1 leak — weekly spec-hunting that delays dispatch 2–3 days (§1.1). Delivers the six-month finish line: "repeat orders confirmed within minutes instead of waiting for my team to check old files."

### System 2 — Auto-Quotation Engine
**What it does:** Inquiry data is punched in once; the system runs the technical calculations, prices the job, and produces a quotation in the standard format with terms and conditions attached.
**Solves:** Painkiller #1, verbatim from the brief. Manual price calculation is on the "never again" list.
**Guardrail:** Pricing for new customers always goes to a human before it leaves the building — Mitesh's explicit sign-off rule. Standard pricing to regular customers can go out directly.

### System 3 — One-Window Order Tracker & Status Agent
**What it does:** Every order carries its stage from inquiry to dispatch in the system. An AI agent answers status questions — from customers directly (Mitesh's comfort level allows this) and from support staff, ending the interdepartmental relay.
**Solves:** Painkiller #2 (§1.2, §1.4). Also sends proactive order-status updates, which the brief authorises AI to do autonomously.

### System 4 — QC Report Generator
**What it does:** QC formats are defined per product/parameter set; observed values are entered against them and the report compiles itself, including customer-specific advanced documentation requirements.
**Solves:** The weekly QC documentation failures (§1.3); "make QC reports" never again.
**Guardrail:** Dispatch clearance stays human. Calibration certificates stay internal unless approved for release.

### System 5 — Payments & Purchase-Bill Automation
**What it does:** Automatic payment follow-up sequences on outstanding invoices with a collection dashboard; inward purchase invoices captured and entered without manual typing.
**Solves:** The daily finance leak (§1.5) and two "never again" items.

### System 6 — Task, Reporting & Accountability System
**What it does:** Every task is assigned in the system with an owner and deadline; reminders go out automatically; daily/weekly reports reach the concerned manager without being asked; performance evaluation builds from completion data. Includes a simple reporting frame for the marketing role.
**Solves:** The core reason for the purchase (§1.6) — replaces verbal follow-up and Mitesh's everywhere-presence. Mistake protocol per the brief: anything uncertain is marked "needs review" and routed to staff, never confirmed to a customer.

### System 7 — Dealer, Distributor & Supplier Windows
**What it does:** Access-controlled portals: dealers and distributors see stock, prices, and delivery estimates from anywhere; registered suppliers receive RFQs, fill in price and delivery, and orders assign based on the customer's expectations — the flow Mitesh described in his vision.
**Solves:** The "everyone calls the factory" problem at the network level, after the internal single window (System 3) is proven.

### System 8 — Training Module Builder
**What it does:** Converts each department's now-documented processes into standardized training modules with photos and video, so staff, suppliers, dealers, and distributors learn their window without verbal instruction.
**Solves:** Mitesh's 3-month training deadline, and protects the guardrail he set: AI helps staff work faster and trains them — it does not replace them.

---

## 3. Implementation Roadmap

Mitesh can invest 6 hours/week personally, so the build leans on delegation: **Tannu is the natural internal champion** — she already owns Odoo CRM with a team of 8, and that team is the engine for the data-foundation track. Mitesh's hours go to approvals, guardrail decisions, and a weekly review. Odoo and Tally both stay running until one system has proven it can replace them with old data intact (Mitesh's stated condition).

The "no verbal work communication" rule rolls out **one department at a time** — Sales/CRM first (Tannu's home turf), then Dispatch, then Accounts, then Production/QC — rather than everywhere at once, so a team that tends to "stick at one place" with new tools is never asked to change everything in one go.

### Track 0 — Data Foundation (starts immediately, runs through all phases)
Get customer database, BOMs, drawings, stock, and process stages into the system — prioritised by what Phase 1 needs first: the top ~repeat customers' specs and drawings, then stock, then the rest. Without this track, every system below stalls.

### Phase 1 — Repeat Orders & Quotations (the daily bleeding)
Systems **1, 2, 3**: repeat-order memory, auto-quotation, order tracking with the status agent.
**Done when:** a regular customer's repeat order is confirmed in minutes; a new inquiry gets a calculated, formatted quote the same day with human approval where required; nobody walks the floor to answer "where is my order?"

### Phase 2 — Quality, Money & Accountability
Systems **4, 5, 6**: QC report generation, payment/purchase automation, task and reporting system.
**Done when:** advanced QC documentation goes out without a senior person standing over it; payment follow-ups run without reminders from Mitesh; every department reports to its manager on time without being asked.

### Phase 3 — The Network & the Season
Systems **7, 8**: dealer/distributor/supplier windows, training modules — plus the customer-relationship layer from Painkiller #3 (marketing updates, birthday messages, regular customer touchpoints).
**Done when:** the system is live and the team comfortable on it before the pre-winter order season — Mitesh's stated deadline.

---

## 4. Guardrails (set by Mitesh, enforced by design)

- **AI may act alone:** confirm repeat orders from regular customers, share standard pricing and specs, send order status updates, message customers directly.
- **Always human sign-off:** final technical drawing approval for custom control panels, pricing quotes for new customers, dispatch clearance for finished goods.
- **Never shared by AI:** customer-specific drawings, custom panel designs, special pricing given to regular clients; RTD/thermocouple calibration certificates stay internal unless approved.
- **On uncertainty:** the AI confirms nothing — it marks the order "needs review" and notifies office staff before any customer response.
- **People:** the system trains and accelerates staff, including senior technicians; it does not replace them.

---

## 5. Numbers to Confirm at the Next Call

The brief's volumes (≈1,200 leads and ≈900 quotes/orders per month, 70% repeat customers, sales cycle from 2 days to 2 months) point to a high-volume, fast-turn business — which is exactly why per-order manual work hurts. Three figures need confirming before they anchor any sizing decision, as the brief entries appear to be typos:

1. **Average order value** (entered as "1000020000" — likely a ₹10,000–₹20,000 range).
2. **Quote-to-order conversion** (entered as "750 out of 100").
3. **Total headcount** (entered as ~13, but the team map lists closer to 75–80 people across production, QC, stores, and office, and the functional split sums to 78).

---

## 6. Dependencies & Risks

- **Data debt is the biggest risk.** Drawings 0%, BOM 2%, customer database 20%, stock 40% in Odoo. Every system above reads from this data; Track 0 is not optional and Phase 1 fails without it.
- **WhatsApp Business API.** Automated customer messaging requires an official WhatsApp Business number — inquiries must migrate off personal numbers of Mitesh and the managers.
- **Odoo Community limits.** Confirm the version, hosting, and which modules are actually live; manufacturing stages and external portals may need community add-ons or custom development.
- **Tally/Odoo duplication.** Billing runs in Tally, accounting in Odoo. Payment automation can only trust the ledger once the two are bridged or consolidated.
- **Adoption.** Mitesh flagged that staff "stick at one place" as technology changes. The counter-strategy is built into the phasing: each phase removes a chore the team hates (spec hunting, reminder calls, bill typing, QC paperwork), so the system is felt as working *for* them before the training modules lock it in.

---

## 7. Next Steps

1. **Re-listen to the audit-call audio** — the auto-transcript lost most of the Hindi discussion; any verbally agreed scope should be reconfirmed in writing.
2. **Confirm the three numbers** above, plus the working go-live date ("before winter season" — is 1 October the target?).
3. **Kick off Track 0** with Tannu's team: top repeat customers' specs and drawings into the system first.
4. **Collect 3–5 sample advanced QC reports** from real customer orders — these become the templates for System 4.
5. **Agree the Phase 1 build plan** — to contradict, add to, or accept as-is.

---

*Every item in this document traces to the submitted Systems Brief. No figures have been added beyond those the client provided; unclear entries are flagged, not guessed.*
