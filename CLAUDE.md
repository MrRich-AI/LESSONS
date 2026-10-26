# Lessons repo — Lesson HTML builds

Teacher-led, projected HTML slideshows of Cambridge IGCSE ESL coursebook unit activities, built from PDFs the teacher (Richard, Grade 9 & 10 ESL, Royal International School, Vietnam) provides. Answers are built in and revealed on click. Presented in class, then shared with students (via Google Classroom) for home review.

These are NOT student games: no name/class screen, no scoring submission, no data sent anywhere, no Try Again.

## Repo layout
- One folder per unit, by grade: `/G9/unit-03-food/index.html`, `/G10/unit-13-success-and-fame/index.html` (two-digit unit number, lowercase hyphenated name). A deck covering part of a unit may sit in a subfolder of the unit.
- Landing page with Unit buttons — add new builds to it.
- Classes: G9 = 9A1, 9A2, 9A3; G10 = 10A1. Roster nicknames are built into each file — copy them from the most recent build of the same grade and keep them easy to edit.

## Commits
- New build: always ask before the first commit.
- Edits to an existing build: commit without asking.
- Message format: `Add Lesson HTML: G9 Unit 3 Food (A, B1–5)` / `Update Lesson HTML: …` — always name the unit sections covered (the browser-tab `<title>` does too).
- Never commit API keys or other secrets.

## CONTROL (master copy of every shared feature; formerly the Lesson Template)
- `_shared/control/control.html` (README beside it) has every standard feature already working: header and bottom bar, REV, CLICK, reveals, sorters, drag-into-gap, choice buttons, phrase spotting, work timer (with "+1m"), PROVE note-making windows, CLUE/VISCLUE, Words from today, EXPLAIN, all teacher tools and keys, `?student` / `?zh`, the quiz engine, the GAMIFY engine and the listening module.
- **It is the master for every build in every Project.** Any build that uses a shared feature — Lesson HTML, INCLASS, RVW, or any other build type that uses only some features — takes that feature's code from the current CONTROL, not from an older build. The written rules describe how a feature behaves; CONTROL holds the code that does it.
- New Lesson build: copy CONTROL to the build's folder as `index.html`, then write only what's unique — book slides, answers, warmers, "Open your book" transition, 5/6 theme, quiz questions and style, GAMIFY games — and fill in the data blocks (rosters for this grade, title screen, words, notes, zoom/read-aloud targets, EXPLAIN panels). `_shared/control/README.md` lists every block to replace and which sample slide shows each feature.
- Don't rewrite the shared features from scratch.
- **Keep CONTROL current:**
  - **New rules / new shared features or fixes — always, no need to ask:** apply the same change to `_shared/control/control.html` (with a working sample if it's a new feature) and its README, add the rule here, and commit it together with the build change.
  - **Changes to an established rule — ask first:** ask Richard "Update CONTROL too?" before changing how an existing rule/feature works in CONTROL (and its wording here). Yes → apply and commit with the build change; No → CONTROL stays as it is.
  - Only things unique to one build stay out (its slides, answers, warmers, transition, 5/6 theme, quiz questions, games). If it's unclear whether a change is shared or build-only, ask Richard.

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
- **Standard layout** (from G9 Unit 3 Food): top — oversized page-number badge and unit label; bottom bar — Contents, current section/slide title, Reveal all, Back, slide counter, Next.
- **Navigation:** Next/Back, arrow keys, counter, Contents listing every slide (scrolls inside its window, opens with the current slide in view).
- **Answers:** each hidden until clicked individually, plus Reveal all / Hide all per slide. Open/discussion activities: bullet ideas or sample answers behind the reveal.
- **Images:** crop photos from the PDF, embed as base64, avoid parts with text printed over them. Rebuild text-heavy graphics (articles, gap-fill texts) as real HTML so answers reveal in place.
- **Delivery:** one self-contained HTML file.
- **Offline-font notice:** small dismissible notice if web fonts fail to load.
- **Click-to-pause:** every timer or countdown pauses/resumes when the timer itself is clicked.

## Checking (before delivering)
Render every slide at 1920×1080 (answers hidden and revealed). Confirm no overflow, every reveal works, Contents matches the slides. Screenshot-and-refine every warmer/non-book slide.

## Slide features
- **Interactive by default:** e.g. sorting → drag-and-drop with Check answers, not a static table.
- **Drag-into-gap:** word-bank gap fills; on reveal a correct guess turns green ✓, a wrong one is crossed out red and the correct word slides in. Clear button. Single-use banks grey out placed words; reusable banks stay available.
- **Choice buttons:** "A or B" items (however/although, true/false) get vote buttons; correct turns green, a wrong pick shakes red.
- **Phrase spotting:** "what phrase does the writer use…" → text split into clickable parts; wrong flashes red, right turns green and reveals.
- **Model-text summary slide:** when a section builds a sample text piece by piece, add a slide with the whole text, labelled parts and a looping highlight.
- **Information-only slides:** a looping animation that brings the content to life (e.g. plan steps lighting up in turn).
- **Subtle animations:** slow photo zoom, content rising in, small drifts/pulses on icons. Optional menu when suitable: flip reveals, typewriter sample answers, tick pop, highlight sweep, direction-aware slide changes, badge flip, underline draw, activity-number pop, photo parallax, hover glow, chip wiggle, drop bounce, Reveal-all cascade, paragraph spotlight.
- **Work timer:** planning/drafting/writing slides — 10 and 15 min presets, start/pause/reset, red near the end; a small "+1m" button adds 1 minute to the set time or while it counts down (also after Time's up). Once started it stays on screen on every slide, forward or back (small, time + pause + "+1m" only, away from the writing slides); ↺ ends that. Never covers slide content (move it to a free corner on a crowded slide).
- **Coursebook videos:** no embedded video; show the book's questions plus an animated "play it on the website" placeholder.
- **Texts from earlier in the unit:** show the completed texts with page numbers, zoomable.
- **Click-to-zoom:** small magnifier on reading texts and photos; gap answers can be revealed by clicking the gap while zoomed. The zoomed view keeps the item's on-slide look (colours, crop) and always has a solid background — the item's own, else the colour behind it on the slide, else white; never transparent.

## REV (answer progression)
- Applies to activities with specific answers from the key (incl. "suggested" answers). Never to open activities or Claude-generated ideas. Applies to every warmer slide with reveals.
- Blank click / Space / → reveals the next hidden answer; when all show, advances.
- One answer per step, never several at once: drag-and-drop sorters/matches place one item per step (in reading order, with anything tied to it, e.g. its opposite); never wire REV to Check answers / Reveal all. ← hides the last revealed; with none revealed, goes back.
- Individual answers still toggle; progression skips opened ones. Bottom Next/Back always change slides immediately. Returning keeps answers as left.
- Non-REV slides: Space/arrows change slides; blank clicks do nothing — unless CLICK applies (below).
- Highlighting text (drag-select, or double-click a word) never counts as a click: no reveal, no REV step, no slide change.

## CLICK (step-through for everything REV skips)
- **Default** on every slide where pressing Next would change the slide while something is still waiting to be revealed or played: play buttons / audio, open-activity and Claude sample answers, warmer reveals and cards. Not optional pop-ups (GAMIFY, EXPLAIN, zoom, CLUE cards, teacher tools).
- **Same triggers as REV:** blank click / Space / → = next step; ← undoes the last step (hides it, or stops it and marks it unplayed); with none done, ← goes back a slide. When every step is done, the next step changes slide. Bottom Next/Back always change slides immediately. Ignored while an overlay or the "Open your book" transition is showing.
- **One step at a time,** in reading order or the order the presenter notes describe. On slides that also have REV answers, CLICK and REV share one sequence (e.g. play each option → reveal the answer → play the record speed → reveal the card).
- **Audio:** a click while something is playing stops it and does the next step (plays the next option or reveals the next item). Leaving the slide stops audio.
- **By hand still works:** anything revealed or played by hand counts as done and is skipped. Returning to a slide keeps it as left.
- **Markup:** `data-click="1"` on the slide; `data-step="1"`, `"2"`, … on each play button or revealable, in order.

## PROVE (evidence window, Reading)
- Default for Exam-style question sections; ask for other Reading activities.
- Pop-up over the other questions, rest dimmed, question outlined.
- Multiple choice / matching (4 steps): answer paragraph + one red-herring paragraph in source order → distractor line light red → answer sentence yellow → window closes, answer with trimmed excerpt.
- Note-making / short answer (4 steps): answer paragraph → paraphrased part light blue → answer words yellow bold → answer with excerpt labelled by paragraph.
- Claude picks distractors; ask only if several are plausible. Reveal all skips windows; leaving mid-window resets that question.

## Vocabulary cards
- **CLUE:** 2-s hover (or 2-s press-and-hold on touch) opens an oversized card: short definition in large text + Vietnamese translation. CLUE words in plain dark green text — no highlight, no underline. Heading shows the base form ("appetites" → "appetite").
- **VISCLUE:** same trigger; large linked photo (freely licensed, e.g. Wikimedia Commons) + very short definition, no Vietnamese. Known words (pizza, banana) get no card.
- A CLUE/VISCLUE word gets its card on every book slide it appears on (first appearance per slide), not just the first slide.
- At the end of each build, list CLUE candidates for approval — never add automatically; skip the unit's target vocabulary.

## EXPLAIN (rule/pattern explainer)
- **What it is:** a light-bulb button that opens a B1-level explanation of the slide's content and the English rule or pattern behind it, based on the slide and standard English rules/guidelines.
- **Criteria:** a book slide whose activity depends on an English rule or pattern (grammar, word formation, collocations, linking words, punctuation, text organisation, register, exam strategy) that the book doesn't clearly state or name on that slide. Not for warmers, games, open discussion with no pattern, or slides where the book already explains the rule in full.
- **Ask first:** whenever Claude finds a slide that meets the criteria (before building, or while editing an existing build), list it by slide number + activity number with a one-line summary of the rule and ask Richard whether to include it. Never add it automatically.
- **Icon:** a classic glowing light bulb, code-drawn SVG (glass bulb, zigzag filament, screw base, glass highlight, gently pulsing rays). No text, no emoji. Never faded. A slight continuous wobble that pauses on hover. Placed in a free corner: bottom-left just above the bottom bar by default (GAMIFY uses bottom-right); if that corner is taken on a slide, use the nearest free corner. Never covers slide content.
- **Panel:** click opens a large pop-up over the dimmed slide, readable from the back of the room. B1 English: short sentences, common words, grammar terms only when needed and explained. Four parts: (1) **What this slide is about** — one line; (2) **The rule / pattern** — 2–4 sentences; (3) **Examples** — 2–3 examples with the pattern highlighted; (4) **Watch out!** — one common mistake with the correction.
- **No spoilers:** never shows hidden answers. Use the book's own example items, items already completed in the book, or new examples of the same pattern.
- **Behaviour:** close with the bulb, a click outside, or Esc; opening/closing never triggers REV or changes the slide; closes on slide change. Listed in the ? sheet; shown in presenter view.
- **Student versions:** the bulb appears in `?student` with the Vietnamese under each part (Chinese only in `?zh`), plus read-aloud on the panel and a title-screen tile.

## Warmers and non-book slides
- Never the word "Warmer" on slides; teacher instructions never on slides; no page badge.
- Go first (or before a later section if asked). Energetic, kinetic, very different from book slides.
- Every set gets a new design — never reuse an earlier set's look.
- Premium visuals: layered depth, realistic lighting/shadows/textures, particle/light effects, real photos combined with detailed SVG/canvas art; never flat shapes or emoji as main graphics; smooth on a classroom PC.
- Recap / "choose one" cards repeat each option's details, not just its name.
- **"Open your book" transition** (warmer → book slides): "Open your book | › [unit or page]", skippable, a new animation every build (used: crickets + book; 3D book on a desk; silver cloche).

## Teacher tools (teacher version)
- **Roster picker 🎡** next to the page badge (bottom margin on warmers). First click asks which class (skipped if only one or a class was already chosen anywhere in the file); "Change class" beside the class name. 2-s scroll-and-slow pick with digital ticking (no mute); name enlarges/glows, window fades, name stays by the icon until clicked or slide change. Picked students left out of later picks; no absentee feature.
- **Slide stopwatch ⏱** left of the unit title: 1, 2, 3, 4, 5, 7.5, 10, 12, 15 min; glowing display, click to start/pause; last 10% red pulse (silent); at zero a random sound 3 s and TIME'S UP (flashes 3 s, then stays until clicked); cleared on slide change. Sound pool, never the same twice in a row: digital alarm, game-show buzzer, boxing bell, 8-bit jingle, gong, school bell, arcade fanfare, spaceship alert, xylophone run, air horn, cuckoo clock, drum roll + cymbal, train whistle, doorbell, laser zaps, wind chimes, sad trombone.
- **Language sign:** faded England flag (St George's cross, SVG not emoji) next to 🎡. First click → straight to the Vietnamese flag + "ĐƯỢC DÙNG TIẾNG VIỆT": enlarges to centre, glows ~1 s, then returns beside 🎡 keeping the flag + text (vivid); next click flips to the England flag + "ENGLISH ONLY", then back and forth. Clicking the enlarged sign switches it to the other language. Quick double click on the header sign → back to the faded England flag. Resets each slide. Not on warmers, games, quiz or Words from today.
- **COPY / NOTE pencil ✏️** beside ⏱ on book slides, faded until used: 1st click "Copy into your notebook" strip, 2nd "Make your notes. Only key words/phrases", 3rd "Add ideas to your notebook", 4th hides. The strip glows, pulses and wobbles slightly while it shows; press and hold, then drag, to move it anywhere on the screen (stays there for that slide); on audio slides it sits above the audio bar. No progress bar. Glows faintly once answers are revealed where copying fits; never appears by itself. Resets each slide.
- **Keys:** B blackout ("Eyes on me 👀" + looping shhh); W whiteout; 5 themed "5-MINUTE BREAK" timer (theme-specific countdown, sound + TIME'S UP at zero); 6 still "Break Time" image; O replays the build's "Open your book" transition (label: this page, or the first book page from a warmer) without changing the slide; T "TIME'S UP" (one of 4 loud but gentle buzzers, never the same twice in a row, + glowing digital TIME'S UP in the slide-timer style; flashes 3 s, stays until click / T / Esc; doesn't change the slide); P presenter view (second window: current + next slide, answers, notes, kept in step); ? shortcut sheet; Esc closes; 5/6/B/W/C/T switch directly.
- **C — Close your books:** top-down wooden desk; the open blue book swings shut with a paper-dust puff, pencil rolls, sticky note flutters, eraser hops, the closed book slides off the desk, a card drops in and CLOSE YOUR BOOKS stamps onto it in red with a small screen shake; synthesised sounds. Click during the animation skips to the stamp; click / C / Esc wipes it away back to the slide. Same animation in every build: paste `_shared/close-your-books/snippet.html` before `</body>` and add its Anton font link to `<head>` (it mounts on `#stage` and registers itself in `window.LX_SCREENS`; `demo.html` shows it stand-alone). Teacher only; add C to the ? sheet.
- **First screen:** shown still and dimmed until clicked, no prompt text.
- **Cover boxes:** hold the right mouse button and drag to draw a solid white box over part of the slide (browser right-click menu disabled in the slideshow); several allowed; left-click a box to remove it; never triggers REV; cleared on slide change. Shift + left-drag (mouse, pen or touch) also draws, for whiteboards. In the ? sheet.

## End of deck
- **Words from today:** every CLUE/VISCLUE word with definition, plus words from vocabulary exercises.
- **Quiz (both versions):** 8–10 multiple choice with a score; style random from game show / arcade neon / exam-hall clean / quiz-app. Vocabulary and language focus only; for reading/listening test the strategies, not content; speaking = conversation starter + best reply; never warmers or copied models. Listening builds add "Listen & spell" items.

## Listening builds
- Audio embedded. Full-width audio bar above the bottom margin, only on audio slides: play/pause, back 10 s/5 s, draggable track, time, 0.75×/1×. Stops when leaving. Space plays/pauses there.
- Toggles: answer markers on the bar (click = play from just before), auto-pause after each answer.
- "Hear it" clip with each reveal (sentence before + answer sentence).
- Synced audioscript slide (highlights as it plays; click a sentence to play from there).
- Word-in-context clips only on Words from today.

## Student versions (same file)
- `?student` (all builds) and `?zh` (G9 only, never G10). Hide 🎡, ⏱, B/W, 5/6, C, T, language sign, COPY/NOTE. No warmer slides.
- **Title screen:** unit-opener photo on top (cut-outs shown whole on a soft gold-to-teal glow); teal band "› Unit X: Title", sections, pages, "▶ Start / Bắt đầu"; purple pill "HOME REVIEW · ÔN TẬP TẠI NHÀ · GRADE X"; "HOW TO USE THIS LESSON" + Vietnamese; one tile per student feature (icon, English title + instruction, Vietnamese in purple); "press ? for all shortcuts". Text fixed at 30px titles / 24px instructions — the photo shrinks, never the text; 9+ tiles → 5 columns.
- **Features:** VI toggle next to the page number (instructions into Vietnamese; book text and answers stay English); read-aloud (American accent, voice matches speaker, male by default; Slow/Normal; karaoke highlighting); Words from today as flip cards; Check your progress (tappable 1–5 + typed examples) — student versions only.
- `?zh`: Simplified Chinese replaces Vietnamese everywhere (toggle labelled 中文); no pinyin.

## GAMIFY
- Suitable exercises only: vocabulary and grammar; maybe short reading/writing; not listening, speaking or warmers.
- After a build, list each suitable exercise by slide number + activity number with 3 game options and styles; teacher approves one or skips. About 10 min; uses the exercise's correct answers. "Align to theme" = re-theme to the build's topic.
- Warmer-quality look, REV on reveals, notes off-screen, no "Open your book".
- Quiet corner button (faded in the teacher version; in student versions never faded, with a slight glow and wobble) → slide deconstructs into the game's Start screen; overlay only (counter unchanged, slide returned as left). 🎮 in Contents; notes in presenter view.
- **Class mode:** team button (class → players per team via 2-s spinner, or "full"); Team A first, then alternate; the answering team glows brightly and wobbles; a small "Ready?" appears under the team that answers next (can be the same team after a steal), cleared when its turn starts; in-game spinner picks from the current team; rotation favours students who haven't played; absent swap (number teams only, not "full"): hovering a team name shows ✕, one click removes that student from that team for that game and a 2-s spin picks a replacement from students on neither team, preferring those who haven't played; ✓/✗ after every answer: ✓ adds a point to the answering team automatically (✓ again or ✗ takes it back), team pill click still adds a point and − beside each team takes one away — scores can go below 0 (negative scores show with a real minus sign, readable on any team colour); reveals centred and labelled; timers never auto-reveal.
- **Solo mode** (`?student` / `?zh`): no teams/spinners/scores/✓✗; one student answers on screen, auto-marked; score as a fraction; end screen lists misses with correct answers; Play again; bilingual how-to-play (Chinese for ?zh).
