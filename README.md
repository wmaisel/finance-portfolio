# finance-portfolio
Overview

This project is a personal Finance & Consulting Portfolio Website built with HTML/CSS/JS in VS Code and deployed via GitHub Pages.
Its purpose is to expand on my resume, showcase consulting and finance projects, and serve as a professional online presence linked directly from my resume and LinkedIn.

The site will contain:

A homepage that functions as an expanded resume + personal pitch

Deep-dive project pages for my consulting engagements (Coverd, Santa Barbara Gift Baskets)

A Finance Projects section, including:

my XYZ vs PYPL financial statement analysis

my DCF valuation application (with run-locally instructions)

This spec defines the full structure, content requirements, file architecture, and development workflow for the site.

1. Goals of the Site

Present a professional, resume-adjacent homepage that hiring managers can skim in minutes.

Provide project deep dives highlighting:

My consulting engagements (Coverd, Santa Barbara Gift Baskets)

My finance/data projects (SQ vs PYPL analysis, DCF app)

Serve as a hosted portfolio accessible via a simple GitHub Pages URL.

Be clean, minimal, accessible, and easy to maintain with pure static code.

2. Technology Stack

Frontend:

HTML5

CSS3

Basic JavaScript (optional, minimal)

Tooling:

VS Code

Codex / GitHub Copilot for rapid scaffold & component consistency

Git & GitHub for version control

GitHub Pages for hosting

No backend except for linking to my DCF app repo.

3. Repository Structure
finance-portfolio/
│
├── index.html
│
├── projects/
│   ├── coverd.html
│   ├── sbgb.html
│   ├── finance.html
│   └── (optional additional detail pages)
│
├── assets/
│   ├── css/
│   │   └── styles.css
│   ├── img/
│   │   ├── headshot.jpg
│   │   ├── coverd-hero.png
│   │   ├── sbgb-hero.png
│   │   └── (project images)
│   └── js/
│       └── (optional scripts.js)
│
└── README.md   <-- This document

4. Page-by-Page Content Requirements

Below is a full content blueprint for every page. Codex should follow this structure when generating or updating components.

4.1 Home Page — index.html
Purpose

This is the expanded resume and landing page for the entire portfolio.

Sections
1. Header / Navigation

Logo or name on left

Links on right:

Home

Projects

Contact

2. Hero Section

Circular headshot

Name (large text)

Tagline (e.g., “Finance & Consulting Student | UCSB”)

1–2 sentence professional summary

Buttons:

“Download Resume (PDF)”

“View Projects”

3. Education

UCSB — Financial Mathematics & Statistics

GPA, relevant coursework, extracurriculars

4. Experience Highlights

Each entry includes:

Role | Organization | Dates

1–2 sentence summary

Link to deep dive page (if applicable)

Projects linking to deep dives:

Engagement Manager — Santa Barbara Gift Baskets (CYC)

Product Consultant — Coverd (Ascend Consulting Group)

Other entries:

CYC Recruitment Chair

Product Strategy work

Director roles

UPenn entrepreneurship program involvement

5. Finance & Technical Projects Overview

Include project cards linking to /projects/finance.html:

SQ vs PYPL portfolio analysis

DCF valuation app (React + FastAPI)

6. Skills Section

Technical Skills: Python, React, FastAPI, Git, quantitative finance, etc.

Consulting Skills: user research, synthesis, operations mapping, client presentations

Personal Interests (optional)

7. Contact Section

Email

LinkedIn

GitHub

4.2 Coverd Deep Dive — projects/coverd.html
Purpose

Provide a detailed, narrative case study showing my product consulting and user research skills.

Sections
1. Hero / TL;DR

Title: Coverd — Product & UX Research Consulting

3 bullets summarizing:

My role and time frame

Nature of the startup

High-level impact

2. Background

What Coverd is

The challenge they were facing

Why user research was needed

3. My Role

Designed interview frameworks

Led 50+ user interviews

Synthesized findings

Delivered weekly recommendations to founders

Framed product positioning based on insights

4. Research Approach

Planning

Interview execution

Thematic synthesis

Key insights discovered

5. Impact

Frame impact in terms of:

Decisions that changed

Prioritization improvements

Insights founders adopted

6. Artifacts (optional)

Redacted slide thumbnails

Research frameworks

7. Reflection

What was learned about:

PMF discovery

Gen Z finance behavior

Product storytelling

4.3 Santa Barbara Gift Baskets Deep Dive — projects/sbgb.html
Purpose

Showcase end-to-end consulting ability, engagement leadership, and quantifiable business impact.

Sections
1. Hero / TL;DR

Title: Santa Barbara Gift Baskets — Business & Acquisition Consulting

3 bullets summarizing:

EM role

Engagement scope

Deliverables

2. Client Background

Local retailer preparing for acquisition

Operational challenges and opportunities

3. My Role

Led a 5-person team

Ran client meetings

Scoped engagement deliverables

Delegated and reviewed workstreams

4. Workstreams

SEO/SMO improvements

Baseline snapshot

Technical fixes (image compression, meta descriptions, review mechanisms)

Operational SOP creation

Process documentation methodology

Structure of SOP binder

Acquisition pitch development

Storyline

Key metrics and buyer narrative

5. Impact

Examples:

Delivered acquisition-ready SOP manual

Improved website presentation and visibility

Delivered pitch deck for prospective buyers

6. Artifacts (optional)

Redacted SOP pages

Deck snippets

7. Reflection

Small-business operational insight

Leadership lessons

Learnings about client communication

4.4 Finance Projects — projects/finance.html
Purpose

Showcase quantitative, analytical, and technical finance projects.

Sections
1. Intro Paragraph

Context on why I do finance projects: valuation, risk modeling, portfolio analytics, etc.

2. Project Card: SQ vs PYPL Portfolio Analysis

Include:

Purpose of analysis

Tools used (Python, Pandas, numpy, market data)

Metrics calculated (return, volatility, Sharpe, correlations)

Key findings

Button/link:

“View Writeup”

“View Code (GitHub)”

3. Project Card: DCF Valuation App

Include:

Stack (React + Vite, FastAPI, yfinance)

What the app does

Interesting engineering/design choices

Links:

“Visit Repository”

“Run Locally Instructions”

4. DCF Local Installation Guide

Include:

git clone <repo-url>

cd backend
pip install -r requirements.txt
uvicorn main:app --reload

cd ../frontend
npm install
npm run dev

5. Visual Design System

Codex should follow these rules consistently across the site:

Color Palette

Background: #ffffff or #f7f7f7

Accent color: a single bold color (e.g. navy, forest green)

Text color: #1a1a1a

Links: accent color

Typography

Use a clean sans-serif stack:

font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;

Components

Reusable .card class

Reusable .section class

Reusable .btn classes

Responsive grid/flex layout

Hero section using flex (image + text)

Responsive Rules

On mobile, collapse hero to vertical

Cards become 1 column instead of 2

Nav collapses into stacked links or simple horizontal layout

6. Development Workflow

This is the exact step-by-step workflow for building and maintaining the project.

Phase 1 — Repo Setup

Create GitHub repo

Enable GitHub Pages

Clone into VS Code

Create base folder structure

Phase 2 — Scaffold Pages with Codex

For each HTML file, prompt Codex:

“Generate a responsive HTML5 page using the sections defined in the project specification README. Use semantic tags, import styles.css, and create placeholder content for each section.”

Phase 3 — Build Global Styles

Create styles.css including:

Typography rules

Color palette variables

Reusable components

Flex/grid layout rules

Phase 4 — Fill in Real Content

Insert actual resume content into homepage

Write narrative sections for project deep dives

Insert finance project summaries

Phase 5 — Test & Deploy

Test with VS Code Live Server

Verify mobile layout

Fix internal links

Commit & push

Check live GitHub Pages site

7. Future Enhancements (Optional)

Add dark mode

Add JavaScript animations / transitions

Add a blog post system using markdown + JS

Add downloadable project PDFs

Add analytics (Plausible, Cloudflare, or GitHub Pages native)

8. Codex Usage Notes

When using Codex in this repo:

Always reference the README for structure

Follow the design system and components

Maintain consistent HTML semantics

Keep CSS modular — no inline styling

Use placeholder text but maintain section hierarchy

9. Final Deliverable

A clean, professional portfolio website with:

An expanded resume homepage

Structured consulting case studies

Documented finance/data projects

A consistent visual identity

Fully responsive design

Live deployment on GitHub Pages
