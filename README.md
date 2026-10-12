# Protmūšis · VU FSMD

Public one-page site for the VU FSMD protmūšis on 26 October 2026: event info, format, rules, team registration and organizers. Plain HTML, no build step, hosted on GitHub Pages.

## Editing event details

Open `index.html`, scroll to the `<script>` at the bottom and edit the `EVENT` object (date, time, place, address, fee, registration deadline, contact email). Every place on the page that shows those details updates from there.

## Registrations

Each registration is emailed to the organizers through [Web3Forms](https://web3forms.com), a free form-to-email service (no account needed).

1. Go to https://web3forms.com, enter the organizer's email and click **Create Access Key**. The key arrives by email.
2. Paste it into `WEB3FORMS_KEY` in `index.html` and commit.
3. Every registration then arrives as an email: team name, captain's email and phone, each member with their status, and notes. Replying to it replies to the captain.

The access key is meant to be public; it only lets people send messages to that one inbox.

Until the key is set, the site shows "Registracija atsidarys netrukus" instead of sending.

The form enforces the team rules before sending: 4–5 players, at least one doctoral student or lecturer, and no more than one lecturer.

## Faculty logo

Add the official Lithuanian logo of the VU Faculty of Philosophy as `vu-filosofijos-fakultetas.png` in the repo root (PNG, transparent or white background). It appears automatically in the Organizers section; until then that box shows the faculty name as text.

## Files

- `index.html` – the whole site
- `fsmd-herbas.jpg` – VU FSMD crest
- `logo.svg` – protmūšis brain/question-mark mark (favicon)
