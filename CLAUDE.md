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
- **Work timer:** planning/drafting/writing slides — 5 and 10 min presets, start/pause/reset, runs across those slides, red near the end.
- **Coursebook videos:** no embedded video; show the book's questions plus an animated "play it on the website" placeholder.
- **Texts from earlier in the unit:** show the completed texts with page numbers, zoomable.
- **Click-to-zoom:** small magnifier on reading texts and photos; gap answers can be revealed by clicking the gap while zoomed. The zoomed view keeps the item's on-slide look (colours, crop) and always has a solid background — the item's own, else the colour behind it on the slide, else white; never transparent.

## REV (answer progression)
- Applies to activities with specific answers from the key (incl. "suggested" answers). Never to open activities or Claude-generated ideas. Applies to every warmer slide with reveals.
- Blank click / Space / → reveals the next hidden answer; when all show, advances.
- One answer per step, never several at once: drag-and-drop sorters/matches place one item per step (in reading order, with anything tied to it, e.g. its opposite); never wire REV to Check answers / Reveal all. ← hides the last revealed; with none revealed, goes back.
- Individual answers still toggle; progression skips opened ones. Bottom Next/Back always change slides immediately. Returning keeps answers as left.
- Non-REV slides: Space/arrows change slides; blank clicks do nothing.
- Highlighting text (drag-select, or double-click a word) never counts as a click: no reveal, no REV step, no slide change.

## PROVE (evidence window, Reading)
- Default for Exam-style question sections; ask for other Reading activities.
- Pop-up over the other questions, rest dimmed, question outlined.
- Multiple choice / matching (4 steps): answer paragraph + one red-herring paragraph in source order → distractor line light red → answer sentence yellow → window closes, answer with trimmed excerpt.
- Note-making / short answer (4 steps): answer paragraph → paraphrased part light blue → answer words yellow bold → answer with excerpt labelled by paragraph.
- Claude picks distractors; ask only if several are plausible. Reveal all skips windows; leaving mid-window resets that question.

## Vocabulary cards
- **CLUE:** 2-s hover (or 2-s press-and-hold on touch) opens an oversized card: short definition in large text + Vietnamese translation. CLUE words in plain dark green text — no highlight, no underline. Heading shows the base form ("appetites" → "appetite").
- **VISCLUE:** same trigger; large linked photo (freely licensed, e.g. Wikimedia Commons) + very short definition, no Vietnamese. Known words (pizza, banana) get no card.
- At the end of each build, list CLUE candidates for approval — never add automatically; skip the unit's target vocabulary.

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
- **Language sign:** faded England flag (St George's cross, SVG not emoji) next to 🎡. Click → enlarges to centre with "ENGLISH ONLY", glows ~1 s, then returns beside 🎡 keeping the flag + text (vivid); next click flips to Vietnamese flag + "ĐƯỢC DÙNG TIẾNG VIỆT". Clicking the enlarged sign switches it to the other language. Quick double click on the header sign → back to the faded England flag. Resets each slide. Not on warmers, games, quiz or Words from today.
- **COPY / NOTE pencil ✏️** beside ⏱ on book slides: 1st click "Copy into your notebook" strip, 2nd "Add ideas to your notebook", 3rd hides. No progress bar. Glows faintly once answers are revealed where copying fits; never appears by itself. Resets each slide.
- **Keys:** B blackout ("Eyes on me 👀" + looping shhh); W whiteout; 5 themed "5-MINUTE BREAK" timer (theme-specific countdown, sound + TIME'S UP at zero); 6 still "Break Time" image; P presenter view (second window: current + next slide, answers, notes, kept in step); ? shortcut sheet; Esc closes; 5/6/B/W switch directly.
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
- `?student` (all builds) and `?zh` (G9 only, never G10). Hide 🎡, ⏱, B/W, 5/6, language sign, COPY/NOTE. No warmer slides.
- **Title screen:** unit-opener photo on top (cut-outs shown whole on a soft gold-to-teal glow); teal band "› Unit X: Title", sections, pages, "▶ Start / Bắt đầu"; purple pill "HOME REVIEW · ÔN TẬP TẠI NHÀ · GRADE X"; "HOW TO USE THIS LESSON" + Vietnamese; one tile per student feature (icon, English title + instruction, Vietnamese in purple); "press ? for all shortcuts". Text fixed at 30px titles / 24px instructions — the photo shrinks, never the text; 9+ tiles → 5 columns.
- **Features:** VI toggle next to the page number (instructions into Vietnamese; book text and answers stay English); read-aloud (American accent, voice matches speaker, male by default; Slow/Normal; karaoke highlighting); Words from today as flip cards; Check your progress (tappable 1–5 + typed examples) — student versions only.
- `?zh`: Simplified Chinese replaces Vietnamese everywhere (toggle labelled 中文); no pinyin.

## GAMIFY
- Suitable exercises only: vocabulary and grammar; maybe short reading/writing; not listening, speaking or warmers.
- After a build, list each suitable exercise by slide number + activity number with 3 game options and styles; teacher approves one or skips. About 10 min; uses the exercise's correct answers. "Align to theme" = re-theme to the build's topic.
- Warmer-quality look, REV on reveals, notes off-screen, no "Open your book".
- Quiet corner button → slide deconstructs into the game's Start screen; overlay only (counter unchanged, slide returned as left). 🎮 in Contents; notes in presenter view.
- **Class mode:** team button (class → players per team via 2-s spinner, or "full"); Team A first, then alternate; the answering team glows brightly and wobbles; a small "Ready?" appears under the team that answers next (can be the same team after a steal), cleared when its turn starts; in-game spinner picks from the current team; rotation favours students who haven't played; absent swap (number teams only, not "full"): hovering a team name shows ✕, one click removes that student from that team for that game and a 2-s spin picks a replacement from students on neither team, preferring those who haven't played; ✓/✗ after every answer: ✓ adds a point to the answering team automatically (✓ again or ✗ takes it back), team pill click still adds a point and − beside each team takes one away; reveals centred and labelled; timers never auto-reveal.
- **Solo mode** (`?student` / `?zh`): no teams/spinners/scores/✓✗; one student answers on screen, auto-marked; score as a fraction; end screen lists misses with correct answers; Play again; bilingual how-to-play (Chinese for ?zh).
