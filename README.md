# Lurelens

An educational phishing email explainer. Paste a suspicious email and Lurelens quotes the exact phrases and links that look risky, highlights them in the message, and explains why each one matters.

Everything runs in the browser: no build step, no dependencies, and nothing is uploaded or saved.

- `index.html`: English
- `index.de.html`: German (also catches German phishing wording, e.g. *dringend*, *gesperrt*, *Zahlungsdaten bestätigen*)

## What it checks

- Link text that doesn't match the real destination (plain `text <url>`, Markdown, or pasted HTML)
- Destinations hidden with `@` (`brand.com@198.51.100.24`), numeric IP links, URL shorteners, non-HTTPS links
- Look-alike or keyword-stuffed host names (`paypa1`, `brand-secure`, punycode, deep subdomains)
- Sender domains that pair a name with words like "billing" or "support"
- Urgent or threatening language, requests for passwords or payment details, payment/prize lures
- Risky attachments (archives, executables, macro-enabled documents) and generic greetings

## Run it

Open `index.html` in a browser.

## Limits

The rules are transparent heuristics, so Lurelens can miss real phishing and flag legitimate mail. Treat it as a learning aid, not a verdict, and never click a suspicious link to test it.
