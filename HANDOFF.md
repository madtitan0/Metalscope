# MetalScope India — Session Handoff

## Project
Pure vanilla HTML5 / CSS3 / JS — zero frameworks.
Repo: `madtitan0/Metalscope` (GitHub), branch `main`.
Local path: `/Users/muhammedriyaz/Projects/metalscope-website/`

---

## Brand Tokens (css/style.css :root)
- `--red: #d72226` / `--red-dark: #b31c20`
- `--navy: #1a7fc1` / `--navy-dark: #1568a0`
- `--black: #0A0A14` / `--black-mid: #12121F`
- Fonts: Rajdhani (display), Inter (body), Barlow Condensed (numbers)
- Clearbit logo API: `https://logo.clearbit.com/{domain}`

---

## Pages
| File | Status |
|---|---|
| `index.html` | Home — mostly done, content tweaks needed |
| `about.html` | About / Who We Are — content tweaks needed |
| `mission-vision.html` | Vision + Mission + Values — content tweaks needed |
| `verticals.html` | Business Verticals overview — content tweaks needed |
| `peb.html` | Pre-Engineered Buildings landing page |
| `structural-steel.html` | Structural Steel landing page |
| `bridges.html` | Bridges & Infrastructure landing page |
| `railcar.html` | Railcar & Rolling Stock landing page |
| `steel-doors.html` | Steel Doors landing page |
| `epc.html` | EPC Projects — "content to be provided by client" |
| `highrise-datacentres.html` | High-Rise & Data Centres — "content to be provided by client" |
| `projects.html` | Projects portfolio — needs industry-wise cards |
| `excellence.html` | Excellence — "content awaited from client" |
| `media.html` | Media — "content to be provided by client" |
| `contact.html` | Contact Us |

---

## Content Source — STRICT RULE
**ALL text content must come exclusively from the PDF / content brief provided by the client.**
File in repo: `METAL SCOPE - WEBSITE CONTENT Breakdown.pdf`
Do NOT use AI-generated placeholder text. If a section says "(Content to be provided by client)" leave a visible placeholder.

---

## Pending Tasks (Priority Order)

### 1. Content Audit & Replacement — All Pages
Go through every page and replace any text not from the PDF with exact PDF wording.

**Home page (`index.html`) — key content checks:**
- Numbers section left side: Headline = "BUILT TO DELIVER PROJECTS", Sub = "ONE STOP SOLUTION FOR ALL YOUR STRUCTURAL NEEDS", paragraph verbatim from PDF p.2
- Numbers right side: 20+ Years, 2 Factories, 20+ Bridges, 7000+ Coaches, 5000+ Projects
- WOW section heading = "WAY OF WORKING", subheading = "PROJECT DELIVERY IS NOT OUR CLAIM, IT IS OUR SYSTEM!"
- Key statement = "WE THINK IN KITS. EXECUTE IN PRECISION. DELIVER WITH CERTAINTY — END TO END"
- Steps: DESIGN → ENGINEERING → PRODUCTION → PAINTING → DESPATCH → SITE ERECTION
- Relay quote: "Every function is a runner in the relay, and passing the baton right, at the right time, to the right person is the essence of our culture."
- Commitment section heading: "OUR COMMITMENT – POWERED BY THE THEORY OF CONSTRAINTS (TOC)"
- Commitment cards (8): On-time Delivery / Reliable After-Sales Service / Over 20+ Years of Expertise / Valued Engineering Solution (Efficient Solution) / Quality System (Stringent) / Dynamic Team Work / Committed Partnership / Total Solution Provider

**About page (`about.html`) — key content:**
- Tagline: "Built on Steel, Driven by Vision: A Legacy of Engineering Excellence"
- 6 pillars: Engineering Legacy / Infrastructure at Scale / Built for Tomorrow / Precision in Every Structure / Trusted Across Industries / Strength Through Innovation (exact text from PDF p.12)
- What We Do heading: "Engineering the Future of Steel Infrastructure"
- 6 boxes from PDF p.13 (End-to-End Execution / Built for Scale / Manufacturing Excellence / Powering Industries / Sustainable by Design / Precision. Quality. Delivery.)
- Finishing line: "By combining engineering intelligence with execution flexibility, MetalScope delivers customized steel solutions aligned with timelines, budgets, operational goals, and global quality standards."
- Chairman's Message: V. Santhanam, exact text from PDF p.14

**Mission-Vision page (`mission-vision.html`):**
- Vision heading: "BUILD WHAT ENDURES." + 2 bullet points from PDF p.14
- Mission heading: "DELIVER CERTAINTY." + 2 bullet points from PDF p.15
- 4 Core Values from PDF p.15: Engineering Excellence / On-time Delivery / Sustainable Building / Customer Trust

### 2. WOW Section — Line During Hover (FIXED in commit 3d...)
The connecting line was bleeding through the hovered icon because the hover background was semi-transparent. Fixed by keeping `background: var(--black-mid)` (solid) on hover.

### 3. Hero Tag (FIXED)
"India's Trusted Structural Engineering Partner" bar — background is now `var(--navy)` (blue), text is white.

### 4. Projects Page — Industry Cards
`projects.html` needs industry-wise cards per PDF pp.25-30. Each card: image, industry name, associated clients (text or logos), hover interaction.
Full industry list from PDF: Automotive / Construction Equipment / EV / Electronic Mfg Services / Equipment & Machinery / Heavy Equipment / Home Appliances / FMCG / Food & Beverage / Pharmaceutical / Semi-conductor / Tire & Rubber / Oil & Gas / Renewable Energy / SEZ / Shoe Mfg / Yellow Goods / Japanese Industrial / Speciality Chemical / Process Industry / Pressure Valve / High-Rise Buildings / Data Centres / Social Infrastructure / Commercial Complexes / Multi-Level Buildings / Transportation & Logistics

### 5. Projects — "Know More" Redirection (Team Issue #3)
Currently all project "Know More" buttons go to `projects.html` generically. Each should eventually link to a per-project detail page or at minimum anchor to the relevant industry section.

### 6. Flip Cards on Home — Exact PDF Content
Current flip cards may have incomplete content. Verify against PDF:
- PEB flip side: 5 sectors with all sub-items (Industrial / Warehouse / Commercial / Social & Institutional / Transportation Infrastructure)
- Infrastructure: ROB / RUB / FOB / Flyover / Network Marine Arch Bridge
- Rail Coaches: MEMU 2000+ / EMU 2000+ / DMU 2000+ / Vande Bharat 520 / LHB 3500+ / 5950 components
- Modular Buildings: Assembling at Site / Interlocked Cabinets / Modular Homes / Modular Buildings / High Rise Buildings / Data Centres / Composite Structures

### 7. Images (Team Issue #2)
Actual MetalScope project images need to be added. Currently using Unsplash placeholders. Client to provide images.

### 8. Clientele Section
- Major brand logos load via Clearbit API (`logo.clearbit.com/{domain}`)
- On image load failure → styled name badge (red-tinted odd, navy-tinted even)
- Scale on hover: `transform: scale(1.18)` with smooth transition
- Government/small entities without Clearbit entries remain as badges: CSD, Indian Railways, ICF Chennai, JIPMER, MES, MORTH, Ocean, S&T, Zigma, Senara, VME Precast, Qualtech Engineers

### 9. Testimonials
- 3 video cards, all play buttons are navy blue
- Cards: Honda Cars India (Automotive/PEB), Foxconn (Semiconductor/EMS), ICF Chennai (Railways/Rolling Stock)
- Per PDF p.8: "A set of 3 testimonial videos to be placed" — actual YouTube/video links to be added by client

---

## UI/Design Rules Applied
- Active nav link → `var(--navy)` color + navy underline
- Nav dropdown hover → `var(--navy)`
- WOW section: odd steps = red icons, even steps = navy icons; connector line = red→navy gradient
- WOW relay quote block → navy left border
- Cert cards: odd = red icon/hover, even = navy icon/hover
- Awards timeline year number → `var(--navy)` (was near-invisible rgba red)
- Lead form tag + input focus → navy blue
- Hero tag bar → `var(--navy)` background, white text

---

## Git History (recent)
```
24fe66d Fix WOW hover line, blue hero tag, blue play buttons, logo domains
6dc4fa4 UI polish: blue accents, blur fix, logo hover scale, year visibility
9ffe98a Client revisions: brand colors, logos, clientele grid, 20-Years badge, portfolio gaps, mobile nav, about page
```

---

## Known Issues / Warnings
- Clearbit free API may rate-limit or return 404 for less-known companies — onerror badge fallback handles this gracefully
- `projects.html` "Know More" links all point to `projects.html` — needs per-project routing
- Some vertical landing pages (`epc.html`, `highrise-datacentres.html`) are "content to be provided by client" — keep placeholders
- Excellence page and Media page are both "content awaited/to be provided by client"
