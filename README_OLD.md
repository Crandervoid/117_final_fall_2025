# IS117 Final Project Instructions

## Overview
For your final project, you will be demonstrating your mastery of web development, design principles, and professional positioning. This project consists of three main technical components and a final presentation.

## Project Requirements

### 1. Design Style Site Implementation
*   **Goal:** Complete the implementation of the Design Style site you started earlier in the semester.
*   **Requirements:** Ensure the site is fully responsive, polished, and accurately reflects the chosen design style.

### 2. Personal Portfolio
*   **Goal:** Develop a professional portfolio that positions you as an **AI Product Engineer** or **AI + X** specialist (e.g., AI + Computer Security, AI + UX, AI + Healthcare, etc.).
*   **Brand Strategy:**
    *   Leverage **Brand Archetypes** to select a design style and adapt it to your chosen archetype.
    *   Incorporate **Robert Cialdini’s Principles of Persuasion** (Reciprocity, Scarcity, Authority, Consistency, Liking, Consensus) into your copy and layout to effectively market yourself.
*   **Integrations:**
    *   **Zapier:** Implement a Zapier integration to handle your contact form submissions (e.g., send an email, add to a spreadsheet, or notify you on Slack).
    *   **Calendly:** Embed or link a Calendly scheduler for visitors to book a "Free 30 Minute Business Consultation".

### 3. Client Website & Sales Funnel
*   **Goal:** Create a website for a real or hypothetical client using the same process as your portfolio.
*   **Sales Funnel:** Develop a basic sales funnel within the site to guide visitors towards a specific conversion goal (e.g., newsletter signup, product purchase, or service inquiry).

## Technical Specifications (Applies to all 3 sites)
*   **Tech Stack:** Pure HTML/CSS/JS is the standard. However, you are permitted to use static site generators/frameworks like **Next.js**, **Eleventy**, or **Astro**.
*   **Hosting:** All projects must be deployed and hosted on **GitHub Pages**.
*   **Analytics:** You must implement web analytics (e.g., Google Analytics, Plausible, etc.) on all three sites to track visitor behavior.

## Quality Assurance & CI/CD
To ensure your projects meet professional engineering standards, you must implement a **deterministic quality gate**. This ensures that no broken or low-quality code makes it to your live site.

1.  **Node.js Project Structure**: Initialize your repository as a Node.js project (`npm init`).
2.  **Linting**: Configure **HTMLHint** and **Stylelint** to enforce code quality.
3.  **Pre-commit Hooks**: Use **Husky** and **lint-staged** to prevent bad code from being committed.
4.  **Lighthouse CI**: Configure **Lighthouse CI** to audit your sites for Performance, Accessibility, Best Practices, and SEO.
    *   *Requirement*: You must achieve a score of **100** on Accessibility and **90+** on all other categories.
5.  **GitHub Actions**: Create a CI/CD pipeline that runs these checks automatically on every push.

## Quality Assurance Checklists
To ensure your projects meet professional standards, please review your work against the following checklists before submission. These are designed to help you, not overwhelm you.

*   [Accessibility (a11y) Checklist](./requirements/accessibility_checklist.md)
*   [Legal & Compliance Checklist](./requirements/legal_checklist.md)
*   [UI/UX Design Checklist](./requirements/ui_ux_checklist.md)
*   [Technical & SEO Checklist](./requirements/technical_checklist.md)
*   [Presentation Checklist](./requirements/presentation_checklist.md)

## Example Project
We have provided a complete example project to demonstrate what a "perfect" submission looks like. You can explore the code and structure in the `docs/` folder.

**Live Example:** [View the deployed example project](https://kaw393939.github.io/117_final_project_consultant_portfolio/)

*   **[Portfolio Site](./docs/portfolio/index.html)**: The main student portfolio (Swiss Style, AI Product Engineer positioning).
*   **[Design Style Site](./docs/design_style/index.html)**: The "museum piece" site (Swiss International Style).
*   **[Client Site](./docs/client_site/index.html)**: The small business site (GreenLeaf Landscaping).

## Final Presentation
*   **Format:** A 5-minute pitch deck.
*   **Scenario:** Present your work as if you are pitching your consulting services to a prospective client. You are showcasing your portfolio and the client work as case studies of your capabilities.
*   **Required Slides:**
    *   **Course Learnings:** A slide detailing your key takeaways from the semester.
    *   **AI Collaboration Process:** A slide analyzing your workflow with AI. You must prompt your AI assistant with the following two questions and include the insights in your presentation:
        1.  *"Describe our collaboration and my prompting strategy"*
        2.  *"How can I improve my collaboration and prompting strategy?"*
*   **Tools:** You are encouraged to use tools like **Canva** and **ChatGPT** to create a visually stunning and persuasive presentation.

## Submission
*   Submit the GitHub repository links for all three projects.
*   Submit the live URLs for all three projects.
*   Submit a link to your presentation deck.
