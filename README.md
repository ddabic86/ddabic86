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

Most of my serious repositories are private because they belong to commercial platforms.

They are not three separate ideas. BBGI-OPS is the operational engine; the others apply the same engine to a different domain.

### BBGI-OPS — the operational engine

A generic engine for structured execution, responsibility, visibility, operational governance, priority, risk awareness, and control.

It models entities, sites, roles, permissions, scheduling, assignments, configurable procedures, execution state, evidence, escalation, risk, and history — without assuming an industry. It is built for work that needs ownership, follow-through, permissions, proof, auditability, and live operational visibility, where spreadsheets, notes, chats, and disconnected dashboards are too weak.

The domain layer changes per product. The engine does not.

### MDXT-OPS — the engine applied to healthcare

Patient-centered workflows, multidisciplinary collaboration, planning, permissions, structured records, and traceability.

It connects patients, professionals, care teams, family members, representatives, authorized caregivers, services, schedules, records, permissions, risk, and history. Different professionals work around the same patient without losing structure, responsibility, or visibility, while family members and authorized caregivers participate where appropriate.

The patient stays central, and can understand what is happening, who is involved, what has been done, what is planned, and what changed.

### ECPK — the engine applied to buildings, then opened as a platform

Fragmented building work across real locations: buildings, apartments, offices, rooms, shared areas, assets, tenants, administrators, internal teams, and external service providers.

A request can be opened from the place where the problem exists — home, office, building area, QR point, asset, room, or service zone — then routed, assigned, scheduled, executed with evidence, approved, and closed with cost and completion history attached. Recurring subscriptions run through the same record as one-off requests, with plans, allowances, scheduled pauses, and invoices. Work is dispatched as offers against real capacity — crews, shifts, duty templates, vehicles — that a provider accepts or declines before anything is committed.

Sensitive actions can require a named approver instead of a role check alone. AI sits on top as accountable assistance rather than authority: triage and routing suggestions carry a confidence score, the model and prompt version behind them, and a dismiss/flag loop that records when the system was wrong.

Then the system opened up. A service company onboards as a provider, is approved by the platform, and runs its own storefront on its own verified domain with its own branding, catalog, pricing, and published content — while dispatch, evidence, governance, and billing stay shared underneath. Commercial terms are data rather than code: packages carry entitlements and limits, and fees, billing state, and suspension are part of the model.

The place stays central. Requests, interventions, costs, and proof accumulate against the location itself, so the history survives a change of tenant, team, or provider.

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
