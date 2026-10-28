# Lessons repo — Lesson HTML builds

Teacher-led, projected HTML slideshows of Cambridge IGCSE ESL coursebook unit activities, built from PDFs the teacher (Richard, Grade 9 & 10 ESL, Royal International School, Vietnam) provides. Answers are built in and revealed on click. Presented in class, then shared with students (via Google Classroom) for home review.

These are NOT student games: no name/class screen, no scoring submission, no data sent anywhere, no Try Again.

## Pending (remind Richard at the start of the next session)
- Roll out CLICK to all builds (so far only G10 Unit 13 Exam slides 1–2 and G9 Unit 3 Speaking slide 14 use it; CONTROL has it). Remove this line once done.

## Repo layout
- One folder per unit, by grade: `/G9/unit-03-food/index.html`, `/G10/unit-13-success-and-fame/index.html` (two-digit unit number, lowercase hyphenated name). A deck covering part of a unit may sit in a subfolder of the unit.
- Landing page with Unit buttons — add new builds to it.
- Classes: G9 = 9A1, 9A2, 9A3; G10 = 10A1. Roster nicknames are built into each file — copy them from the most recent build of the same grade and keep them easy to edit.

## Commits
- New build: always ask before the first commit.
- Edits to an existing build: commit without asking.
- Message format: `Add Lesson HTML: G9 Unit 3 Food (A, B1–5)` / `Update Lesson HTML: …` — always name the unit sections covered (the browser-tab `<title>` does too).
- Never commit API keys or other secrets.

## SHARED (master code for every shared feature; replaces CONTROL)
- The master code for every shared feature is the **SHARED** repo (mrrich-ai/SHARED), not `_shared/control/control.html`. Every Lesson HTML build takes shared code from SHARED, never from an older build or from `_shared/control/` (frozen as it was on 26 Oct 2026; old builds are updated only when they are edited).
- Each shared feature's full rules are in its SHARED module README (pointers below). This file keeps only what is unique to Lesson HTML builds. Frame: `lesson` (SHARED/control/variants/README.md).
- Whenever a shared feature is added or changed, update the module code, README and demo in SHARED in the same commit (SHARED/WORKFLOW.md, SHARED/CLAUDE.md).

## Workflow: Step 1 (chat) and Step 2 (Claude Code)
Full workflow: SHARED/WORKFLOW.md. Tags and data blocks: SHARED/TAGGING.md.
- **Step 1 (chat): the main build only.** Unique slides (book slides, answers, warmers, "Open your book" transition, 5/6 theme), the tags and JSON data blocks from SHARED/TAGGING.md, and space reserved for the CONTROL frame. Ends with **one combined approval list**: CLUE candidates, EXPLAIN slides, GAMIFY options, PROVE for non-exam Reading. The quiz, Words from today and PROVE on Exam-style question sections are automatic.
- **Step 2 (Claude Code)**, triggered by "Add CONTROL and approved FEATURES to <path>": copy the current code from SHARED (never from older builds); wire it to the tags and data blocks; build each GAMIFY game from `gamify-data` on top of the GAMIFY engine, class and solo versions, following the GAMIFY rules; render-check at 1920×1080; commit with no raw HTML pasted.

## Before building
1. Read every page of the PDF.
2. Ask if the unit title or grade isn't clear.
3. Work out the answers. List any that are ambiguous, depend on material not in the PDF (audioscripts, appendices, videos) or have several acceptable answers. Ask for the key for those activities and wait. Never guess.
4. Ask first if how to present an activity is unclear.
5. Always suggest warmer options, even if not asked; the teacher decides.
6. Before building any warmer or non-book slides, present a menu of named visual styles (cinematic photo, 3D game show, premium flat illustration, painterly canvas, a look inspired by a show/app/game students know, etc.) with short descriptions. Wait for a pick.
7. Reading activities: ask whether each needs PROVE (default only for Exam-style question sections).
8. Listening builds: get the answer key and audioscript first.
9. If a request clashes with these rules, ask before building.
10. EXPLAIN: list every slide that meets the EXPLAIN criteria (see below) with a one-line summary of its rule/pattern, and ask Richard which to include. Never add EXPLAIN without asking.

## Base rules
- **Style:** match the book (colours, section letters, activity numbering, coloured word boxes, tip/reflection boxes, tables). Book-page slides keep the same format build to build.
- **Branding:** remove all Cambridge IGCSE branding, incl. the running header "CAMBRIDGE IGCSE™ ENGLISH AS A SECOND LANGUAGE: COURSEBOOK".
- **Page numbers:** kept, enlarged, on every book slide.
- **Screen:** 16:9, everything on one projected screen, no scrolling, high contrast, readable from the back of the room.
- **Font size:** as large as the slide allows with no overflow, especially revealed answers. If a slide is dense, rearrange (e.g. instructions strip on top, text full width) rather than shrink.
- **Slides:** one activity per slide unless the book links activities (e.g. a text and its questions).
- **Standard layout, navigation, reveals (Reveal all / Hide all), offline-font notice, click-to-pause:** see SHARED/control/README.md.
- **Answers:** open/discussion activities: bullet ideas or sample answers behind the reveal.
- **Images:** crop photos from the PDF, embed as base64, avoid parts with text printed over them. Rebuild text-heavy graphics (articles, gap-fill texts) as real HTML so answers reveal in place.
- **Delivery:** one self-contained HTML file.

## Checking (before delivering)
Render every slide at 1920×1080 (answers hidden and revealed). Confirm no overflow, every reveal works, Contents matches the slides. Screenshot-and-refine every warmer/non-book slide.

## Slide features
- **Interactive by default:** e.g. sorting → drag-and-drop with Check answers, not a static table.
- **Drag-into-gap:** see SHARED/activities/drag-into-gap/README.md.
- **Choice buttons:** see SHARED/activities/choice-buttons/README.md.
- **Phrase spotting:** see SHARED/activities/phrase-spotting/README.md.
- **Sorters (drag-and-drop with Check answers):** see SHARED/activities/sorter/README.md.
- **Model-text summary slide:** when a section builds a sample text piece by piece, add a slide with the whole text, labelled parts and a looping highlight.
- **Information-only slides:** a looping animation that brings the content to life (e.g. plan steps lighting up in turn).
- **Subtle animations:** slow photo zoom, content rising in, small drifts/pulses on icons. Optional menu when suitable: flip reveals, typewriter sample answers, tick pop, highlight sweep, direction-aware slide changes, badge flip, underline draw, activity-number pop, photo parallax, hover glow, chip wiggle, drop bounce, Reveal-all cascade, paragraph spotlight.
- **Work timer:** see SHARED/control/README.md (Lesson presets 10 and 15 min).
- **Coursebook videos:** no embedded video; show the book's questions plus an animated "play it on the website" placeholder.
- **Texts from earlier in the unit:** show the completed texts with page numbers, zoomable.
- **Click-to-zoom:** see SHARED/control/README.md.

## REV (answer progression)
- See SHARED/control/README.md.

## CLICK (step-through for everything REV skips)
- See SHARED/control/README.md.

## PROVE (evidence window, Reading)
- See SHARED/features/prove/README.md (window: SHARED/activities/evidence-window/README.md).

## Vocabulary cards
- CLUE / VISCLUE: see SHARED/features/clue-visclue/README.md.

## EXPLAIN (rule/pattern explainer)
- See SHARED/features/explain/README.md.

## Warmers and non-book slides
- Never the word "Warmer" on slides; teacher instructions never on slides; no page badge.
- Go first (or before a later section if asked). Energetic, kinetic, very different from book slides.
- Every set gets a new design — never reuse an earlier set's look.
- Premium visuals: layered depth, realistic lighting/shadows/textures, particle/light effects, real photos combined with detailed SVG/canvas art; never flat shapes or emoji as main graphics; smooth on a classroom PC.
- Recap / "choose one" cards repeat each option's details, not just its name.
- **"Open your book" transition** (warmer → book slides): "Open your book | › [unit or page]", skippable, a new animation every build (used: crickets + book; 3D book on a desk; silver cloche).

## Teacher tools (teacher version)
- Roster picker 🎡, slide stopwatch ⏱, language sign, COPY / NOTE pencil ✏️, keys (B, W, 5, 6, O, T, P, ?, Esc), C — Close your books, first screen, cover boxes: see SHARED/control/README.md (C: SHARED/control/close-your-books.html).

## End of deck
- **Words from today:** see SHARED/features/words-from-today/README.md.
- **Quiz (both versions):** see SHARED/features/quiz/README.md.

## Listening builds
- See SHARED/features/listening/README.md.

## Student versions (same file)
- See SHARED/student/README.md.

## GAMIFY
- See SHARED/features/gamify/README.md (the engine; each approved game is built per lesson in Step 2).
