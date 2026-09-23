# DEMO SITE SPEC — Ô Braisé Lomé

## Purpose
Build a demo one-page ordering site to pitch to Ô Braisé Lomé.
This is an UNSOLICITED PROPOSAL. The business has not commissioned it.

## CRITICAL RULES (do not skip)
1. Add a visible, permanent banner at the very top of the page:
   `DÉMO — maquette non officielle réalisée par [MY NAME] · non affiliée à Ô Braisé`
   Banner must be sticky and readable on mobile. Never hide it.
2. Do NOT collect real money. Payment buttons are visual only, disabled, with a
   tooltip "Démo — paiement non actif".
3. Do NOT invent customer reviews, testimonials, ratings, or awards.
4. Do NOT copy their logo file. Build a text-based wordmark "Ô BRAISÉ" instead.
5. Use ONLY the real public contact details listed below. Invent nothing else.
6. Page title/meta must include "Démo" so it never reads as the official site.

## The business
- Name: Ô Braisé Lomé
- Type: grilled chicken / fast food restaurant
- Address: Avenue de la Paix, Super Taco, non loin de l'ESA, Lomé, Togo
- Phone / WhatsApp: +228 91 28 10 30
- Instagram & TikTok: @obraise_lome
- Facebook: "Ô Braisé Lomé"
- Google rating: 4.4 (84 reviews) — do not display this, just context
- Hours: Mon–Tue 11h–22h, Wed CLOSED, Thu 11h–22h, Fri–Sat 11h–23h, Sun 15h–22h
- Price point: budget ~7,000–10,000 FCFA per person
- Existing delivery partners mentioned in their own posts: Gozem, Kaba
- Known menu items (from their public posts): Combo Poulet Ô Braisé,
  Combo BBQ Chicken Wings, Solo, Salade César (halal), burgers, frites

## The problem this demo solves
Customers currently order by WhatsApp message. Orders are free text, so items
get missed, prices are re-typed by hand, and the staff can't take orders while
busy. They have strong TikTok/Instagram presence but no order link in bio.

Pitch angle: "Gardez votre TikTok. Je règle ce qui se passe APRÈS le message."

## Colors
I could not confirm their official hex codes — they have no website.
STEP 1: Open instagram.com/obraise_lome, take the profile picture / a recent
post, and sample the 2–3 dominant brand colors. Use those as primary.
STEP 2: If sampling is not possible, use this fallback palette, built around
grilled-chicken / flame-grill visual language:

```
--charcoal:    #1C1917   /* backgrounds, nav */
--flame:       #E2571E   /* primary CTA, accents */
--ember:       #F5A524   /* hover, highlights */
--cream:       #FAF7F2   /* page background */
--leaf:        #3F7D3C   /* "halal" / fresh badges */
--text:        #2A2422
```
Rationale: dark charcoal + flame orange reads instantly as braisé/barbecue,
holds up against food photography, and stays legible on cheap phone screens.

## Typography
- Headings: a heavy condensed sans (Anton, Archivo Black, or Bebas Neue)
- Body: Inter or Work Sans
- Load from Google Fonts. Keep total weights to 2 files max.

## Build requirements
- Single self-contained HTML file. Inline CSS and JS. No build step.
- Mobile-first. Most viewers open this on a phone over mobile data.
- Total page weight under 500KB. Lazy-load images.
- French language throughout (Togo is francophone).
- No external JS libraries. Vanilla only.
- Must work offline once loaded (no CDN dependencies beyond the font).

## Images
Do NOT hotlink their Instagram photos.
Use CSS gradient / solid-color placeholder blocks sized like real photos, each
labeled "photo à remplacer". This keeps the demo honest and loads instantly.

## Page sections (in order)
1. **Demo banner** (sticky, per rules above)
2. **Hero** — wordmark, one line: "Poulet braisé, wings, burgers. Commandez en
   2 minutes." Two buttons: "Commander" (scrolls to menu) and "Appeler".
3. **Menu with live cart** — the core of the demo.
   - Categories: Combos, Wings, Burgers, Salades, Accompagnements, Boissons
   - 3–4 placeholder items per category with name, short description, price in
     FCFA, quantity +/- buttons
   - Prices are ESTIMATES in the 1,500–7,000 FCFA range. Label the menu section
     "Prix et plats à confirmer avec le restaurant" so nothing reads as fact.
   - Running cart total fixed to the bottom of the screen on mobile
4. **Checkout block** — name, phone, delivery or pickup toggle, address field,
   optional note. On submit: build a formatted WhatsApp message and open
   `https://wa.me/22891281030?text=...` with the full order pre-filled.
   THIS IS THE KILLER FEATURE — the order arrives in their existing WhatsApp,
   perfectly formatted, with zero new software for them to learn. Make this
   obvious and make it work flawlessly.
5. **Paiement (visual only)** — disabled buttons for T-Money, Flooz, espèces à
   la livraison. Caption: "Paiement mobile intégrable — démo non active."
6. **Infos** — hours table (mark Wednesday CLOSED clearly), address, embedded
   map link, Gozem/Kaba mention, links to their real Instagram and TikTok.
7. **Footer** — repeat the demo disclaimer + my name and contact.

## WhatsApp message format the checkout must generate
```
Bonjour Ô Braisé, je voudrais commander :
- 2x Combo Poulet Ô Braisé — 7 000 FCFA
- 1x Frites — 1 000 FCFA
Total : 8 000 FCFA
Mode : Livraison
Nom : [name]
Tél : [phone]
Adresse : [address]
Note : [note]
```

## Deliverable
`index.html`, ready to drop on Netlify or Vercel. Also output a one-paragraph
French summary of what the site does, which I will paste into WhatsApp with
the link.
