# westover.dev Design Brief

**Purpose**: Reference for recreating westover.dev in Penpot for design modifications and automated deployments.

**Penpot File**: "westover.dev Homepage" in "westover.dev Site" project
**Current Live Site**: https://westover.dev
**Target Deployment**: https://westover.dev (via GitHub Pages)

---

## Design System

### Color Palette
- **Background**: `#0a0a0a` (near-black)
- **Text Primary**: `#f5f5f5` (off-white)
- **Text Secondary**: `#a0a0a0` (gray)
- **Accent/Links**: `#60a5fa` (blue)
- **Accent Hover**: `#3b82f6` (darker blue)
- **Card Background**: `#111111` (dark gray)
- **Border**: `#222222` (subtle border)

### Typography
- **Font**: System font stack (sans-serif)
- **Hero Title**: 64px, gradient from `#60a5fa` to `#a78bfa` (blue to purple)
- **Hero Subtitle**: 24px, color `#a0a0a0`
- **Section Headers**: 32px, bold
- **Card Titles**: 24px, bold
- **Body Text**: 16px, line-height 1.6
- **Stats Numbers**: 48px, bold, gradient accent

### Layout Structure
- **Max Width**: 1200px container
- **Padding**: 6rem vertical, 1.5rem horizontal
- **Responsive**: Mobile-first, single column on small screens
- **Spacing**: 3rem between sections

---

## Page Sections

### 1. Hero Section
**Layout**: Centered content
```
James Westover
[Gradient Title: 64px]

Builder. Technologist. Problem Solver.
[Subtitle: 24px, gray]

Crafting scalable systems and innovative solutions
at the intersection of distributed computing and artificial intelligence.
[Description: 18px]

[View Projects Button] [Contact Me Button]
```

**Key Elements**:
- Gradient text animation on title (blue → purple)
- Two CTA buttons: "View Projects" (filled blue), "Contact Me" (outlined)
- Generous spacing (8rem padding)

### 2. Stats Grid
**Layout**: 4-column grid (responsive to 2-col, then 1-col)

**Stats**:
1. **15+** Years Experience
2. **10M+** Requests/Second Scaled
3. **50+** Production Systems
4. **3** Continents Deployed

**Styling**:
- Numbers: 48px, gradient accent
- Labels: 16px, gray
- Cards with subtle borders

### 3. Expertise Section
**Layout**: 3-column grid of cards (responsive)

**Cards**:
1. **Distributed Systems**
   - Icon: ⚡ (lightning bolt)
   - Description: Building high-scale infrastructure with focus on reliability and performance

2. **Python & Modern Stacks**
   - Icon: 🐍 (snake)
   - Description: Expert in FastAPI, async patterns, and data processing pipelines

3. **Autonomous Systems**
   - Icon: 🤖 (robot)
   - Description: AI-powered automation and intelligent system design

4. **Infrastructure as Code**
   - Icon: 🏗️ (construction)
   - Description: Ansible, Terraform, containerization, and GitOps workflows

5. **API Design**
   - Icon: 🔌 (plug)
   - Description: RESTful services, OpenAPI, rate limiting, and authentication

6. **Real-time Systems**
   - Icon: ⚙️ (gear)
   - Description: WebSockets, streaming data, and low-latency architectures

**Card Styling**:
- Background: `#111111`
- Padding: 2rem
- Border: `#222222`
- Hover: Slight scale and shadow
- Icon: 48px emoji

### 4. Featured Projects
**Layout**: 2-column grid of project cards

**Projects**:

1. **Uber Navigation Systems**
   - At: Uber Technologies
   - Years: 2015-2020
   - Description: Core contributor to routing and ETA services, handling 10M+ requests/second
   - Tech: Python, Go, distributed systems

2. **HERE Fleet Telematics**
   - At: HERE Technologies
   - Years: 2020-2023
   - Description: Real-time vehicle tracking and route optimization for commercial fleets
   - Tech: Python, Kafka, time-series databases

3. **Ghost Hunter**
   - Type: iOS App
   - Description: AI-powered paranormal detection using ONNX runtime and computer vision
   - Tech: React Native, FastAPI, ONNX
   - Link: App Store

4. **SkinVault**
   - Type: iOS App
   - Description: Privacy-focused photo scanning with AI content detection
   - Tech: React Native, FastAPI, NudeNet
   - Link: App Store

**Card Styling**:
- Dark background with border
- Company/type badge at top (small, gray)
- Title in accent color
- Years/date in small gray text
- Tech stack as comma-separated list

### 5. Neher Data Systems Section
**Layout**: Centered content with logo/branding

**Content**:
```
Neher Data Systems

Building the future of intelligent infrastructure

Independent software development and consulting focused on:
• Distributed systems architecture
• AI/ML integration and deployment
• API design and scalability
• Infrastructure automation

[Learn More →]
```

**Styling**:
- Dark background section
- Centered text
- Bullet points in grid layout
- "Learn More" link in accent color

### 6. Contact Section
**Layout**: Centered content

**Content**:
```
Let's Build Something

Whether you need technical consulting, system architecture,
or custom development - let's discuss your project.

[Get in Touch Button]
```

**Contact Methods** (displayed as icon row):
- 📧 Email: james@westover.dev
- 💼 LinkedIn: linkedin.com/in/james-westover
- 🐙 GitHub: github.com/neherdata
- 🌐 Blog: blog.westover.dev

### 7. Footer
**Layout**: Centered, minimal

**Content**:
```
© 2025 James Westover. Built with care.
```

---

## Interactive Elements

### Buttons
**Primary Button** (View Projects, Get in Touch):
- Background: `#60a5fa`
- Padding: 1rem 2rem
- Border-radius: 8px
- Hover: Scale 1.05, background `#3b82f6`

**Secondary Button** (Contact Me):
- Border: 2px solid `#60a5fa`
- Background: Transparent
- Hover: Background `#60a5fa`

### Cards (Projects, Expertise)
- Hover: Transform translateY(-4px), shadow
- Transition: 300ms ease

### Links
- Color: `#60a5fa`
- Hover: `#3b82f6`
- No underline

---

## Responsive Breakpoints

### Desktop (> 768px)
- Stats: 4-column grid
- Expertise: 3-column grid
- Projects: 2-column grid
- Max-width: 1200px

### Tablet (481px - 768px)
- Stats: 2-column grid
- Expertise: 2-column grid
- Projects: 1-column grid

### Mobile (< 480px)
- All grids: 1-column
- Hero title: 48px (reduced)
- Padding: 3rem vertical (reduced)

---

## Animations

### On Load
- Hero title: Fade in with slight upward motion
- Gradient text: Subtle color shift animation

### On Scroll
- Cards: Fade in as they enter viewport
- Stats: Counter animation (0 → final number)

### On Hover
- Buttons: Scale transform
- Cards: Lift with shadow
- Links: Color transition

---

## Technical Notes

### Current Implementation
- Single-page static HTML
- Inline CSS (no external stylesheet)
- No JavaScript framework (vanilla JS for animations)
- Font loading: System fonts for performance

### Deployment Target
- GitHub Pages (westover.dev repository)
- CNAME: westover.dev
- Cloudflare DNS

### Design Export Requirements
1. Export from Penpot as HTML/CSS
2. Maintain responsive grid system
3. Preserve gradient effects and animations
4. Optimize for performance (minimal CSS, no external deps)

---

## Future Enhancements (Post-Penpot)
- Dark/light theme toggle
- Blog integration (blog.westover.dev)
- Project filtering/search
- Contact form (vs. mailto link)
- Resume download (resume.westover.dev integration)
