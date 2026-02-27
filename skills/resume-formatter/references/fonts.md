# Font Resources & Recommendations

This document provides curated font recommendations and resources for creating beautiful, readable resumes.

## Google Fonts

**Primary Resource**: https://fonts.google.com/

Google Fonts offers a vast collection of free, open-source fonts that can be easily integrated into any web-based resume. All fonts are optimized for web use and support various weights and styles.

## Recommended Fonts by Profession

### Tech / Engineering

| Usage | Font | Characteristics |
|-------|------|-----------------|
| Headers | **Inter** | Clean, modern, highly legible |
| Headers | **Roboto** | Google's signature font, neutral and friendly |
| Headers | **Space Grotesk** | Geometric, technical feel |
| Body | **Inter** | Optimized for UI, excellent readability |
| Monospace | **Fira Code** | Programmer-friendly, ligature support |
| Monospace | **JetBrains Mono** | Distinctive, easy to scan code |
| Monospace | **Source Code Pro** | Adobe's clean monospace font |

**Google Fonts Import Example:**
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
```

### Creative / Design / Marketing

| Usage | Font | Characteristics |
|-------|------|-----------------|
| Headers | **Playfair Display** | Elegant serif with high contrast |
| Headers | **Cormorant Garamond** | Refined, artistic serif |
| Headers | **Outfit** | Modern geometric, playful |
| Headers | **Syne** | Bold, contemporary display |
| Body | **Lato** | Friendly, professional sans-serif |
| Body | **Open Sans** | Neutral, humanist design |
| Body | **Nunito** | Rounded, approachable |

**Google Fonts Import Example:**
```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
```

### Corporate / Business / Management

| Usage | Font | Characteristics |
|-------|------|-----------------|
| Headers | **Cormorant** | Classic, authoritative serif |
| Headers | **Libre Baskerville** | Traditional book style |
| Headers | **Merriweather** | Readable, professional serif |
| Body | **Source Sans Pro** | Adobe's clean sans-serif |
| Body | **Work Sans** | Optimized for long-form reading |
| Body | **IBM Plex Sans** | Corporate, neutral tone |

**Google Fonts Import Example:**
```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant:wght@400;600&family=Source+Sans+Pro:wght@400;600&display=swap" rel="stylesheet">
```

## Font Pairing Principles

1. **Contrast**: Pair serif headers with sans-serif body text (or vice versa)
2. **Hierarchy**: Use 1-2 fonts maximum; too many fonts look chaotic
3. **Weight**: Use 400 (regular) for body, 600-700 (bold) for headers
4. **Size**: Maintain comfortable reading size (16px minimum for body)

## Chinese/多语言 Font Recommendations

For resumes requiring Chinese characters:

| Font | Use Case |
|------|----------|
| **Noto Sans SC** | Clean, modern Chinese sans-serif |
| **Noto Serif SC** | Traditional, elegant Chinese serif |

**Google Fonts Import Example:**
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&family=Noto+Sans+SC:wght@400;500&display=swap" rel="stylesheet">
```

## Font Loading Best Practices

1. **Use `display=swap`**: Prevents invisible text during loading
2. **Preload critical fonts**: `<link rel="preconnect" href="https://fonts.googleapis.com">`
3. **Limit weights**: Only import weights you'll actually use
4. **Fallback stack**: Always define system font fallbacks
   ```css
   font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
   ```

## Useful Tools

- **Google Fonts**: https://fonts.google.com/
- **Font Pair**: https://fontpair.co/ (font pairing inspiration)
- **Type Scale**: https://type-scale.com/ (visual type scale generator)
