# HireHub marketing redesign

Eight responsive, statically generated marketing pages using the original HireHub logo, black-and-white branding, Red Hat Display font and existing website copy. No portal or backend implementation. Employer and candidate registration links use the existing portal destinations.

Run `npm run build` to generate `dist/`, `npm run check` to verify page structure and links, and `npm run preview` for a local server on port 4173.

## Conversion design

The homepage preserves “Verified people. Smarter matching. Faster hiring.” and turns the existing product propositions into CV-builder, employer-shortlist, verification, matching, workflow, commission, flexible-work and badge graphics. Employer and candidate pages provide campaign-specific destinations. Pricing and FAQ interactions work entirely in the browser. The header registration chooser avoids assuming a visitor's audience.

Product visuals are illustrative, not screenshots of the actual portal. Example people and opportunities are labelled. No customer logos, testimonials or performance figures are invented. Fonts are loaded from Google Fonts, with local fallbacks. The client explicitly confirmed separate identity and UK right-to-work checks in this chat; the graphic represents them as separate statuses.

## Measurement

Registration links dispatch `hirehub:registration-click` and push `registration_cta_click` into `window.dataLayer` only if that array already exists. Fields: `audience`, `placement`, `page_path`, `destination`. No analytics ID, consent manager, cookies or portal conversion integration is added. Connect the event to the client's approved analytics implementation. CTA clicks are not completed registrations.

## Handoff

Build entry: `brand-site.mjs`; graphics: `graphics.mjs`; original rendered copy snapshots and source URLs: `content/*.json`; brand assets: `assets/`; visual style: `brand.css`. Pricing reflects the public HireHub pricing page reviewed during implementation. Original policy and blog links remain in the footer. The source site contains raw text blocks as well as paragraphs; the copy helper preserves both forms for the main propositions.

Reference sites: https://linear.app/ , https://attio.com/ , https://www.ashbyhq.com/ . Inspiration concerns messaging hierarchy and product presentation; their content and assets are not copied.
