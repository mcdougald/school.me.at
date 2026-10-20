<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="school.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">school.me.at</h1>

<p align="center"><strong>A gradebook that never erases the old mark.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/self--host-supported-525252?style=flat-square" alt="Self-host: supported">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

In a lot of gradebooks, changing a mark erases the old one, along with any record of who changed it and when. I built school.me.at so a grade is a history: courses with roles, where instructors author, students enroll in cohorts, and work is submitted, quizzed and graded on the server. It is the machinery, not the coursework, so what a class teaches stays with the institution that runs it.

> **Status:** the engine is built and tested. The teaching pages are not open yet, and version 1 is scoped to adult education only.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="school.me.at at a glance: grades are a history, questions are versioned, deny by default, stats never a ranking" width="880">
  </picture>
</p>

## Why school.me.at

| The usual gradebook | school.me.at |
| --- | --- |
| A correction overwrites the old mark | A correction is a new event, with its author and the server time |
| Editing an answer key can rescore old work | Each attempt is pinned to the question versions the student saw |
| Late is whatever the clock on the device says | Submissions are timestamped by the server |
| Class lists sorted by score | Counts, ratios and anonymous score ranges, never a ranking |

## Features

- **Append-only grades**: each grade is a list of events with an author and a server timestamp, so a correction adds an entry instead of overwriting the last one.
- **A gradebook computed from the record**: weighted categories recompute from the grade history, and students, teachers and admins each see only their own scope.
- **Versioned questions**: each quiz attempt is pinned to the question versions the student saw, so a later edit to the answer key cannot rescore handed-in work.
- **Server-side grading**: objective answers are scored on the server against a key the browser never receives, and written answers wait for a teacher.
- **Deny-by-default permissions**: every read and write is checked in one place against role, page and action, scoped to a school or cohort membership.
- **Invite-only enrollment**: invite codes that can expire, be revoked or cap seats, with roster import from a spreadsheet.
- **Submissions on the server clock**: work is timestamped by the server and marked late against the due date and any cut-off.
- **Class statistics with no ranking**: teachers get counts, ratios and anonymous score ranges, never an ordered list of students.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How school.me.at works: enroll, submit, grade, record, report" width="880">
  </picture>
</p>

Students join a cohort through an invite code or a spreadsheet roster. Their work is timestamped by the server when it is submitted, objective answers are scored on the server, and written answers wait for a teacher. Every grade, including each correction, is appended as an event, and the gradebook is computed from that record for each role's own scope.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
  <img src="https://img.shields.io/badge/MDX-lessons-737373?style=flat-square&logo=mdx&logoColor=white" alt="MDX for lessons">
</p>

- Next.js 16 (App Router) and React 19
- TypeScript
- Tailwind CSS 4
- Drizzle ORM and Postgres (with in-memory stores when no database is configured)
- MDX for lessons
- Better Auth (shared me.at account)

## Part of the me.at family

school.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
