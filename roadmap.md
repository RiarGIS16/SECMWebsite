# SEC Maharashtra prototype — roadmap

Authoritative source: `SEC_website_core_Analysis_FULL_UPDATED.xlsx` (89 action
points; severity Critical > High > Medium > Low; priority Immediate > Phase 1 >
Phase 2/3). Audit basis: GIGW 3.0 + WCAG 2.1 AA.

## Foundation (Priority 1 core platform)

- [x] Design system / tokens (ink + saffron on paper, Devanagari-capable type)
- [x] Translation architecture (en/mr, CMS-replaceable dictionary + `{en,mr}` fields)
- [ ] Document metadata model (row 24, 51, 54: form no., purpose, owner, election
      type, version, effective-from, superseded, accessible-PDF flag)
- [ ] Geo master data with valid-only Local Body Type → District → Local Body →
      Ward combinations (rows 8, 9, 15, 16 — Critical mapping defect)
- [ ] Global search with result counts, type filters, snippets (rows 6, 55)
- [ ] Inclusive date-range filter utility (rows 17, 18, 19, 20 — filter returns
      nothing for valid ranges)
- [ ] Link classification: internal / other-government / external, with
      session-suppressible interstitial (rows 11, 12, 15)
- [ ] Accessibility shell: skip links, landmarks, focus order, text resize,
      high contrast, `lang` switching (rows 82–89 cross-cutting QA)
- [ ] Site shell: masthead, mega-nav, mobile nav, footer, page template with
      breadcrumb + content owner + last-reviewed

## Pages

- [ ] Home — Latest Updates with update type, priority indicator, owner,
      search + filters; urban AND rural election tiles; quick links; role entry
      points (rows 1–12)
- [ ] Search results page
- [ ] Notices / circulars register with preview (rows 3, 4, 5, 6)
- [ ] Election programme: ongoing / upcoming / recently completed (rows 18–20)
- [ ] Candidate journey hub + eligibility, nomination form UX, affidavit search
      (accessible CAPTCHA alternative), candidate list + CSV, symbols,
      expenditure (rows 31–38, 82)
- [ ] Voter: roll search with dependent filters, inline validation, polling
      station (rows 7, 15, 16)
- [ ] Help for ROs: stage-based workflows, acts & rules filters, forms metadata,
      interactive checklist, circular taxonomy, calendar, escalation matrix
      (rows 21–30)
- [ ] Political Party: classification, registration wizard, status register,
      symbol gallery, circular filters, compliance calendar (rows 39–45)
- [ ] Events calendar with filters + iCal export (rows 46–50)
- [ ] Publications taxonomy, full-text search, accessible-PDF status (rows 51–56)
- [ ] RTI: Section 4 disclosure dashboard, PIO directory, process (rows 57–62)
- [ ] EVM knowledge hub, categorised FAQs, security chain (rows 63–68)
- [ ] Feedback: categories + routing, tracking ID + SLA, accessibility channel,
      status tracking, escalation matrix (rows 69–74)
- [ ] Contact: purpose-based routing, searchable officer directory, district
      offices, election-period control room, last-verified governance (rows 75–81)

## Constraints

- Demo data only, clearly labelled. No invented official dates, legal
  provisions, officers, results or contacts presented as fact.
- All official content treated as CMS/API-replaceable.

## Update cycle 2 — incremental (see docs/gap-map.md)

- [x] Audit of existing pages/components against the workbook, with the
      enhance-vs-create decision recorded per requirement.
- [x] 33 missing sub-pages added under existing parents (About, Voter,
      Elections, RO, Candidate, Parties, Events, Publications, RTI, EVM,
      Feedback) — no duplicate pages, no new top-level rebuild.
- [x] Each new page declares its record fields, filters and actions plus the
      owning office, with official values left as CMS placeholders.
- [ ] Populate the new pages with official SECM data (blocked: awaiting content
      from the Commission).

## Update cycle 3 — official header branding

- [x] Official SEC Maharashtra and Lion Capital artwork added to the existing masthead.
- [x] Utility bar enhanced with live India time, search, page audio, text sizing,
      contrast, Marathi and a clearly labelled demo-login control.
- [x] Shared visual markers added to quick-service and section-service cards.
- [x] WCAG 2.1 AA utility validation: descriptive labels/roles, visible focus,
      logical keyboard order, no traps, and live announcements for every state change.

## Update cycle 4 — requested navigation and GIGW 3.0 alignment

- [x] Primary navigation reordered to Home, About Us, Imp Statistics, Voters,
      Election Program, Help for ROs, Candidate and Political Party.
- [x] Requested submenu labels mapped to existing pages where possible.
- [x] Missing statistics, judgment, candidate-instruction and de-registered-party
      pages added with bilingual, CMS-ready content structures.
- [x] Desktop dropdowns and mobile accordions use the same logical order, real
      links, accessible names/states, 44px targets and visible keyboard focus.

## Update cycle 5 — reference-aligned header

- [x] Masthead proportions, centered identity typography and official emblems aligned to the supplied visual reference.
- [x] Primary navigation restyled as a high-contrast teal sub-header while preserving all menus and accessible interactions.

## Update cycle 6 — real SECM records
- [x] Collect published records from the Commission site (317 records)
- [x] Add `sourceUrl` / `sections` to the document model
- [x] Serve section registers from official records, with real PDF downloads
- [ ] Re-collect periodically / connect to a live feed
