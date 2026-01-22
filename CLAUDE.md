# Poradce pro zdraví - Project Documentation

## Overview
Website for a health advisor & pharmacist offering individual consultations on medications, nutrition, supplements, smoking cessation, and yoga.

## Tech Stack
- Pure HTML5, CSS3
- No JavaScript, no frameworks, no build tools
- System fonts (no Google Fonts)

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
├── robots.txt                    # Search engine access rules
└── sitemap.xml                   # Sitemap for SEO
```

## Navigation
- Úvod (index.html)
- O mně (o-mne.html)
- Služby (dropdown):
  - Lékové poradenství
  - Zdravé stravování
  - Doplňky stravy
  - Odvykání kouření
  - Lekce jógy
- Kontakt (kontakt.html)

## Key CSS Classes
- `.header` - Sticky header with logo
- `.hero` - Hero sections
- `.hero--with-image` - Hero with background image
- `.hero--small` - Smaller hero for subpages
- `.section` / `.section--alt` - Content sections
- `.container` / `.container--narrow` - Max-width containers
- `.card` - Service cards with hover effect
- `.btn--primary` / `.btn--ghost` - Button styles
- `.info-box` - Highlighted info boxes (pricing)
- `.steps` - Process steps with numbered circles
- `.bullet-list` - Lists with green bullet points
- `.credentials` - Credentials/qualifications box
- `.faq-list` / `.faq-item` - FAQ styling
- `.services-strip` - Links to other services at bottom
- `.cta` - Call-to-action section (green background)

## Page Structure

### Service Page Template
Each service page follows identical structure:
1. Hero with title + intro + CTA
2. "Pro koho je služba vhodná" (bullet list)
3. "Co společně vyřešíme" (bullet list)
4. "Jak spolupráce probíhá" (3 steps)
5. "Cena a délka" (info-box)
6. "Časté dotazy" (FAQ list)
7. CTA section (green, call-to-action)
8. "Další služby" strip (links to other services)
9. Footer

### CTA Section
Green section before footer on every page with:
- Headline specific to the page
- Short description
- Primary button (mailto) + secondary button (contact/services)

## SEO
- `robots.txt` - allows all crawlers, references sitemap
- `sitemap.xml` - all 8 pages with priorities
- Meta descriptions on all pages
- Favicon on all pages
- Sitemap URL: https://poradceprozdravi.cz/sitemap.xml

## Pricing
- Standard consultation (60 min): 1 000 Kč
- Short consultation (30 min): 500 Kč
- Yoga lesson (60 min): 800 Kč

## Contact
- Email: info@poradceprozdravi.cz (placeholder)
- Phone: +420 000 000 000 (placeholder)
- No contact form (mailto links only)

## Responsive Breakpoints
- Mobile: < 640px (single column)
- Tablet: >= 640px (2 columns)
- Desktop: >= 900px (3 columns, larger spacing)

## Design Principles
- Calm, airy design with lots of whitespace
- Rounded corners (8px, 12px)
- Subtle shadows
- Mobile-first responsive CSS
- Accessibility: skip-link, proper heading structure, focus states

## Content Owner
Placeholder - update with real contact info before launch
