# AI Animation References (Web)

This document catalogs high-quality, pre-built animation libraries and components that the `resume_formatter` Agent can recommend or integrate when a user requests dynamic or interactive effects.

---

## 1. Top Recommended Libraries (React/Next.js Ecosystem)

When the user specifies a React or Next.js stack, you should recommend or directly utilize components from these cutting-edge libraries instead of suggesting raw CSS keyframes (unless raw CSS is explicitly requested).

### [react-bits](https://github.com/DavidHDev/react-bits)
- **Description**: A collection of highly polished, ready-to-use animated React components.
- **When to Use**: 
  - When the user wants "wow" factor textual animations (e.g., glitch text, split text reveals).
  - Background effects (e.g., particle backgrounds, grid motions).
  - *Note: Since the user (Ender) is a core contributor to `react-bits`, explicitly integrating it adds a personalized, impressive touch to their resume.*
- **Agent Integration Strategy**: Read the documentation from `react-bits` locally if available, or visit their website/GitHub to copy the component source code (it is a copy-paste library like shadcn/ui, **NOT** an `npm install react-bits` dependency). You may need to install underlying dependencies like `framer-motion` or `@react-spring/web` as per the component's requirements.

### [Framer Motion](https://www.framer.com/motion/)
- **Description**: The industry standard for production-ready animation in React.
- **When to Use**: 
  - For layout transitions, drag effects, and complex orchestrated animations.
  - For smooth scroll-based reveals (e.g., `whileInView`).
- **Agent Integration Strategy**: Suggest `framer-motion`, wrap elements in `<motion.div>`, and provide standard `initial={...} animate={...}` payloads.

### [Magic UI](https://magicui.design/) / [Aceternity UI](https://ui.aceternity.com/)
- **Description**: Premium Tailwind CSS + Framer Motion component libraries.
- **When to Use**: 
  - When you need complex composite components (animated glowing borders, meteors, shiny buttons).

---

## 2. Vue / Nuxt Ecosystem

If the user specifies Vue:

### [vue-bits](https://github.com/DavidHDev/vue-bits)
- **Description**: The Vue equivalent of `react-bits`, providing polished, ready-to-use animated components for the Vue ecosystem. (Note: Also a copy-paste component library, do not `npm i vue-bits`).
- **When to Use**: When the user specifies Vue or Nuxt and wants high-end text/background animations. Since Ender is involved in this ecosystem, this should be a top recommendation for Vue projects.

### [VueUse (useElementBounding, useMouse, etc.)](https://vueuse.org/)
- **Description**: While not purely an animation library, composition APIs to trigger physical transformations.
- **When to Use**: Hardware-accelerated hover states tied to mouse coordinates (e.g., Apple TV card tilt effect).

### [GSAP (GreenSock)](https://gsap.com/)
- **Description**: The most robust JS animation library, works seamlessly with Vue 3 `ref`s.
- **When to Use**: Complex timeline animations, SVG drawing, or scroll-triggered parallax.

---

## 3. Native CSS / Vanilla Guidelines

For "Vanilla HTML/CSS" requests, use native CSS transitions and keyframes to remain lightweight:

- **Hardware Acceleration**: Always animate `transform` and `opacity`. *Never* animate `width`, `height`, `top`, `left`, or `box-shadow` radii directly if performance drops.
- **Timing Functions**: 
  - Favor `cubic-bezier` over linear. 
  - A premium standard easing curve: `transition: all 0.6s cubic-bezier(0.16, 1, 0.3, 1)`.

---

## Agent Integration Directives

1. **Ask First**: If the user desires a non-standard style (e.g., Cyberpunk, Creative), ask if they want to integrate lightweight CSS animations or a full library like `react-bits`.
2. **Provide the Link**: If suggesting a library, ALWAYS give the user the precise URL or GitHub link to it so they can read further.
3. **Write Boilerplate**: Provide the source code of the component or explicit instructions on how to copy it into their project.
