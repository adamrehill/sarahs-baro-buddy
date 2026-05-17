# Sarah's Baro Buddy

A simple barometric pressure tracker for Winnipeg, MB and Kelowna, BC.

> **Vibe coded** with Claude. No effort to produce quality code on this one haha

## What it does

- Live barometric pressure, temperature, and weather conditions for both cities
- 7-day pressure forecast with high/low temps
- Historical pressure chart (7 days / 30 days / 3 months)
- Migraine likelihood estimate based on pressure swings over the past few days and the upcoming forecast

## How it works

Static single-page app (`index.html`) that fetches free weather data from [Open-Meteo](https://open-meteo.com) — no API key required, no server needed. Deployable directly on GitHub Pages.

## Migraine likelihood

Scores pressure swing severity on a 5-level scale (Very Low → Very High). It factors in:
- Largest drop or rise in the past 24 hours
- Biggest day-over-day swing in the next 3 forecast days
- Current 6-hour pressure trend

It will show **Low** or **Very Low** on genuinely stable days (small pressure swings, calm forecast). Winnipeg especially tends to sit in the Medium–High range because continental weather systems bring larger swings than coastal climates.
