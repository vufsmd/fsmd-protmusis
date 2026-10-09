# Protmušis · VU FSMD

Public one-page site for the VU FSMD protmušis on 26 October 2026: event info, format, rules, team registration and organizers. Plain HTML, no build step, hosted on GitHub Pages.

## Editing event details

Open `index.html`, scroll to the `<script>` at the bottom and edit the `EVENT` object (date, time, place, address, fee, registration deadline, contact email). Every place on the page that shows those details updates from there.

## Registrations

Each registration is emailed to **l.btkvcs@gmail.com** through [FormSubmit](https://formsubmit.co), a free service that needs no account.

1. After the site is live, submit one test registration. The very first submission sends an **Activate Form** email to that address; click the link in it. (That test registration itself is not delivered.)
2. From then on every registration arrives as an email with a table: team name, captain's email and phone, each member with their status, and notes. Replying to it replies to the captain.
3. Optional: FormSubmit's activation email also gives a random alias. Replace the address in `FORM_ENDPOINT` with `https://formsubmit.co/ajax/<alias>` to hide the email from the page source.

The form enforces the team rules before sending: 4–5 players, at least one doctoral student or lecturer, and no more than one lecturer.

## Faculty logo

Add the official Lithuanian logo of the VU Faculty of Philosophy as `vu-filosofijos-fakultetas.png` in the repo root (PNG, transparent or white background). It appears automatically in the Organizers section; until then that box shows the faculty name as text.

## Files

- `index.html` – the whole site
- `fsmd-herbas.jpg` – VU FSMD crest
- `logo.svg` – protmušis brain/question-mark mark (favicon)
