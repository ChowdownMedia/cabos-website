# Cabos Mexican Restaurant - Harvest Sheet (Nolensville, TN)

Single location. Sibling brand to El Metate / El Sombrero / El Molcajete (LiveWire).

## Identity / contact (live GHL site, rendered)
- Name: Cabos Mexican Restaurant (Nolensville)
- Address: 7336 Nolensville Rd, Nolensville, TN 37135
- Phone: (615) 819-0341
- Google Place ID: ChIJVdOshK52ZIgR3wctdf-3npg  (map embed + reviews)
- Facebook: https://www.facebook.com/CabosNolensville/
- Instagram: https://www.instagram.com/cabosmexicanrestaurants/
- GHL location id: WEmDSkogylXEGfLcn1NK

## Ordering / VIP
- Online ordering (SkyTab): https://online.skytab.com/39d01a1c2bfd34d87a6d530da328ae24
- Legacy OLO (livewireorders acct 1227928): https://www.livewireorders.com/api/fb/dp_xpo
- VIP (LiveWire/Boomerangme): https://cabosnolensville.livewiremediapartners.com/join-now
- VIP stats: https://cabosnolensville.livewiremediapartners.com/campaign-stats

## Current site structure (GHL, to re-create)
Home / Menu / Become a VIP / Gallery / Online Ordering / Events
- Home: video hero, "Order Online" band, Reviews, "Get in Touch" contact form (First/Last/Email/Message), footer.

## Brand DNA (from real logo: LOGO CABOS OK copy copy.jpg)
Oval beach badge. Cabo San Lucas El Arco rock arch over turquoise sea + blue sky.
"CABOS" wordmark = teal/turquoise elegant serif, white outline, spiral swirl inside the O.
"MEXICAN RESTAURANT" white beneath. Beaded oval border of lime-green + golden-yellow dots.
Palette: turquoise/teal (#0E9BA6-ish), ocean/sky blue, sandy tan/cream, lime green + golden yellow accents.
Motif: sea, arch, sun, coastal Baja. (Opposite of El Metate's stone/terracotta.)

## Assets on Drive
- Logo hi-res: LOGO CABOS OK copy copy.jpg  id 1TfmmIpw87mamN_gVylpfXH5MMfiA--dq  (in shared logo folder 16oLeGPwX0aYJYqxqXcTRAaNzcOy8cSNR)
- Logo round button: Cabos_Logo_Button.png  id 1oNHojh0AIaAbqAAcExWvTViDyIjzI_lI
- LATEST photo shoot (May 2026 pro dishes) folder id: 1lzadzpi9pTGmgOlW6pNSTb0gFhJZ2QN2
  Chicken Quesadilla, Chimichanga (6), Diablo Shrimp (4), Chicken Tacos (4),
  Birria Tacos (2), Guacamole (4), Enchiladas (3). 20-33MB each, need downsize.
- Nashville video (June 2026) folder id: 1ZY4CEJkWuR6c-d0mg6_JoHrxn5s-3f7f (CABOS NASHVILLE_1/2/3.mp4)
- Interior/older shots folder id: 1v7mfURBz5TyooaCRmCR-RI1zwatN7fls (CaboTacoInterior4, spreads)
- Control sheet: Cabos - NolensvilleTN - LiveWire Control Sheet (id 1pUBZTv1dNUxLy-vrpeDXVvlweeZ_8bIuaXT_s9cBwQg)

## OPEN ITEMS (need before/at build)
1. ChowdownOS forms client id for Cabos (contact form routing) - same source as El Metate 364.
   -> Either generate the Cabos shell in ChowdownOS Website Builder (bakes it in), or look up.
2. VIP system decision: keep LiveWire join-now link, OR wire ChowdownOS /api/public/vip/signup
   (needs a Cabos vip client id). El Metate used ChowdownOS.
3. Menu content: pull from /menu render or SkyTab at build (content-frozen, re-chrome only).
4. Hours: not on control sheet; pull from Google (Place ID) or confirm.
5. CF Pages project name + custom domain cutover plan (mirror el-metate: repo -> CF git deploy).
