## Plan: Professional Technology Leader Portfolio Refresh

Transform the current single-column markdown-heavy portfolio into a cleaner executive-tech presence by introducing a design system (type, color, spacing), clearer information hierarchy, and modern content presentation (hero, project cards, metrics, stronger CTAs) while staying within GitHub Pages + Jekyll constraints.

**Steps**
1. Phase 1 - Visual direction and content hierarchy (foundation): Define a single visual direction for technology leader positioning: stronger headline/value proposition, trust signals (years, domains, outcomes), and concise section intros. Convert long narrative blocks into scannable sections with short summaries and outcome bullets. This step sets the information architecture that all styling/layout updates depend on.
2. Phase 2 - Design tokens and typography system (depends on 1): Introduce CSS custom properties for brand palette, spacing scale, border radius, shadows, and type scale in the existing stylesheet. Replace ad-hoc font sizing/margins with token-based values. Move from generic Open Sans-only styling to a paired, more executive look (headline font + readable body font) while preserving web-safe fallbacks.
3. Phase 3 - Header and hero modernization (depends on 1,2): Redesign header in the default layout to include role statement, one-line value proposition, compact social/contact actions, and a clear primary CTA (View Projects) plus secondary CTA (Contact). Tighten profile image treatment, spacing, and alignment so above-the-fold section communicates authority quickly.
4. Phase 4 - Project showcase redesign (depends on 1,2; parallel with 5): Replace text-heavy projects section with card-style project summaries (problem, method, measurable impact, links). Add visual consistency across project entries and optionally a featured-project block for IntelliFraud. Keep markdown-friendly structure but add semantic wrappers/classes for reliable styling.
5. Phase 5 - Case study and experience readability upgrade (depends on 1,2; parallel with 4): Reformat Work Experience and Case Study content into concise impact-first bullets. Add lightweight visual separators (timelines, section dividers, badges/chips for AI/ML/NLP/Forecasting) to improve scan speed without heavy JS.
6. Phase 6 - Navigation, footer, and trust signals (depends on 3): Add simple anchor navigation for major sections (About, Experience, Projects, Case Study, Contact). Implement a purposeful footer with quick links, copyright, and optional last-updated signal. Ensure external links use consistent labeling and open-in-new-tab behavior.
7. Phase 7 - Responsive and accessibility hardening (depends on 3,4,5,6): Add mobile-first breakpoints for header/content/cards, ensure readable line lengths, improve focus states, maintain color contrast, and validate keyboard navigation/alt text semantics. Reduce icon-only ambiguity with labels or tooltips where needed.
8. Phase 8 - Performance and polish (depends on 7): Optimize image usage (sizes/lazy loading where possible), reduce visual noise, tune hover/motion effects to subtle professional interactions, and ensure visual consistency across homepage and project readme pages.

**Relevant files**
- _layouts/default.html: Primary layout shell; update header/hero structure, CTAs, section wrappers, and footer.
- assets/css/style.scss: Central styling surface; add design tokens, responsive rules, typography scale, card/grid styles, and interaction polish.
- README.md: Homepage content source; restructure sections for concise executive storytelling and card-friendly project summaries.
- _config.yml: Site metadata (title/description/theme/logo) to align SEO/title/tagline with technology leadership positioning.
- projects/Intellifraud_Bank_Account_Fraud_Detection/README.md: Reference structure for improved project narrative consistency.
- projects/Amazon_Product_Bundling/README.md: Reference structure for concise impact-method-outcome framing.
- projects/Ryain_Air_Passenger_Review/README.md: Reference structure for consistent project card content and link patterns.

**Verification**
1. Run local Jekyll serve and verify homepage + project pages render correctly with no Liquid/markdown regressions.
2. Validate responsive behavior at 360px, 768px, 1024px, and desktop widths for header, project cards, and text wrapping.
3. Run accessibility checks (contrast, heading order, keyboard focus visibility, icon labels/aria semantics).
4. Confirm outbound links, report/project links, and anchor navigation work as expected.
5. Perform a visual consistency pass across headings, spacing, button styles, and card components.
6. Confirm page load remains lightweight after styling updates and image handling changes.

**Decisions**
- Included scope: foundational visual modernization, readability improvements, structured project presentation, responsive/accessibility polish.
- Excluded scope: full framework migration, heavy JavaScript interactivity, CMS/content backend changes.
- Recommended approach: keep the existing Jekyll theme base but layer a deliberate custom design system in stylesheet + layout overrides for minimal risk and fast iteration.

**Further considerations**
1. Typography direction recommendation: Option A (executive serif + sans body), Option B (modern neo-grotesk), Option C (technical mono-accent + sans body).
2. Visual brand emphasis recommendation: Option A (deep blue + slate + cyan accents), Option B (charcoal + emerald accents), Option C (clean neutral + single accent).
3. Content density recommendation: Option A (concise, recruiter-friendly), Option B (balanced detail), Option C (deep technical narrative).