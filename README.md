[![make.fun · news-image-20261118](https://make.fun/badge/news-image-20261118.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![rank](https://make.fun/badge/news-image-20261118/mekzibnn/news-world-today/rank.svg)](https://make.fun/bounty/news-image-20261118/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)
[![reward](https://make.fun/badge/news-image-20261118/mekzibnn/news-world-today/reward.svg)](https://make.fun/bounty/news-image-20261118?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261118)

# The World Today — Wednesday 18 November 2026

A one-page newspaper front page summing up the world's news of
Wednesday 18 November 2026: 40 stories across 7 regions, with the day's
three lead stories (Xi welcomes Trump in Shenzhen, Iran's drones over
Bahrain and Kuwait, Voyager 1 reaching one light-day from Earth), a
"Where it happened" world map, a UTC timeline, the day in numbers, and a
date check listing the stories that were first reported on 17 November
and so were deliberately left out.

Entry for the [make.fun bounty](https://make.fun/bounty/news-image-20261118)
"Sum up 18 November's world news in one image".

## How the image was built

- `stories.json` — the 40 stories (11 lead stories with drawn panels, 29
  numbered briefs) plus the 6 date-check exclusions. Every story was
  checked against at least two independent sources; claims are attributed
  on the page (CONFIRMED / CLAIM tags with the source).
- `render.py` — builds `page.html` from `stories.json` (inline SVG panels,
  system fonts, no network) and screenshots it at exactly 1024×1024 with
  headless Chromium, with an overflow audit. Run it to regenerate
  `entry.png`.
- `main.py` — the entry program: a standard-library-only copy of
  `entry.png` to `/output/entry.png`. Deterministic by construction — two
  runs write identical bytes.

## Files

- `main.py` — entry program (Python 3.13, standard library only)
- `entry.png` — the image (1024×1024, PNG)
- `stories.json` — the news data
- `render.py`, `page.html` — the build pipeline
- `LICENSE` — MIT
