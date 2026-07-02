# THE BET — Complete Production Package for Text-to-Video Generation

**Film title:** THE BET
**Source:** Adapted from Anton Chekhov's short story "The Bet" (1889, public domain)
**Total runtime:** 30 minutes (1800 seconds) across 9 scenes
**Format:** Period drama, Imperial Russia, 1885–1900
**Principal cast:** 2 leads (PYOTR SEMYONOVICH VOLKOV, NIKOLAI ANDREYEVICH MOROZOV), 2 supporting (STEPAN, YEVGENY IVANOVICH ORLOV), 6 background party guests
**Locations:** 5 (Drawing Room; Garden Lodge with four dressed states; Study; Estate Garden; Estate Gate and Road)

## File Map

| File | Content | Produced by |
|---|---|---|
| `01_storyline.md` | Selected storyline, logline, full narrative summary, themes, 30-minute rationale | Agent 1 — Storyline Discovery |
| `02_script.md` | Section A: character guide (all 4 named characters + guests). Section B: complete 9-scene script with every line of dialogue, scene durations totaling 1800 s | Agent 2 — Screenwriter |
| `03_production_design.md` | Section A: costume design per character per scene, with change rationale. Section B: full set design for all 5 locations, including the lodge's four time-states (A: 1886, B: 1890, C: 1891–94, D: 1900) | Agent 3 — Production Designer |
| `04_directorial_breakdown.md` | Shot-by-shot breakdown of all 9 scenes: shot type, angle, lens/DoF, camera movement, framing, blocking, dialogue with performance notes, lighting, grade, per-shot duration, and transition. Shot durations sum to each scene's duration; scenes sum to 1800 s | Agents 4–12 — one Director Agent per scene, run in parallel |
| `scenes/scene_01.md` … `scenes/scene_09.md` | Per-scene source sections assembled into `04_directorial_breakdown.md` | Director Agents |

## Scene / Runtime Index

| # | Scene | Location | Duration |
|---|---|---|---|
| 1 | The Wager | INT. Volkov Mansion — Drawing Room — Night, 14 Nov 1885 | 240 s |
| 2 | Year One | INT. Garden Lodge (State A) — Day to Night, 1886 | 180 s |
| 3 | Year Five | INT. Garden Lodge (State B) — Night, 1890 | 150 s |
| 4 | The Hunger for Everything | INT. Garden Lodge (State C) / EXT. Garden — Day, 1891–94 | 210 s |
| 5 | The Banker's Arithmetic | INT. Volkov Mansion — Study — Night, 13 Nov 1900 | 240 s |
| 6 | Across the Garden | EXT. Estate Garden — Night, rain | 120 s |
| 7 | The Letter | INT. Garden Lodge (State D) — Night | 330 s |
| 8 | The Sleepless House | INT. Study — Night to Pre-Dawn | 120 s |
| 9 | Five Hours Early | INT. Study / EXT. Garden, Lodge, Gate & Road — Morning, 14 Nov 1900 | 210 s |
| | **Total** | | **1800 s = 30 min** |

## Rendering Notes for the Video Model

- Character and location name strings are identical across all four files; treat them as entity keys.
- Every shot in `04_directorial_breakdown.md` carries explicit duration (seconds) and an explicit transition-out; concatenating shots 1.1 → 9.final in order yields the full film.
- Costume/set continuity anchors to track across scenes: Volkov's gold signet ring (tight in 1885, loose in 1900); Morozov's black frock coat (worn in Scene 1, on the wall nail in Scenes 2–4, worn again in Scene 7, nail bare in Scene 9); the dried inkwell stain on the lodge table from Scene 3 onward; the 1885 portrait of Volkov (drawing room in Scene 1, study in Scenes 5–9); the letter (written Scene 7 era, read Scene 7, folded into the coat Scene 9, locked in the safe Scene 9).
