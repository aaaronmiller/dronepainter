---
description: Generate investment-grade portfolio/resume website with adversarial validation
---

# Portfolio-Resume Generator

Generate premium personal portfolio/resume websites using adversarial validation, premium design, and web-grounded research.

---

## Quick Reference

### Default Configuration

| Profile | Validation | Projects | Sections |
|---------|------------|----------|----------|
| Lite | V(3, 1, 0) | 3 | 4 |
| **Standard** | **V(5, 2, 1)** | **5** | **5** |
| Deep | V(8, 3, 1) | 8 | 7 |

### Mode Detection

- **CREATE mode**: User provides name/GitHub → Generate new portfolio
- **REFINE mode**: User provides existing site → Improve design/content

### Prerequisites

- Name and title
- GitHub profile URL
- LinkedIn URL (optional)
- Target role/industry

---

## Phase 1: Research & Data Collection

### 1. Profile Research

- Capture current portfolio (if exists)
- Scrape GitHub for repos, activity, languages
- Check LinkedIn for experience, skills
- Identify top projects by recency, complexity, variety

### 2. Project Selection (5-Persona Validation)

Score projects 1-10 on five dimensions:

| Persona | Question | Focus |
|---------|----------|-------|
| Hiring Manager | Job-relevant skills? | Relevance |
| Tech Lead | Technically impressive? | Complexity |
| UX Designer | Looks good / has demos? | Visual Appeal |
| Recruiter | Understand in 10 seconds? | Clarity |
| Competitor | Would I be intimidated? | Impact |

Select top 5-8 projects that score highest.

---

## Phase 2: Content Development

### Core Sections (all profiles)

1. **Landing/Hero** - Name, title, tagline, CTA
2. **About** - 2-3 paragraph bio, key strengths
3. **Resume** - Experience timeline, skills matrix
4. **Portfolio** - Top 5 projects with screenshots
5. **Contact** - Email, LinkedIn, GitHub links

### Deep Profile (add these)

6. **GitHub Activity** - Contribution visualization
7. **Tech Stack** - Tools overview with proficiency
8. **Blog/Writing** (optional)
9. **Testimonials** (optional)

---

## Phase 3: Design System

### Visual Identity

- **Mode**: Dark mode primary (cyberpunk aesthetic)
- **Palette**: Cyan (#00f3ff) / Purple (#a855f7) accents
- **Typography**: Inter (body) + JetBrains Mono (code)
- **Spacing**: 8px grid system

### Micro-animations

- Fade-in on scroll
- Hover effects on project cards
- Typing animation for tagline
- Smooth section transitions

---

## Phase 4: HTML Assembly

### Structure

```html
<nav><!-- Sticky nav --></nav>
<section id="hero"><!-- Name, title, CTA --></section>
<section id="about"><!-- Bio --></section>
<section id="resume"><!-- Experience, Skills --></section>
<section id="portfolio"><!-- Project cards --></section>
<section id="contact"><!-- Links --></section>
<footer><!-- Credits --></footer>
```

### Requirements

- Single-page or multi-page (based on content)
- Mobile-responsive grid
- Semantic HTML5
- Optimized images

---

## Execution Checklist

```
[ ] 1. Detect MODE (CREATE or REFINE)
[ ] 2. Research GitHub/LinkedIn profiles
[ ] 3. Select top 5 projects via validation
[ ] 4. Validate each section with V(5, 2, 1)
[ ] 5. Apply design system
[ ] 6. Implement micro-animations
[ ] 7. Test responsiveness and links
[ ] 8. Deploy to GitHub Pages
```

---

## Quality Checklist

- [ ] Hero has clear value proposition
- [ ] Resume shows progression and impact
- [ ] Portfolio has 5+ well-documented projects
- [ ] Each project: title, description, tech stack, screenshot
- [ ] Contact has working links
- [ ] Dark mode looks premium
- [ ] Animations are smooth
- [ ] Mobile responsive
- [ ] Page loads in <3 seconds

---

## Anti-Patterns

❌ **Generic bio**: Must be specific to target role
❌ **Dead projects**: All portfolio links must work
❌ **No screenshots**: Every project needs visual
❌ **Missing tech stack**: List technologies used
❌ **Slow animations**: Keep transitions under 300ms

---

## ⚠️ Attention Boost: Critical Reminders

> **This section repeats key instructions for long-context processing.**

### DO NOT SIMPLIFY

1. **5-persona project validation mandatory** — Score before including
2. **Each project needs screenshot** — No placeholder images
3. **Dark mode by default** — Premium cyberpunk aesthetic
4. **Micro-animations required** — Fade-in, hover effects
5. **Mobile responsive** — Test at 375px width

### Quick Formula

```
Portfolio = 5 projects × 5-persona validation
         + 5 sections × V(5, 2, 1) each
         = Premium, validated portfolio site
```

**END OF SKILL DOCUMENT**
