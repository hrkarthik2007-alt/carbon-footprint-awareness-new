# Groundwork — Carbon Footprint Awareness Platform

PromptWars (H2S) — Challenge 3 submission.

## Live demo
Visit: https://legendary-frangipane-621805.netlify.app

## Chosen vertical
Carbon Footprint Awareness Platform — a tool that helps individuals understand, track, and reduce their carbon footprint through simple actions and personalized insights.

## Approach and logic
1. **The number needs a body.** Results shown as a footprint silhouette filled like soil strata — one band per category (diet, energy, travel, waste). A dashed line marks the ~190 kg/month 1.5°C-aligned benchmark.
2. **Insight, not advice.** The app finds the biggest category, then runs the same formula backwards on the user's own numbers to produce a specific computed saving — not a generic tip.
3. **No accounts, no tracking.** Everything runs client-side. Nothing is sent to a server.

## How it works
- User fills four sections: travel, home energy, diet, waste.
- computeFootprint() applies standard emission factors to produce kg CO2e per category and total.
- Footprint SVG fills bottom-up, banded by category share, measured against the target line.
- renderInsight() identifies the largest category and computes a specific numeric suggestion.
- Each calculation is logged in-session to demonstrate tracking over time.

## Assumptions
- Emission factors are simplified averages for intuition, not a certified audit.
- 190 kg CO2e/month = rough monthly slice of the 2.3 t/year 1.5°C-aligned per-person budget.
- Session log clears on refresh by design (privacy by default).

## Tech
Plain HTML + CSS + vanilla JS. No framework, no build step. Well under the 10 MB repo limit.
