# G9 Unit 4 Transport (A, B1–6, C1–4) — Step 1 (chat) → Step 2 (Claude Code)

Step 1 files (this folder): `head.html` (build CSS + fonts), `slides.html` (slides, build-only early scripts, data blocks), `body-end.html` (build scripts).
Step 2 writes `G9/unit-04-transport-a-c/index.html` — do not edit the Step 1 files except to fix bugs.

## Assemble (from SHARED, current code)
```
python3 tools/assemble.py --frame lesson \
  --modules activities/drag-into-gap,activities/choice-buttons,features/clue-visclue,features/explain,features/gamify,features/prove,activities/evidence-window,features/quiz,features/words-from-today,student \
  --head <LESSONS>/G9/unit-04-transport-a-c/step1/head.html \
  --slides <LESSONS>/G9/unit-04-transport-a-c/step1/slides.html \
  --body-end <LESSONS>/G9/unit-04-transport-a-c/step1/body-end.html \
  -o <LESSONS>/G9/unit-04-transport-a-c/index.html
```

## Wire
- `<title>`: "G9 Unit 4: Transport (A, B1–6, C1–4)"; unit label "Unit 4: Transport"; G9 rosters.
- Slides already use the names CONTROL reads: `data-rev="1"` + `.ans` / `.ans-ph`, `data-click` + `data-step`, `data-copy`, `data-timer`, `.gbank` / `.gap`, `.hvrow` / `.hvote`, `data-bridge`, `data-xpl`, `data-game`.
- Data blocks → globals: `clue-data` (wrap first appearance on C3; repeats on C4's completed text), `explain-data` → `EXPLAIN_DATA` (C2 `superlatives`, C3 `passive-text`, with vi / zh), `quiz-data`, `words-data`, `notes-data` → `LESSON_NOTES`, `student-title-data` → `STUDENT_TITLE` (+ `STUDENT_TITLE_PHOTO` = `#openerPhoto img`; its warmers selector keeps `.keepstu`: Customs control and A1 stay in ?student / ?zh).
- PROVE (approved: C1 a and c; C3 no): the multiple-choice evidence window is **not built in SHARED yet** — build it in features/prove + activities/evidence-window (code, README, demo, same commit) from `prove-data`. Rows: `.hvrow[data-prove-key]` on C1; paragraphs `#text41 p[data-p]`, `data-text="Text 4.1"`.
- GAMIFY (approved): build `GAMES.customs` (B3 "Customs Sort") and `GAMES.airship` (C2 "Airship Drop") from `gamify-data`, class + solo versions, Passivania poster look.
- Zoom targets: `#text41` (C3), `#text41done` (C4, completed Text 4.1, p. 52), the photos.

## Build-only code (keep; not shared features)
B3 multi-column sorter (words in several columns; one column per REV step; Check answers / Clear), warmer video + scream, Passivania poster scenes (`PV_SCENE`), flying-car card art, split-flap "Open your book" board (`#bridge`), 5/6 theme "The Passivania Express" (`LX_THEME`). `PV_SCENE` + `LX_THEME` sit at the end of `slides.html` on purpose: they must run before the SHARED engine and screens-5-6 code.

## Then
- Add the build to the LESSONS landing page (G9 → Unit 4).
- Render-check every slide at 1920×1080 (hidden + revealed), games, windows, student versions; no console errors.
- Commit: `Add Lesson HTML: G9 Unit 4 Transport (A, B1–6, C1–4)` (no raw HTML in chat or commit).
