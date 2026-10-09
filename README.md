# Protmušis · VU FSMD

Public one-page site for the VU FSMD protmušis (pub quiz): event info, format, rules and a team registration form. Plain HTML, no build step, hosted on GitHub Pages.

## Editing event details

Open `index.html`, scroll to the `<script>` at the bottom and edit the `EVENT` object (date, time, place, address, fee, registration deadline, contact email, Facebook / Instagram links). Every place on the page that shows those details updates from there. Leave a link empty to hide it.

## Connecting the registration form to Google Forms

Registrations are sent to a Google Form, so they land in a Google Sheet.

1. Create a Google Form with these questions (short answer unless noted):
   Komandos pavadinimas · Kapitono vardas ir pavardė · El. paštas · Telefonas · Žaidėjų skaičius · Komandos nariai (paragraph) · Pastabos (paragraph).
   Make all of them optional in Google Forms (the site already checks required fields), and turn **off** "Collect email addresses" and sign-in requirements.
2. In the form, open **⋮ → Get pre-filled link**, type a dummy value in every field (e.g. `a1`, `a2`, …) and click **Get link**.
3. The link looks like `https://docs.google.com/forms/d/e/FORM_ID/viewform?entry.123=a1&entry.456=a2…`
   - `action` = the same URL with `viewform?…` replaced by `formResponse`
   - each `entry.NNN` belongs to the field whose dummy value follows it.
4. Paste those into the `GOOGLE_FORM` object in `index.html`, commit, and the live site starts accepting registrations.

Until `action` is filled in, the form shows "Registracija atsidarys netrukus" instead of submitting.

## Files

- `index.html` – the whole site
- `logo.svg` – the brain/question-mark mark (also the favicon)
