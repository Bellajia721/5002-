# Final Exam — AI-Assisted Python Programming (Brief Summary)

> Generated on 2025-11-07. This README.md follows the brief‑summary guidance from the attached Word file.

> Detected requirement context (excerpt):
>
> ructure:
> final-exam-[yourname]/
> ├── Final_Exam.ipynb (main notebook)
> ├── conversation_log.txt
> ├── task_manager.py (if created separately)
> ├── weather_fetcher.py (if created separately)
> └── README.md (brief summary)
> Save to GitHub after completing each section
> Final submission: Share private repo with instructor GitHub account
> Tag final version as v1.0 using GitHub interface
> Notebook Cell Structure (Follow Course Standard)
> # Section X.Y - [Description]
> # Course constraint: [Week X concept being u
> ...
> pository structure:
> final-exam-[yourname]/
> ├── Final_Exam.ipynb (main notebook)
> ├── conversation_log.txt
> ├── task_manager.py (if created separately)
> ├── weather_fetcher.py (if created separately)
> └── README.md (brief summary)
> Save to GitHub after completing each section
> Final submission: Share private repo with instructor GitHub account
> Tag final version as v1.0 using GitHub interface
> Notebook Cell Structure (Follow Course Standard)
> # Section X.Y - [Description]
> # Course constraint: [Week X conc
> ...
> Time Management Guide
> Section 1: 45 minutes (Iterative Prompting)
> Section 2: 40 minutes (Debug & Correct)
> Section 3: 50 minutes (Debug & Refine)
> Section 4: 45 minutes (Implement & Reflect)
> Submission Requirements
> GitHub Repository Setup:
> Create private repository: final-exam-[yourname]
> Work in Google Colab with our standard course environment
> Repository structure:
> final-exam-[yourname]/
> ├── Final_Exam.ipynb (main notebook)
> ├── conversation_log.txt
> ├── task_manager.py (if created separately)
> ├── 
> ...
> ell to test your functions
> if __name__ == "__main__":
>     import doctest
>     doctest.testmod(verbose=True)
> GitHub Workflow:
> # To tag your final version (use GitHub web interface):
> # Go to your repo → Releases → Create new release → Tag: v1.0
> Academic Integrity Reminder:
> All course references must be authentic (we can verify)
> Code complexity must match your previous coursework
> 
> doctest examples should reflect Week 9 lab style
> AI interactions should show you constraining responses to course level
> 
> ...
> Setup:
> Create private repository: final-exam-[yourname]
> Work in Google Colab with our standard course environment
> Repository structure:
> final-exam-[yourname]/
> ├── Final_Exam.ipynb (main notebook)
> ├── conversation_log.txt
> ├── task_manager.py (if created separately)
> ├── weather_fetcher.py (if created separately)
> └── README.md (brief summary)
> Save to GitHub after completing each section
> Final submission: Share private repo with instructor GitHub account
> Tag final version as v1.0 using GitHub interf


## Overview
This repository contains my Final Exam deliverables for the introductory Python course. It demonstrates iterative prompt engineering, debugging with AI, basic API refinement, and a manual implementation constrained to Weeks 1–10 techniques (lists/dicts, simple functions, while‑loops, basic try/except, and simple file I/O).

## Repo Contents
- **Final_Exam.ipynb** — Main Colab notebook with all sections executed in order.
- **conversation_log.txt** — Short, structured prompts and AI responses per subsection, with course constraint checks.
- **task_manager.py** — Beginner‑friendly CLI Task Manager (fixed and rewritten in Section 2.2).
- **weather_fetcher.py** — refined_safe_weather_data_fetch() (Section 3.2) with basic error handling and friendly messages.
- **README.md** — This brief summary.

## Section Highlights
### Section 1 — Iterative Prompt Engineering (30%)
- Initial pseudocode and two refinements improving robustness (validation, duplicate checks, safe removal) and UX (clean menu, counts, exit confirm).
- ~150‑word analysis linking improvements to Week 3–6 concepts (user interaction; defensive programming).

### Section 2 — Debug & Correct with AI (25%)
- Error Identification for a broken task manager: naming/reference typos, range checks, negative index behavior, input conversion, unclear messages.
- Fix & Rewrite: task_manager.py using a list of dicts {'id': int, 'text': str}, while‑loop menu, simple file I/O, and try/except for int() and open().

### Section 3 — WeatherWise API (20%)
- Issue Analysis: bare except, missing status check, blind JSON assumptions, inconsistent returns, http vs https, unfriendly messages.
- Refined Function: refined_safe_weather_data_fetch(city) uses https, checks status code, basic json() handling, guarded key access, and prints beginner‑friendly errors.

### Section 4 — Manual Implementation & Reflection (25%)
- Manual (Week‑4/5/6‑only) Task Manager: in‑memory list[str], add/list/remove with simple validation and try/except for conversion, plus a minimal menu.
- Course‑Connected Reflection: planning before coding, loops/menus, defensive programming; how these shaped the final deliverables.

## How to Run
1. Open Final_Exam.ipynb in Google Colab (badge at the top of the notebook).
2. Run cells from top to bottom; each subsection includes notes and doctest examples.
3. (Optional) Run local scripts:
   
   ```bash
   python -m doctest -v task_manager.py
   python -m doctest -v weather_fetcher.py
   ```

## Submission & Release
- Ensure conversation_log.txt is UTF‑8 text, includes at least one prompt per required subsection, and sits alongside Final_Exam.ipynb and task_manager.py.
- Push to a private GitHub repo and create a Release tag (e.g., v1.0).

## Academic Integrity & AI Use
- Prompts and AI outputs are summarized in conversation_log.txt (5–10 lines per prompt), with explicit course constraint checks.
- All code confines itself to intro level techniques (Weeks 1–10) and avoids advanced patterns or libraries.

---

*If any required phrasing from the brief differs, please let me know and I will adapt this README wording to exactly match the Word file’s checklist.*
