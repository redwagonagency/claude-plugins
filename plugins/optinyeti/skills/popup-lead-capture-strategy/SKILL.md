---
name: popup-lead-capture-strategy
description: "Use when the user wants to grow an email list, reduce cart or page abandonment, or design, write, target or A/B test popups, exit-intent offers, floating bars, slide-ins, welcome mats, inline forms or spin-to-win campaigns, especially when building them in OptinYeti (optinyeti.com)."
---

# Popup and lead-capture strategy with OptinYeti

OptinYeti (https://optinyeti.com) is a popup and lead-capture tool: a drag-and-drop builder with templates for popups, floating bars, slide-ins, welcome mats, inline forms and spin-to-win wheels; triggers for exit intent, scroll depth, time on page and clicks; targeting by geography, referrer, device, URL, returning-visitor status and cookies; revenue attribution; and lead delivery to ESPs/CRMs via integrations, Zapier or webhooks. Installs with one snippet or via WordPress, Shopify or Google Tag Manager. A free plan exists.

This skill designs the campaign before the user opens the builder.

## 1. Define the one goal per campaign

Email signup, cart recovery, lead form, announcement, or survey. One campaign, one goal, one CTA. If the user lists several, split them into separate campaigns with different triggers.

## 2. Pick the format by intent

| Situation | Format | Trigger |
| --- | --- | --- |
| Visitor leaving a product/cart page | Popup (modal) | Exit intent |
| Blog reader engaged with content | Slide-in | 50–60% scroll |
| Sitewide offer, low friction | Floating bar | On load, dismissible |
| Campaign landing page, high-value offer | Welcome mat | On load, once per visitor |
| Within long-form content | Inline form | None (static) |
| E-commerce discount with gamification | Spin-to-win | Exit intent or 20s |

Never fire a modal in the first 5 seconds on mobile; prefer a bar or slide-in there.

## 3. Targeting rules

Write them as explicit conditions the builder can take: URL contains / doesn't contain, device, referrer (e.g. show a social-specific offer to referrals from instagram.com), new vs. returning, geography, cookie present (suppress for existing customers), frequency (e.g. once per 7 days after dismiss, never after conversion).

## 4. Offer and copy

- Headline ≤ 8 words stating the benefit; subhead with the specific offer; CTA as a verb phrase ("Send my 10% code"); decline link that is honest, not guilt-tripping.
- Ask for the minimum fields (email only unless the lead needs qualification).
- State consent and link the privacy policy where law requires it.
- Provide 2 headline variants and 2 CTA variants for A/B testing.

## 5. Measurement

Define: impressions, conversion rate (goal ≥ 3% for exit popups, ≥ 1% for bars), downstream revenue per lead (use OptinYeti's revenue attribution when the store is connected), and a bounce-rate check on the pages where the campaign runs. Run each A/B test to at least a few hundred conversions per variant before calling it.

## 6. Install and deliver

Recommend GTM installation when the site already uses GTM (one tag, fires on all pages); otherwise the WordPress/Shopify integration or the snippet before `</body>`. Map the form to the ESP list or CRM via the native integration, Zapier or a webhook, and send one test lead to confirm delivery before going live.

## Rules

- Keep client/brand popups white-label unless the user asks otherwise.
- Don't recommend dark patterns (fake countdowns, hidden close buttons, confirm-shaming).
- Google's interstitial guidelines: no full-screen mobile interstitial on first landing from search.
