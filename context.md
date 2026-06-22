# SYSTEM CONTEXT: DronePainter Portfolio Project
**Timestamp**: 2025-12-21 09:15 AM
**Location**: `/Users/macuser/git/0MY_PROJECTS/dronepainter`
**Agent**: Antigravity (Google Deepmind)

---

## 1. EXECUTIVE SUMMARY
**Objective**: Transform personal portfolio into an "Awwwards-level" experience using "Way Doper" aesthetic and FORGE refinement methodology.
**Current Phase**: **VERIFICATION / POLISH**
**Active Task**: Final UI Fixes (Mobile Responsiveness, Cursor Restoration, Color/Brightness Tuning).

### Critical Rules
- **Design Philosophy**: "Intentional Minimalism" + "Avant-Garde". Reject templates.
- **Protocol**: FORGE V(8,3,1) for text/code refinement.
- **Tone**: Personality-driven, developer-native (e.g., "systems that don't break at 3am").
- **Constraints**: 
  - Single file delivery (`index.html`) preferred where possible.
  - No "Placeholders" (use generative tools).
  - Date: 2025.

---

## 2. PROJECT FILES & STRUCTURE

### Core Application
- **`new-personal-website/index.html`**: The Monolith.
  - **Size**: ~3,400 lines
  - **Tech**: HTML5, Vanilla CSS (Variables), Vanilla JS (No frameworks)
  - **Key Sections**: Hero, About (Terminal), Resume (Timeline), Projects (Cards), GitHub, Contact.

### Artifacts & Memory
- **`implementation_plan.md`**: Approved plan for 8 "Doper" upgrades.
- **`task.md`**: Live checklist of active tasks.
- **`walkthrough.md`**: Visual verification log with screenshots.
- **`context.md`**: This file (The Brain).

### Assets
- `assets/images/`: Nano Banana easter eggs, sprites for bomber game.
- `assets/resume.pdf`: Resume file.

---

## 3. FEATURE IMPLEMENTATION STATE

| Feature | Implementation Details | Status |
|---------|------------------------|:------:|
| **Glassmorphism** | `--glass-bg: rgba(255, 255, 255, 0.03)`, `backdrop-filter: blur(10px)` on cards/nav. | ✅ |
| **Magnetic Cursor** | Custom JS (`.cursor-dot`, `.cursor-ring`). Magnetic effect on buttons. *Fix applied for init.* | ✅ |
| **Scroll Reveals** | `IntersectionObserver` triggers `.active` class for slide-up/scale effects. | ✅ |
| **Floating Orbs** | CSS Keyframe animation `float`. Gradient orbs in background. Hidden on mobile. | ✅ |
| **3D Tilt Cards** | `mousemove` event calc `rotateX/Y` based on cursor position relative to card center. | ✅ |
| **Glitch Text** | CSS `@keyframes glitch-anim` on `.hero-name` hover. | ✅ |
| **GitHub Calendar** | `ghchart.rshah.org` embed with `filter: brightness(0.85)` + Link to profile. | ✅ |
| **Responsiveness** | Mobile-first breakpoints at **1024px**, **768px**, **480px**. Fluid typography using `clamp()`. | ✅ |

---

## 4. FORGE REFINEMENT LOG (V8.3.1)

### Text Refinement (CEO Council)
*Rationale: Moving away from "Corporate LinkedIn" to "Senior Engineer Personality"*

1.  **HERO**:
    *   *Before*: "I turn complex problems into elegant solutions..."
    *   *After*: "I ship **AI that works** and **systems** that don't break at 3am."
    *   *Why*: Demonstrates reliability and experience with on-call reality.

2.  **PROJECTS**:
    *   **DataKiln**: "Like Zapier meets Airflow. Built because YAML configs are a circle of hell."
    *   **StartFlow**: "A new tab page that doesn't suck. Built for people who hate clicking."
    *   **Oblivion**: "Turns PDFs and chaos into usable data."

3.  **CONTACT**:
    *   *Before*: "Let's build something."
    *   *After*: "Say Hello. Got a project? Or just want to argue about the best terminal font? I'm in."

---

## 5. CODEBASE SNAPSHOTS (Critical Sections)

### Custom Cursor (CSS Variables)
```css
.cursor-dot {
    position: fixed;
    width: 8px;
    height: 8px;
    background: var(--cyan);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    /* Fix: Initial off-screen pos */
    left: -100px; top: -100px; 
}
```

### Responsive Typography (Mobile First)
```css
@media (max-width: 768px) {
    .hero-name {
        /* Fluid scaling based on viewport width */
        font-size: clamp(2.5rem, 10vw, 4rem);
    }
    .hero-title {
        font-size: clamp(1rem, 4vw, 1.3rem);
    }
}
```

### GitHub Graph Embed
```html
<img src="https://ghchart.rshah.org/00f0ff/aaaronmiller" 
     alt="GitHub Graph"
     style="width: 100%; filter: brightness(0.85) saturate(1.2);">
```

---

## 6. ACTIVE ISSUES & NEXT STEPS

### 🔴 Immediate Fixes (Just Applied)
1.  **Email Typo**: Fixed `hello@` -> `aaaronmille@gmail.com` (Note: User specified `aaaronmille`, confirm if `aaaronmiller` was intended?).
2.  **Graph Brightness**: Reduced brightness to 0.85 to fit dark mode better.
3.  **Cursor CSS Error**: Fixed orphaned syntax in `.cursor-ring`.

### 🟡 Verification Needed
1.  **Cursor Visibility**: Does the dot/ring appear correctly on first load?
2.  **Mobile Layout**: Do the new grid adjustments (1 column) work on 480px?
3.  **Performance**: Are floating orbs correctly hidden on mobile?

---

## 7. USER PREFERENCES (The "Ultrathink" Protocol)

**When "ULTRATHINK" is triggered:**
- Override brevity.
- Multi-dimensional analysis (Psych, Tech, Access, Scale).
- Intentional Minimalism (If it has no purpose, delete it).

**Default Mode:**
- Concise.
- Output first.
- Visual excellence (WOW factor).

---

## 8. ENVIRONMENT
**OS**: Mac
**Git Root**: `/Users/macuser/git/0MY_PROJECTS/dronepainter`
**Browser**: Playwright available for testing.
**Tools**: `browser_subagent`, `run_command`, `write_to_file`.
