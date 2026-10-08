# JQG Labs Web

Corporate website for **JQG Labs**, an independent technology lab from Colombia that builds business software and interactive experiences. Intended to be served at [jqglabs.com](https://jqglabs.com/).

The site is plain HTML, CSS and JavaScript: no framework, no dependencies, no build step. Site content is in Spanish (`es-CO`).

## Running locally

Serve the project root with any static server. The favicon is linked as `/favicon.svg`, so the site should be served from the root rather than opened as a `file://` URL.

- **VS Code Live Server**: open `index.html` and choose "Go Live". The workspace is configured for port `5501`, so the site opens at <http://localhost:5501>.
- **Python**: `python -m http.server 5501`
- **Node**: `npx serve .`

## Project structure

```
index.html        Landing page (hero, software, games, about, contact)
privacidad.html   Privacy policy
terminos.html     Terms of use
styles.css        All styles, shared by the three pages
script.js         Mobile menu, contact form handling, footer year
favicon.svg       Site icon
public/           Logo and isotype images
agents/skill.md   Brand and site strategy brief, used as guidance for AI assistants
```

## Page sections

`index.html` is a single page with anchor navigation:

| Anchor | Section |
| --- | --- |
| `#inicio` | Hero with the value proposition and logo |
| `#software` | Services: custom software, automation, digital products |
| `#interactivo` | Games and interactive experiences |
| `#nosotros` | About JQG Labs |
| `#contacto` | Contact form |

The footer links to the legal pages and to the Facebook and Instagram profiles.

## Design

Colors and fonts are defined as CSS custom properties at the top of `styles.css`, so the theme can be changed in one place.

| Token | Value | Use |
| --- | --- | --- |
| `--paper` | `#f6f3ed` | Page background |
| `--ink` | `#211f1b` | Main text |
| `--muted` | `#70695e` | Secondary text |
| `--acid` | `#d5b15d` | Gold accent |
| `--gold-deep` | `#997329` | Borders, hover states |
| `--forest` | `#25231f` | Dark sections |

Typography is Space Grotesk for text and DM Mono for labels, both loaded from Google Fonts.

## Known limitations

- **The contact form does not send anything.** On submit, `script.js` cancels the request and shows a message saying the official contact channel is not yet enabled. It needs a backend or a form service before it can receive messages.
- The games section is a placeholder; no titles are listed yet.

## Roadmap

`agents/skill.md` describes where the site is headed: corporate email under `@jqglabs.com`, visible legal information in the footer, a B2B software catalog with quote requests, game pages with store links, and an online store for physical products. Much of this supports organization verification on Google Play Console, the Apple Developer Program and Steam Direct.

## Links

- Website: <https://jqglabs.com/>
- Facebook: <https://www.facebook.com/jqglabs>
- Instagram: <https://www.instagram.com/jqglabs/>

© JQG Labs. All rights reserved.
