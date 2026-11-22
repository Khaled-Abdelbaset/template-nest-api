# Agent instructions — NestJS

## Commands

- Install: `npm ci`
- Dev: `npm run dev`
- Prisma: `npx prisma generate` (before build when schema changes)
- Build: `npm run build`

## Repository

- **Stack:** NestJS, Prisma, TypeScript
- **Default branch:** `main` (protected; PRs only)

## Git & PR

- **Handbook:** [GIT_WORKFLOW.md](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/GIT_WORKFLOW.md)
- **Commit email:** [GIT_IDENTITY.md](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/GIT_IDENTITY.md)
- Branch from `main`: `feat/`, `fix/`, `chore/`, `docs/`
- **Conventional Commits:** `feat(backend): …`, `fix(api): …`, `chore(ci): …`
- PR body: Summary, Test plan, note API contract changes for frontend
- Squash merge after CI **build** is green
- Do **not** `git commit` or `git push` unless the user explicitly asks
- Never commit `.env`, secrets, or `dist/`

## Cross-repo

- Document breaking API changes in the backend PR; frontend depends after merge/deploy

## Large initiatives

- One branch and one PR per phase; tracker in `docs/*-TRACKER.md` when present
- See [GIT_WORKFLOW §11](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/GIT_WORKFLOW.md#11-large-initiatives-multi-phase-work)

## Tool-specific mirrors

| Tool | Path |
|------|------|
| Cursor | `.cursor/rules/git-workflow.mdc` (always apply) + stack rule |
| Claude Code | `CLAUDE.md` imports this file; `.claude/rules/git-workflow.md` |

**Agent layering:** [AGENT_INSTRUCTIONS.md](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/AGENT_INSTRUCTIONS.md)