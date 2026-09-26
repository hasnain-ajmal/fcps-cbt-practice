# FCPS-I CBT Practice Simulator

A Vite + React browser-based mock exam for practice. It is intentionally an independent Medicine + Paediatrics question bank and is **not official CPSP material**.

## Features
- 100 questions selected randomly from the built-in bank for each attempt
- One question at a time
- Five options A–E
- Previous questions can be reviewed from the right panel, but the normal forward flow does not allow returning to a question after moving on
- 120-minute countdown with auto-submit
- Finish early
- Score + answer explanations after submission
- Candidate name + local attempt history stored in browser localStorage
- Responsive desktop/mobile layout

## Run locally
```bash
npm install
npm run dev
```
Open the localhost URL printed by Vite.

## Deploy to Vercel
1. Create a GitHub repository and upload this folder.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Framework: Vite (Vercel normally detects it automatically).
4. Build command: `npm run build`
5. Output directory: `dist`
6. Deploy.

No API key or database is required.

## Important
The current app stores history in the browser only. That means each device/browser has its own history. If you want a central admin dashboard showing attempts from multiple candidates/devices, add Supabase (or another database) rather than relying on localStorage.

The question bank is educational content generated for practice. Have a qualified medical educator review questions/answers before relying on them for high-stakes preparation.

## Skipped-question review behavior

- Clicking Next without selecting an answer marks the question as **Skipped**.
- The question navigator lets you open a skipped question **once** for review.
- While reviewing a skipped question, the **Next question** button returns you to the forward question where you left off; it does not take you to the following question number.
- Other skipped questions remain available for one-time review, so you can move from Q3 to Q8 to Q17 by clicking them in the navigator.
- Answered questions cannot be reopened from the navigator.
