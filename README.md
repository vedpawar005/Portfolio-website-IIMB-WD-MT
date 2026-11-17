# Resume Website: CSS Styling Assignment

**Ved Pawar | B3T1 | Web Development Mid-Term Project**

**Live website:** [vedpawar005.github.io/Portfolio-website-IIMB-WD-MT](https://vedpawar005.github.io/Portfolio-website-IIMB-WD-MT/)

**GitHub repository:** [https://github.com/vedpawar005/Portfolio-website-IIMB-WD-MT](https://github.com/vedpawar005/Portfolio-website-IIMB-WD-MT)

The repository has two main code files: `index.html` for the content and `styles.css` for all the styling.

## Sections of the website and why I designed them this way

| Section | What it shows | Design decision |
| :--- | :--- | :--- |
| **Hero** | My name, tagline, dual-degree details, contact links, four key impact metrics (₹50K+, 350K+, 90+, 30+), action buttons, and my portrait photo. | The name is the biggest text on the page so it is seen first. A four-column metric strip sits right above the buttons so visitors see my biggest numbers immediately, and a tilted handwritten badge overlaps my photo to add personality. |
| **The Thesis (About)** | Two short paragraphs about combining a BBA at IIM Bangalore with a BSc in Business AI at the Institute of Science, Mumbai, plus two comparison cards and a quote. | Two side-by-side cards (*Engine A: Commercial* and *Engine B: Computational*) let the visitor compare my deal-making side and my AI side without reading a long block of text. |
| **Track Record (Experience)** | My roles as Vice President and Entrepreneurship Development Co-ordinator at the Rotaract Club of Ramnarain Ruia College, with dates, bullets, and outcome tags. | This section flips the layout so the cards are on the left and the section heading is on the right. Dates and club names come first in monospace font, followed by bullet points and summary tags at the bottom. |
| **The Playbook** | Three pillars on how I work: *Value-First Sponsorship Engineering*, *Student Founder Acceleration*, and *Multi-Department Execution at Scale*. | Instead of only listing past titles, I added this section to explain how I actually negotiate sponsorships, run student startup pitches, and manage 30+ directors across 13 departments. |
| **Dual-Track Academics** | IIM Bangalore (BBA), Institute of Science, Mumbai (BSc Business AI), Ramnivas Ruia Junior College (93.46% in MAH CET), and my State and District Science Contest wins. | The three education entries stack vertically so my concurrent degree timelines are clear, while the two science competition wins sit in a two-column card grid right below them so they do not get lost. |
| **The Operator's Stack (Skills)** | Technical and analytics tools, commercial and deal skills, governance tools, and five spoken languages. | Four grouped cards in a 2×2 grid with rounded pill tags instead of one long comma-separated list, with a one-line explanation under each heading. |
| **Off the Clock** | My personal interests outside work: playing Guitar and Flute, Chess, and Table Tennis. | Two columns side by side (*Acoustics & Breath* and *Tactics & Tempo*) so my musical instruments and strategy/reflex games stay separate. |
| **Executive Dossier (Resume)** | A full one-page printable resume preview alongside buttons to download the official PDF or print the page. | Styled like a white sheet of paper over the dark background so it reads like a traditional resume, paired with print media rules so Save as PDF outputs a clean one-page sheet. |
| **Initiate a Deal (Contact)** | IIM Bangalore email, phone/WhatsApp link, PDF resume download, and Google Maps link to Mumbai. | Each contact link is a large full-width row with an arrow icon so my email and phone number are easy to spot and click on any screen. |

## Improvements made

* Moved all the styling out of the HTML into one file, `styles.css`, and linked it in `index.html`. Colours, fonts, widths, and transitions are saved as CSS variables at the top of the file, so I can change them in one place.
* **Fonts:** *Bricolage Grotesque* for my name and headings, *Fraunces* italic for highlighted accent words and quotes, *Caveat* for handwritten badges and side notes, *Space Mono* for dates, numbers, and tags, and *DM Sans* for the main body text. All five come from Google Fonts with system fallbacks.
* **Colours:** A five-colour palette built around Prussian Blue (`#1d3557`), Steel Blue (`#457b9d`), Powder Blue (`#a8dadc`), Honeydew (`#f1faee`), and Imperial Red (`#e63946`) for buttons, active links, badges, and section borders. I also added a light/dark mode toggle button that updates the same CSS variables and remembers the choice in `localStorage`.
* **Navigation bar:** It stays at the top while scrolling with a blurred glass effect and is built with flexbox. Links change colour and get a red underline on hover, and on smaller screens it becomes a menu button.
* **Alternating layout:** Every section uses CSS Grid with two asymmetric columns (`0.78fr` and `1.22fr`). Odd sections put the sticky heading on the left and content on the right, while even sections (`.reverse`) flip the columns so the content is on the left and the heading is on the right. Inside the sections, 2-column and 4-column grids are used for metrics, skills, and achievements, while flexbox handles the header, buttons, and rows of pill tags.
* **Spacing and text:** A centred container up to `1180px` wide, generous vertical padding between sections, readable line lengths, and a line height of `1.68`. Heading sizes use `clamp()` so they shrink smoothly on smaller screens.
* **Hover effects and highlights:** Key words in section titles are emphasised with the `<em>` tag in italic serif and a wavy underline. Buttons, cards, and skill tags lift and tilt slightly with a spring transition of `0.28` seconds, and the tilted handwritten photo caption straightens out on hover.
* **Responsiveness and print:** The page uses responsive media queries at `900px` and `640px` so all alternating grids collapse into a single column on tablets and phones. I also added a print stylesheet so Save as PDF gives a clean one-page resume, and animations are turned off for visitors who have reduced motion enabled on their device.

## CSS concepts used

* **Selectors:** Element selectors for the base styles (`body`, `h1` to `h3`, `p`, `ul`, `a`, `button`, `blockquote`), class selectors for all page components (`.hero`, `.section`, `.reverse`, `.timeline-item`, `.skill-card`, `.paper`), ID selectors (`#home`, `#about`, `#experience`, `#playbook`, `#education`, `#skills`, `#offclock`, `#resume`, `#contact`), descendant selectors, and `:nth-child()` selectors for alternating card borders and pill colours.
* **Pseudo-classes and pseudo-elements:** `:hover`, `:first-child`, and `:last-child` for interactive states and layout alignment, `::before` and `::after` for custom star bullets (`✦`) and box-sizing resets, and `::selection` to set the background and text colour of selected text.
* **Display and position:** `display: flex` and `display: grid` for layout. `position: sticky` for the top navigation bar and the section titles while scrolling, and `position: absolute` inside a relative parent to overlap the handwritten caption badge onto the portrait image.
* **Box model and colour:** `padding`, `margin`, `border`, `border-left`, `border-top`, `border-radius`, offset `box-shadow`s on buttons and the portrait photo, `rgba` and `color-mix()` for the semi-transparent header and borders, and `radial-gradient` and `linear-gradient` for background depth and cards.
* **Transitions and animations:** Spring hover transitions using `cubic-bezier` and `transform` (`translateY`, `rotate`, `scale`), plus a scroll reveal animation where each section fades and slides up when JavaScript adds the `.visible` class on screen.

## Design decisions

I wanted the website to feel unique to my profile as a dual-degree student studying Digital Business & Entrepreneurship at IIM Bangalore and Business AI at the Institute of Science, Mumbai, while still reading clearly as a professional resume. Alternating the section headings between the left and right columns gives the long single-page layout a dynamic visual rhythm, and thin horizontal lines between sections keep every part clearly separated. The five-colour palette pairs deep navy and steel blue surfaces with one bright Imperial Red accent (`#e63946`) so key metrics, dates, and call-to-action buttons stand out immediately.

Using multiple fonts gives each type of information a clear visual role: a bold display font for headings, a playful italic serif and handwritten font for personality, a monospace font for dates and tags, and a clean sans-serif font for body paragraphs. I also added a few practical extras with vanilla JavaScript: a light/dark theme toggle that saves the user's preference, a responsive mobile menu toggle, a print-to-PDF resume button, and a scroll-reveal animation controlled entirely by CSS classes.
