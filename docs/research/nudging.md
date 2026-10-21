# The science of nudging

**Scope:** Which cues (light, sound, social comparison, timing, defaults, feedback) change drinking behavior, and why.

## Open questions

- Which cue changes drinking most: light, sound, social comparison or personal feedback?
- Does a shared, floor-level goal (the "mineral level") work better than individual feedback?
- How fast do people get used to a cue and stop noticing it, and how do we keep it fresh?
- Does an ASMR-style pour sound work from a speaker in a noisy office, or only on headphones?
- What did the 2023 *Nutrients* review on nudging fluid intake find? ([doi:10.3390/nu15122702](https://doi.org/10.3390/nu15122702), not yet read)

## Summary

Sound prompts at the point of use reliably change behavior: motion-triggered audio reminders raised hand-hygiene compliance a lot. People respond best to natural, recognizable sounds, and water sounds are the most strongly linked to positive affect and health. That points to three short layers: a natural water sound when someone walks up, a pour sound whose pitch rises as the bottle fills, and a bright, crystalline "mineral" chime when they finish. Continuous water soundscapes backfired in an open office, and people habituate to repeated sounds, so sounds should be event-triggered, soft (about 45–50 dB at 1 m) and varied. ASMR-style crisp, close-up sounds can relax people and lift ad response, but results are mixed and the effect depends on closeness to the listener, so treat ASMR as a study condition, not the default.

Hardware: the Pi 5 has no 3.5 mm audio jack, so the audio chain needs an I2S DAC/amp board (for example HiFiBerry MiniAmp or MAX98357A) and full-range speakers covering at least about 100 Hz–15 kHz. If ASMR-style sound is tested, aim the speakers at the nook, close to the listener's head.

## Findings

### ASMR ads beat plain ads for fashion, but not for food
- **Source:** @douce2023 (Doucé, 2023), https://documentserver.uhasselt.be/bitstream/1942/42051/1/ASMR_Lieve%20Douce_Euregio2023.pdf
- **Type:** other (conference presentation, Euregio Marketing Colloquium)
- **Evidence:** Two online 2×2 experiments. Study 1 (n = 308): non-ASMR ads scored higher on every measure, including imagery, ad and brand attitude, and purchase intention (p ≤ .03). Study 2 (n = 217): ASMR helped a Coach handbag ad (purchase intention 3.34 → 4.25) but barely helped a McDonald's food ad and lowered brand attitude (5.00 vs 4.65).
- **For AquaNudge:** ASMR is not a sure win for things you consume. Test it as one condition instead of building the whole sound design on it.
- **Affects:** ws: dsp, ws: eval-abet
- **Confidence:** low, because it's a slide deck with partial methods and an inconsistent sample count
- **Added:** 2026-10-21

### ASMR audio in ads raises skin conductance and frontal brain activity
- **Source:** @liang2023 (Liang & Li, 2023), *Journal of Sensory Studies*, doi:10.1111/joss.12888
- **Type:** peer-reviewed study
- **Evidence:** Towel ads with ASMR audio raised skin conductance and left anterior frontal brain activity. The authors read this as more attention, and the survey supported all of their hypotheses on attention and purchase intention.
- **For AquaNudge:** Crisp, tactile ASMR sound grabs attention, which supports an ASMR-style pour sound as a candidate for the feedback layer.
- **Affects:** ws: dsp
- **Confidence:** medium, because only the abstract was read
- **Added:** 2026-10-21

### ASMR ads lift affect most for low-involvement products from familiar brands
- **Source:** @utaustin-asmr (UT Austin repository, author and year not listed), https://repositories.lib.utexas.edu/handle/2152/83140
- **Type:** other (likely a thesis)
- **Evidence:** ASMR ads produced more positive affect, better ad attitudes and higher purchase intention than non-ASMR ads. The affect gain was largest with low product involvement and high brand familiarity.
- **For AquaNudge:** Office water is a low-involvement product, which is the case where ASMR helped most.
- **Affects:** ws: dsp
- **Confidence:** low, because the author and methods are unknown
- **Added:** 2026-10-21

### ASMR cues in ads raise purchase intention through relaxation
- **Source:** @dekerpel2023 (De Kerpel, Van Kerckhove & Tessitore, 2023), *International Journal of Advertising*, doi:10.1080/02650487.2023.2262328
- **Type:** peer-reviewed study
- **Evidence:** A web-scraping study and two experiments. ASMR cues raised purchase intention, and a serial mediation showed relaxation and a flow-like state explained the effect.
- **For AquaNudge:** ASMR works through relaxation, which fits a health-oriented brand better than arousing reward sounds.
- **Affects:** ws: dsp
- **Confidence:** medium, because only the abstract was read
- **Added:** 2026-10-21

### ASMR changes heart rate and skin conductance, but only some people respond
- **Source:** @poerio2018 (Poerio, Blakey, Hostler & Veltri, 2018), *PLoS ONE* 13(6): e0196645, https://eprints.whiterose.ac.uk/132445
- **Type:** peer-reviewed study
- **Evidence:** An online experiment and a lab study. Heart rate dropped and skin conductance rose during ASMR videos. The emotional effects appeared only in people who experience ASMR.
- **For AquaNudge:** Expect ASMR-style sound to work strongly on some people and not at all on others, and some will dislike it. Keep it short and soft.
- **Affects:** ws: dsp, ws: eval-abet
- **Confidence:** high
- **Added:** 2026-10-21

### The most common ASMR triggers are whispering, personal attention and crisp sounds
- **Source:** @barratt2015 (Barratt & Davis, 2015), *PeerJ* 3:e851, https://peerj.com/articles/851
- **Type:** peer-reviewed study (survey)
- **Evidence:** Triggers reported: whispering 75%, personal attention 69%, crisp sounds 64%, slow movements 53%, repetitive tasks 34%.
- **For AquaNudge:** Close-mic pouring, bubbles and ice clinks fall under "crisp sounds". ASMR relies on intimacy and closeness, and most studies used headphones, so a top-firing speaker 50 cm above the head loses much of the effect. Aim speakers at the nook if we test it.
- **Affects:** ws: dsp, ws: parts, ws: enclosure
- **Confidence:** high
- **Added:** 2026-10-21

### People habituate to repeated notifications, and it spreads to similar sounds
- **Source:** @fogofwarnings (SOUPS, "The Fog of Warnings: How Non-essential Notifications Blur with Security Warnings"), https://par.nsf.gov/biblio/10176924
- **Type:** peer-reviewed study
- **Evidence:** Habituation to frequent non-essential notifications carried over to a one-time warning and reduced attention and adherence. The carry-over came from generalization, not fatigue, and grew with similarity between the two.
- **For AquaNudge:** One fixed chime will stop working. Use a rotating pool of variations and keep cues distinct from each other.
- **Affects:** ws: dsp
- **Confidence:** medium, because the study is about visual security warnings, not sound
- **Added:** 2026-10-21

### A continuous water soundscape in an open office did worse than plain masking noise
- **Source:** @hongisto2017 (Hongisto, Varjo, Oliva, Haapakangas & Benway, 2017), *Frontiers in Psychology* 8:1177, https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2017.01177/pdf
- **Type:** peer-reviewed study
- **Evidence:** One office, 18 respondents, five 3-week conditions at 43–45 dB LAeq. None of four water sounds (waterfall, river, babbling river, river with birds) beat pseudo-random noise on any subjective measure. Acoustic and job satisfaction dropped.
- **For AquaNudge:** Don't run a continuous ambient loop. Make sounds event-triggered, short, and around 45–50 dB at 1 m.
- **Affects:** ws: dsp, ws: feedback
- **Confidence:** medium, because it's one office with a fixed condition order
- **Added:** 2026-10-21

### Win sounds raise arousal and make people overestimate wins
- **Source:** @dixon2013 (Dixon et al., 2013), *Journal of Gambling Studies*, doi:10.1007/s10899-013-9391-8
- **Type:** peer-reviewed study
- **Evidence:** 96 gamblers played with and without sound. Sound raised skin conductance and was preferred, and players overestimated wins by 24% with sound vs 15% without.
- **For AquaNudge:** A completion chime will reinforce drinking, but keep it honest and tied to real poured volume to avoid a dark pattern.
- **Affects:** ws: dsp, ws: data
- **Confidence:** high
- **Added:** 2026-10-21

### High pitch is linked with sweet and sour tastes, low pitch with bitter
- **Source:** @crisinel2010 (Crisinel & Spence), "A sweet sound? Food names reveal implicit associations between taste and pitch", https://www.neuroscience.ox.ac.uk/publications/54760
- **Type:** peer-reviewed study
- **Evidence:** Implicit association and go/no-go tasks linked sweet and sour food names with high-pitched sounds. Earlier work (Crisinel & Spence 2009) linked bitter with low pitch.
- **For AquaNudge:** A bright, glassy, crystalline register fits "magnesium", "clean" and "fresh". Avoid low, heavy tones.
- **Affects:** ws: dsp
- **Confidence:** medium, because the effect is on taste words, not water
- **Added:** 2026-10-21

### Listeners can hear fill level in a filling vessel's rising pitch
- **Source:** @cabe2000 (Cabe & Pittenger, 2000), "Human Sensitivity to Acoustic Information From Vessel Filling", *JEP: Human Perception and Performance*; cited in https://export.arxiv.org/pdf/2403.14740
- **Type:** peer-reviewed study
- **Evidence:** The air-column resonance rises in pitch as a vessel fills. The title says the study tested human sensitivity to this cue, but the original paper hasn't been read yet.
- **For AquaNudge:** A synthesized rising pitch during the pour gives a natural progress cue toward a "full" bottle.
- **Affects:** ws: dsp, ws: sensing
- **Confidence:** low until the original paper is read
- **Added:** 2026-10-21

### People can hear whether poured water is hot or cold
- **Source:** @velasco2013 (Velasco, Jones, King & Spence, 2013), *Journal of Sensory Studies* 28(5): 335–345, https://ora.ox.ac.uk/objects/uuid:9192d0b2-50bd-492c-9f83-dabc0732544d
- **Type:** peer-reviewed study
- **Evidence:** Three experiments. Listeners told hot from cold pours by sound across four cup materials, held implicit sound-temperature associations, and changed their temperature judgments when the sound's acoustics were altered. The authors name drink dispensers as an application.
- **For AquaNudge:** The pour sound can make the water seem colder and fresher, which supports sonifying the pour.
- **Affects:** ws: dsp
- **Confidence:** high
- **Added:** 2026-10-21

### Recognizable real-world sounds beat abstract tones as notifications
- **Source:** @garzonis2009 (Garzonis, Jones, Jay & O'Neill, 2009), CHI '09, doi:10.1145/1518701.1518932
- **Type:** peer-reviewed study
- **Evidence:** In two lab experiments, a field study and a web experiment, auditory icons (real-world sounds) beat earcons (abstract tones) on intuitiveness, learnability, memorability and preference.
- **For AquaNudge:** Use real water sounds as cues instead of synthetic beeps.
- **Affects:** ws: dsp
- **Confidence:** high
- **Added:** 2026-10-21

### Nature sound speeds stress recovery compared with traffic noise
- **Source:** @alvarsson2010 (Alvarsson, Wiens & Nilsson, 2010), *IJERPH* 7(3): 1036–1046, https://www.mdpi.com/1660-4601/7/3/1036
- **Type:** peer-reviewed study
- **Evidence:** 40 students recovered from a stress task with one of four sounds. Skin conductance recovered faster with a fountain plus birdsong at about 50 dB (half-life about 101 s) than with 80 dB traffic (about 160 s). That was the only significant difference, and heart rate variability showed no effect.
- **For AquaNudge:** Supports a fountain or birdsong approach cue at about 50 dB as calming.
- **Affects:** ws: dsp
- **Confidence:** medium
- **Added:** 2026-10-21

### Water sounds have the largest effect of any natural sound on health and positive affect
- **Source:** @buxton2021 (Buxton et al., 2021), *PNAS*, https://pmc.ncbi.nlm.nih.gov/articles/PMC8040792
- **Type:** review / meta-analysis
- **Evidence:** Across 18 studies, natural sounds improved health and positive affect (g = 1.63) and reduced stress and annoyance (g = −0.60). Water sounds had the largest effect on health and positive affect (g = 2.01). Bird sounds were best for stress, but that came from only 2 studies. Heterogeneity was high, and 61% of studies were in labs or hospitals.
- **For AquaNudge:** Water sounds are the best-supported base for a health-oriented soundscape, and they match Aqvita's brand.
- **Affects:** ws: dsp
- **Confidence:** high
- **Added:** 2026-10-21

### Music in a shop shifted wine choice without shoppers noticing
- **Source:** @north1999 (North, Hargreaves & McKendrick, 1999), *Journal of Applied Psychology* 84(2): 271–276; summary at https://thedecisionlab.com/fr-CA/intervention/how-in-store-music-increased-french-wine-sales-by-330
- **Type:** peer-reviewed study
- **Evidence:** On French music days the shop sold about 40 French vs 12 German wines. On German music days it sold 22 German vs 8 French. Only 1 of 44 surveyed shoppers named the music as the reason.
- **For AquaNudge:** Sound can prime a choice quietly, without being loud or explicit.
- **Affects:** ws: dsp
- **Confidence:** high
- **Added:** 2026-10-21

### An audible alert held hand-hygiene compliance at 90% or more; without it, compliance fell to about 74%
- **Source:** @webster2022 (Webster et al., 2022), *Infection Control & Hospital Epidemiology* 44(5), https://www.cambridge.org/core/journals/infection-control-and-hospital-epidemiology/article/automated-hand-hygiene-compliance-systems-audible-alert-reminder-increases-healthcare-worker-hand-hygiene-compliance/43F5C762E3626600109ABE4BB5144D84
- **Type:** peer-reviewed study
- **Evidence:** A 51-day on/off/on design across 9 inpatient units. Compliance held at 90% or more with the audible alert, fell to an average of 74% (62–78%) without it, and returned to 90% or more when the alert came back.
- **For AquaNudge:** The on/off/on (ABA) design is a model for our office study.
- **Affects:** ws: dsp, ws: eval-abet
- **Confidence:** high
- **Added:** 2026-10-21

### A motion-triggered audio reminder raised hand hygiene from 7.6% to 49.9%
- **Source:** @fakhry2012 (Fakhry, Hanna, Anderson, Holmes & Nathwani, 2012), *American Journal of Infection Control* 40(4): 320–321, https://healthdesign.org/sites/default/files/article-pdfs/Fakhry-et%20al-2012-CHD-KPS.pdf
- **Type:** peer-reviewed study
- **Evidence:** An eight-month pre/post study at ward entrances (706 actions before, 2,157 after). Overall compliance rose from 7.6% to 49.9%, and visitors rose from 10.6% to 63.7% (all p < .001).
- **For AquaNudge:** This is the closest example to our ToF plus sound idea: a proximity-triggered audio prompt at the point of use.
- **Affects:** ws: dsp, ws: sensing
- **Confidence:** high
- **Added:** 2026-10-21

### Piano Stairs claimed 66% more stair use, but it isn't a study
- **Source:** @funtheory2009 (Volkswagen Fun Theory, 2009), https://classicfm.com/discover-music/instruments/piano/musical-staircase-experiment
- **Type:** product (marketing campaign)
- **Evidence:** A marketing video claimed 66% more people took musical stairs than the escalator. It wasn't peer-reviewed.
- **For AquaNudge:** Cite as inspiration for playful sound nudges, not as evidence.
- **Affects:** ws: eval-abet
- **Confidence:** low
- **Added:** 2026-10-21
