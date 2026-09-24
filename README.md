# Eric Ernstberger — Paintings

Development Preview — Sherfick Design

A dependency-free static gallery. Open `index.html` directly in a browser, or serve this folder with `python3 -m http.server 8080` and visit http://localhost:8080. No build, installation, backend, payment account, or external fonts required.

## Included experience

- Black entrance; one artwork at a time; stationary desktop information rail.
- Uncropped, proportional artwork; horizontal slides without fades.
- Previous/next, left/right arrows, Space (when focus is not on a button), swipe and mouse drag. Navigation wraps at the ends.
- F or Exhibition Mode enters fullscreen where supported, with an in-page fallback. Escape exits. Controls return on pointer movement; keyboard-focused controls stay visible.
- Optional poem drawer and Print → Delivery → Review → Payment demonstration.
- Native modal focus handling, labelled controls, reduced-motion support, and mobile/tablet layouts.

## Artwork and content status

Eight original working uploads could be recovered from the referenced conversation: Brookwood, Blue Semicircle, Greeting Party, Afar, Ten Little Deplorables, Winter Retreat (corrected upload), The Sea and Me, and Reefer. **Out to Dry and Family Affair were not available.** The earlier wrong-orientation Winter Retreat is excluded. No replacement artwork was invented.

`catalog.js` is the editable collection. IDs EE-003 through EE-010 are provisional, matching the recovered working collection's original order; confirm permanent catalog numbers with Eric. Source photographs were 1947–2048 pixels wide. Only resized WebP derivatives (maximum 1800 pixels on the longest side plus 800-pixel small copies) are included. Metadata is stripped. No PNG originals or production masters are packaged. Web images remain downloadable by viewers; they are not copy-protected.

Poems are currently null and the drawer says they have not been supplied. Add Eric's actual text to each `poem` field to replace the development message. No biography, price, edition, date, signature, or archival-paper claims have been invented.

Print dimensions are **illustrative, not approved production specifications**: Large image height 22 inches; Medium 75% and Small 55% of that height. Width is derived from the supplied photograph's aspect ratio. The sheet adds 6 inches to each dimension for the requested 3-inch border on each side. Eric must confirm original measurements, actual paper/printer limits, Small/Medium rules, and prices. `options()` in `app.js` owns the current calculation and can be replaced with approved per-artwork variants.

Delivery fields are an in-memory demonstration only. Use sample details. Nothing is transmitted or persisted, and closing the drawer clears the order. Payment collects no financial information, connects to no processor, and never places an order. Pricing, shipping and tax are explicitly unconfirmed.

## Files

- `index.html`, `styles.css`, `app.js`: presentation and interactions.
- `catalog.js`: artwork records and poems.
- `assets/`: web-sized artwork derivatives only.
- `_headers`, `robots.txt`: development indexing and browser policy settings.
- `404.html`: missing-page response.

## Private GitHub repository

Create a new **private** repository named `eric-ernstberger-art` in the intended GitHub account/organization. Upload the contents of this folder to its root, including dotfiles. Do not upload the ZIP inside the repository. Never add the production artwork library or credentials. GitHub Pages is not needed.

For a strictly private review, keep `main` as a neutral holding page until access protection is verified; put the artwork package on a `preview` branch. This avoids accidentally exposing the art through the Pages production hostname during setup. Restrict repository access to authorized collaborators.

## Cloudflare Pages deployment

Use **Workers & Pages → Create application → Pages → Connect to Git**, select GitHub, and grant access only to this repository. Use framework preset **None**, build command **`exit 0`**, build output directory **`.`**, and repository root as root directory. There are no environment variables. The `index.html` file must be at the output root. Choose `main` as production branch and enable preview builds for `preview`.

After pushing the package to `preview`, use the branch alias shown on the deployment details page as the stable client-review link. Commits to that branch update its alias. Individual deployment URLs remain accessible until removed.

**A private repository does not make a Pages deployment private.** In the Pages project, enable the access policy under **Settings → General**. In Cloudflare Access, configure the application policy to admit only the intended reviewer identities (for example, Eric's approved email and yours). Test an unauthenticated browser and an unauthorized identity, and then verify that the authorized reviewer can enter.

The Pages preview access toggle does **not** protect the production `<project>.pages.dev` hostname or custom domains. Keep artwork off production until separate Access coverage is configured for every hostname serving it. For production/custom-domain protection, follow Cloudflare's current Pages known-issues guidance linked below. Check branch aliases, hashed deployment URLs, production hostnames and custom domains individually before sharing. Do not rely on obscure URLs, `robots.txt`, or `noindex` for privacy.

Official deployment and privacy references (checked September 21, 2026):
- [Static HTML on Cloudflare Pages](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/)
- [Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/)
- [Preview deployments and Access protection](https://developers.cloudflare.com/pages/configuration/preview-deployments/)
- [Pages known issues, including Access coverage](https://developers.cloudflare.com/pages/platform/known-issues/)

This package has not been uploaded to GitHub or deployed to Cloudflare. Account setup and Access policies must be completed in the intended accounts.

## Before public launch

Recover the remaining two images, confirm all catalog facts and print dimensions, add poems and approved pricing/fulfillment information, and integrate a real payment provider with server-side order validation and fulfillment. Replace the preview label and remove development noindex directives only when Eric approves a public release. Test authorized/unauthorized access again after hosting changes.

## Browser verification checklist

Check entrance, all artwork navigation including wraparound, mouse drag and touch swipe, keyboard shortcuts, reduced motion, fullscreen exit, modal Escape/focus return, all order steps and back buttons, invalid delivery fields and quantity limits. Check phone portrait, tablet landscape, and desktop. Browser fullscreen support varies (especially on phones); in-page exhibition mode remains available.
