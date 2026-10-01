<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="school.me.at landing page" width="880">
  </picture>
</p>

# school.me.at

A gradebook that never erases the old mark.

School is courses with roles: instructors author, students enroll in cohorts, and work is submitted, quizzed and graded. It is the machinery, not the coursework, so what a class teaches stays with the institution that runs it. The engine is built and tested; the teaching pages are not open yet, and version 1 is scoped to adult education only.

## Features

- **Append-only grades**: each grade is a list of events with an author and a server timestamp, so a correction adds an entry instead of overwriting the last one.
- **A gradebook computed from the record**: weighted categories recompute from the grade history, and students, teachers and admins each see only their own scope.
- **Versioned questions**: each quiz attempt is pinned to the question versions the student saw, so a later edit to the answer key cannot rescore handed-in work.
- **Server-side grading**: objective answers are scored on the server against a key the browser never receives; written answers wait for a teacher.
- **Deny-by-default permissions**: every read and write is checked in one place against role, page and action, scoped to a school or cohort membership.
- **Invite-only enrollment**: invite codes that can expire, be revoked or cap seats, with roster import from a spreadsheet.
- **Submissions on the server clock**: work is timestamped by the server and marked late against the due date and any cut-off.
- **Class statistics with no ranking**: teachers get counts, ratios and anonymous score ranges, never an ordered list of students.

## Built with

- Next.js 16 (App Router) and React 19
- TypeScript
- Tailwind CSS 4
- Drizzle ORM and Postgres (with in-memory stores when no database is configured)
- MDX for lessons
- Better Auth (shared me.at account)

## Part of the me.at family

school.me.at is one of the [`*.me.at`](https://me.at) apps by Trevor McDougald. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

See [LICENSE](LICENSE).
