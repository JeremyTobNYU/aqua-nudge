# Research

Sources and findings that shape the AquaNudge design. Sources live in Zotero; what we learned from them lives here.

## Where things go

- **Zotero** holds every source: the citation, the PDF and the highlights. Use one `AquaNudge` collection with sub-collections that match the topic files below. Export BibTeX from it for the reports.
- **Topic files** hold the findings. Each finding is one short entry that names its source by Zotero citekey and says what it means for AquaNudge.
- **The logbook** records the decision when a finding changes the design or the parts list. Link the finding and the issue from that day's entry.

| File | Topic |
|---|---|
| [`nudging.md`](nudging.md) | The science of nudging: which cues change behavior, and why |
| [`prior-systems.md`](prior-systems.md) | Similar products and research systems, and what they learned |
| [`metrics.md`](metrics.md) | What to measure, how accurately, and how to run the study |

## Adding a finding

Copy this block to the top of the "Findings" section of a topic file (newest first):

```
### <One-line finding>
- **Source:** @citekey (Author, Year), <link or DOI>
- **Type:** peer-reviewed study | review / meta-analysis | product | article | other
- **Evidence:** what they did and found, with numbers (sample size, effect size, duration)
- **For AquaNudge:** what this means for the design, parts or study
- **Affects:** ws: <label>, #<issue> (if any)
- **Confidence:** high | medium | low, and why
- **Added:** YYYY-MM-DD
```

Keep the "For AquaNudge" line concrete, such as "keep the halo, drop the display" or "the flow meter needs ±5% to see a 100 mL change". That line is what feeds design decisions and the ABET reports.

## Citekeys

Use Zotero's Better BibTeX plugin with the default `authorYear` format (for example `thaler2008`), so the keys here match the exported `.bib` file.
