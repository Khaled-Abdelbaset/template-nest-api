# Template — Nest API

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?logo=github)](https://github.com/Khaled-Abdelbaset/template-nest-api/generate)

Minimal **[NestJS](https://nestjs.com/)** service with **[Prisma](https://www.prisma.io/)**, org **CI**, and **Discord** workflow hooks. Created from [engineering-standards](https://github.com/Khaled-Abdelbaset/engineering-standards).

---

## What you get

- Health route (`GET /health`)
- Empty Prisma schema (MySQL) — ready for `db push`
- `.github/workflows/ci.yml` → `engineering-standards` reusable Nest CI (`@v1.0.0`)
- `.github/workflows/discord-notify.yml` (optional webhook)
- [CONTRIBUTING.md](CONTRIBUTING.md), PR template, **`AGENTS.md`** + **`CLAUDE.md`**, Cursor & Claude git rules

---

## Create a project from this template

1. GitHub → **Use this template** → name your repo under `Khaled-Abdelbaset`.
2. Clone:

   ```bash
   git clone git@github.com:Khaled-Abdelbaset/your-api.git
   cd your-api
   ```

3. Configure git author for your GitHub account: [GIT_IDENTITY.md](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/GIT_IDENTITY.md).

4. Bootstrap:

   ```bash
   cp .env.example .env
   npm ci
   npx prisma generate
   npm run dev
   ```

5. Repo **Settings → Secrets** → `DISCORD_WEBHOOK_URL` (optional).
6. **Branch protection** on `main`: require PR + `build` check — see [NEW_PROJECT.md](https://github.com/Khaled-Abdelbaset/engineering-standards/blob/main/docs/NEW_PROJECT.md).

---

## Prerequisites

- Node.js 22+
- MySQL (local or Docker) — set `DATABASE_URL` in `.env`

---

## Scripts

| Command | Purpose |
|---------|---------|
| `npm run dev` | Nest watch mode |
| `npm run build` | Compile to `dist/` |
| `npm run start` | Run production build |

---

## Customize

1. Replace `template-nest-api` in `package.json`.
2. Extend `prisma/schema.prisma`; run `npm run prisma:push` or migrations.
3. Add modules under `src/`.
4. Rename Discord embed username in `discord-notify.yml` if desired.

---

## Related

| Resource | Link |
|----------|------|
| Full API example | [focus-planner-backend](https://github.com/Khaled-Abdelbaset/focus-planner-backend) |
| Handbook | [engineering-standards](https://github.com/Khaled-Abdelbaset/engineering-standards) |
| Frontend template | [template-next-app](https://github.com/Khaled-Abdelbaset/template-next-app) |

---

## License

Private / customize per new repo.