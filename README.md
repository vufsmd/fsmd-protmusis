# Protmūšis · VU FSMD

Public one-page site for the VU FSMD protmūšis on 26 October 2026: event info, format, rules, team registration and organizers. Plain HTML, no build step, hosted on GitHub Pages.

## Editing event details

Open `index.html`, scroll to the `<script>` at the bottom and edit the `EVENT` object (date, time, place, address, fee, registration deadline, contact email). Every place on the page that shows those details updates from there.

## Registrations

Registrations go to a Google Form, so every team lands in a Google Sheet and Google can email you about each one.

1. Create a Google Form (signed in as the organizer) with these 5 **short answer / paragraph** questions, all optional (the site already checks everything):
   `Komandos pavadinimas` · `Kapitono el. paštas` · `Kapitono telefonas` · `Komandos nariai` (paragraph) · `Pastabos` (paragraph).
   In **Settings → Responses**, turn **off** "Collect email addresses" and "Limit to 1 response" (no Google sign-in).
2. **Responses** tab → ⋮ → **Get email notifications for new responses**. Optionally **Link to Sheets**.
3. ⋮ (top right) → **Get pre-filled link**, type `1`, `2`, `3`, `4`, `5` into the questions in order, click **Get link** and copy it.
4. Paste that link into `GOOGLE_FORM` in `index.html` (or send it to whoever maintains the site):
   - `action` = the link with `viewform?…` replaced by `formResponse`
   - each `entry.NNN` in the link goes to the field whose number follows it.

Until `action` is filled in, the site shows "Registracija atsidarys netrukus" instead of sending.

The form enforces the team rules before sending: 4–5 players, at least one doctoral student or lecturer, and no more than one lecturer.

## Faculty logo

Add the official Lithuanian logo of the VU Faculty of Philosophy as `vu-filosofijos-fakultetas.png` in the repo root (PNG, transparent or white background). It appears automatically in the Organizers section; until then that box shows the faculty name as text.

## Files

- `index.html` – the whole site
- `fsmd-herbas.jpg` – VU FSMD crest
- `logo.svg` – protmūšis brain/question-mark mark (favicon)
