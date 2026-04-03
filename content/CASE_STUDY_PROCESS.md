# CASE_STUDY_PROCESS.md
# How to create a case study — based on Clean Share project
# Follow these steps in order for each new case study.

---

## OVERVIEW

Each case study is produced in two stages: content (here in Claude.ai) and build (in Claude Code). This document covers the content stage only. The output is a completed `project-[name].md` file ready to hand to Claude Code.

---

## STEP 1 — PROJECT BRIEFING

Provide a plain text description of the project covering:

- **Product context** — what the app/product is, who it's for
- **Business problem** — the specific problem the project was trying to solve
- **Goal** — what success looked like
- **Solution** — what was designed and why
- Any **key decisions or tradeoffs** made during the process — especially pushbacks, scope changes, or direction shifts

Don't worry about structure at this stage. A rough description is fine. The more honest and specific, the better the output.

---

## STEP 2 — RESEARCH FILES

Share any relevant research documents (PPTX, PDF, etc.).

**Important instruction to give Claude:**
> "Go through these. Not everything will be relevant. Find only the data points that directly support this case study's narrative and show them to me for approval before using them."

Claude will extract candidates and present them for review. Approve, cut, or modify before moving on. Typically only 3–5 data points end up being used — specificity matters more than volume.

---

## STEP 3 — SCREENSHOTS

Share all design screenshots. Provide them in logical groups (e.g. onboarding flow, core flow, extension flow) and label each group briefly. Claude will hold and wait for more if you say so.

Screenshots don't need captions at this stage — those get written as part of the draft.

---

## STEP 4 — CLARIFYING QUESTIONS

Before writing, Claude should ask a small set of clarifying questions. For every case study, these should cover at minimum:

1. **Your role** — sole designer or team? Full scope or partial?
2. **Naming** — confirm the correct product/feature name
3. **Results** — any post-launch metrics? Even directional. If none, confirm the feature shipped.
4. **The most interesting design decision** — what was the hardest call, the biggest constraint, or the most unexpected finding? This usually becomes the strongest section.
5. **Any deliberate UX decisions** that might not be obvious from the screens alone (e.g. sequence choices, tone decisions, things that were cut)
6. **Brand/confidentiality** — can the company/product be named?

Don't start writing until these are answered.

---

## STEP 5 — FIRST DRAFT

Claude writes a full draft following `CASE_STUDY_NARRATIVE.md` and structured according to `CASE_STUDY_TEMPLATE.md`.

**What to check in the draft:**
- Does the opening problem get closed by the end?
- Is the most strategic decision given its own section and pull quote?
- Are pull quotes observations/tensions, not summaries of what you did?
- Is every design decision connected to a constraint, research finding, or deliberate rationale?
- Does the story flow chronologically through the process?

---

## STEP 6 — REVIEW AND CORRECTION

Read the draft carefully and correct anything that is:
- Factually wrong about the project
- Missing important context
- Misrepresenting a decision or its rationale
- Over- or understating your role

**The Clean Share example:** The first draft misrepresented the extension as being for users who never open the app. The designer corrected this with a detailed explanation of the actual funnel logic (educate in-app → drive to extension). This produced an entirely different and stronger section. Don't skip this step.

Corrections can be provided as plain text — Claude will rewrite the relevant sections while leaving everything else untouched.

---

## STEP 7 — LINE EDITS

Once the content is factually correct, review for tone and phrasing. Request specific changes to individual sentences or paragraphs. Claude makes surgical edits using str_replace — nothing else changes.

**The Clean Share example:** The tagline originally referenced "pushing back on the original brief" — the designer felt this was already covered by the dedicated section and removed it from the tagline. One line changed, everything else stayed.

---

## STEP 8 — ENDING

Every case study needs a closing beat that reconnects to the opening problem. If you have data, use it. If you don't:

- **Option A** — a pull quote that states the core strategic logic, followed by 2 sentences connecting back to the original goal
- **Option B** — an honest statement of the assumption the design is built on, and what would confirm or disprove it
- **Avoid** — forced conclusions, vague positive statements, or "lessons learned" sections

**The Clean Share example used a combination:** a pull quote stating the strategic goal ("The goal was never to make users open Cleaner more often. It was to make Cleaner useful in a place they already were.") followed by two sentences framing the habit assumption honestly.

---

## STEP 9 — FINAL FILE

The completed `project-[name].md` contains:

- Tagline
- Metadata block (My role + Results)
- Hero image reference
- Body with alternating pull quotes, paragraphs, and image references
- All image references use exact filenames mapping to `/assets/[project-name]/`
- A closing section

This file goes into `/projects/` in the portfolio repo. Images go into `/assets/[project-name]/`. Claude Code then uses both, along with `CASE_STUDY_TEMPLATE.md`, to build the page.

---

## THINGS THAT CONSISTENTLY IMPROVE OUTPUT

- **The clarifying questions step is not optional.** The Clean Share draft had to be substantially rewritten because one key process detail was missing. Questions first, writing second.
- **The most interesting section is usually a decision, not a feature.** What you pushed back on, what you chose not to build, what surprised you in research — these make stronger pull quotes than descriptions of what the UI does.
- **Don't describe what's in the screenshots.** Image reference notes are for Claude Code's orientation, not for the reader. The text above each image does the framing.
- **Results honesty is fine.** "Feature shipped" with no metrics is better than inflated or vague outcome claims. Update the results block when data is available.
- **One change at a time.** Request specific edits to specific sections rather than asking for a full rewrite. This keeps everything else stable and avoids losing good writing.
