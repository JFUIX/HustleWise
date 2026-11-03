<div align="center">

# Waypoint

**You’ve got the idea. Let’s get it moving.**

A project assessment and discovery platform concept that helps early-stage founders and business owners understand what they need next, explore useful resources, and connect with people who can help.

<img src="https://raw.githubusercontent.com/JFUIX/waypoint/main/screenshots/assesment.png" width="100%" alt="Waypoint project assessment screenshot">

[Overview](#about-the-project) · [Problem](#problem-it-addresses) · [Features](#key-features) · [Tech stack](#technology-stack) · [Live demo](#live-demo)

</div>

---

## About the Project

Waypoint is a platform concept built around a simple idea: people working on a business or project should be able to understand their next steps and find relevant support without having to search in ten different places.

Visitors can describe what they are building, complete a short guided assessment, and receive a report covering their current stage, possible gaps, challenges, resources they may need, and suggested next steps. The project also includes a searchable-style directory concept for discovering service providers, mentors, and potential collaborators.

## Problem It Addresses

Starting or growing a project can be overwhelming. Founders may know they need help but not know exactly what kind, where to find it, or what to prioritize first.

Waypoint explores a more structured starting point: understand the project, identify the immediate needs, and make it easier to discover relevant people and services.

## Key Features

- **Guided project assessment** — a 10-step questionnaire covering the project, stage, goals, challenges, needs, budget, online presence, and contact details
- **Project readiness overview** — a rules-based score across clarity, validation, build, reach, and resources
- **Personalized report** — highlights possible gaps, challenges, support needs, opportunities, and suggested actions for the next 30 days
- **Provider directory concept** — sample profiles across development, design, marketing, legal and finance, mentoring, funding, and co-founding
- **Relevant profile highlighting** — highlights sample directory profiles based on the needs selected in the assessment
- **Report actions** — copy the report or save it as a PDF through the browser print dialog
- **Provider submission form** — lets a potential provider enter their details and describe the help they offer
- **Responsive interface** — layouts designed for desktop and mobile
- **Theme support** — follows the system color preference and includes a manual light/dark theme foundation
- **Local data fallback** — saves assessment and provider form data in the browser when the optional host integration is unavailable

## Technology Stack

- **HTML5** — page structure, assessment, directory, and forms
- **CSS3** — responsive layouts, custom styling, theme variables, and interface components
- **Vanilla JavaScript** — questionnaire flow, scoring logic, report generation, directory filtering, and browser-side storage
- **Google Fonts** — Space Grotesk and DM Sans typography
- **Optional host integration** — the code attempts to use the available Claude environment integration for lead storage; local browser storage is used as a fallback

The project is currently contained in a single `index.html` file and does not require a package installation or build step.

## Live Demo

[Open Waypoint](https://jfuix.github.io/waypoint/)

## Run Locally

```bash
git clone https://github.com/JFUIX/waypoint.git
cd waypoint

# Start a local server
python -m http.server 8080
```

Open `http://localhost:8080` in your browser.

## Project Status & Limitations

**Status:** Front-end prototype / platform concept.

- The assessment uses predefined rules and scoring logic. It is not an AI-powered analysis engine, even though the interface presents it as an AI-guided assessment.
- Provider profiles are sample content created to demonstrate the directory and matching experience. They are not verified businesses or real recommendations.
- Profile matching is based on the needs selected in the questionnaire and the categories assigned to sample profiles. It is not an intelligent recommendation system.
- Assessment and provider submissions fall back to browser local storage. Without a working backend integration, information is not sent to a central Waypoint database and will not be available across devices.
- There is no live account system, provider verification, messaging, booking, payment, or full marketplace workflow.
- The readiness scores and suggested actions are directional prompts to help users think through their projects, not professional advice or a definitive measure of business potential.
- The Waypoint name is a working name and has not yet been cleared for domain, competitor, or trademark conflicts.

## Credits

Designed and developed by [JFUIX](https://github.com/JFUIX).
