# Lesson Template

`template.html` is the starting point for every new Lesson HTML build. Copy it into the new build's folder as `index.html`, then replace only what is unique to the build.

## Already built in (don't rewrite)
- **Page frame:** header (page badge, 🎡 roster picker, language sign, ✏️ COPY/NOTE pencil, ⏱ slide stopwatch, unit label) and bottom bar (Contents, Reveal all, Back, counter, Next).
- **Answers:** REV progression, click-to-reveal, Reveal all / Hide all, highlighting never counts as a click.
- **Interactive features:** drag-into-gap, sorters with Check answers, choice/vote buttons, phrase spotting, model-text summary loop, info-slide loops, work timer (10/15 min).
- **PROVE:** evidence windows for note-making answers (rows with class `evr`).
- **Vocabulary:** CLUE / VISCLUE cards (on every slide a word appears) and the automatic Words from today slide.
- **Keys:** B, W, 5, 6, C, O, T, P, ?, Esc. Also cover boxes, click-to-zoom and the offline-font notice.
- **Student versions:** `?student` and `?zh` with the title screen, VI/中文 toggle, read-aloud, flashcards and Check your progress (`stuOnly` slides).
- **End of deck:** the quiz engine.
- **EXPLAIN 💡:** the light-bulb engine — bulb (bottom-left, raised on audio slides; `data-xpl-pos="bl|br|tl|tr"` moves it), B1 panel (about · rule · examples · watch out), text auto-fit, Esc/outside click to close, presenter-view notes, ? sheet row, and in student versions the Vietnamese/Chinese lines, read-aloud and title tile.
- **GAMIFY:** the full engine — button, transition, teams, spinner, ✓/✗ marks, absent-student swap and solo mode.
- **Listening:** the audio module (audio bar, markers, auto-pause, "Hear it" clips, synced audioscript). It switches on when a slide has `data-audio="1"` and `LX_AUDIO` is set.

## Replace for every build
| What | Where |
|---|---|
| `<title>` and unit label | `<head>` and the header `unitlabel` |
| All sample slides | between the `TEMPLATE SAMPLE SLIDES` comment and the roster window |
| Rosters | `var ROSTERS`. Keep only this grade's classes. |
| Student title screen | `STUDENT_TITLE_PHOTO`, `STUDENT_TITLE` |
| Words from today | `LESSON_WORDS` |
| Presenter notes | `LESSON_NOTES` |
| EXPLAIN panels | `EXPLAIN_DATA` (one entry per slide Richard approved) + `data-xpl="<key>"` on that slide. Delete the sample entry. |
| Zoom / read-aloud targets | `LESSON_EXTRAS` |
| Quiz questions and style | `QUIZ`; quiz slide title. Change the quiz look to this build's random style. |
| 5/6 screens theme | `LX_THEME` and its CSS. The example is the judges' kitchen; make a new theme. |
| "Open your book" transition | `#bridge` markup and CSS. The example is the cloche; make a new design every build. |
| Warmers | new design every build. The sample warmer is only a placeholder. |
| GAMIFY games | `GAMIFY_DATA` plus a `GAMES.<key>` function per game. Reply Rally and Bento Planner are examples of the game interface. |
| Listening audio | add `<audio id="lxAudioEl">` and `var LX_AUDIO={…}` (see G10 U13 Section E). |

## Sample slides and the feature each shows
| Sample | Feature |
|---|---|
| Sample warmer (2 slides) | warmer + REV + `data-bridge` transition |
| C Writing: Review — Before writing | info-only slide with a looping plan |
| C The task | click-to-reveal answers |
| C2 Positive or negative adjectives? | sorter (drag into a table + Check answers) |
| C6 The opinion paragraph | drag-into-gap with a word bank |
| C9 The recommendation | phrase spotting |
| Language focus 3 | choice/vote buttons + GAMIFY button + EXPLAIN 💡 bulb (`data-xpl`) |
| C The complete sample review | model-text summary |
| C10 Plan your review | work timer (`data-timer="1"`) |
| Sample reading text + Sample notes | PROVE evidence windows (`data-text` names the text) |
| Students Speak | coursebook-video placeholder |
| Exam-style question | writing task + timer + GAMIFY |
| Self-check | tick-box self-check |
| Check your progress | student-only slide (`stuOnly`) |
| Section Quiz | end-of-deck quiz |

## Not yet in the template
- **PROVE for multiple choice / matching:** the 4-step window with a red-herring distractor isn't built in any build yet. Build it the first time it's needed, then add it here.

## Source
Built on 22 Oct 2026 from G9 Unit 3 Speaking (engine, tools, student versions, GAMIFY, audio), with sample slides from G9 Unit 3 Writing and evidence windows from the G10 Unit 13 exam build. When a shared feature changes, update this template as well as the builds.
