<div align="center">

# Waypoint

**Big ideas need a way forward.**

A consent-first project assessment prototype that helps early-stage founders and business owners understand where they stand, see what to do next, and explore the kinds of support that could help.

<!-- Replace with your own screenshot, e.g. screenshots/assessment.png -->
<img src="screenshots/assessment.png" width="100%" alt="Waypoint assessment screenshot">

[Overview](#about-the-project) · [Problem](#problem-it-addresses) · [Features](#key-features) · [How it works](#how-it-works) · [Tech stack](#technology-stack) · [Live demo](#live-demo) · [Limitations](#project-status--limitations)

</div>

---

## About the Project

Waypoint is a platform concept built around a simple idea: people working on a business or project should be able to understand their next steps and find relevant support without searching in ten different places.

Visitors choose a starting point (starting something new, or growing an existing business), tell Waypoint a little about their project, answer a short guided assessment, and receive a report with a readiness score, a category breakdown, a 30-day action plan, and suggested areas where outside support might help.

Waypoint is deliberately honest about what it is: a **rules-based assessment**, not AI analysis and not professional advice. Data use is explained up front, and nothing is shared with a provider without the visitor's explicit opt-in.

## Problem It Addresses

Starting or growing a project can be overwhelming. Founders often know they need help but not what kind, where to find it, or what to prioritize first.

Waypoint offers a structured starting point: understand the project, identify the immediate needs, and make it easier to move forward, with the right kind of help available when (and only if) the person wants it.

## Key Features

- **Two journeys**: "I'm starting something" and "I already have a business", each with its own intake fields, questions, scoring weights, and report copy
- **Intake form**: name, email, optional phone, preferred contact method, plus journey-specific questions (idea and audience, or business name, industry, size, and main problems)
- **Guided assessment**: a 10-question, one-at-a-time questionnaire with a progress bar and a four-point answer scale
- **Readiness score**: a weighted, rules-based score from 0 to 100 across clarity, validation, build readiness, reach, and resources
- **Personalized report**: category breakdown (Strong / In progress / Needs work), a 30-day action list chosen by score band, and suggested support categories matched from the visitor's stated needs
- **Consent-first data handling**: a plain-language data notice, a required consent checkbox to generate the report, a separate optional checkbox to be contacted, and a consent text version recorded with each submission
- **Withdrawal token**: each submission gets a random token the visitor can use to request withdrawal of consent
- **Report actions**: copy the report as text, or save it as a PDF through the browser print dialog
- **Provider network pitch**: a "For Professionals" section explaining the consent-based introduction model, with an invite request link
- **Responsive interface**: layouts designed for desktop and mobile
- **Local data fallback**: submissions are saved in the browser (last 50 kept) unless a backend URL is configured

## How It Works

1. **Choose your journey**: starting something new, or growing what you already have
2. **Tell us about it**: a short intake form
3. **Complete the assessment**: 10 guided questions
4. **Review the consent notice**: required consent to generate the report, optional consent to be contacted
5. **Get your report**: score, category breakdown, 30-day actions, and suggested support areas

## Technology Stack

- **HTML5**: page structure, assessment screens, forms, and report
- **CSS3**: responsive layouts, custom properties, and interface components, using a system font stack (Inter if installed)
- **Vanilla JavaScript**: screen routing, questionnaire flow, scoring logic, report generation, and browser-side storage
- **Optional backend**: set `CONFIG.backendUrl` in the script to a POST endpoint (for example a Supabase Edge Function) to send submissions to your own server; the browser copy is still kept

The project is a single `index.html` file with no dependencies, package install, or build step.

## Live Demo

<!-- Replace with your own link once deployed, e.g. GitHub Pages -->
[Open Waypoint](https://your-username.github.io/waypoint/)

## Run Locally

```bash
git clone https://github.com/your-username/waypoint.git
cd waypoint

# Start a local server
python -m http.server 8080
```

Open `http://localhost:8080` in your browser.

## Configuration

At the top of the script:

```js
const CONFIG = {
  backendUrl: "",   // e.g. "https://<project>.supabase.co/functions/v1/submit-lead"
  consent: { version: "1.0", text: "..." }
};
```

If `backendUrl` is empty, or the request fails, the submission is saved only to the browser's `localStorage` under `waypoint.leads.v1`. Bump `consent.version` whenever you change the consent wording.

## Project Status & Limitations

**Status:** Front-end prototype / platform concept.

- The assessment uses predefined rules and scoring logic. It is **not** AI-powered, and the interface says so.
- The "Explore Solutions" cards are category previews, not live listings. There is no provider directory, verification, messaging, booking, or payment flow yet.
- Support suggestions are matched by simple keyword rules on the visitor's stated needs, with a fallback based on their lowest-scoring categories. This is not an intelligent recommendation system.
- Without a configured backend, submissions are not sent anywhere and are not available across devices.
- Consent withdrawal is not automated: the token is shown to the visitor, but you need to build the withdrawal flow (or handle requests by email) yourself.
- The Privacy Policy and Terms links are placeholders and need real pages before any public launch.
- Readiness scores and suggested actions are directional prompts, not professional advice or a measure of business potential.
- Waypoint is a working name and has not been cleared for domain, competitor, or trademark conflicts.

## Roadmap Ideas

- Connect a real backend for lead storage
- Add real Privacy Policy and Terms pages
- Automate consent withdrawal using the token
- Email the report to the visitor
- Add real, verified provider profiles
- Save assessment progress so visitors can resume later

## Credits

Designed and developed by [your name](https://github.com/your-username).
