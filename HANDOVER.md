# Yes& — Handover Report

**Prepared:** 2026-04-24
**Brand:** Yes& (rebrand of Amy Victoria Rowe, relaunched 2026)
**Founder:** Amy Rowe
**Positioning:** "Thoughtful by design." — premium, immersive experience design for private (HNW) clients and culturally driven brands.

> **Important note on scope of this document.**
> The technical/SEO sections below were audited directly against the live HTML in this repository (`index (10).html` and `index__9_ (1).html`) and are factual.
> The marketing-strategy, partner, and historical-conversation sections are marked **`[FILL IN]`** — they need to be populated from the WhatsApp threads and prior chat history, which were not available when this report was generated. Please paste / dictate that context in and a follow-up pass can complete it.

---

## 1. Brand snapshot (from live site copy)

- **Name:** Yes&
- **Tagline:** Thoughtful by design.
- **One-line description:** "Yes& creates premium experiences that bring people together and live on as stories."
- **Origin story (verbatim from site):** Founder Amy Rowe trained in drama in NYC (Meisner technique). Brought that approach into immersive storytelling via Secret Cinema, then launched Amy Victoria Rowe (2022) for HNW audiences and culturally driven brands. Relaunched as Yes& in 2026 — "a refined identity with renewed ambition." The name is borrowed from theatrical improvisation: an additive, dialogue-led way of working. Always asking what comes next.
- **Two audience pillars:** Private clients · Brand clients

### Service lines (as listed on the site)
1. Immersive Experiences
2. Flagship Activations
3. Private Festivals & Retreats
4. Curated Residencies & Seasons
5. Milestones & Celebrations
6. Cultural Collaborations
7. Year-Round Engagements
8. Private Audience Engagement
9. Content & Storytelling
10. Styling & Costume Design
11. Strategic Advisory

> Positioning line under Services: *"An end-to-end approach to event creation, with a specialism in immersive experience design."*

---

## 2. Technical / SEO audit (factual, from repo)

### What's working
- Title present and brand-led: *"Yes& — Thoughtful by design."*
- Meta description present and on-message (157 chars, within Google's display window).
- Open Graph title, description, and type set.
- Viewport + charset declared.
- All 11 `<img>` tags have `alt` attributes (accessibility + image SEO win).
- Hosted via Cloudflare (CDN, TLS, email obfuscation already in place).
- Web fonts (Playfair Display + DM Sans) loaded from Google Fonts with `display=swap`.

### Gaps to close (priority order)

| # | Gap | Why it matters | Fix |
|---|-----|----------------|-----|
| 1 | **No H1 on the page.** Only an H2 ("Something in mind?") and two H3s ("Private clients", "Brand clients") exist. | Search engines and screen readers expect a single, descriptive H1. Currently the page has no top-level heading. | Add an H1 in the hero, e.g. *"Yes& — premium, immersive experience design"* (visually styled to match the existing tagline, can be `sr-only` if the design doesn't allow visible text). |
| 2 | **No `rel="canonical"` link.** | Prevents duplicate-URL indexing issues (with/without trailing slash, www vs apex, UTM-tagged shares). | Add `<link rel="canonical" href="https://yesand.[tld]/">` to `<head>`. |
| 3 | **No Open Graph image / Twitter card.** | Social shares (Instagram DM, WhatsApp link previews, LinkedIn, X) currently render with no preview image. Critical for a brand that lives on referral. | Add `og:image` (1200×630), `og:url`, `og:site_name`, and `twitter:card = summary_large_image` with `twitter:image`. |
| 4 | **No structured data (schema.org).** | Misses eligibility for rich results — Organization, LocalBusiness, Person (Amy Rowe), and Service schemas are all relevant. | Add JSON-LD blocks: `Organization` (with `founder`, `sameAs` social links, logo), and a `Service` block per service line. |
| 5 | **No `robots` meta and no `sitemap.xml` / `robots.txt` in repo.** | Crawlers can't discover canonical URLs cleanly. | Add `robots.txt` allowing all + pointing to `sitemap.xml`. Generate a single-URL sitemap for now; expand as case-study pages launch. |
| 6 | **No analytics tag visible in the source.** Strings like `gtag`, `fbq`, `gtm` only appear inside an unrelated obfuscated blob — there is no GA4 / GTM / Meta Pixel / Plausible / Fathom snippet. | You can't measure SEO or marketing performance without it. | Install GA4 (or Plausible if you want cookie-light) + Meta Pixel if paid social is in scope. Add to `<head>`. |
| 7 | **Single-page site, no indexable case-study URLs.** | Long-tail SEO ("immersive event designer London", "private retreat producer", "Secret Cinema alumni event design") has no landing page to rank. | Publish at least one case study per service pillar as its own URL (`/work/[slug]`). Each gets its own title, meta, H1, schema, and OG image. |
| 8 | **No favicon / app icons declared.** | Brand polish on tabs, bookmarks, mobile home screens. | Generate full favicon set + `apple-touch-icon` + web manifest. |
| 9 | **No `lang` attribute observed on `<html>`** (verify). | Accessibility + locale signals. | Set `<html lang="en-GB">` (or appropriate). |
| 10 | **Two large HTML exports in the repo (~2.5 MB and ~2.6 MB).** | These look like full Editor X / Wix / Webflow exports — heavy and not a maintainable source of truth. | Decide on a canonical source (Webflow CMS? hand-built? Framer?) and treat the repo as deployable code, not exports. |

---

## 3. SEO setup — what to put live next

### Phase 1 — On-page (1–2 days work)
- [ ] Add H1 + canonical + OG image + Twitter card meta to the homepage.
- [ ] Add `Organization` and `Person` JSON-LD.
- [ ] Add `robots.txt` + single-URL `sitemap.xml`.
- [ ] Install GA4 + (if applicable) Meta Pixel.
- [ ] Verify the property in **Google Search Console** and **Bing Webmaster Tools**; submit the sitemap.
- [ ] Set `<html lang>`.

### Phase 2 — Content scaffolding (2–4 weeks)
- [ ] Decide URL structure: `/work`, `/services/[slug]`, `/journal`, `/about`, `/contact`.
- [ ] Publish 3–5 hero case studies (real clients, with permission, or anonymised).
- [ ] Publish a `/services` overview page + a page per top-tier service (Immersive Experiences, Flagship Activations, Private Festivals & Retreats first — those have the highest commercial intent).
- [ ] Add a contact page with a form + structured `ContactPoint` schema.
- [ ] Set up a journal/editorial section for thought leadership (helps E-E-A-T and gives PR coverage somewhere to live).

### Phase 3 — Off-page & authority (ongoing)
- [ ] Build a backlink target list: design press (Wallpaper, It's Nice That, Dezeen events), HNW lifestyle (Robb Report, How to Spend It, Tatler), industry (Event Magazine, C&IT, BizBash UK, Conde Nast Traveller).
- [ ] Founder profile: Amy Rowe positioned as the named expert (LinkedIn cadence, podcast outreach, speaker submissions).
- [ ] Capture press / awards mentions in a `Press` page with logos — also doubles as social proof.
- [ ] Consistent NAP (Name, Address, Phone) across LinkedIn, Companies House (if registered), any directories.

### Target keyword themes (initial hypothesis — needs SEO tool validation)
- "immersive experience designer" / "immersive event design London"
- "private event producer UK"
- "luxury retreat design"
- "brand activation agency London"
- "cultural programming consultancy"
- Branded: "Yes&", "Yes and event design", "Amy Rowe Yes&" (protect against the rebrand losing equity from "Amy Victoria Rowe" — set up 301s if old domain exists).

### Critical migration check (rebrand from AVR → Yes&)
- [ ] Does the old `amyvictoriarowe.com` (or equivalent) still exist? If yes → 301 every URL to the matching Yes& URL. If lost, recover any backlink equity via outreach.
- [ ] Update Google Business Profile, LinkedIn company page, Instagram bio, all directory listings to the new brand + URL.
- [ ] Search Console: keep both properties verified during transition; use the Change of Address tool.

---

## 4. SEO report — current baseline

| Metric | Value | Source |
|--------|-------|--------|
| Pages indexable | 1 (homepage only) | Repo audit |
| Title tag | Present | `<title>` |
| Meta description | Present, 157 chars | `<meta name="description">` |
| H1 | Missing | DOM scan |
| Canonical | Missing | DOM scan |
| Schema.org | None | DOM scan |
| OG image | Missing | DOM scan |
| Twitter card | Missing | DOM scan |
| Image alt coverage | 100% (11/11) | DOM scan |
| Analytics installed | None detected | DOM scan |
| Sitemap | Not in repo | Filesystem |
| Robots.txt | Not in repo | Filesystem |
| Mobile viewport | Set | `<meta name="viewport">` |
| HTTPS / CDN | Cloudflare | Asset paths |
| Page weight (HTML only) | ~2.5 MB | `wc` |

**Baseline traffic / rank data:** `[FILL IN — needs Google Search Console + GA4 export. Once installed, rerun in 30 days for first real baseline.]`

---

## 5. Marketing support — what's been done & what's next

> Everything in this section needs the WhatsApp / prior-chat context to be accurate. Treat the bullets below as the **structure** of the handover; the content under each is a placeholder.

### 5.1 Brand & creative
- Identity status (logo, type system, colour, photography direction): **`[FILL IN]`**
- Brand guidelines doc location: **`[FILL IN]`**
- Photography / video assets library location: **`[FILL IN]`**

### 5.2 Channels
| Channel | Handle / URL | Status | Owner | Cadence | Notes |
|---------|-------------|--------|-------|---------|-------|
| Website | `[FILL IN domain]` | Live (single page) | Amy / dev | — | See SEO audit above |
| Instagram | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Primary discovery channel for HNW |
| LinkedIn (company) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Brand-client funnel |
| LinkedIn (Amy personal) | `[FILL IN]` | `[FILL IN]` | Amy | `[FILL IN]` | Founder-led thought leadership |
| Newsletter | `[FILL IN platform]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | List size: `[FILL IN]` |
| Press / PR | `[FILL IN agency or in-house]` | `[FILL IN]` | `[FILL IN]` | — | Active pitches: `[FILL IN]` |

### 5.3 Campaigns in flight
- **Rebrand launch (Yes&, 2026):** announcement plan, asset list, embargo dates → **`[FILL IN]`**
- Paid activity (if any): **`[FILL IN]`**
- Partnerships / collaborations in negotiation: **`[FILL IN]`**

### 5.4 Pipeline / commercial
- Active enquiries: **`[FILL IN]`**
- Proposals out: **`[FILL IN]`**
- Confirmed projects 2026: **`[FILL IN]`**
- CRM / pipeline tool: **`[FILL IN]`**

### 5.5 Suppliers, freelancers & key contacts
| Role | Name | Contact | Notes |
|------|------|---------|-------|
| Web dev | `[FILL IN]` | `[FILL IN]` | |
| Designer | `[FILL IN]` | `[FILL IN]` | |
| Photographer | `[FILL IN]` | `[FILL IN]` | |
| PR | `[FILL IN]` | `[FILL IN]` | |
| Production partners | `[FILL IN]` | `[FILL IN]` | |

### 5.6 Decisions already taken (from prior chats / WhatsApp)
- **`[FILL IN — paste key decisions, e.g. "Don't pursue paid Meta until brand identity v2 is live", "Hold off on case studies until X client approves", etc.]`**

### 5.7 Open questions / things parked
- **`[FILL IN]`**

---

## 6. Access & credentials checklist

To be handed over (do **not** paste secrets here — use a password manager and reference the entry name):

- [ ] Domain registrar — `[FILL IN]`
- [ ] DNS / Cloudflare account — `[FILL IN]`
- [ ] Hosting / CMS — `[FILL IN]`
- [ ] GitHub repo (this one) — `lucywrapp10/yesyes`
- [ ] Google Workspace / email — `[FILL IN]`
- [ ] Google Search Console — `[FILL IN]`
- [ ] Google Analytics 4 — `[FILL IN]`
- [ ] Google Business Profile — `[FILL IN]`
- [ ] Meta Business Manager (FB / IG) — `[FILL IN]`
- [ ] LinkedIn page admin — `[FILL IN]`
- [ ] Newsletter platform — `[FILL IN]`
- [ ] CRM — `[FILL IN]`
- [ ] Brand asset store (Dropbox / Drive / Notion) — `[FILL IN]`
- [ ] Password manager invite — `[FILL IN]`

---

## 7. Recommended first 30 days for whoever picks this up

1. **Week 1:** Install GA4 + Search Console, ship the on-page SEO fixes (H1, canonical, OG, schema, robots/sitemap). Audit social handle consistency.
2. **Week 2:** Rebrand-redirect audit — make sure no Amy Victoria Rowe equity is leaking. Outreach to anyone linking to old URLs.
3. **Week 3:** Stand up the first case-study URL + one service deep-dive page. Brief copywriter / photographer for the next two.
4. **Week 4:** First baseline SEO report (rankings + impressions from GSC, even if thin) + content calendar for the next quarter.

---

## 8. What this document is missing (be honest)

This handover was generated against the codebase only. To be a real handover it needs:
- The WhatsApp thread context (decisions, supplier names, client conversations).
- Prior chat-thread context (strategy work, copy iterations, naming rationale beyond what's on the site).
- Actual analytics baselines once tracking is installed.
- Confirmed domain, social handles, and team contacts.

Paste any of the above into a follow-up and this report can be completed properly.
