# CLAUDE.md - Aurora Game

This file provides guidance for AI assistants working with the Aurora Game codebase.

## Project Overview

**Aurora** is an interactive romantic visual novel game in Italian, designed as a personalized love story experience. The game features:

- A beautiful starry night aesthetic with aurora effects
- Two customizable protagonists (player inputs names at start)
- 5 romantic scenes with branching dialogue choices
- Tender, romantic, and slightly ironic tone
- A heartfelt ending with an achievement unlock

## Repository Structure

```
aurora-game/
├── CLAUDE.md          # AI assistant guidelines (this file)
└── index.html         # Complete game (HTML + CSS + JavaScript)
```

## Technology Stack

- **Pure HTML5/CSS3/JavaScript** - No external frameworks or build tools required
- **Google Fonts** - Quicksand and Dancing Script for typography
- **CSS Animations** - For floating hearts, twinkling stars, and aurora effects
- **Responsive Design** - Works on desktop and mobile devices

## Running the Game

Simply open `index.html` in any modern web browser. No server or build process needed.

```bash
# Option 1: Open directly in browser
open index.html  # macOS
xdg-open index.html  # Linux
start index.html  # Windows

# Option 2: Use a simple HTTP server
python -m http.server 8000
# Then visit http://localhost:8000
```

## Game Architecture

### Structure (index.html)

1. **CSS Styles** (lines 1-350): Visual styling including:
   - Star field background with twinkling animation
   - Aurora borealis gradient effect
   - Glassmorphism UI elements
   - Character avatars
   - Responsive breakpoints

2. **HTML Markup** (lines 350-420):
   - Title screen with name inputs
   - Game screen with scene display, dialogue box, and choices
   - Ending screen with achievement

3. **JavaScript Game Logic** (lines 420-end):
   - `scenes[]` array containing all 5 scenes with dialogues and choices
   - `startGame()` - Initializes player names and starts scene 1
   - `loadScene(index)` - Renders scene content and choices
   - `selectChoice(index)` - Handles player choice and shows response
   - `showEnding()` - Displays the romantic finale
   - `createFloatingHearts()` - Visual effect for emotional moments

### Scene Data Structure

```javascript
{
    title: "Scene Title",
    description: "Narrative description of the setting",
    speaker: "partner",  // Who is speaking
    dialogue: "The dialogue text",
    choices: [
        {
            letter: "A",
            text: "Choice text shown to player",
            response: "Partner's response to this choice"
        },
        // ... more choices
    ]
}
```

## Code Style Conventions

- **Indentation**: 4 spaces
- **CSS**: BEM-like naming, grouped by component
- **JavaScript**: Vanilla ES6+, descriptive function names
- **Italian text**: All player-facing text is in Italian
- **No external dependencies**: Everything is self-contained

## Key Conventions for AI Assistants

1. **Preserve the romantic tone**: Keep dialogue tender, romantic, and slightly playful
2. **Italian language**: All in-game text must remain in Italian
3. **No vulgarity**: Maintain family-friendly, sweet content
4. **Self-contained**: Avoid adding external dependencies
5. **Test visually**: Changes should be tested in a browser
6. **Responsive**: Maintain mobile compatibility

## Customization Points

When modifying the game, common customization areas include:

- **Scene content**: `scenes[]` array in JavaScript
- **Final speech**: `finalSpeech` constant
- **Colors**: CSS custom properties and gradients
- **Character avatars**: `.avatar-lei` and `.avatar-lui` emoji content
- **Number of scenes**: Add/remove from `scenes[]` array

## Development Workflow

### Branch Naming

- Feature branches: `feature/<description>`
- Bug fixes: `fix/<description>`
- AI-assisted: `claude/<session-id>`

### Commit Messages

- `feat: add new scene`
- `fix: correct typo in dialogue`
- `style: improve mobile responsiveness`
- `docs: update CLAUDE.md`

---

*Last updated: 2026-01-29*
