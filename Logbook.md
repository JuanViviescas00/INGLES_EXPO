# Project Logbook: Problem-Solving Through Responsive Web Design
**Student Program**: ADSO (Análisis y Desarrollo de Software)  
**Instructor**: Helmer Duarte Murallas  
**Course Code**: 319  
**Academic Year**: 2026  

---

## Logbook Entry #1 — Problem Exploration (Moment 1)

### 1. What problem did I choose and why?
I chose the workplace problem: **Problems in project planning or estimation**. In software engineering and development teams, incorrectly predicting the time, effort, and resources required to complete a project is an extremely common issue. I selected this problem because estimation errors directly affect the well-being of the development team, lead to missed deadlines, and compromise client trust. As future software developers, learning how to handle planning risks is essential for our professional success.

### 2. What contexts or data influenced my choice?
During my research, I noticed that according to industry statistics (such as the Standish Group Chaos Report), over 50% of software projects exceed their initial budget or timeline, and many are cancelled due to unrealistic planning. Furthermore, in my local academic and personal coding projects, I have experienced how easy it is to underestimate the time required to write, test, and debug a simple feature. This gap between initial plans and final reality is a systemic issue in software engineering.

### 3. What are the possible solutions I identified?
I identified four primary solutions to improve estimation accuracy:
- **Story Points (Agile Estimation)**: Measuring tasks by complexity instead of raw hours. This removes psychological pressure and accounts for unforeseen technical challenges.
- **Three-Point Estimation**: A statistical technique where teams estimate three scenarios (Optimistic, Pessimistic, and Most Likely) to calculate a realistic probability distribution.
- **Historical Data Analytics**: Tracking past velocity and comparing current tasks with completed baseline metrics from previous projects.
- **Agile Methodologies (Scrum & Kanban)**: Breaking projects into short, iterative cycles (sprints) to allow progressive refinement of scope and plans.

### 4. What questions or doubts do I have?
- How can a junior developer negotiate a realistic estimate when a project manager or client is pushing for an aggressive, unrealistic deadline?
- How do we balance historical data with brand new technologies that the team has never used before?

---

## Logbook Entry #2 — Design & Prototype (Moment 2)

### 1. What HTML structure did I design and why?
I designed a semantic, single-page document structure containing the following core HTML5 elements:
- `<header>` and `<nav>`: Positioned at the top to provide clear navigation links linking directly to page sections.
- `<main>`: Wraps the core content of the page to ensure accessibility.
- `<section class="hero">`: Serves as the introductory visual block, presenting the topic instantly.
- `<section id="problem">` with two `<article>` elements: Splits the problem into its core description and its direct consequences.
- `<section id="solutions">` with a wrapper `.solutions-grid` containing four `<article class="card">` elements: Separates each of the four solutions into individual components.
- `<section id="contact">` with a `<form>`: Contains an accessible layout (associated labels and inputs) for user inquiries.
- `<footer>`: Concludes the page with metadata and copyright info.

This semantic structure was selected because it makes the document readable for search engine web crawlers (SEO), ensures screen reader compatibility for accessibility, and creates a logical hierarchy that makes CSS styling much easier to maintain.

### 2. What CSS strategies am I planning (Flexbox, Grid, colors, spacing)?
To create a premium-quality website, I planned the following CSS techniques:
- **HSL-Based Color Palette**: I chose HSL colors to create a modern theme. I used a deep slate blue (`hsl(222, 47%, 12%)`) for backgrounds and headers, an electric indigo (`hsl(250, 89%, 65%)`) for the primary accent, and clean grays for content.
- **Flexbox**: Used for single-dimensional layouts. It aligns items in the navigation header (logo and links side-by-side) and positions the two problem articles. Flexbox is also used to stack elements vertically on mobile.
- **CSS Grid**: Used for the two-dimensional solutions gallery (`.solutions-grid`). I used `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` to make the card grid automatically wrap and resize depending on screen width without breaking.
- **Glassmorphism**: Added a semi-transparent blur effect to the sticky navigation header using `backdrop-filter: blur(10px)` to give the page a premium, modern software feel.
- **Typography & Spacing**: Imported Google Fonts (`Outfit` for headings and `Inter` for body copy) to replace generic browser fonts. Spacing is controlled using standard REM/EM margins and paddings for clean alignment.

### 3. What challenges appeared?
- **Responsive Layout Collapse**: Ensuring that the side-by-side problem articles and the solutions grid collapsed neatly on smaller screens. I solved this by using Flexbox column-wrap adjustments and CSS Grid `auto-fit` settings combined with custom `@media` queries.
- **Form Styling**: Textareas and input fields look very raw by default. Custom styling was required for `:focus` and `:hover` states to provide smooth glowing borders and shadows, which improves the overall user experience.

### 4. What feedback did I receive after socialization?
During our team socialization round, my classmates gave me the following feedback:
- **Visuals**: They liked the dark slate color scheme and the typography choice, stating it looked like a real SaaS (Software as a Service) planning tool.
- **Interactivity**: They suggested adding clearer hover transitions. In response, I added subtle float-up animations (`transform: translateY(-8px)`) and scaling to the grid cards and the submit button, making the UI feel more alive and responsive to mouse movements.
