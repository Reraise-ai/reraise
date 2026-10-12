# Security policy

## Privacy model

Reraise is local-first. These properties are design rules, not options:

- **Files are the truth.** A world is stored as Markdown files with YAML front matter on
  your own device. Any database or index is derived and rebuildable.
- **Disclosure gate, default deny.** Nothing leaves the screen unless the disclosure gate
  allows it. Cloud use is logged, and a switch locks it off.
- **Stances never leave the device.** Your position on a card (believed, rejected,
  undecided) and your conclusions are private. A shared card is content plus provenance only.
- **Agents are players, the human sets belief.** Agents lay cards, make cards and draw
  connections at the board, and every card and connection records who made it. Only the
  human sets what is believed.
- **Training export is opt-in** per card.

## Supported versions

There is no release yet. The app code is not published. This repository holds the card
format specification and the project documents.

## Reporting a vulnerability

Please use GitHub private vulnerability reporting: go to the repository's **Security** tab
and choose **Report a vulnerability**. Do not open public issues for vulnerabilities.
Reports are handled on a best-effort basis.

## Repository safeguards

Secret scanning and push protection are to be enabled in the repository settings.
Never commit secrets or real personal data, not even in example cards.
