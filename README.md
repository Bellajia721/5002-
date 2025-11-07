# Final_Exam – Brief Summary

This repository contains my final assessment for the introductory Python course. It demonstrates **iterative prompt engineering**, **beginner‑level debugging and corrections**, a **refined HTTP/JSON function with basic error handling**, and a **manual CLI mini‑app** built only with Week 1–10 concepts.

## Files
- **Final_Exam.ipynb** — Full write‑up with prompts, pseudocode, analyses, and code cells.
- **task_manager.py** — Beginner‑friendly CLI Task Manager (add/list/remove, simple file I/O).
- **conversation_log.txt** — Short logs of prompt iterations per exam section (as required).

## Section Overview
### Section 1 — Iterative Prompt Engineering (30%)
- **1.1** Initial prompt + **modular pseudocode** for a CLI Task Manager using only lists/dicts, loops, and basic try/except.
- **1.2** Two refinements:
  - Robustness: blank/duplicate titles, safe removals, blank filenames, gentle recovery.
  - UX: clean `show_menu()`, “Your Tasks (N)”, concise save/load messages, exit confirm.

**Outcome:** Shows how successive prompts improve **defensive programming**, **control‑flow clarity**, and **user experience**.

### Section 2 — Debug & Correct with AI (25%)
- **2.1** Error list for a flawed beginner script: name/iterable typos, negative index behavior, 0‑ vs 1‑based mismatch, missing conversions, unclear messages.
- **2.2** **Rewritten `task_manager.py`**:
  - Data model: `tasks = [{"id": int, "text": str}]` + incremental `next_id`.
  - Safe input conversion, range checks, duplicate/empty validation.
  - Simple, robust file I/O (`save_tasks`, `load_tasks`) using `try/except` and UTF‑8.
  - Clear CLI loop and messages, with 1‑based list display.

### Section 3 — WeatherWise API Refinement (20%)
- **3.1** Issue analysis (bare `except`, no status check, JSON/key assumptions, inconsistent return, http vs https, etc.) linked to course weeks.
- **3.2** **`refined_safe_weather_data_fetch(city)`**:
  - Uses **https**, checks `status_code`, basic `try/except`, `dict.get` + type/length checks.
  - Returns `dict` or `None` with friendly prints; includes doctest‑style examples.
- **3.3** Comparison: similarities (intro error handling), differences (explicit guards), improvement note (document function contract).

### Section 4 — Manual Implementation & Reflection (25%)
- **4.1** Minimal CLI (Week 4–6 scope): in‑memory list of strings + add/list/remove with safe `int()` conversion and boundary checks; simple menu.
- **4.2** Reflection: where course concepts (Weeks 3–8) shaped validation, UX, and graceful failure; plan to document function contracts and returns.

## How to Run
### Task Manager (beginner CLI)
```bash
python task_manager.py
```
Menu:
1. Add task
2. List tasks
3. Remove task (by shown number, 1‑based)
4. Save tasks to file
5. Load tasks from file
6. Quit

- Saves as TSV lines: `id\ttext`
- Handles blank/duplicate titles, bad numbers, missing files.

### Notebook
Open **Final_Exam.ipynb** in Jupyter/Colab to view prompts, pseudocode, analyses, and examples.

## Tested Concepts (Course Mapping)
- **Week 3–5**: menu loops, clean prompts, guard clauses.
- **Week 6**: defensive programming, simple `try/except`, input validation.
- **Week 8**: JSON access via `get` and length/type checks.
- **Week 9–11 (light)**: http→https choice and basic status checks (kept at beginner level).

## Academic Notes
- Beginner scope only (lists/dicts, loops, prints, basic file I/O, basic `try/except`).
- No advanced libraries, no custom exceptions, no async/OO required.
