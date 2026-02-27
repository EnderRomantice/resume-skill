---
name: resume_formatter
description: Generates comfortable, soft, and highly readable resume layouts and interactive styling based on profession types, including automatic tag extraction for project experiences.
---

# Resume Formatter Skill

This Skill is designed to help users generate comfortable, soft, and highly readable personal resume layouts tailored to different professions (e.g., Tech, Creative, Corporate). It focuses on visual excellence, modern typography, intelligent content parsing, and dynamic interactive effects.

## Core Objectives

1. **High Readability**: The resume content must be scannable and crystal clear, regardless of the profession.
2. **Soft & Comfortable Aesthetics**: Avoid harsh colors, pure blacks (`#000000`), and overcrowded layouts. Utilize curated color palettes and ample whitespace.
3. **Profession-Specific Adaptability**: Dynamically adjust fonts, color schemes, spacing, layouts, and interactive micro-animations based on the target role.
4. **Intelligent Tag Extraction**: Automatically analyze "Project Experience" sections to extract key technologies, tools, or methodologies and display them as visually distinct tags below the project title.
5. **Typography Excellence**: Curate font pairings using Google Fonts resources (`references/fonts.md`) to enhance readability and professional aesthetics for each profession.
6. **Dynamic & Interactive Effects**: Rather than writing pure CSS keyframes from scratch, prefer integrating high-quality animation libraries cataloged in `references/animations.md` (e.g., `react-bits`, `framer-motion`) when appropriate for the tech stack.
7. **Tech-Stack Agnostic & User-Centric**: Respect the user's chosen technology stack (e.g., React, Vue, HTML/CSS, Tailwind, Next.js). Do NOT force a specific stack unless the user leaves it up to you. Always explicitly ASK for their aesthetic preference before generating the final code.

## Pre-defined Aesthetic Styles & Design Reference

Before generating the resume, you **MUST** reference `references/style.md` for complete design guidelines, CSS implementations, and structural inspiration. 

If the user does **not** specify a style, you **MUST default to the "Hyper-Minimalist (Vercel/Next.js Ecosystem Aesthetic)"** as cataloged in `style.md`. This is the preferred default to avoid generic "AI-generated" looks. 

Otherwise, explicitly ask the user if they prefer the default or want to choose from these alternatives:

1. **Minimalist Clean**: Classic airy with soft drop-shadows.
2. **Cyberpunk / Tech Bold**: Dark mode (`#0A0A0A`), neon accents.
3. **Playful / Creative**: Pastel backgrounds, rounded elements.
4. **Elegant / Serif**: Warm ivory, serif fonts.
5. **Corporate / Professional**: Crisp white, strong margins.

## Profession Layout & Styling Guide

### 1. Tech / Engineering
- **Typography**:
  - Headers: Clean Sans-Serif (e.g., Inter, Roboto, SF Pro Display).
  - Body: Legible Sans-Serif (e.g., Inter) combined with Monospace (e.g., Fira Code, JetBrains Mono) for inline code, tech stacks, or tags.
- **Color Palette**:
  - Background: Pure White (`#FFFFFF`) or subtle Slate/Cool Gray (`#F8F9FA`).
  - Text: Deep Gray (`#212529`) for body, softer Gray (`#495057`) for secondary info.
  - Accents: Soft Blue (`#228BE6`) or Teal (`#12B886`) for links, section dividers, and tags.
- **Spacing & Layout**:
  - Compact yet logical structure. Single-column or a two-column layout (narrow left for skills/meta, wide right for experience).
  - Line height: `1.5` to `1.6`; Paragraph spacing: `8px`.
- **Dynamic & Interactive Effects**:
  - Tags hover effect: Subtle scale-up (`transform: scale(1.05)`) with a slight glow or border-color shift (`transition: all 0.2s ease`).
  - Links: Smooth underline expansion on hover.

### 2. Creative / Design / Marketing
- **Typography**:
  - Headers: Elegant Serif (e.g., Playfair Display, Merriweather) or modern Display fonts (e.g., Montserrat, Outfit).
  - Body: Clean Sans-Serif (e.g., Lato, Open Sans) to maintain long-term reading comfort.
- **Color Palette**:
  - Background: Warm White (`#FFFCF9`) or Ivory/Beige (`#FDFBF7`).
  - Text: Deep Charcoal or Brownish Gray (`#343A40`).
  - Accents: Desaturated Morandi tones such as Dusty Rose (`#E5989B`), Sage Green (`#84A98C`), or Terracotta (`#CB997E`).
- **Spacing & Layout**:
  - Generous whitespace. Bold and flexible grid layouts.
  - Strong visual hierarchy using a mix of bold weights and varying font sizes.
- **Dynamic & Interactive Effects**:
  - Soft fade-ins for sections on scroll (`opacity: 0 to 1`, `transform: translateY(10px)`, `transition: all 0.6s ease`).
  - Project cards or elements: Smooth shadow expansion and soft lifting effect on hover (`box-shadow` transition).

### 3. Corporate / Business / Management
- **Typography**:
  - Headers: Classic Serif (e.g., Georgia, Garamond) or authoritative Sans-Serif (e.g., Helvetica Neue, Arial).
  - Body: Highly legible Serif or Sans-Serif.
- **Color Palette**:
  - Background: Pure White (`#FFFFFF`).
  - Text: Near-black Dark Gray (`#1A1A1A`) for maximum print and screen contrast.
  - Accents: Navy Blue (`#1D3557`) or Deep Burgundy (`#6C2936`) to convey professionalism and stability.
- **Spacing & Layout**:
  - Traditional top-down single-column layout or robust asymmetrical balance.
  - Symmetrical margins, emphasis on line spacing (Line height: `1.6`) for rapid scanning.
- **Dynamic & Interactive Effects**:
  - Keep animations minimal and conservative.
  - Links/Buttons: Simple, crisp color fade (`transition: color 0.2s`) or subtle background darkening on hover. Avoid bouncy or overly flashy animations.

## Core Features & Instructions for the Agent

When a user requests a resume design or formatting advice, follow these STRICT steps:

0. **Study References**: If you haven't already, thoroughly review `references/style.md`, `references/animations.md`, and `references/fonts.md`.
1. **Clarify Preferences & Defaults (CRITICAL)**: Before writing any code, you MUST:
   - Ask what **technology stack** they are using (e.g., Plain HTML/CSS, React + Tailwind, Vue + SCSS, Next.js).
   - Tell them you default to the highly requested **Hyper-Minimalist (Vercel-like)** style to ensure professional premium quality. Ask if they accept this or prefer a different listed style.
   *Wait for the user's response before proceeding.*
2. **Identify the Target Profession**: Ask the user for their profession if not provided or clear from the prompt.
3. **Auto-Extract Project Tags**: 
   - Parse the user's "Project Experience" or "Work Experience" content.
   - Automatically extract key tools, frameworks, languages, or methodologies (e.g., "React", "Docker", "Agile", "SEO").
   - Format these as distinct UI tags placed immediately underneath the project title or company name.
4. **Apply the Styling Guide & User Preference**: 
   - **Fonts**: Consult `references/fonts.md` and Google Fonts (https://fonts.google.com/) to select profession-appropriate font pairings. Provide exact font names and Google Fonts import URLs.
   - Provide specific recommendations for Hex color codes, line heights, margins, and animations based on their chosen style and profession.
5. **Generate Code/Templates**: Output a complete template (Markdown, HTML, React components, Vue components, etc.) incorporating the typography, colors, layout, tags, and animations, **strictly adhering to their requested tech stack**.
6. **Accessibility Check**: Ensure text-to-background contrast ratio meets or exceeds WCAG AA standards.
