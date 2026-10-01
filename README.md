# 🌸 Blush Usability Tracker

A single-file usability tracker with a pink interface. It records how people click, move and scroll on a page, then shows where they run into friction. The demo page is a pretend boutique called **Petal & Co.**, so you can test it right away.

## What It Does

**Tracking**
- Click tracking with numbered dots
- Rage click detection (three or more fast clicks in the same spot)
- Dead click detection (clicks on things that aren't buttons or links)
- Mouse movement points and mouse path
- Scroll depth tracking
- Element visibility tracking (sale banner entering and leaving view)
- Time to first click and time on page

**Visuals**
- Click dots, heatmap and scatter plot
- Dashed dots for dead clicks, dark red dots for rage bursts
- Toggle dot numbers on or off

**Results**
- Live stats panel with a friction-free score out of 100
- Session summary pop-up with a verdict and a most-clicked elements table
- Live event log
- Download results as a JSON file, or copy the JSON to your clipboard

## Getting Started

1. Download `usability-tracker.html`.
2. Open it in your browser.
3. Click around, scroll and move your mouse over the page.
4. Use the panel on the right to switch views, open the summary or download your results.

No install or server needed.

## How the Friction Score Works

The score starts at 100 and goes down as problems are detected:

| Issue | Penalty |
|---|---|
| Rage click burst | −12 each |
| Dead click | −4 each |

| Score | Verdict |
|---|---|
| 85 and above | Smooth experience |
| 60 to 84 | Some friction |
| Below 60 | High friction |

## Saved Results

Results are not saved automatically. They live in the open browser tab and disappear when you refresh or close it. Click **Download JSON file** before leaving to keep your session.

The file contains:
- A summary (clicks, rage bursts, dead clicks, friction score, scroll depth, time)
- Every click with its position, element and timestamp
- Mouse points and scroll events
- The full event list

## Tech Stack

- HTML
- CSS
- JavaScript

## Notes

- Everything runs in your browser. Nothing is sent to a server.
- The tracker panel and summary pop-up are excluded from tracking.
- Mouse points are capped at 5,000 and events at 20,000 per session to keep the page fast.
