# Ministry of Problems

A single-file browser game about product thinking. Seven anti-patterns have occupied
the building, and you cannot out-build them — the only weapon that lands is a better
question.

Answer questions in **Field Study** to earn grant credits, spend them at
**Procurement** on instruments and armour, then **Deploy** against the case files.

## Play

**Play it here: https://earendelnat.github.io/quiz-app/** — no install, works on phone or laptop.

Open `index.html` in any modern browser. No build step, no server,
no dependencies to install — everything (styles, logic, content) lives in the one file.
Web fonts are pulled from Google Fonts, so first load looks best online.

## Doctrine

- **Problems over solutions.** Diagnose before you build.
- Ask better questions first.

## Inputs and outputs

Everything the game touches, in full:

| Direction | What | Where |
| --- | --- | --- |
| In | Player clicks — answers, purchases, deployments | the page itself |
| In | Saved progress, on load | `localStorage["ministry-of-problems.v1"]` |
| In | Three typefaces, on first paint | `fonts.googleapis.com`, `fonts.gstatic.com` |
| Out | Progress, after each scoring event | `localStorage["ministry-of-problems.v1"]` |
| Out | Reset, which clears the save | the same key, removed |

There is no `fetch()`, no form post, no analytics and no backend anywhere in the
file. Apart from pulling the fonts, nothing you do in the game leaves the
browser — and because the save lives in `localStorage`, it never leaves the
machine it was made on. Clearing site data or opening the game in a different
browser starts you from scratch.

## Structure

```
index.html   the entire game
```
