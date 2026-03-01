# AI Leadership & Project Management Masterclass

<!-- BADGES:START -->
[![exec-ed](https://img.shields.io/badge/-exec--ed-673ab7?style=flat-square)](https://github.com/topics/exec-ed) [![presentation](https://img.shields.io/badge/-presentation-9c27b0?style=flat-square)](https://github.com/topics/presentation) [![artificial-intelligence](https://img.shields.io/badge/-artificial--intelligence-blue?style=flat-square)](https://github.com/topics/artificial-intelligence) [![edtech](https://img.shields.io/badge/-edtech-4caf50?style=flat-square)](https://github.com/topics/edtech) [![html](https://img.shields.io/badge/-html-e34f26?style=flat-square)](https://github.com/topics/html) [![leadership](https://img.shields.io/badge/-leadership-blue?style=flat-square)](https://github.com/topics/leadership) [![project-management](https://img.shields.io/badge/-project--management-blue?style=flat-square)](https://github.com/topics/project-management) [![teaching-materials](https://img.shields.io/badge/-teaching--materials-blue?style=flat-square)](https://github.com/topics/teaching-materials) [![website](https://img.shields.io/badge/-website-2196f3?style=flat-square)](https://github.com/topics/website) [![workshop](https://img.shields.io/badge/-workshop-blue?style=flat-square)](https://github.com/topics/workshop)
<!-- BADGES:END -->

Comprehensive masterclass materials for teaching AI project leadership and decision-making frameworks.

## Quick Start

### For Instructors Delivering the Course

1. **Review the structure:** Read `PROJECT_STRUCTURE.md` to understand file organisation
2. **Access instructor materials:**
   - Via website: Visit the companion site and click "🔐 Instructor" (password: `instructor2025`)
   - Via files: All guides are in `/instructor-materials/` organised by activity
3. **Prepare materials:**
   - Print facilitator quick reference (your day-of cheat sheet)
   - Print student materials (cards, worksheets) from `/activities/materials/`
   - Review activity facilitation guides
4. **Build the website:** Run `./scripts/render-all.sh` to generate all materials
5. **Test locally:** Open `docs/index.html` in a browser

### For Students

- **Website:** Access all materials at the companion website (hosted via GitHub Pages)
- **Pre-readings:** Available at the website before the course
- **RetailFlow case study:** Access the company simulation at [retailflow.serveur.au](https://retailflow.serveur.au)
- **Frameworks:** Download reference materials from Resources menu

---

## Project Organisation

```
/activities/materials/     → Cards and cases used IN activities
/instructor-materials/     → Facilitation guides by activity (instructor-only)
  ├── activity-1-pilot-scoping/
  ├── activity-2-speed-dating/
  ├── activity-3-crisis-management/
  └── activity-4-scale-pivot-kill/
/handouts/                 → Reference materials students take home
/docs/                     → Website files (auto-generated)
  ├── index.html           → Main companion site
  ├── instructor.html      → Password-protected instructor portal
  └── instructor/          → Rendered instructor materials
/retailflow-site/          → Company simulation website
  └── internal.html        → Password-protected pilot data dashboard
/scripts/                  → Build and utility scripts
```

**See `PROJECT_STRUCTURE.md` for detailed explanation of the organisation logic.**

---

## Masterclass Flow

**Duration:** 1 day (8 hours including breaks)

1. **Lecture** (90 min) - Introduction and framework overview
2. **Morning Tea** (30 min)
3. **Activity 1: Pilot Scoping** (30 min working + 20 min debrief)
   - Materials: Constraint cards, case brief
   - Output: Pilot plan with success criteria
4. **Activity 2: Speed-Dating** (40 min)
   - Materials: Stakeholder role cards
   - Output: Stakeholder mapping and communication strategies
5. **Lunch** (45 min)
6. **Activity 3: Crisis Management** (75 min)
   - Materials: Crisis cards (3-4 scenarios)
   - Framework: Diagnose → Decide → Communicate → Document
   - Output: Crisis response plans
7. **Afternoon Tea** (30 min)
8. **Debrief Crises** (15 min)
9. **Activity 4: Scale/Pivot/Kill** (45 min)
   - Materials: Pilot data dashboard, original criteria
   - Output: Scale/Pivot/Kill recommendation with rationale
10. **Wrap-up** (30 min) - Action planning, Q&A

---

## Key Materials by Activity

### Activity 1: Pilot Scoping
- **Case:** Scoping exercise worksheet
- **Cards:** Constraint cards (budget-cut, scope-creep, timeline-acceleration, vendor-lock-in)
- **Handout:** Project scoping framework
- **Instructor guide:** `instructor-materials/activity-1-pilot-scoping/`

### Activity 2: Speed-Dating (Stakeholder Conversations)
- **Cards:** 6 stakeholder role cards (CEO, CFO, Data Scientist, CS Manager, IT Security, End User)
- **Handout:** Stakeholder mapping template
- **Instructor guide:** `instructor-materials/activity-2-speed-dating/`

### Activity 3: Crisis Management
- **Cards:** Crisis cards (data-quality, team-resistance, executive-pressure, ethical-dilemma)
- **Handout:** Crisis response framework (DDCD)
- **Instructor guide:** `instructor-materials/activity-3-crisis-management/`

### Activity 4: Scale/Pivot/Kill
- **Data:** Pilot metrics dashboard (accessed via RetailFlow internal portal)
- **Handout:** Scale/Pivot/Kill decision framework
- **Instructor guide:** `instructor-materials/activity-4-scale-pivot-kill/`

---

## Building the Website

### Generate all materials
```bash
./scripts/render-all.sh
```

This renders all `.qmd` files to HTML and PDF, then organizes them into the `docs/` folder.

**What gets rendered:**
- Student materials → `docs/activities/`, `docs/handouts/`
- Instructor materials → `docs/instructor/`
- Slides → `docs/content/`
- Pre-readings → `docs/pre-readings/`

### Test locally
```bash
open docs/index.html
```

### Deploy to GitHub Pages
1. Ensure `docs/` folder is committed to git
2. GitHub Pages settings: Deploy from `main` branch, `/docs` folder
3. Site will be live at: `https://[username].github.io/[repo-name]/`

---

## Important Notes

### Constraint Cards vs Crisis Cards

**CONSTRAINT CARDS** (`/activities/materials/constraint-cards/`)
- Used in: Activity 1 (Pilot Scoping)
- Represent: Planning challenges BEFORE pilot starts
- Examples: Budget cuts, scope creep, timeline pressure, vendor constraints
- Files: `budget-cut.qmd`, `scope-creep.qmd`, `timeline-acceleration.qmd`, `vendor-lock-in.qmd`

**CRISIS CARDS** (`/activities/materials/crisis-cards/`)
- Used in: Activity 3 (Crisis Management)
- Represent: Issues that arise DURING live pilot
- Examples: Data quality, team resistance, executive pressure, ethical dilemmas
- Files: `data-quality.qmd`, `team-resistance.qmd`, `executive-pressure.qmd`, `ethical-dilemma.qmd`

**Don't mix them up!** Constraints are for planning; crises are for simulation.

### Student Materials vs Instructor Materials

**Student materials** (concise, 1-2 pages):
- Location: `/handouts/` and `/activities/materials/`
- Purpose: Quick reference during and after course
- Access: Via companion website Resources menu

**Instructor materials** (detailed, 10+ pages):
- Location: `/instructor-materials/` (organized by activity)
- Purpose: Facilitation guides, sample answers, teaching notes
- Access: Via instructor portal (password-protected)

Both exist for the same frameworks, just different detail levels.

### Instructor Portal

**Access:** Click "🔐 Instructor" in companion site navigation
**Password:** `instructor2025`

**What's included:**
- Facilitator quick reference (PRINT THIS!)
- Activity facilitation guides (all 4 activities)
- Framework walkthroughs
- Sample answers and assessment rubrics
- Feedback from previous deliveries

### RetailFlow Case Study

**Main site:** [retailflow.serveur.au](https://retailflow.serveur.au)
- Company overview, staff bios, products
- Provides context for all activities

**Internal portal:** [retailflow.serveur.au/internal](https://retailflow.serveur.au/internal)
- Password: `pilot2024`
- Contains Week 6 pilot data dashboard
- Used in Activity 4 (Scale/Pivot/Kill)

### Source Files vs Generated Files

**Never edit files in `/docs/` directly** - they're auto-generated.

- **Edit:** Files in `/activities/`, `/handouts/`, `/content/`, `/instructor-materials/`
- **Render:** Run `./scripts/render-all.sh`
- **Output:** Appears in `/docs/`

---

## Troubleshooting

### Render script fails
- Check Quarto is installed: `quarto --version`
- Ensure you're in the project root directory
- Run: `./scripts/render-all.sh` (note: script is now in scripts/ folder)
- Check .qmd files have valid YAML headers

### Website links broken
- Re-run render script: `./scripts/render-all.sh`
- Check file names match links in `docs/index.html`
- Verify files were generated in `docs/` folders

### Cards missing from docs/
- Check source file exists in `/activities/materials/`
- Re-run render script
- Check for errors in Quarto YAML headers
- Verify file naming (lowercase, no prefixes)

### Instructor portal not loading
- Check `docs/instructor.html` exists
- Verify password: `instructor2025`
- Clear browser cache and try again

### RetailFlow internal portal not loading
- Check password: `pilot2024`
- Verify `retailflow-site/internal.html` exists
- Clear browser cache

---

## Documentation

- **PROJECT_STRUCTURE.md** - Detailed organisation guide (read this!)
- **scripts/render-all.sh** - Build script for generating website
- **instructor-materials/README.qmd** - Instructor materials guide

---

## Questions?

For detailed explanations of:
- Folder organisation logic → See `PROJECT_STRUCTURE.md`
- Activity delivery structure → See `PROJECT_STRUCTURE.md` > "Activity Delivery Map"
- File naming conventions → See `PROJECT_STRUCTURE.md` > "File Naming Conventions"
- Adding new materials → See `PROJECT_STRUCTURE.md` > "Common Tasks"
- Instructor materials → See `instructor-materials/README.qmd`

---

## License & Attribution

This masterclass was developed for Curtin University.

**Last updated:** October 30, 2024
