# Woolton FC Tournament Planner

A single-page, browser-based tournament planning tool built for **[Woolton FC](https://www.wooltonfc.co.uk/)** youth football tournaments.

No installation, no server, no internet connection required — just open `tournament-planner.html` in Chrome.

---

## Features

- **Live duration calculator** — total tournament time updates instantly as you adjust any setting
- **Timeline visualisation** — SVG bar chart of the full day with hover tooltips showing exact kick-off and finish times for every slot
- **Pitch allocation map** — shows which groups play on which pitches in each time slot
- **Knockout bracket preview** — visual bracket tree for all concurrent knockout phases
- **Pitch diagram** — overhead view of a full-size pitch showing how it is divided for the chosen format (5-a-side quarters, 7-a-side thirds, 9-a-side halves, or 11-a-side)
- **Phase breakdown table** — per-phase summary of games, slots, and duration
- **Referee calculator** — minimum, recommended, and comfortable referee counts

---

## How to Use

### 1. Open the app

Download or clone this repository, then open `tournament-planner.html` directly in Google Chrome:

```
File → Open File → tournament-planner.html
```

No web server is needed. The file runs entirely in the browser.

### 2. Configure your tournament

Use the controls on the left panel to set up your event:

| Control | Description |
|---|---|
| **Teams** | Total number of teams entering the tournament |
| **Pitches** | Number of pitches available for play |
| **Teams per group** | How many teams share a group (valid divisors of team count only) |
| **Knockout phase structure** | Band size — how many consecutive group positions advance to the same knockout bracket (e.g. band of 2 with 6 teams per group = 3 concurrent knockout phases) |
| **Match length** | Duration of each game in minutes |
| **Break between games** | Minimum gap between consecutive games on the same pitch |
| **Extra time between rounds** | Buffer between the group stage and knockout rounds, and between knockout rounds |
| **Start time** | Kick-off time for the first game (defaults to 09:00) |

### 3. Understand the knockout structure

The **Knockout phase structure** control lets you run multiple concurrent knockout brackets from the same group stage:

- With 4 groups of 6 and a band size of **2**: positions 1–2 go into Bracket E, positions 3–4 into Bracket F, positions 5–6 into Bracket G — every team enters a knockout, all three brackets run at the same time.
- With a band size of **6**: all 6 positions from each group enter the same single bracket.
- The bracket preview below the chips shows the exact position-to-bracket mapping and round structure for each bracket.

### 4. Read the timeline

Hover over any bar on the timeline to see:
- The phase and slot number
- Exact start and end times
- Number of games in that slot

Gap annotations show break durations between slots. Yellow arrows mark the longer inter-round breaks.

### 5. Switch pitch format

The **Pitch Diagram** panel has four format chips:

| Format | Split | Typical dimensions |
|---|---|---|
| 5-a-side | 4 quarters (2×2) | 40×30 m |
| 7-a-side | 3 vertical thirds | 55×40 m |
| 9-a-side | 2 vertical halves | 70×46 m |
| 11-a-side | Full pitch | 100×64 m |

Yellow dashed lines show how the full-size pitch is divided. Each sub-pitch shows its own centre circle and goals.

---

## Example: Woolton FC Multi-Age Tournament

A typical Woolton FC setup running two age groups simultaneously:

| Setting | Under 6s / 7s | Under 8s | Under 9s |
|---|---|---|---|
| Teams | 24 | 24 | 24 |
| Pitches | 6 | 6 | 4 |
| Format | 5-a-side | 5-a-side | 7-a-side |
| Groups | 4 × 6 | 4 × 6 | 4 × 6 |
| Knockout bands | 2 (3 phases) | 2 (3 phases) | 2 (3 phases) |
| Match length | 12 min | 12 min | 14 min |
| Est. duration | ~3h 57m | ~3h 57m | ~5h 10m |

With Under 6s and Under 7s running on separate sets of 6 pitches simultaneously, all 48 teams complete a full group stage and knockout on the same day.

---

## Intellectual Property

This application was created for **[Woolton FC](https://www.wooltonfc.co.uk/)**, who retain the intellectual property rights. It is made freely available to the football community under the MIT licence (see below). Woolton FC are not responsible for any inaccuracies in tournament scheduling that may result from use of this tool.

---

## Licence

MIT License

Copyright (c) 2025 Woolton FC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
