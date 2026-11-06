# HustleWise

**From ideas to execution.**

HustleWise is a business discovery and execution platform for founders and business owners. It guides users through a short assessment, produces a personalised readiness report, and (only with explicit consent) connects them with relevant professionals and services.

**Live site:** https://jfuix.github.io/HustleWise/

> **Status:** Prototype. Scores and provider listings shown on the site are illustrative.

---

## What it does

HustleWise is built around three ideas:

1. **Clarity**: understand your idea or business through a structured assessment.
2. **Direction**: get a personalised report and an actionable 30-day plan.
3. **Connections**: find relevant professionals and services when you're ready for expert help.

### User flow

| Step | What happens |
|------|--------------|
| 1. Choose your journey | Pick "I'm starting something" or "I already have a business". This shapes the questions and the report. |
| 2. Tell us about you | Name, email, optional phone, and preferred contact method (email, phone, or WhatsApp). |
| 3. Guided assessment | A 10-question questionnaire about the project, goals, and challenges. |
| 4. Data and consent | Plain-language summary of what is collected and how it is used, with a required consent box and an optional opt-in for provider introductions. |
| 5. Your report | Readiness score (0-100), category breakdown, gaps, a 30-day action plan, and suggested support categories. Users can copy the report or save it as a PDF. |
| 6. Submitted | Confirmation screen with a withdrawal token for revoking consent. |

### How scoring works

Each answer is scored on a 4-point scale and grouped into five categories: **clarity, validation, build readiness, reach, and resources**. Categories are weighted differently for startups and established businesses, then combined into a single 0-100 score.

The assessment is **rules-based, not AI-driven**, and is meant as a directional prompt, not professional advice.

---

## Site sections

- **Home**: hero, example project snapshot, and the HustleWise approach
- **How It Works**: the four-step journey
- **Explore Solutions**: Web & product, Growth & marketing, Business & finance (category previews, not live listings)
- **For Professionals**: information and invite request for service providers joining the network
- **About**: principles, team, and FAQ
- **Legal pages**: Privacy Policy, Terms of Use, and a Withdraw Consent page

---

## Privacy and consent

The product is designed to be consent-first:

- No account is required to take the assessment.
- Required consent covers generating the report; provider introductions are a separate, optional opt-in.
- Every introduction requires the user's explicit consent.
- Each submission issues a withdrawal token so consent can be revoked at any time.
- Users can request deletion by emailing `privacy@hustlewise.com`.

See the in-site Privacy Policy and Terms of Use for full details.

---

## Tech stack

<!-- Fill this in to match the repo -->
- HTML, CSS, and JavaScript
- Hosted on GitHub Pages

## Running locally

```bash
# Clone the repository
git clone https://github.com/jfuix/TurningPoint.git
cd TurningPoint

# Open index.html in your browser, or serve it locally:
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Project structure

<!-- Update to match the actual files in the repo -->
```
TurningPoint/
├── index.html      # Main page and assessment flow
├── ...             # Styles, scripts, and assets
└── README.md
```

## Deployment

The site is deployed with GitHub Pages. Pushing to the configured branch publishes the update at https://jfuix.github.io/TurningPoint/.

---

## Before going to production

The site currently contains placeholders that should be completed before launch:

- [ ] Add the registered legal entity name and country to the Privacy Policy
- [ ] Specify the data storage region in the Privacy Policy
- [ ] Set the governing-law jurisdiction in the Terms of Use
- [ ] Replace illustrative provider categories with real provider profiles
- [ ] Confirm the Open Graph image and canonical URLs point to the live domain

## Contact

- General: hello@hustlewise.com
- Privacy and data requests: privacy@hustlewise.com

## License

<!-- Add a license, e.g. MIT, or "All rights reserved." -->
