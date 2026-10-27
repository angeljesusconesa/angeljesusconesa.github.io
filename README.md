# Hypermedia Project — Part 1: Personal CV & Portfolio Website

**Author:** Ángel Jesús Conesa Martínez  
**Degree:** Video Game Design and Development (University of Girona)  

---

## 🔗 Project Links

* **Live Website (GitHub Pages):** 
* **Figma Design Proposal:** https://www.figma.com/design/SJxERoosUmWAv32hf5u11d/CV?m=auto&t=YWcCQ6Fhd9aHYnIk-1

---

## 1. Project Analysis

### 1.1 User Profile (User Persona)

To guide the design and content structure of this personal CV and portfolio website, a primary target user (User Persona) has been defined. Because my background combines web engineering, Unreal Engine 5 game development, and visual arts like photography, the main audience consists of technical recruiters, studio leads, and creative directors in the video game and interactive media industries.

* **Name:** Elena Rostova

* **Role:** Lead Technical Recruiter & Art Producer at a Mid-sized Indie Game Studio

* **Age:** 34

* **Location:** Barcelona, Spain (Hybrid/Remote hiring across Europe)

* **Background:** Elena reviews dozens of portfolios every week looking for junior-to-mid level developers and creative technologists who not only understand code and game engines (like Unreal Engine 5 and C++) but also have a strong visual sensibility and artistic eye.

* **Goals & Expectations:**

  * Quickly identify the candidate's core profile, location, and technical stack within the first 30 seconds of browsing.

  * See tangible proof of game development capability (playable prototypes on itch.io, gameplay videos, and engine knowledge).

  * Evaluate the candidate's aesthetic taste and multidisciplinary skills (such as lighting, composition, and UI design, reflected both in the website's layout and the photography section).

  * Find clear, frictionless contact channels to schedule an interview.

* **Pain Points & Frustrations:**

  * Overly cluttered or generic CV templates that fail to show personality or visual criteria.

  * Having to download heavy PDFs or navigate through complex multi-level menus just to find a gameplay video or contact email.


### 1.2 Information Architecture

For this project, I have implemented a single-page application (SPA) static layout organized vertically into a logical, narrative flow. The goal of the information architecture is to take the user from an impactful high-level introduction down to specific technical credentials, creative showcases, and a final call to action, while allowing instant navigation at any moment via a sticky top header.

At the very top, a fixed navigation bar (`<header class="menu">`) remains visible during scrolling. It uses a three-column CSS Grid layout: my full name on the left acting as a return-to-top anchor, direct section links in the center (`Profile`, `Experience`, `Skills`, `Photograph`, `Video games`), and a highlighted call-to-action (`Let's talk >`) on the right.

The vertical distribution of the page is divided into a Hero introduction followed by six numbered thematic sections (`01` to `06`), creating an editorial index feel:

1. **Hero Section:** Acts as the cover of the portfolio. It presents my personal value proposition (*"Bridging interactive logic, real-time graphics, and visual design with a touch of nostalgic"*), my origin, and a direct social link.
2. **01 — Profile:** Introduces who I am as a creative technologist and game developer. It pairs a concise narrative summary on the left with a structured definition list (`<dl>`) of quick personal facts (origin, current city, languages, and birth date) on the right.
3. **02 — Experience:** Displays my academic and professional journey chronologically from 2021 to the present. Using a right-aligned ordered list, it highlights my transition from Web Application Development (DAW) and full-stack work at OESIA to a Master's in Unreal Engine 5 and my current degree at the University of Girona.
4. **03 — Skills:** Categorizes my technical and soft skills into four clear blocks: Programming, 3D & Game Development, Photography & Image Editing, and Collaboration.
5. **04 — Photography:** Serves as a visual break and artistic showcase. It features a three-column asymmetric gallery of black-and-white personal photography, demonstrating composition and lighting skills.
6. **05 — Game Projects:** Focuses on practical game development output, highlighting *DOMINDO* (2025). It separates the project's identity and summary from its technical details and embeds both the playable itch.io widget and a YouTube gameplay video side by side.
7. **06 — Contact:** Closes the page with a high-contrast footer inviting collaboration, offering large interactive blocks for Email, Phone, and Instagram.

---

### 1.3 Visual Design

The visual design of the website is inspired by contemporary editorial design and a "nostalgic analog-meets-digital" aesthetic. Rather than using a standard corporate template, the page relies on strong typographic hierarchy, intentional asymmetry, tactile textures, and a high-contrast monochromatic color palette that lets both the text and multimedia content stand out.

**Color Palette:**  
The entire composition revolves around a strict, warm monochromatic scheme defined via CSS custom properties. The primary dark tone is a deep charcoal ink (`#11120f`), paired with a warm off-white paper tone (`#f1f0e9`). Secondary hierarchy is achieved through muted greys (`#5c5c5c` for technical labels and borders, and `#6a6c64` for body copy). Alternating the background colors between sections—starting with a dark Hero, moving through light paper sections for textual CV data (`01` to `03`), switching back to dark ink for the `04 Photography` showcase, returning to light for `05 Game Projects`, and finishing with a dark `06 Contact` section—creates visual rhythm and clearly separates content blocks.

**Typography:**  
Three complementary Google Fonts were chosen to reinforce the bridge between engineering and visual art:
* **Manrope (Sans-serif):** Used for primary headings (`.display` at `96px`) and body text. Its clean geometric forms ensure modern readability and strong structural impact.
* **Playfair Display (Italic Serif):** Applied selectively to emphasized words (`<em>`) within large titles (such as *"nostalgic"* or *"talk"*), adding an expressive, editorial, and human touch.
* **DM Mono (Monospace):** Used for the navigation bar, section numbers (`01`–`06`), dates, and category labels, evoking code, technical blueprints, and metadata.

**Layout & Visual Effects:**  
The layout alternates left-aligned and right-aligned display headers (e.g., Experience and Photography align right, while Profile and Skills align left) to guide the user's eye dynamically down the page. Hairline `1px` borders divide sections and metadata tables cleanly. Finally, the Hero section incorporates a custom multi-layered background featuring an `exclusion` blend-mode logo, a `110px` CSS `backdrop-filter` blur mask, and two overlapping white-noise dithering grain textures (`mix-blend-mode: overlay`), immediately establishing the nostalgic and graphic atmosphere described in the headline.
