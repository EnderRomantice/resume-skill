# Resume Formatter Skill

This is an AI Agent Skill designed to help users generate comfortable, soft, and highly readable personal resume layouts and interactive stylings customized for different professions.

## Directory Structure
- `SKILL.md`: The core formatting guidelines, rules, and AI instructions.
- `README.md`: Project overview and introduction.
- `LICENSE`: The license file.
- `references/`: Additional design resources
  - `style.md`: Design styles, color palettes, and CSS implementations
  - `animations.md`: Animation libraries and micro-interaction references
  - `fonts.md`: **Font recommendations and [Google Fonts](https://fonts.google.com/) integration guide**

## Installation

### Manual Installation
Copy or move the entire `resume_skill` folder into your agent tool's skills directory:

- **Kimi Code CLI**: Copy to the agent's skills folder (path varies by installation)
- **Cursor**: Place in your project's `.cursor/skills/` directory
- **Other agents**: Place in the agent's designated skills directory

### Using [skills-npm](https://github.com/antfu/skills-npm) (Coming Soon)

Once this skill is published as an npm package:

```bash
npm i -D resume_skill
```

Then add a `prepare` script to your `package.json`:

```json
{
  "private": true,
  "scripts": {
    "prepare": "skills-npm"
  }
}
```

Run `npm install` and the skill will be automatically symlinked for your agent.

## How to Use
Provide the contents of `SKILL.md` as context to any Large Language Model (LLM) or AI Agent. This equips the AI with the knowledge to offer professional typography, color palettes, spacing advice, and CSS-based micro-animations for Tech, Creative, or Corporate resumes, along with intelligent content extraction.

## Key Features
- **Profession-Specific Aesthetics**: 
  - **Tech**: Emphasizes clean monospace elements, crisp sans-serifs, and slick hover effects.
  - **Creative**: Blends elegant serifs with Morandi color palettes, generous whitespace, and soft fade-in animations.
  - **Corporate**: Features high-contrast, classic styling suitable for intense scanning, with refined, minimal interactions.
- **Intelligent Tagging**: Automatically parses project descriptions to extract key technologies and skills, formatting them as prominent tags below project headers.
- **Dynamic Interactions**: Includes curated, smooth CSS micro-animations tailored to the vibe of each profession, guaranteeing a premium feel without sacrificing readability.
