# Website Evaluation — Heart & Soul Therapy (Tania Ono)

**URL reviewed:** https://heartandsoul.lovable.app/
**Date:** 2 October 2026
**Reviewer:** Kiro
**Method:** Live walkthrough (headless browser snapshot + screenshots), DOM/metadata inspection, and benchmarking against current best practices for high-end private psychotherapy practices.

---

## 1. Who this site is for (target audience)

The site defines its own niche very precisely — this is a strength:

- **International / expat families living in Madrid** (the hero names them explicitly; a testimonial is from a *"familia brasileira residente en Madrid"*).
- **High-achieving professionals** — the positioning *"para quienes exigen excelencia"* ("for those who demand excellence") and the service *"Soledad en el Éxito"* ("loneliness in success") target an affluent, successful audience.
- People who prize **discretion, confidentiality, and clinical rigor** over a warm/casual tone.
- **Trilingual**: Spanish · English · Português.

**Audience mindset:** affluent, discerning, time-poor, privacy-sensitive, often in emotional distress (relocation stress, couple tension, identity between cultures, isolation). This audience rewards: credibility signals, effortless and *private* contact, and premium visual polish — and is quick to abandon anything that feels generic, slow, or clumsy.

---

## 2. Scorecard

Each criterion scored 1–5 (5 = excellent). Weighted toward what matters most for this audience.

| # | Criterion | Score | Weight | Notes |
|---|-----------|:---:|:---:|-------|
| 1 | First impression & visual design | **5** | High | Elegant navy + gold, serif display type, warm interior photography. Premium feel that matches the audience. |
| 2 | Positioning & messaging clarity | **5** | High | Niche is razor-sharp. Copy speaks to a specific person, not "people in general" — textbook best practice. |
| 3 | Trust & credibility signals | **4** | High | Credentials (EMDR, systemic, CBT), 15+ yrs experience, Trustpilot 5.0, testimonials. Missing: license/registration number, professional-body membership, real reviews linked. |
| 4 | Call-to-action & booking flow | **2** | **Highest** | Biggest weakness — see §3. CTAs route to email/phone only; no self-serve scheduler. High-friction for this audience. |
| 5 | Information architecture / navigation | **4** | Med | Clean single-page flow: About → Specialties → Approach → Contact. Logical and matches the fit→trust→process→action decision order. |
| 6 | Content depth & "the process" | **3** | Med | Strong on *what* and *who*, light on *how it works* (first session, fees, duration, online logistics). This audience wants to know what to expect. |
| 7 | Multilingual execution | **3** | High | ES/EN/PT switcher present — excellent for the niche. But `<html lang>` and content appear to default to one language; needs verification that each language is complete and that `lang`/`hreflang` are correct per selection. |
| 8 | Accessibility | **3** | Med | Images have alt text, viewport meta present, one H1. Concerns: light-grey text on white (contrast), text-over-photo in hero (legibility), reliance on scroll-reveal animations. |
| 9 | SEO & metadata | **3** | Med | Good `<title>` and meta description, OG image set. Missing/weak: **no favicon**, no visible structured data (LocalBusiness/`MedicalBusiness` schema), single-page limits keyword surface. |
| 10 | Performance & technical | **3** | Med | Client-rendered SPA (content needs JS). Lovable branding badge present. Hero is a large photo — needs optimization/preload. Measure Core Web Vitals before launch. |
| 11 | Mobile experience | **3?** | **High** | Could not fully verify in headless. Must confirm: hamburger menu, sticky "Reservar" button, hero text legibility, tap-target sizes. This audience is heavily mobile. |

**Weighted overall: ~3.6 / 5 — a beautiful, well-positioned site held back mainly by a high-friction contact flow and a few trust/technical gaps.**

---

## 3. The single most important fix: the booking / contact flow

Current state: the primary actions ("Consulta Privada", "Reservar", "Llamar ahora") lead to **email or a phone call**. Best-practice research is unanimous that for mental-health audiences a phone call is a *high-risk, high-friction* action — people who are vulnerable or private often won't make it. For an affluent, time-poor, privacy-sensitive audience the friction is even costlier.

Recommended:
1. **Add a confidential scheduler** (e.g. Calendly / Cal.com / Google Appointments) so visitors can book a "primera consulta privada" without a phone call or exposing themselves in an open email. Keep phone/email as secondary options.
2. **Reframe the CTA around safety, not transaction.** Best practice favours reassuring language over "Reserve". Example: *"Solicita una primera conversación confidencial"* with a one-line reassurance ("Respuesta en 24h · Estrictamente confidencial") — which the site already has and should keep next to the button.
3. **Make the CTA persistent** on scroll (sticky header "Reservar" is a good start — ensure it's prominent and present on mobile).
4. **If using a form**, keep it short (name, preferred language, brief message, preferred contact method) and state the confidentiality promise directly beside it.

---

## 4. Prioritised recommendations

### Must-fix (before promoting the site)
- [ ] Replace email-only booking with a **confidential self-serve scheduler**; keep CTA language reassuring.
- [ ] **Verify the mobile experience end-to-end** (menu, sticky CTA, hero legibility, tap targets, no horizontal scroll).
- [ ] Add a **favicon** and confirm **`lang`/`hreflang`** switch correctly per language.
- [ ] Confirm **all three languages (ES/EN/PT) are fully translated** — this is the core of the niche; partial translation would undermine credibility.
- [ ] Check **colour contrast** (grey-on-white body, text-over-hero-photo) against WCAG AA.

### High-impact (strengthens trust & conversion)
- [ ] Add a short **"How it works / Your first session"** section: what to expect, session length, in-person vs online, approximate fees or "fees on request".
- [ ] Add concrete **credibility markers**: professional registration/colegiado number, professional-body membership, and link testimonials/Trustpilot to a verifiable source.
- [ ] Add **`MedicalBusiness`/`LocalBusiness` structured data** (name, address in Retiro, phone, languages, geo) to help local SEO in Madrid.
- [ ] Remove or replace the **"Edit with Lovable"** badge for a professional, owned-domain launch (custom domain, e.g. taniaono.es, which the email already implies).

### Polish
- [ ] Ensure scroll-reveal animations **degrade gracefully** (content visible even if JS/animation fails; respect `prefers-reduced-motion`).
- [ ] Optimize/preload the **hero image** and run a Core Web Vitals check (LCP, CLS, INP).
- [ ] Add an **FAQ** addressing expat-specific questions (languages, insurance/reimbursement for internationals, online across time zones).
- [ ] Consider a lightweight **privacy/confidentiality note** and cookie/GDPR compliance (Spain/EU).

---

## 5. What the site already does very well (keep it)

- **Niche positioning** is excellent and specific — the hardest thing to get right, and it's done.
- **Premium visual identity** (palette, typography, photography) is genuinely well-matched to an affluent clientele.
- **Copy** speaks to one precise person and names real pains (relocation strain, children's identity, loneliness in success).
- **Trilingual intent** directly serves the international-family audience.
- **Confidentiality** is woven through the messaging — exactly what this audience needs to hear.

---

## 6. Benchmarks & sources

Evaluation criteria were grounded in current best-practice guidance for therapy/mental-health websites. *Content from these sources was rephrased for compliance with licensing restrictions.*

- Patient decision order (fit → trust → process → action) — [Behavioral-health conversion framework, Unicorn Platform](https://unicornplatform.com/blog/behavioral-health-conversion-pages-in-2026/)
- Why a phone call is a high-friction CTA for therapy clients — [CounselingWise](https://www.counselingwise.com/effective-call-to-action/), [Beacon Media + Marketing](https://www.beaconmm.com/blog/wondering-why-your-mental-health-websites-call-to-action-isnt-converting/)
- Reassuring vs transactional CTA language — [DigitalDot](https://digitaldot.com/how-to-create-engaging-ctas-for-therapy-practices/)
- Website's job is to reassure and remove friction — [Wandr Studio](https://www.wandr.studio/blog/therapist-website-design)
- Clear, mobile-friendly, trust-building, single clear CTA per screen — [10Web](https://10web.io/blog/therapist-websites/), [Practice Copilot](https://practicecopilot.com/websites-for-therapists/)
- Writing for one specific ideal client, not "people in general" — [Go Bloom Creative](https://gobloomcreative.squarespace.com/the-boss-blog/how-to-write-your-website-to-attract-your-ideal-client)
- Define goals, personas, and success metrics; effortless booking and WOW first impression — [CyberOptik](https://www.cyberoptik.net/blog/best-psychotherapist-websites/), [Azuro Digital](https://azurodigital.com/therapist-website-examples/)
