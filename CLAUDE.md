# Poradce pro zdraví - Project Documentation

## Overview
Website for a health advisor & pharmacist (Mgr. Kristýna Šubrtová) offering individual consultations on medications, nutrition, supplements, smoking cessation, and private yoga lessons.

## Tech Stack
- Pure HTML5, CSS3
- No JavaScript, no frameworks, no build tools
- System fonts (no Google Fonts)
- Clean URLs via Apache `.htaccess` RewriteEngine (removes .html extensions)

## Color Palette
| Variable | Hex | Usage |
|----------|-----|-------|
| `--color-bg` | `#FAFAF8` | Main background |
| `--color-bg-alt` | `#F5F5F2` | Alternate sections |
| `--color-primary` | `#6B8E6B` | Muted green accents, CTA background |
| `--color-primary-dark` | `#5A7A5A` | Hover states |
| `--color-primary-light` | `#E8F0E8` | Light green backgrounds |
| `--color-text` | `#4A4A48` | Main text |
| `--color-text-light` | `#6B6B69` | Secondary text |
| `--color-text-muted` | `#8A8A88` | Muted text |

## File Structure
```
poradceprozdravi/
├── assets/
│   └── img/
│       ├── logo.jpg              # Mandala logo (header)
│       ├── favicon.jpg           # Favicon (browser tab)
│       ├── hero-home.jpg         # Homepage hero (flowers)
│       ├── hero-about.jpg        # O mně hero (birch leaves)
│       ├── hero-leky.jpg         # Lékové poradenství (capsules)
│       ├── hero-stravovani.jpg   # Zdravé stravování (food)
│       ├── hero-doplnky.jpg      # Doplňky stravy (turmeric)
│       ├── hero-koureni.jpg      # Odvykání kouření (leaf)
│       ├── hero-joga.jpg         # Lekce jógy (meditation)
│       └── hero-kontakt.jpg      # Kontakt (chamomile)
├── css/
│   └── styles.css                # All styles
├── materialy/                    # Source images (not used on web)
├── index.html                    # Homepage
├── o-mne.html                    # About page
├── lekove-poradenstvi.html       # Medication consultations
├── zdrave-stravovani.html        # Nutrition consultations
├── doplnky-stravy.html           # Supplements consultations
├── odvykani-koureni.html         # Smoking cessation
├── lekce-jogy.html               # Private yoga lessons
├── kontakt.html                  # Contact page
├── .htaccess                     # Apache clean URL rewrite rules
├── robots.txt                    # Search engine access rules
└── sitemap.xml                   # Sitemap for SEO
```

## URLs & Navigation
All internal links use clean URLs (without `.html`), e.g. `/o-mne`, `/kontakt`, `/lekove-poradenstvi`. The `.htaccess` file handles rewriting on the server.

- Úvod (`/`)
- O mně (`/o-mne`)
- Služby (dropdown):
  - Lékové poradenství (`/lekove-poradenstvi`)
  - Zdravé stravování (`/zdrave-stravovani`)
  - Doplňky stravy (`/doplnky-stravy`)
  - Odvykání kouření (`/odvykani-koureni`)
  - Lekce jógy (`/lekce-jogy`)
- Kontakt (`/kontakt`)

## Key CSS Classes
- `.header` - Sticky header with logo
- `.hero` - Hero sections
- `.hero--with-image` - Hero with background image (horizontal gradient overlay on desktop)
- `.hero--small` - Smaller hero for subpages
- `.section` / `.section--alt` - Content sections
- `.container` / `.container--narrow` - Max-width containers
- `.card` - Service cards with hover effect
- `.btn--primary` / `.btn--ghost` - Button styles
- `.info-box` - Highlighted info boxes (pricing, GDPR)
- `.steps` - Process steps with numbered circles
- `.bullet-list` - Lists with green bullet points
- `.credentials` - Credentials/qualifications box
- `.faq-list` / `.faq-item` - FAQ styling
- `.cta` - Call-to-action section (green background)
- `.footer__info` - Business info in footer (only on Kontakt page)

## Page Structure

### Service Page Template
Each service page follows identical structure:
1. Hero with title + intro + email CTA button (no ghost button)
2. "Pro koho je služba vhodná" (bullet list)
3. "Co společně vyřešíme" (bullet list)
4. "Jak spolupráce probíhá" (3 steps)
5. "Cena a délka" (info-box)
6. "Časté dotazy" (FAQ list)
7. CTA section (green, email button only)
8. Footer

### CTA Section
Green section before footer on every page with:
- Headline specific to the page
- Short description
- Primary button (mailto) only — no ghost/secondary button on service pages and homepage

## Typography
- Body text: System sans-serif font stack (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, ...`)
- Hero h1: Serif font (`Georgia, "Palatino Linotype", "Book Antiqua", Palatino, serif`) — darker color `#2A2A28`
- Hero p: Darker color `#3A3A38`
- Homepage h1: Larger size (3.5rem)
- H2: `--font-size-3xl` (2rem)
- Czech typographic orphans: All single-letter prepositions (a, i, k, o, s, u, v, z) use `&nbsp;` to prevent orphans at line ends

## Hero Image Overlay
Hero images use a CSS gradient overlay for readability:
- **Mobile**: Uniform semi-transparent overlay (`rgba(250,250,248, 0.75)`)
- **Desktop (900px+)**: Horizontal gradient — vivid/transparent edges, opaque center behind text
- **Homepage**: Taller hero (min-height 600px), radial gradient centered on text area, more vivid image on all sides

## Images
All hero images optimized with ImageMagick:
- Max width: 1920px
- Quality: 80%
- Metadata stripped
- Total size: ~2.7 MB (reduced from 22 MB, 88% savings)

| Image | Size |
|-------|------|
| hero-stravovani.jpg | 504 KB |
| hero-kontakt.jpg | 450 KB |
| hero-home.jpg | 376 KB |
| hero-doplnky.jpg | 371 KB |
| hero-about.jpg | 274 KB |
| hero-joga.jpg | 265 KB |
| hero-leky.jpg | 166 KB |
| hero-koureni.jpg | 91 KB |
| logo.jpg | 90 KB |
| favicon.jpg | 90 KB |

## SEO
- `robots.txt` - allows all crawlers, references sitemap
- `sitemap.xml` - all 8 pages with priorities, clean URLs
- Meta descriptions on all pages
- Canonical tags (`<link rel="canonical">`) on all pages
- Open Graph tags (`og:type`, `og:url`, `og:title`, `og:description`, `og:image`) on all pages
- Favicon on all pages
- Sitemap URL: https://poradceprozdravi.cz/sitemap.xml

## Pricing
- Osobní konzultace (60 min): 1 200 Kč
- Online konzultace (45 min): 1 000 Kč
- Navazující konzultace (30 min): 500 Kč
- Jednotlivý, konkrétní dotaz: do 500 Kč (po domluvě)
- Lekce jógy (60 min): 1 200–1 500 Kč (dle pronájmu prostor)
- Balíček 5 lekcí jógy: sleva 10 %
- Platba předem

## Contact
- Email: info@poradceprozdravi.cz
- No contact form (mailto links only)
- No phone on public pages (phone only in fakturační údaje)

## GDPR & Business Info
Contact page includes:
- GDPR info box (Nařízení EU 2016/679)
- Fakturační údaje:
  - Mgr. Kristýna Šubrtová
  - IČO: 05273021
  - Sídlo: Jižní VII, Praha 4, 141 00
  - Telefon: +420 737 915 403

## Footer
All pages share the same footer with:
- Logo text "Poradce pro zdraví"
- Navigation links (Úvod, O mně, Kontakt)
- Copyright 2026
- Business info (IČO, adresa) only on Kontakt page

## Navigation
- Služby dropdown uses `tabindex="0"` on the trigger `<a>` element for mobile touch support (`:focus-within`)
- Dropdown menu aligned right (`left: auto; right: 0`) on tablet (640px+) to prevent overflow

## Responsive Breakpoints
- Mobile: < 640px (single column)
- Tablet: >= 640px (2 columns)
- Desktop: >= 900px (3 columns, larger spacing, hero gradient)

## Design Principles
- Calm, airy design with lots of whitespace
- Rounded corners (8px, 12px)
- Subtle shadows
- Mobile-first responsive CSS
- Accessibility: skip-link, proper heading structure, focus states

## Content Owner
Mgr. Kristýna Šubrtová — lékárnice, poradkyně pro výživu, lektorka jógy
