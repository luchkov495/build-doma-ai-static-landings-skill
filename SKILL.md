---
name: build-doma-ai-static-landings
description: Build or review static DOMA.ai-style landing pages for ЖКХ products. Use when the user asks to create, adapt, audit, or generate a landing/site/лендинг/лендос in the visual and copywriting style of DOMA.ai pages such as client_center, count_center, or strahovanie-zhkkh; especially for static HTML/CSS pages, product landing prototypes, and AI prompts/specs for future DOMA.ai pages.
---

# Build DOMA.ai Static Landings

## Core Rule

Create static DOMA.ai product landing pages, not dynamic applications. Use DOMA.ai's dark teal rounded-card system, green CTAs, ЖКХ-specific copy, and B2B operational tone. Dynamic controls such as calculators, tabs, sliders, forms, and quizzes should be represented as static visual states unless the user explicitly asks for interactivity.

## Resources

Load resources progressively:

- `references/brand-static-landing-guide.md` - primary guide. Read before creating or reviewing a DOMA.ai-style landing.
- `references/screenshots/` - visual references. Use for side-by-side comparison or visual fidelity checks:
  - `doma-client-center-desktop.png`, `doma-client-center-mobile.png`
  - `doma-count-center-desktop.png`, `doma-count-center-mobile.png`
  - `doma-insurance-desktop.png`, `doma-insurance-mobile.png`
  - `doma-legal-demo-desktop.png`, `doma-legal-demo-mobile.png`
- `references/audits/` - computed style and layout JSON from the original sites. Load only when exact sizes, colors, typography, or block measurements are needed.
- `assets/static-landing-template/` - working static HTML/CSS template with local assets. Copy this as a starting point when building a standalone static page.

## Workflow

1. Identify the product, target audience, main pain, product promise, and CTA. If details are missing, make the smallest practical assumption and proceed.
2. Read `references/brand-static-landing-guide.md`.
3. If creating a page from scratch, copy `assets/static-landing-template/` into the user's target folder or adapt the user's existing project structure.
4. Replace the sample product with the requested product while preserving the DOMA.ai page structure:
   - header;
   - hero with left dark card and right photo card;
   - two benefit cards;
   - wide CTA stripe;
   - static tabs/chips plus explanation card;
   - stats row;
   - feature cluster;
   - proof section on white background;
   - ecosystem cross-sell;
   - journal block;
   - footer.
5. Use generated or provided bitmap images for hero/support photos when relevant. Keep text in HTML/CSS, not baked into images.
6. Do not invent real metrics, legal guarantees, customer names, or testimonials. Use neutral proof blocks unless the user provides verified facts.
7. Verify in a browser at desktop and mobile widths. Check loaded images, no unintended horizontal page overflow, readable text, DOMA.ai color/radius/typography match, and static-only behavior.

## Style Anchors

Use the guide as source of truth, but keep these anchors in mind:

- background `#012025`;
- large cards `#17313B`, radius `40px`;
- CTA green `#2BC359`;
- gradients are restrained: dark `#17313B` base with soft blurred `#26C756 -> #4BA2E4` glow, not neon blobs;
- hero left-card background should use local `assets/hero-card-bg.webp` for exact DOMA.ai matching;
- CTA stripe should use the local `assets/stripe-bg.svg` asset or a faithful equivalent;
- white proof/ecosystem sections with large rounded corners;
- desktop H1/H2 around `44px/48px/700`;
- mobile H1 around `28px/31px/700`, H2 around `24px/26px/700`;
- container around `1280px` on desktop;
- header nav/phone/header CTA should be `14px/21px/500`; hero H1 `44px/48px/700`; hero subhead `18px/25px/400`; long cost CTA heading `31px/34px/700`.
- copy must mention concrete ЖКХ operations: УК, ТСЖ, МКД, ЖКУ, жители, заявки, квитанции, начисления, ГИС ЖКХ, договоры, подрядчики, проверки.
- do not add an extra tag/badge under breadcrumbs in the hero; DOMA.ai pages go from breadcrumbs directly to H1.
- icons in benefit cards should be plain line/SVG icons without rounded backing plates and without distortion.
- hero/card surfaces should not have visible border overlays; rely on rounded dark fills and soft gradients.

## Validation Checklist

Before finishing:

- Compare first viewport against `references/screenshots/*desktop.png`.
- Check mobile against `references/screenshots/*mobile.png`.
- Confirm dynamic elements are only static visual states unless requested otherwise.
- Confirm CTAs are short and practical: `Подключить`, `Рассчитать стоимость`, `Получить консультацию`, `Обсудить условия`.
- Report what was created, changed files, how it was checked, and any remaining risks.
