# virtual-tansu
Building a gui to help Florida Kimono Club members organize their closet and plan outfits. 

1) A visual kimono collection management platform that replaces spreadsheets and manual tracking with a digital closet designed specifically for kimono owners.
2) For kimono collectors with growing collections, this app replaces tedious spreadsheets with a visual, purpose-built kimono closet management system that makes it easy to organize, browse, and rediscover what they own without physically handling garments.

Eyebrow/kicker: The first app built for kimono organization — ever.
Hook: Stop scrolling through 200 photos or flipping through heavy stacks of tatoushi on the floor. Plan the perfect kimono coordination — before you're standing in front of your closet.
Hero: Built by kimono wearers, for kimono wearers — finally, a closet app that speaks the language.

Business Model Canvas

Customer Segments: Casual kimono collectors with sizable closets, Collectors with mobility or physical limitations, Kimono sellers, Show-and-tell enthusiasts, Stylists, Influencers and content creators, Value Proposition

Revenue Streams: Free tier for small collections, Collector tier for larger closets, Seller tier for inventory and sales management, Professional tier for stylists and influencers, Optional marketplace transaction fees, Featured listings and premium tools, Key Activities

- Build and maintain the Virtual Closet
- Build and maintain the Flatmono Outfit Planner
- Develop collection organization and search tools
- Support buying/selling workflows

  <h2>Part of the Florida Kimono Club project. A closet cataloging and outfit-planning tool for kimono wearers — the first app built for this niche.

## What it does

**Closet tab**
- Add pieces across (x) categories: Kimono, Obi, Obiage, Obijime, Han-eri, Hakama, Accessories
- Each piece records name, season (Awase / Hitoe / Usumono / Year-round), an image URL or color swatch, and free-form notes for motif/occasion
- Filter the grid by category
- Cards are styled as folded tatoushi, echoing the physical wrapping paper used to store real kimono

**Coordinate tab**
- Pick one item per category to build a coordination
- See a stacked preview of the selected pieces
- Name and save the combination for later reference
- Saved coordinations are listed with quick delete

## Current status

- Built as a React app shell (single-file artifact)
- Data persists via the artifact's built-in storage (private per user — closet contents are not shared)
- Runs as a Progressive Web App target: no App Store / Google Play submission required for launch

## Known limitations / next steps

- **No real photo upload yet.** Pieces currently take a pasted image URL or fall back to a color swatch. Actual image upload/storage needs a backend — Firebase (Storage + Firestore) was the recommended path, chosen over a custom API for speed at solo-founder scale.
- **Accessories is currently a catch-all** — tabi, zori, and other pieces are folded into one category. Worth revisiting if that feels too broad once real wardrobe data is in.
- **No auth yet** — the app currently has no login, so persistence is scoped to this artifact session rather than a real user account.

## Fixed in this pass

- The "Add a piece" modal previously used `position: fixed`, which on mobile could render underneath/behind the phone's system navigation buttons (Google Android gesture bar), causing accidental taps. It's now scoped (`position: absolute`) to the app's own container, with `env(safe-area-inset-bottom)` padding as a backup.

## Related notes from this project

- Hero/hook copy: "Stop scrolling through 200 photos or flipping through heavy stacks of tatoushi on the floor. Plan the perfect kimono coordination — before you're standing in front of your closet." / "Built by kimono wearers, for kimono wearers — finally, a closet app that speaks the language."
- Value chain notes: 20 clients/month target, $5/engagement, PWA-first delivery to avoid app store review overhead
- Lead capture: Tally form on floridakimono.com, feeding a beta tester list
    </h2>
Improve collection visualization features
Support collection sharing and showcasing
