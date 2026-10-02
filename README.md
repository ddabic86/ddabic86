<div align="center">

# Dario Dabic

### I build operational systems from zero: idea → product → architecture → code → AI layer → production.

**Founder-builder · Lugano, Switzerland**

[![GitHub followers](https://img.shields.io/github/followers/ddabic86?label=Follow&style=for-the-badge)](https://github.com/ddabic86)
[![Profile views](https://komarev.com/ghpvc/?username=ddabic86&style=for-the-badge)](https://github.com/ddabic86)

</div>

---

## What I build

I build software for real-world operations.

Not generic templates.
Not landing pages.
Not dashboard-only software.
Not isolated CRUD apps dressed up as products.

I build systems where people, places, entities, roles, permissions, schedules, approvals, records, evidence, risk, priority, business rules, AI support, and execution need to stay connected.

The goal is simple:

> **Turn fragmented real-world operations into live, structured, accountable systems.**

A serious operational system should understand what happened, where it happened, who owns it, who can act on it, which entity it belongs to, what changed, what is blocked, what matters first, what risk exists, what needs approval, what needs proof, what needs history, and what should happen next.

```txt
real-world work → structure → ownership → execution → risk → priority → visibility → accountability
```

The interface is only the visible layer.

The real product is the operating model underneath.

---

## Private products

Most of my serious repositories are private because they belong to commercial platforms, so this page shows them instead: each one running locally on an invented world, with the real interface.

They are not separate ideas. **BBGI-OPS** is the operational engine. **MDXT-OPS** and **ECPK** apply the same engine to healthcare and to field services. **MiniPlatform** takes its rules down to a single small business that runs for free.

| | Domain | What it runs on |
|---|---|---|
| [**ECPK**](#ecpk--field-services-and-buildings-opened-up-as-a-multi-provider-platform) | Field services & buildings, multi-provider | Next.js 16 · Fastify + tRPC · Prisma/Postgres · Redis/BullMQ · Socket.io · Google Maps · Claude |
| [**BBGI-OPS**](#bbgi-ops--the-operational-engine) | Multi-site security & facilities | Next.js 16 · Fastify + tRPC · Prisma/Postgres · Socket.io · BullMQ · WebAuthn |
| [**MDXT-OPS**](#mdxt-ops--the-engine-applied-to-care) | Nursing homes & home care | Next.js 16 · Fastify + tRPC · Prisma/Postgres · Redis |
| [**MiniPlatform**](#miniplatform--a-subscription-manager-that-costs-nothing-to-run) | One small business, subscriptions & billing | Next.js 16 · Server Actions · Prisma/Postgres · Vitest · Playwright |

### ECPK — field services and buildings, opened up as a multi-provider platform

**The whole life of a service job on one record: the request, the van on the map, the signed report, the paid invoice.**

Built for a Swiss field-service company, then opened up so any service company can run its own branded storefront on the same engine. The place stays central: every job, cost and photo accumulates on the location itself, so the history outlives a change of tenant, team or provider.

`131 data models` · `57 API routers` · `4 languages` · `realtime everywhere`

<p align="center">
  <img src="assets/ecpk/order-enroute.png" alt="An order on its way: the tracker, the van on the road and its route to the door" width="100%">
</p>
<p align="center">
  <img src="assets/ecpk/phone-order-enroute.png" alt="The order on a phone, the van on its way" width="24%">
  <img src="assets/ecpk/phone-team-map.png" alt="The crew on the map, on a phone" width="24%">
  <img src="assets/ecpk/phone-today.png" alt="The operator's day on a phone" width="24%">
  <img src="assets/ecpk/phone-storefront-service.png" alt="A provider's storefront on a phone" width="24%">
</p>

| | |
|---|---|
| **Orders** | Live tracker with the van on the map, route and ETA · customer/team chat with read receipts · extra-work quotes the customer approves · problem reports · ratings and tips · full history |
| **Dispatch** | What needs someone now · crew and free vans on the map · seats offered and claimed · absences, moved days, timesheets |
| **On site** | Offline report with price-list lines, parts, readings, photos, time and the customer's signature — no order closes without it |
| **Clients & plans** | Client book · subscriptions with allowances, pauses, self-service cancellation · planned pickup rounds |
| **Swiss billing** | QR-bill · quotes → orders · deposits · credit notes · camt.054 bank import · dunning by country with interest · scheduled sends · VAT return prefill · accounting export |
| **Marketplace** | Each provider gets a storefront on a subdomain or its own domain, with its brand, catalogue and plans · platform packages, limits and fees |
| **Reach** | Bell → live toast → Web Push → e-mail, SMS, WhatsApp or Telegram, each opt-in and verified |
| **Trust** | Passkeys and 2FA · fail-closed permissions · one-role-per-company · three audit streams · a double tap never files twice |
| **AI** | Claude translates the catalogue and invoices into four languages and drafts invoice wording from the facts — never the numbers |

<table>
<tr><td width="50%" valign="top"><b>The crew and the vans, live</b><br><img src="assets/ecpk/team-map.png" alt="Team map: operators at their positions, free vans at their bases"></td><td width="50%" valign="top"><b>The dispatcher's day</b><br><img src="assets/ecpk/today.png" alt="The day page: what needs someone, the day's figures, the crew on the map"></td></tr>
<tr><td width="50%" valign="top"><b>The on-site report</b><br><img src="assets/ecpk/order-report.png" alt="On-site report: lines, parts, readings, photos and time beside the printed report"></td><td width="50%" valign="top"><b>Signed by the customer</b><br><img src="assets/ecpk/order-report-signed.png" alt="The customer signing the report"></td></tr>
<tr><td width="50%" valign="top"><b>Chat on the order</b><br><img src="assets/ecpk/order-chat.png" alt="Customer and team chat on an order, with read ticks"></td><td width="50%" valign="top"><b>The order's history</b><br><img src="assets/ecpk/order-history.png" alt="Every moment of an order"></td></tr>
<tr><td width="50%" valign="top"><b>Closed, rated, paid</b><br><img src="assets/ecpk/order-closed.png" alt="A closed order with its rating, report and paid invoice"></td><td width="50%" valign="top"><b>Invoice register</b><br><img src="assets/ecpk/billing-register.png" alt="Invoice register with drafts, reminders and paid bills"></td></tr>
<tr><td width="50%" valign="top"><b>Invoice with Swiss QR-bill</b><br><img src="assets/ecpk/invoice-qr.png" alt="An invoice with its Swiss QR-bill"></td><td width="50%" valign="top"><b>Billing trends</b><br><img src="assets/ecpk/billing-stats.png" alt="Billing trends: invoiced vs collected, overdue, days to get paid"></td></tr>
<tr><td width="50%" valign="top"><b>A provider's storefront</b><br><img src="assets/ecpk/storefront.png" alt="A provider's public catalogue"></td><td width="50%" valign="top"><b>Loading</b><br><img src="assets/ecpk/loading.png" alt="The Ecopick loading screen"></td></tr>
</table>


**Each provider dresses its own storefront** — logo, colours, home sections and a photo per page and per order stage, edited with a live preview. Below, an invented plumber running on the same engine:

<p align="center">
  <img src="assets/ecpk/provider-storefront.png" alt="An invented provider's public storefront, in its own colours" width="73%">
  <img src="assets/ecpk/phone-provider-storefront.png" alt="The same storefront on a phone" width="24%">
</p>
<table>
<tr><td width="50%" valign="top"><b>Brand, with a live preview</b><br><img src="assets/ecpk/storefront-editor-brand.png" alt="Storefront editor: logo, colours and a live preview"></td><td width="50%" valign="top"><b>A photo per order stage</b><br><img src="assets/ecpk/storefront-editor-order-photos.png" alt="Storefront editor: one photo per tracker stage"></td></tr>
<tr><td width="50%" valign="top"><b>Changing an image</b><br><img src="assets/ecpk/storefront-editor-photo-picker.png" alt="The media library open to pick a new image"></td><td width="50%" valign="top"><b>The provider's own sign-in</b><br><img src="assets/ecpk/provider-login.png" alt="A provider's branded sign-in page with its photo"></td></tr>
</table>

### BBGI-OPS — the operational engine

**Structured execution, ownership, proof and live risk for work that happens across many sites.**

A generic engine for work that needs follow-through: who owns it, who may act on it, what proof it needs, what is late, and what that lateness costs. It assumes no industry; its first domain is multi-site security and facilities — guards, reception, patrols, alarms, door checks — where spreadsheets, chats and disconnected dashboards are too weak. The domain layer changes per product. The engine does not.

<p align="center">
  <img src="assets/bbgi-ops/cockpit-desktop.png" alt="The cockpit: a live door-held response beside the office handover" width="100%">
</p>
<p align="center">
  <img src="assets/bbgi-ops/phone-cockpit.png" alt="The cockpit on a phone" width="24%">
  <img src="assets/bbgi-ops/phone-command-center.png" alt="The Command Center on a phone" width="24%">
  <img src="assets/bbgi-ops/phone-handover.png" alt="The handover on a phone" width="24%">
  <img src="assets/bbgi-ops/phone-loading.png" alt="Loading screen on a phone" width="24%">
</p>

- **Space as a model** — organization → region → site → building → floor → zone → room, with typed assets (doors included) and checkpoints.
- **Procedures, not checklists** — reusable templates of ordered steps with typed answers, per-step competency gates, multiple signatures, dependencies, issue flagging and follow-up work triggered by an answer; each site can override a step without forking the procedure.
- **Planning separate from staffing** — posts carry their recurring work, shift templates define seats; people claim seats gated by role, certification, post qualification, working-time limits and overlap checks.
- **The cockpit** — a live timeline of the operational day: check-in and check-out as presence, join, pause, postpone, skip and assign on duties, urgent responses that hold other work, and a handover that carries what is still open into the next shift.
- **Alarms and issues** — alarms spawn response procedures; issues are collaborative tickets linked to the duty, step and asset they came from.
- **Explainable risk** — 0–100 per duty, alarm, issue and site, rising with lateness and falling with each completed step; the Command Center ranks offices and duties with their trends.
- **Governance** — stacked roles with per-membership permission matrices, per-item stakeholders and overrides; every mutation is tagged and audited, and a governance view shows accountability, weak points and permission posture.

<table>
<tr><td width="50%" valign="top"><b>Command Center</b><br><img src="assets/bbgi-ops/command-center.png" alt="Command Center ranking offices and duties by risk"></td><td width="50%" valign="top"><b>A duty with its evidence</b><br><img src="assets/bbgi-ops/duty-steps-evidence.png" alt="A fire-door audit: each step with who ticked it and when, an issue flagged, the signature"></td></tr>
<tr><td width="50%" valign="top"><b>Schedule and coverage</b><br><img src="assets/bbgi-ops/schedule-day-plan.png" alt="Schedule day view with shifts, seats, the day's duties and coverage"></td><td width="50%" valign="top"><b>An issue ticket</b><br><img src="assets/bbgi-ops/issue-ticket.png" alt="An issue as a thread of typed updates"></td></tr>
<tr><td width="50%" valign="top"><b>Roles and permissions</b><br><img src="assets/bbgi-ops/roles-permissions.png" alt="A membership's role, scope and permission matrix"></td><td width="50%" valign="top"><b>Loading</b><br><img src="assets/bbgi-ops/loading.png" alt="The app's loading screen"></td></tr>
</table>

### MDXT-OPS — the engine applied to care

**Patient-centred care for nursing homes and home-care services, where every read of a record is logged.**

Structures, locations, wards, rooms and beds, the people who work there and the patients they look after — with the patient kept at the centre: who is involved, what was done, what is planned, and what changed. Screens follow the system theme: light or dark.

**Not built for one country.** The country is a setting: it decides the coding system for problems, the assessment instrument, the tariff scheme, the payers and the regions people work in. Switzerland is the first one configured; another country is new reference data, not a new product.

<p align="center">
  <img src="assets/mdxt-ops/mdxt-cockpit-duty.webp" alt="A nurse works a duty in the live cockpit: starts it, ticks each step as its risk drops, signs, a colleague co-signs, and it completes" width="100%">
</p>
<p align="center">
  <img src="assets/mdxt-ops/mdxt-tablet-cockpit-duty.webp" alt="The duty on a tablet" width="52%">
  <img src="assets/mdxt-ops/mdxt-phone-cockpit-duty.webp" alt="The duty on a phone" width="46%">
</p>

- **The record** — patient and episode kept apart: problems with ICD codes, medication, allergies, vaccinations, observations, documents and a journal.
- **Access as a list, not a role** — consent per role, a per-record access list, invitations for family and outside professionals, and break-glass emergency access that is loud and logged.
- **Care plans that become the day** — built on the country's care-service catalogue, turned into each day's work, with home-care visit rounds and a bed board with placements over time.
- **Operations each structure shapes** — a base catalogue of operations to start from; a structure takes one and makes it its own (steps, duration, tariffs, risk, who may do it, where it applies) or writes its own from scratch. Nothing changes under it because the base was edited.
- **Staffing** — recurring shift templates published into a rota, absences, contracts and hours balances, working-time and rest rules enforced.
- **An open market for the shifts nobody can cover** — a post the team cannot fill can be opened to outside professionals, one day or a whole week as one job. They see it, apply or get offered it by name, and only qualify if they hold the required role and certifications — an expired credential counts as not held — and the shift fits their working-time and rest limits.
- **Live, who is where and allowed to be** — who is online and available, who is on shift, which duty each person is on right now, and what they are certified for, with expiry dates tracked.
- **The shift** — duties with steps, co-signatures, a shift journal, a signed handover, and risk and escalation sweeps.
- **Billing** — completed care becomes billable items under the country's tariff scheme, split between insurer, public payer and client, then bills, payments and reminders (with the QR-bill in Switzerland).

**On shift, together** — the roster shows who is busy and who is free; a nurse joins a colleague's round, takes a duty from the pool, completes it, and raises a response:

<p align="center">
  <img src="assets/mdxt-ops/mdxt-cockpit-team.webp" alt="The cockpit's roster, joining a colleague's round, taking a pooled duty, completing it and raising a fall response" width="100%">
</p>
<p align="center">
  <img src="assets/mdxt-ops/mdxt-tablet-cockpit-team.webp" alt="The team on shift on a tablet" width="52%">
  <img src="assets/mdxt-ops/mdxt-phone-cockpit-team.webp" alt="The team on shift on a phone" width="46%">
</p>

**Around the record** — a patient's dossier and care plan, the month's rota and the billing register:

<p align="center">
  <img src="assets/mdxt-ops/mdxt-tour.webp" alt="A tour: the patient record, the care plan, the month rota and the bills register" width="100%">
</p>
<p align="center">
  <img src="assets/mdxt-ops/mdxt-tablet-tour.webp" alt="The tour on a tablet" width="52%">
  <img src="assets/mdxt-ops/mdxt-phone-tour.webp" alt="The tour on a phone" width="46%">
</p>

### MiniPlatform — a subscription manager that costs nothing to run

**The same rules at the smallest scale: one business, a handful of customers, no paid services.**

For an owner who tracks renewals in a spreadsheet and wants to stop — without paying for a SaaS, an e-mail provider or an SMS gateway. No Redis, no queue, no object storage: Postgres and a daily job. Italian by default, English included.

<p align="center">
  <img src="assets/miniplatform/dashboard.png" alt="The dashboard with the reminders to send on WhatsApp" width="100%">
</p>
<p align="center">
  <img src="assets/miniplatform/phone-dashboard.png" alt="The dashboard on a phone" width="24%">
  <img src="assets/miniplatform/customer.png" alt="A customer's own area on a phone" width="24%">
  <img src="assets/miniplatform/welcome.png" alt="The first sign-in from a one-time link" width="24%">
  <img src="assets/miniplatform/phone-loading.png" alt="Loading screen on a phone" width="24%">
</p>

- **One book for people and their subscriptions** — renewals, pauses, promotions; access handed over by a one-time WhatsApp link with a step-by-step first sign-in.
- **Reminders that never go twice** — a daily job prepares them before a subscription ends, idempotently; sent on WhatsApp by hand or through the Cloud API, or on Telegram.
- **Billing** — gap-free invoices, payments and credit notes sent as signed links, automatic overdue reminders, the Swiss QR-bill and Italian FatturaPA XML.
- **Security without a provider** — e-mail and password done carefully, Postgres-backed rate limits, a security console with blocks and the activity log, and roles with a permissions matrix.
- **Tested** — Vitest for the money and dates, Playwright end-to-end on GitHub Actions; deployable for free on Vercel and Neon.

<table>
<tr><td width="50%" valign="top"><b>People and subscriptions</b><br><img src="assets/miniplatform/people.png" alt="People and their subscriptions, one person open"></td><td width="50%" valign="top"><b>Billing</b><br><img src="assets/miniplatform/billing.png" alt="The billing register"></td></tr>
<tr><td width="50%" valign="top"><b>Invoice with QR-bill</b><br><img src="assets/miniplatform/invoice.png" alt="An invoice with its Swiss QR-bill"></td><td width="50%" valign="top"><b>Roles and permissions</b><br><img src="assets/miniplatform/roles.png" alt="Roles with a permissions matrix"></td></tr>
<tr><td width="50%" valign="top"><b>Your brand</b><br><img src="assets/miniplatform/settings.png" alt="The company's appearance: logo, button colour, corners"></td><td width="50%" valign="top"><b>Sign-in</b><br><img src="assets/miniplatform/login.png" alt="The sign-in page with the company's logo"></td></tr>
</table>

> All names, addresses, e-mail addresses and phone numbers in the screenshots are made up; every product was run locally on an invented world for them.

---

## Multi-entity operational model

Real operations are not flat. A user should not be locked to one profile, one company, one role, one building, one provider, or one workspace.

```txt
user → entity → role → permission → workflow → data scope → action
```

The same person may be owner of one business, administrator of another entity, operator inside a specific site, professional inside a care provider, manager of multiple buildings, partner assigned to a client, requester in one context and approver in another.

The important part is context. A weak system only asks who the user is. A serious operational system asks:

```txt
Who is the user?
Which entity are they acting under?
What role do they have there?
What can they see and change?
What workflow applies?
What data must stay isolated?
What action must be logged?
```

That is not simply "many users." It is structured control across multiple operational entities.

---

## Domain-modeled systems

I do not treat operational software as a collection of disconnected tables. I build around the real entities, relationships, permissions, workflows, events, risks, and actions the system needs to understand.

```txt
people → entities → places → roles → permissions → work → events → risk → action → history
```

In practice this becomes an operational ontology. The system must know the difference between a user account, a person, a role, an entity, a site, a building, an asset, a patient, a professional, a representative, a task, an operation, an approval, an incident, a risk signal, an execution record, and an audit event — and how all of those relate.

That is the difference between storing data and modeling reality. A weak system has records. A serious system has an operating model behind the records.

---

## Configurable operations

Different sites, businesses, buildings, care providers, teams, and service flows need different steps and rules. So operations are configured, not locked into hardcoded flows.

```txt
operation → steps → assignment → permission → execution → proof → history
```

An operation defines what needs to happen, who can do it, where it applies, which entity owns it, which steps are required, what evidence is needed, what role or qualification is required, what happens if it is late, blocked, skipped, or escalated, and what gets logged on completion.

The point is flexibility without chaos: each organization can follow the way work actually happens while permissions, history, proof, risk, and accountability stay structured.

---

## Operational governance

Roles, permissions, restrictions, approvals, audit logs, escalation paths, and accountability rules are part of the product foundation, not secondary features. This matters most where work is sensitive, regulated, delegated, or shared between different people, businesses, providers, and organizations — the real problem is not access, it is controlled participation.

```txt
entity → role → permission → action → restriction → history → accountability
```

Governance means the system can answer who can see, change, or approve something, which entity owns the record, which role the user was acting under, what happened and why, what was blocked or overridden, and who is responsible next.

Without governance, operational software becomes chaos.

---

## Risk and priority

Not everything has the same weight. Some work can wait, some work blocks other work, and some work creates financial, clinical, safety, or service risk.

```txt
signal → risk → priority → escalation → action
```

Risk is not a static label someone sets once. It is derived from execution state and moves in both directions as the operation progresses: completing a required step, attaching missing evidence, or clearing an approval lowers it, while a skipped, blocked, late, or unassigned step raises it.

```txt
required step completed, evidence attached, approval cleared   → risk down
step skipped, blocked, overdue, unassigned, or repeated        → risk up
```

Nobody has to remember to lower the score by hand, and it does not sit frozen at the level it was created with. It follows the work.

The point is not to generate fake AI scores. Risk must be explainable: a user should understand why something is urgent, blocked, overdue, sensitive, repeated, or unsafe.

Good operational software does not only show a list of work. It helps decide what needs attention now.

---

## Main stack

```txt
Frontend         Next.js · React · TypeScript · Tailwind · shadcn/ui
Backend          Node.js · Fastify · tRPC · API routes · server actions
Database         PostgreSQL · Prisma ORM · relational domain modeling
State/Data       TanStack Query · Zustand · typed API flows
Realtime         Socket.io · Redis · live operational updates
Workers          BullMQ · background jobs · scheduled processing
Auth             custom auth flows · sessions/JWT · 2FA · passkeys/WebAuthn
Security         hashing · rate limiting · CSRF protection · protected actions · audit logs
Authorization    role-based · scoped · entity-aware access control
Architecture     multi-entity account model · organization/site scoping · multi-tenant-ready structure
Infra            AWS · S3 · SES · SNS · deployment pipelines · production config
AI Layer         scoped AI assistance · document parsing · structured automation
```

The stack matters, but it is not the advantage by itself. The advantage is knowing how to turn messy operational reality into a working product model.

---

## Product principles

```txt
1.  The workflow is the product.
2.  The system must model the real-world domain.
3.  Data without structure becomes noise.
4.  Notes are not operations, and dashboards are weak if nothing can be executed from them.
5.  Permissions, governance and history matter before scale, not after.
6.  Risk and priority must be explainable.
7.  Operations should be configurable, not hardcoded.
8.  A user may control or participate in multiple operational entities.
9.  AI should support operations, not pretend to replace them.
10. Good software reduces coordination; weak software creates more.
11. If the logic is weak, the UI is decoration.
```
