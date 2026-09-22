[README.md](https://github.com/user-attachments/files/32510406/README.md)
# mail-admin

A small, self-contained HTML tool for generating the password-delivery email sent to customers when mail admin (Konsoleh) access is set up for a Xneelo-hosted mailbox. Fill in three fields and get a ready-to-copy, formatted message — no build step, no dependencies, no server required.

This is a sibling of the **Mailbox Handover Email Generator** — same tool design, different template wording (mail admin password + Konsoleh login link, instead of the mailbox password).

## Features

- **Three inputs**: Customer Name, Server Address, Password Link
- **Live preview** of the generated email, formatted and spaced to match the standard template
- **Password Link** renders as a clickable "Password Link" hyperlink pointing to the pasted URL
- Includes the fixed **mail admin login link** (`https://login.konsoleh.co.za/cas/login`)
- **Editable preview** — tweak the wording ad hoc before copying, with a basic formatting toolbar (Bold, Italic, Underline, Bullet list, Clear formatting)
- **Two copy options**:
  - *Copy formatted* — rich text with working links and bold labels, for pasting into Gmail/Outlook/webmail
  - *Copy as plain text* — plain text with line breaks preserved, for plain-text email clients
- Ad hoc edits are held in memory only — nothing is saved, and everything resets when the page reloads
- Light/dark mode aware, responsive down to mobile

## Usage

1. Open `mail-admin-handover.html` in any modern browser (double-click the file, or host it anywhere static files are served).
2. Fill in the three fields on the left.
3. Optionally edit the message directly in the preview panel.
4. Click **Copy formatted** or **Copy as plain text**, then paste into your email client.

No installation, build tools, or internet connection required — the page is a single HTML file with everything inlined.

## Files

```
mail-admin-handover.html   # the entire app — open this file directly
```

## Customizing the template

The email template (greeting, mail admin login link, server settings, sign-off, and the closing disclaimer) is defined in the `buildEmailHTML()` function inside `mail-admin-handover.html`. Edit the strings there to change the default wording, then reload the page to see the update.
