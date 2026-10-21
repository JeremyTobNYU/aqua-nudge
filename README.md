# AquaNudge

A retrofit for the Hydr8 4i office water cooler. It senses people approaching and pouring, and it plays a real-time DSP soundscape with light and display feedback. That feedback expresses the floor's shared "mineral level" (magnesium) and nudges people to drink more water.

NYU Tandon ECE Senior Design (DP2, Independent Track), Fall 2026. In partnership with Aqvita SRL. Final deadline: **Dec 20, 2026**.

## Concept

Concept A, "Crown & Rails": a 3D-printed cap on top of the cooler holds a Raspberry Pi 5, speakers, a round display and a ToF presence sensor. LED rails run down the front edges, and a halo frames the dispense nook. A pour is sensed by an inline flow meter on the 1/4" supply line and by a piezo contact mic on the side panel.

## Workstreams

Every issue carries one `ws:` label. See the project board for status.

| Label | Workstream | Folder |
|---|---|---|
| `ws: site` | Real cooler, test site, Aqvita coordination | `docs/` |
| `ws: parts` | Bill of materials and ordering | `hardware/` |
| `ws: dsp` | Real-time C/C++ audio engine | `dsp/` |
| `ws: sensing` | ToF, flow meter, piezo, state machine | `firmware/` |
| `ws: data` | Mineral model, SQLite logging schema | `data/` |
| `ws: feedback` | LED rails, halo, round display | `firmware/` |
| `ws: enclosure` | Cap CAD, printing, splash protection | `hardware/cad/` |
| `ws: eval-abet` | User study, analysis, ABET reports | `analysis/`, `docs/reports/` |

## How work is tracked

- **Issues** are action items that each fit in one work session (2–3 h). Every issue gets one `ws:` label and one `week: N` label.
- **The board** has four columns: Backlog, This week, In progress and Done.
- **The logbook** is `docs/logbook/`, one dated entry per work session. It records decisions, tests and problems, and it feeds the ABET midterm and final reports.
- **Weekly review** happens on Sunday: close what's done, move next week's items into "This week", and write a logbook entry.

## Repository layout

```
dsp/            real-time audio engine (C/C++, PortAudio/ALSA)
firmware/       sensors, state machine, LEDs, display (runs on the Pi)
data/           logging schema and mineral model
analysis/       study analysis scripts and notebooks
hardware/       BOM, wiring, cad/ for the cap enclosure
docs/logbook/   dated engineering log
docs/reports/   ABET proposal, midterm and final reports
```
