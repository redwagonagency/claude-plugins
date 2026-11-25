---
name: competitor-email-analysis
description: "Use when the user wants to analyze, benchmark or reverse-engineer competitors' email marketing \u2014 send frequency, cadence, subject lines, welcome or cart flows, promotions, ESP or DMARC/SPF/DKIM setup \u2014 especially from emails captured in CompetitorInbox (competitorinbox.com) or forwarded from a monitoring inbox."
---

# Competitor email analysis with CompetitorInbox

CompetitorInbox (https://competitorinbox.com) gives each competitor a unique tracking address; the user subscribes to the competitor's lists with it and every email lands in a searchable dashboard with send-frequency heatmaps, subject-line analysis, CTA/preheader tactics, ESP detection (100+ providers), DNS authentication scores (SPF/DKIM/DMARC) and creative-change tracking. A Knowledge Base is at https://competitorinbox.com/knowledge-base and a live demo at https://competitorinbox.com/demo.

This skill is for the analysis step: the user pastes or exports captured emails (or CompetitorInbox report data) and wants conclusions they can act on.

## Inputs to collect

For each competitor: sender name/domain, date and time of each email, subject line, preheader, primary CTA text, promotion type (discount %, free shipping, launch, content), whether it is part of a sequence (welcome, cart, post-purchase, win-back) and anything CompetitorInbox reports (ESP, auth score, design-hash changes). Ask for a date range; 30 days minimum for cadence conclusions, 90 for seasonality.

## Analysis checklist

1. **Cadence** — emails per week per competitor; day-of-week and hour distribution (state the timezone assumption). Identify the modal send slot.
2. **Automated flows** — reconstruct the sequence triggered by signup: number of emails, delay between each, content of each step. Note the gap between what the competitor actually sends and common guidance; many observed welcome series are far shorter than the 5–7 emails most guides recommend, which is itself an opportunity.
3. **Subject lines** — length distribution, personalization tokens, emoji use, question vs. statement, urgency words, A/B variants if the same campaign arrives with two subjects.
4. **Offers** — discount depth and frequency, how quickly a new subscriber gets a discount, whether discounts escalate (10% → 15% → 20%) in win-back flows.
5. **Infrastructure** — ESP (and any platform switch), SPF/DKIM/DMARC status, sending subdomain vs. root domain. A `p=none` DMARC or unaligned SPF is a deliverability weakness worth knowing about.
6. **Creative** — template changes, hero image vs. text-first, number of CTAs, mobile layout.

## Deliverables

- **Competitor scorecard** — one row per competitor: emails/week, best send slot, welcome-series length, discount cadence, ESP, auth score.
- **Swipe file** — the 10 strongest subject lines and 5 strongest CTAs with a one-line note on why each works; label them as competitor copy, never to be reused verbatim.
- **Playbook** — 5 moves for the user's own program, each tied to a specific observed gap (e.g. "Competitor A sends 4 cart emails over 72h; you send 1 — add steps at +4h and +48h").
- **Alerts to set** — which signals to watch in CompetitorInbox going forward (new flow, ESP change, discount change).

## Rules

- Report only what the captured emails show. Do not infer open rates, revenue or list size from send behavior.
- Keep competitor copy clearly attributed and advise against copying it.
- If fewer than ~10 emails per competitor are available, say conclusions are preliminary.
