# StudyQuest — Beta Feedback

A lightweight feedback page for StudyQuest beta testers. Friends and classmates testing the app can send bugs, suggestions, or general feedback straight to the developer's inbox — no group chat, no lost messages.

**Live site:** _add your GitHub Pages URL here once deployed_

## What it does

- Single-page static site, styled to match the StudyQuest app's own brand (warm orange/cream palette, Fredoka One + Inter typography)
- Visitors fill out a short form (name, feedback type, optional email, message)
- Submissions are routed by [Formspree](https://formspree.io) directly to `escubidojeremiah@smcbi.edu.ph` — no backend or server needed
- On successful submit, shows a small particle-burst "stamp" animation instead of a plain confirmation message

## Setup

This site needs one manual step before feedback actually reaches an inbox — GitHub Pages only serves static files, so email delivery is handled by Formspree.

1. Sign up free at [formspree.io](https://formspree.io)
2. Create a new form, set its destination to `escubidojeremiah@smcbi.edu.ph`, and verify the email if prompted
3. Copy the form's endpoint URL (looks like `https://formspree.io/f/xxxxxxx`)
4. Open `index.html`, find this line near the bottom `<script>`:
   ```js
   const FORMSPREE_ENDPOINT = "https://formspree.io/f/YOUR_FORM_ID";
   ```
5. Replace `YOUR_FORM_ID` with your real endpoint and save

Until this is set, the form shows a setup reminder instead of silently failing.

## Deploying

1. Push this repo to GitHub (or add `index.html` to an existing repo, e.g. in a `docs/` folder)
2. Go to **Settings → Pages**
3. Set the source branch (and folder, if using `docs/`)
4. GitHub will publish it at `https://<username>.github.io/<repo-name>`

## Tech

Plain HTML, CSS, and vanilla JS — no build step, no dependencies. Everything lives in a single `index.html` file.

## Credits

Built by [Jeremiah Escubido](https://github.com/ItsmeEremiyaaaa) for the StudyQuest beta test.
