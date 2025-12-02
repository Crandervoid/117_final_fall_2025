# 🎓 IS117 Final Project: Professional Web Portfolio System

> **Build three production-ready websites that demonstrate mastery of modern web development, strategic design thinking, and professional positioning in the AI era.**

[![Lighthouse CI](https://img.shields.io/badge/Lighthouse-100%2F100-brightgreen)](https://github.com/GoogleChrome/lighthouse-ci)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

---

## 📋 Table of Contents

1. [Project Overview](#-project-overview)
2. [Live Example Sites](#-live-example-sites)
3. [What You'll Build](#-what-youll-build)
4. [Technical Requirements](#-technical-requirements)
5. [Design Excellence](#-design-excellence-standards)
6. [Quality Gates](#-quality-gates--cicd)
7. [Final Presentation](#-final-presentation)
8. [Submission Guidelines](#-submission-guidelines)

---

## 🎯 Project Overview

This is your capstone project. You will design, develop, and deploy **three interconnected websites** that showcase your ability to think strategically, code professionally, and position yourself as a cutting-edge **AI Product Engineer** or **AI + X specialist** (e.g., AI + Cybersecurity, AI + UX Design, AI + Healthcare).

### Why This Matters
In today's job market, having a portfolio isn't optional—it's expected. But a *great* portfolio does more than show code. It tells a story, demonstrates strategic thinking, and proves you can ship production-quality work under real-world constraints.

---

## 🌐 Live Example Sites

Explore the reference implementation deployed on GitHub Pages:

### 🏠 [**Landing Page**](https://kaw393939.github.io/117_final_fall_2025/)
A beautiful hub connecting all three projects with smooth animations and modern design.

### 💼 [**Portfolio Site: Alex Chen - AI Product Engineer**](https://kaw393939.github.io/117_final_fall_2025/portfolio/)
**Design System:** Swiss International Style (Modernist Typography)  
**Brand Archetype:** The Sage + The Creator  
**Key Features:**
- Fluid typography (16px → 20px based on viewport)
- CSS Grid mastery with 12-column system
- Calendly integration for consultations
- Zapier-powered contact form
- Responsive design with mobile-first approach

**Design Highlights:**
```css
/* Fluid Typography Example */
font-size: clamp(1rem, 0.92rem + 0.39vw, 1.25rem);

/* Massive Heading Scale */
h1 { font-size: clamp(3rem, 2.07rem + 4.63vw, 8rem); }
```

### 🎨 [**Design Style Site: International Typographic Style**](https://kaw393939.github.io/117_final_fall_2025/design_style/)
An educational "museum piece" exploring the Swiss design movement.  
**Tech Focus:** Pure CSS Grid, asymmetric layouts, bold typography

### 🌿 [**Client Site: GreenLeaf Landscaping**](https://kaw393939.github.io/117_final_fall_2025/client_site/)
A conversion-optimized business website featuring:
- Sales funnel design
- Parallax scrolling effects
- Mobile-optimized service cards
- Form-to-CRM pipeline (Zapier)

---

## 🛠 What You'll Build

### 1️⃣ Personal Portfolio (Main Site)
Position yourself as an **AI Product Engineer** or niche specialist using:

#### Strategic Elements:
- **Brand Archetype Selection:** Choose from The Hero, The Sage, The Creator, etc.
- **Cialdini's Persuasion Principles:** Implement:
  - **Reciprocity:** Free audit/consultation
  - **Scarcity:** Limited availability messaging
  - **Authority:** Testimonials, case studies
  - **Social Proof:** "Trusted by X startups"

#### Required Integrations:
- [ ] **Calendly:** Embed a booking widget for free consultations
- [ ] **Zapier Webhook:** Connect contact form to email/Slack/Sheets
- [ ] **Analytics:** Google Analytics or Plausible

### 2️⃣ Design Style Site
Complete your earlier design style assignment with:
- Fully responsive layout
- Accurate representation of your chosen design movement
- Museum-quality presentation

### 3️⃣ Client Website
Build a professional site for a real or fictional client:
- Clear value proposition
- Sales funnel (Lead Magnet → Form → Conversion)
- Service/product showcase
- Social proof elements

---

## ⚙️ Technical Requirements

### Tech Stack Options
| Standard | Advanced (Optional) |
|----------|---------------------|
| HTML5 + CSS3 + Vanilla JS | Next.js, Astro, Eleventy |
| GitHub Pages hosting | Custom domain (bonus) |

### Mandatory Setup
```bash
# Initialize project
npm init -y

# Install quality tools
npm install --save-dev htmlhint stylelint @lhci/cli husky lint-staged

# Setup pre-commit hooks
npx husky install
```

### File Structure
```
your-repo/
├── .github/
│   └── workflows/
│       └── lighthouse-ci.yml
├── docs/                    # GitHub Pages serves from here
│   ├── index.html          # Landing page
│   ├── portfolio/
│   ├── design_style/
│   └── client_site/
├── .htmlhintrc
├── .stylelintrc.json
├── lighthouserc.json
└── package.json
```

---

## 🎨 Design Excellence Standards

### Responsive Typography
Use fluid type scales for seamless scaling:

```css
:root {
  /* Base: 16px at 320px viewport → 20px at 1400px */
  font-size: clamp(1rem, 0.92rem + 0.39vw, 1.25rem);
}

h1 {
  /* Massive scale: 48px → 128px */
  font-size: clamp(3rem, 2.07rem + 4.63vw, 8rem);
}
```

**Tool:** [Fluid Type Scale Calculator](https://www.fluid-type-scale.com/)

### Mobile-First Breakpoints
```css
/* Mobile: 320px - 768px (base styles) */
body { font-size: 1rem; }

/* Tablet: 768px - 1024px */
@media (min-width: 768px) {
  .container { padding: 0 40px; }
}

/* Desktop: 1024px+ */
@media (min-width: 1024px) {
  .grid { grid-template-columns: repeat(12, 1fr); }
}
```

### Color Contrast Requirements
All text must meet **WCAG AA** standards:
- Normal text: 4.5:1 contrast ratio minimum
- Large text (18px+): 3:1 minimum

**Check your colors:** [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

### Performance Budget
| Metric | Target |
|--------|--------|
| First Contentful Paint | < 1.8s |
| Largest Contentful Paint | < 2.5s |
| Total Blocking Time | < 200ms |
| Cumulative Layout Shift | < 0.1 |

---

## ✅ Quality Gates & CI/CD

### Lighthouse CI Scores
All sites must achieve:
- **Accessibility:** 100/100 ✅
- **SEO:** 100/100 ✅
- **Performance:** 90+ ⚠️
- **Best Practices:** 90+ ⚠️

### Pre-Commit Hooks
```json
// package.json
{
  "lint-staged": {
    "*.html": "htmlhint",
    "*.css": "stylelint"
  }
}
```

### GitHub Actions Workflow
Your CI/CD pipeline will automatically:
1. Lint HTML/CSS on every commit
2. Run Lighthouse audits on every push
3. Block merges if scores fall below thresholds

**View the workflow:** [`.github/workflows/lighthouse-ci.yml`](.github/workflows/lighthouse-ci.yml)

---

## 📊 Final Presentation

### Format
A **5-minute pitch deck** delivered as if you're presenting to a prospective client.

### Required Slides

#### 1. The Hook (30 seconds)
Open with your unique value proposition:  
*"I architect AI systems that don't just think—they work."*

#### 2. Case Study: Personal Brand (1.5 min)
- Show your portfolio site
- Explain your brand archetype
- Highlight one persuasion principle you used

#### 3. Case Study: Client Work (1.5 min)
- Present the client site
- Identify the problem you solved
- Show the sales funnel in action

#### 4. Technical Mastery (1 min)
- Display your Lighthouse scores
- Briefly explain your CI/CD pipeline
- Mention responsive design techniques

#### 5. Course Learnings (30 seconds)
Summarize your top 3 takeaways from IS117.

#### 6. AI Collaboration Analysis (30 seconds)
Include insights from asking your AI assistant:
1. *"Describe our collaboration and my prompting strategy"*
2. *"How can I improve my collaboration and prompting strategy?"*

#### 7. Call to Action (30 seconds)
End with: *"Let's schedule a 30-minute consultation to discuss your next project."*

### Delivery Tips
- Use Canva for professional visuals
- Avoid bullet-point slides—use visuals
- Practice to stay within 5 minutes

---

## 📦 Submission Guidelines

Submit via Canvas:

1. **GitHub Repository URL**
2. **Live Site URLs:**
   - Landing page: `https://yourusername.github.io/your-repo/`
   - Portfolio: `https://yourusername.github.io/your-repo/portfolio/`
   - Design style: `https://yourusername.github.io/your-repo/design_style/`
   - Client site: `https://yourusername.github.io/your-repo/client_site/`
3. **Presentation Deck Link** (Google Slides, Canva, or PDF)
4. **Self-Assessment Checklist** (complete all 5 checklists below)

---

## 📋 Quality Checklists

Before submitting, complete all checklists:

- ✅ [**Accessibility Checklist**](./requirements/accessibility_checklist.md) - Ensure WCAG compliance
- ✅ [**UI/UX Design Checklist**](./requirements/ui_ux_checklist.md) - Verify responsiveness & usability
- ✅ [**Technical & SEO Checklist**](./requirements/technical_checklist.md) - Validate code & optimization
- ✅ [**Legal & Compliance Checklist**](./requirements/legal_checklist.md) - Cover privacy & copyright
- ✅ [**Presentation Checklist**](./requirements/presentation_checklist.md) - Prepare your pitch

---

## 🚀 Getting Started

1. **Fork this repository** (or create your own from scratch)
2. **Study the example sites** in the `docs/` folder
3. **Install dependencies:** `npm install`
4. **Run local server:** `npm start` (or use Live Server extension)
5. **Commit often** and let Husky catch errors early
6. **Deploy to GitHub Pages** via Settings → Pages → Source: `main` branch, `/docs` folder

---

## 💡 Pro Tips

- **Start with mobile design first** - It's easier to scale up than down
- **Use CSS variables** for consistent theming
- **Comment your code** - Future you will thank you
- **Test on real devices** - Browser DevTools aren't enough
- **Ask your AI assistant for code reviews** - It's like having a senior dev on call

---

## 🎓 Learning Outcomes

By completing this project, you will:
- ✅ Master responsive design with fluid typography
- ✅ Implement professional CI/CD pipelines
- ✅ Build accessible, SEO-optimized websites
- ✅ Integrate third-party APIs (Zapier, Calendly)
- ✅ Position yourself strategically in the job market
- ✅ Create a portfolio that opens doors

---

## 📞 Need Help?

- **Office Hours:** Check Canvas for schedule
- **Discord:** Join the class server for peer support
- **AI Assistant:** Use ChatGPT/Claude for code reviews and debugging

**Remember:** This project is your portfolio. Make it something you're proud to show employers.

---

<div align="center">

**Good luck! 🚀**

*"The best way to predict the future is to design it."*  
— Buckminster Fuller

</div>
