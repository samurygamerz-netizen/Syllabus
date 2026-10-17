# Maths Basics Zero — Antigravity One-Shot Build Prompt

You are Antigravity acting as a senior full-stack engineer, product designer, AI tutoring specialist, and QA engineer. Your job is to **build the working Maths Basics Zero application in this repository**, not merely describe a plan. Work autonomously using sensible defaults, inspect the existing code first, implement the best complete vertical slice you can, and verify it.

## Before implementation: enhancement choice
First inspect the repository and identify its current stack, app state, and any existing requirements. If you identify a genuinely important enhancement, architectural choice, or missing user decision that would materially change the result, **ask me a concise, specific question and wait for my answer before making that decision**. Offer practical options and explain the consequence briefly. Do not ask about minor details; use sensible defaults for those and continue. If no important decision is blocked, proceed immediately. Do not repeatedly ask for permission for ordinary implementation steps.

## Product
Build **Maths Basics Zero**, a responsive, mobile-first AI-powered maths learning platform for learners from absolute beginners through advanced/exam level. It should work well on Android phones, tablets, and desktop.

### Learners and teaching style
- Default teaching language: simple **Hinglish in Roman script**; allow English as an option.
- Tone: friendly and conversational, beginner-friendly, with exam-focused practice.
- Audience: everyone, from foundational learners to university students and competitive-exam candidates.
- Priority pathways: B.Sc. at Guru Jambheshwar University of Science and Technology (GJUST), Hisar; SSC; CAT; and government-job exams.
- Maths is the core subject. Related study modules may include Physics, Computer Science, Chemistry, Physical Education, EVS, and English.
- **Never invent GJUST's current official syllabus, paper codes, unit names, exam dates, or rules.** Use an official syllabus file/link supplied by me, store source/session information, and mark anything not verified.

## Core user experience
Implement these connected, functional areas:
1. Onboarding: learning goal, current level, language, exam target, daily study time.
2. Student accounts: sign-up, sign-in, sign-out, profile/preferences, and private per-user progress.
3. Dashboard: continue learning, daily goal, progress, weak areas, revision due, and recommended next step.
4. Curriculum explorer: structured topics, prerequisites, difficulty levels, and learning paths.
5. Lessons: objective, short explanation, worked example, learner attempt, feedback, summary, and next step.
6. Practice: MCQ, numeric response, short answer, progressive difficulty, hints, solutions, timed practice, and review.
7. AI tutor: contextual chat, graduated hints, misconception detection, prerequisite reteaching, alternate explanations, and generated practice.
8. Progress: accuracy, attempts, mastery by topic, study time where available, revision queue, and useful recommendations.
9. Exam preparation: separate GJUST, SSC, CAT, and government-exam paths. Keep official previous-year questions distinct from AI-generated questions; cite sources for anything called official.
10. Syllabus import workflow: accept an official PDF/source, extract unit headings and page references, let me review the extraction, and preserve provenance and academic session.
11. Settings and helpful loading, empty, error, offline, success, and demo-mode states.

## Initial maths roadmap
Use structured editable data with prerequisites. Begin with number sense, integers, factors/multiples, fractions, decimals, percentages, ratio/proportion, operations/BODMAS, powers/roots, averages, profit/loss/discount/interest, algebra, equations, polynomials, exponents/logarithms, sequences, sets/functions/graphs, geometry, mensuration, coordinate geometry, trigonometry, statistics, data interpretation, probability, and combinatorics. Add calculus, matrices, determinants, vectors, differential equations, linear algebra, discrete maths, numerical methods, and other higher-level topics as supported by the verified university syllabus or chosen exam. Do not imply every topic is part of a specific GJUST paper.

Each topic should support objectives, prerequisites, estimated duration, examples, practice questions, common misconceptions, difficulty, and source/version.

## AI tutor rules
- Teach one manageable concept at a time in Roman Hinglish by default.
- Use a worked example, then ask the learner to try a similar problem, then increase difficulty gradually.
- Prefer graduated hints before revealing a complete solution when appropriate.
- Explain mistakes constructively and diagnose missing prerequisites.
- Adapt based on demonstrated performance; offer simpler or alternate explanations when asked.
- Verify arithmetic and algebra using reliable calculation/code when available.
- Summarize learning, gaps, and the next recommended topic.
- Be transparent about uncertainty and never claim a file was read, data saved, a test run, or a feature completed unless it actually happened.

## Engineering and security
- Audit the repository, framework, dependencies, scripts, and current implementation before choosing an approach. Reuse the existing stack unless there is a clear reason not to.
- Build maintainable components and keep UI, curriculum content, persistence, and AI-provider logic separate.
- Use a swappable AI-provider abstraction. Keep keys server-side in environment variables; never commit real credentials or expose them in client code.
- Implement secure authentication/authorization and ensure students can access only their own records. Validate inputs, handle API errors, apply sensible rate limits, and avoid unnecessary personal-data collection.
- If services or keys are not configured, provide a clearly labelled working demo/local mode rather than pretending real AI or cloud persistence is enabled.
- Include setup, environment-variable examples without secrets, development/test/build commands, and deployment instructions.
- Add useful tests. Run available lint, type-check, test, and build commands and report actual results.
- Ensure accessible semantic UI, keyboard support, visible focus, readable contrast, mobile-friendly equations, responsive layouts, and reduced-motion support.
- Do not leave dead buttons, fake success states, or screens that only look complete.

## Visual direction
Create a polished, calm, modern learning interface with clear typography, readable lesson widths, consistent spacing and design tokens, restrained colour, clear hierarchy, and useful progress visualizations. Prioritize clarity and usability over decorative effects. Support light/dark mode if practical.

## Execution workflow
1. Audit the repo and identify important blockers.
2. Ask me only for a consequential decision or missing official syllabus/source that is truly needed; otherwise proceed.
3. Implement a complete runnable vertical slice first: responsive shell, curriculum browsing, real foundational lessons, practice with feedback, and visible progress.
4. Add account/persistence and AI tutor integration using the available configured services; provide explicit setup states if configuration is missing.
5. Add exam paths and syllabus ingestion without fabricating official content.
6. Test, fix issues, and verify the production build where possible.
7. Update the README with setup, environment configuration, features, limitations, tests, and deployment steps.

After each substantial phase, keep the app runnable and report changed files, checks actually run, blockers, and next steps. Do not stop after producing a plan—continue implementing. Do not overwrite working project code without inspecting it first. If the task is too large for one pass, finish the most useful functional MVP, clearly document what remains, and continue as far as tools/time allow.

## Definition of a useful MVP
A learner can open the app on phone or desktop, choose a goal and language, browse foundational maths in prerequisite order, complete several real lessons, answer practice questions, receive correct feedback and hints, see progress in the implemented storage mode, and open the tutor with honest setup/error states. GJUST-specific mapping must wait for an official syllabus source.

**Start by inspecting this repository now. Ask me a concise question only if a consequential enhancement or missing decision is genuinely necessary; otherwise build, test, and verify the best working version.**
