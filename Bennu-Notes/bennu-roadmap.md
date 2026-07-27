# Bennu Roadmap

*A free, privacy-focused iOS/iPadOS menstrual cycle tracking utility with customizable health workflows — GPLv3, no subscriptions, no paywalls.*

---

## Phase 0 — Foundation (Pre-Alpha)

Groundwork that everything else depends on.

- [ ] Define the on-device data model: cycles, periods, symptoms, moods, custom fields
- [ ] Decide local storage approach (e.g. SwiftData / Core Data with on-device encryption at rest)
- [ ] App architecture skeleton (SwiftUI, navigation shell, iPhone-first layout with iPad adaptivity)
- [ ] Initial design system: typography, color, iconography — should read as calm/clinical-but-warm, not clinical-sterile
- [ ] GPLv3 license, repo structure, CONTRIBUTING.md
- [ ] CI setup (build/lint/test on each push)

**Exit criteria:** app builds and runs on a device/simulator with an empty shell and a data layer that can persist a single logged period.

---

## Phase 1 — Core Tracking (MVP)

The minimum that makes Bennu a usable period tracker.

- [ ] Log a period (start/end date, flow intensity)
- [ ] Basic calendar view showing logged cycles
- [ ] Log symptoms and moods per day, from a default preset list
- [ ] Simple cycle-length calculation from historical data
- [ ] Onboarding flow: initial setup (last period date, average cycle length, goals)
- [ ] Local-only storage confirmed working (no network calls at all in this phase)

**Exit criteria:** a user can complete onboarding, log a cycle, log symptoms, and see it reflected on a calendar — fully offline.

---

## Phase 2 — Customizable Workflows

This is Bennu's core differentiator — make it your own.

- [ ] Custom symptom/mood tags (user-defined, not just presets)
- [ ] Customizable tracking workflow: let users choose what they log and how (quick-log vs. detailed-log modes)
- [ ] Reorderable/hideable tracking categories
- [ ] Notes field per day/entry
- [ ] Reminders/notifications (opt-in local notifications, e.g. "log today," "period predicted to start soon")

**Exit criteria:** two different users could configure meaningfully different tracking setups suited to their own needs.

---

## Phase 3 — Insights & Predictions

Turning logged history into something meaningful.

- [ ] Cycle trend visualization (length over time, variability)
- [ ] Symptom/mood pattern correlation views (e.g. "you tend to log X around day Y")
- [ ] Next-period and fertile-window predictions based on personal history
- [ ] Confidence indicators on predictions (avoid false precision, especially with irregular cycles)
- [ ] History browsing — clean long-term view back through past cycles

**Exit criteria:** predictions and trends are visibly driven by the user's own data, with clear (not overstated) confidence.

---

## Phase 4 — Data Portability & Privacy Hardening

Core promises: private by default, and yours to take with you.

- [ ] Export data (PDF and/or CSV) formatted to hand to a health provider
- [ ] Full data export/import for backup or device migration (e.g. encrypted file, iCloud-optional)
- [ ] Explicit privacy review: confirm zero telemetry, zero third-party SDKs touching health data
- [ ] In-app "Privacy" explainer screen — plain language, no legalese, describing exactly what stays on-device
- [ ] Optional Face ID/Touch ID app lock

**Exit criteria:** a user can generate a provider-ready export and fully back up/restore their data without any of it leaving the device unless they explicitly choose to.

---

## Phase 5 — Polish & Accessibility

- [ ] Full iPad layout pass (not just scaled-up iPhone UI)
- [ ] VoiceOver / Dynamic Type / accessibility audit
- [ ] Dark mode
- [ ] Localization scaffolding (even if English-only at launch, structure for future translation)
- [ ] Empty states, error states, edge cases (irregular cycles, gaps in logging, leap years, etc.)
- [ ] Performance pass on large multi-year histories

**Exit criteria:** app feels finished, not just functional — no rough edges, accessible by default.

---

## Phase 6 — Beta

- [ ] TestFlight distribution to a small trusted group
- [ ] Structured feedback loop (in-app feedback or lightweight external form)
- [ ] Bug triage and fix pass
- [ ] Review App Store guidelines specifically for health-category apps (data handling disclosures, privacy nutrition label accuracy)

**Exit criteria:** no known critical bugs; privacy nutrition label and metadata are accurate and ready for submission.

---

## Phase 7 — App Store Submission & Launch

- [ ] Prepare App Store listing (screenshots for iPhone and iPad, description, keywords)
- [ ] Submit for App Store review
- [ ] Handle review feedback/resubmission (budget extra time — noted in README as an inherent constraint of iOS distribution)
- [ ] Public launch
- [ ] Announce via existing channels (FishTankTech, personal site/blog, etc.)

**Exit criteria:** Bennu is live and installable from the App Store.

---

## Phase 8 — Post-Launch Iteration

- [ ] Monitor crash reports / user feedback (still without telemetry — rely on voluntary feedback channels)
- [ ] Prioritize feature requests against the "no subscriptions, no paywalls" constraint
- [ ] Consider: symptom/mood custom charting, widget support, Shortcuts/Siri integration, Apple Health read/write (opt-in, carefully scoped)
- [ ] Ongoing GPLv3 community contributions if the repo is public

---

## Notes on Sequencing

- **Privacy and offline-first are non-negotiable constraints**, not a phase — they should be validated continuously, not bolted on in Phase 4.
- **Customizability (Phase 2)** is what separates Bennu from a generic tracker, so it's worth prioritizing before deep insights work — it shapes what data insights even have to work with.
- **App Store review time (Phase 7)** is outside your control — start metadata/screenshots prep during Phase 6, not after submission.
