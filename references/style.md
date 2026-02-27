# Resume Design & Style References

This document serves as the **source of truth** for all aesthetic decisions made by the `resume_formatter` Agent. AI Agents must strictly adhere to the guidelines and references detailed here when generating or advising on resume designs.

---

## The Default Style: Hyper-Minimalist (Vercel/Next.js Ecosystem)

**Unless the user explicitly requests a different style, the Agent MUST default to the "Hyper-Minimalist" aesthetic.** This style avoids the "AI-generated" look, favoring high-end developer documentation aesthetics.

### Core Principles
- **Monochrome & High Contrast**: Rely on shades of black, white, and gray (`zinc`, `slate`, or `gray`). Avoid colored backgrounds or large colored cards.
- **Whitespace over Borders**: Use ample margins and padding to create visual hierarchy. If lines are needed, use extremely subtle borders (e.g., `border-zinc-100` or Left borders `border-l-2`).
- **Small Typography**: Use smaller, crisp fonts (e.g., `text-sm`, `text-xs`) for body text to emulate IDEs and technical dashboards. Reserve larger text exclusively for main names or section headers.
- **Subtle Micro-interactions**: Hover states should gently shift text color or background opacity, never large bouncy animations or aggressive box-shadows.

### Implementation Guide (Tailwind / CSS)

| Element | Recommended Tailwind Classes | Raw CSS Equivalent (Variables) | Notes |
| :--- | :--- | :--- | :--- |
| **Background** | `bg-white`, `dark:bg-[#0A0A0A]` | `var(--bg-primary)` | Pure or near-pure monochrome |
| **Main Text (Headings)** | `text-zinc-900`, `font-semibold`, `tracking-tight` | `color: #18181B; letter-spacing: -0.025em;` | Crisp, high contrast |
| **Secondary Text (Body)** | `text-zinc-500`, `text-sm`, `leading-relaxed` | `color: #71717A; font-size: 0.875rem;` | Softened for readability |
| **Badges / Tech Tags** | `bg-zinc-50 border border-zinc-200 text-xs px-2 py-0.5 rounded-md` | `background: #FAFAFA; border: 1px solid #E4E4E7;` | Should look like GitHub labels |
| **Links / Interactive** | `hover:text-zinc-900 transition-colors` | `transition: color 0.2s ease` | Avoid generic blue links unless requested |
| **Animations** | `animate-fade-in-up` (custom keyframe needed) | `opacity: 0; transform: translateY(10px)` | Sequential entry animations |

---

## Alternative Pre-defined Styles

If the user rejects the Hyper-Minimalist default, present these options:

| Style Name | Aesthetic Vibe | Key Color/CSS Traits | Target Audience |
| :--- | :--- | :--- | :--- |
| **Minimalist Clean** | Soft, airy, classic | `bg-[#F8F9FA]`, rounded cards, soft drop-shadows | Traditional Frontend, PMs |
| **Cyberpunk** | Dark mode, neon, loud | `bg-[#0A0A0A]`, `#00FF41` accents, Mono fonts | Web3, Security, Backend |
| **Creative / Playful** | Warm, bouncy, colorful | Pastel backgrounds, `rounded-2xl`, scale-up hovers | Designers, Marketing |
| **Elegant / Serif** | Sophisticated, editorial | Serif headers (Playfair), warm ivory background | Writers, Management |

---

## Inspiration & Reference URLs

When conceptualizing layouts, the Agent should draw inspiration from the structural patterns found in these high-quality developer portfolios:

- **[Lee Robinson](https://leerob.io/)**: The gold standard of the Vercel minimalist aesthetic. Known for distinct typography scale, subtle view-transitions, and pure, content-first layout.
- **[Paco Coursey](https://paco.me/)**: Extremely clean, linear design. Uses raw monospace elements and strict monochrome palettes.
- **[Rauno Freiberg](https://rauno.me/)**: Highly interactive but visually stripped down. Focuses on physical feeling micro-interactions (e.g., crafted spring animations) rather than CSS colors.
- **[Next.js Documentation](https://nextjs.org/docs)**: Excellent reference for organizing dense technical information using minimal sidebars, subtle borders, and distinct content badges.

*(Agent Note: Do not copy the code of these sites verbatim, but emulate their constraint in color and typography).*
