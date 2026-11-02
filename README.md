# HireHub marketing redesign

Seven responsive, statically generated marketing pages. No portal or backend implementation. Employer and candidate registration links use the existing portal destinations.

Run `npm run build` to generate `dist/`, `npm run check` to verify page structure and links, and `npm run preview` for a local server on port 4173.

## Conversion design

The homepage introduces the platform, routes both audiences, explains matching and account creation, addresses verification concerns, and repeats registration actions. Employer and candidate pages provide campaign-specific destinations. Pricing and FAQ interactions work entirely in the browser. The header registration chooser avoids assuming a visitor's audience.

Product visuals are illustrative, not screenshots of the actual portal. Example people and opportunities are labelled. No customer logos, testimonials or performance figures are invented. Fonts are loaded from Google Fonts, with local fallbacks.

## Measurement

Registration links dispatch `hirehub:registration-click` and push `registration_cta_click` into `window.dataLayer` only if that array already exists. Fields: `audience`, `placement`, `page_path`, `destination`. No analytics ID, consent manager, cookies or portal conversion integration is added. Connect the event to the client's approved analytics implementation. CTA clicks are not completed registrations.

## Handoff

Pricing reflects the public HireHub pricing page reviewed during implementation. Confirm current commercial terms before replacing the public site. The verification provider, actual portal screenshots, customer permissions and legal documents were not supplied. Replace the illustrations with approved screenshots if available. Existing policy and blog pages remain on the original site and are not recreated with invented content.

Reference sites: https://linear.app/ , https://attio.com/ , https://www.ashbyhq.com/ . Inspiration concerns messaging hierarchy and product presentation; their content and assets are not copied.
