# small-budget-ads

**Meta Ads decision rules for small budgets.**

`small-budget-ads` is an agent skill for Claude Code (and any agent that reads `SKILL.md` skills). Most ad skills assume big budgets and clean A/B tests. Small local businesses run 1-5 USD a day per ad set, one ad set per product, with conversations to WhatsApp or Messenger as the result. With so little data, the usual "kill it after 3 days" advice turns off good ads and resets the learning phase for nothing.

`small-budget-ads` gives the agent safe rules: wait for enough data, judge each ad set only against itself, call an ad bad only after it spent 2x its benchmark, never leave an ad set with a single ad, never duplicate to "fix", and always ask the owner before changing anything.

## See the difference

> **You:** Which ad should I turn off? The ad set spends 2 USD a day.

**Without the skill:** "Kill the losers after 3 days": it turns off a good ad on too little data and resets the learning phase.

**With the skill:** it waits for enough data, compares the ad only against its own ad set, calls it bad only after it spent 2x the benchmark, replaces it with a new version instead of leaving one ad alone, and asks the owner first.

**Skip it if** your ad sets spend hundreds a day; standard testing rules fit you better.

**Status:** in daily use in the author's own setup. Plain instructions, no scripts, no network calls. MIT. Issues and suggestions welcome.

## Install

With the [skills CLI](https://skills.sh):

```bash
npx skills add RabbitDesigns22/small-budget-ads
```

Or manually: copy `skills/small-budget-ads/` into `~/.claude/skills/` for all your projects, or into `.claude/skills/` for one project.

## Works well with

- [`report-now`](https://github.com/RabbitDesigns22/report-now): check the accounts live before reporting.
- [`one-answer`](https://github.com/RabbitDesigns22/one-answer): one checked, final recommendation.

## Español

**Decisiones de Meta Ads para presupuestos chicos.** Para negocios locales con 1 a 5 dólares al día por conjunto y campañas a WhatsApp: esperar datos suficientes (7 días), comparar cada conjunto solo consigo mismo, llamar "malo" a un anuncio solo si gastó 2 veces su costo normal, nunca dejar un conjunto con un solo anuncio, no duplicar para "arreglar" y pedir permiso al dueño antes de cualquier cambio.

Instalar: `npx skills add RabbitDesigns22/small-budget-ads`

## More skills from the same setup

These come from one real workflow: a small agency run with 15+ Claude Code sessions in parallel. Each skill fixes one problem that kept happening there.

| Skill | What it fixes |
|---|---|
| [one-pass](https://github.com/RabbitDesigns22/one-pass) | get it right the first time; stop paying tokens for rework |
| [hora-exacta](https://github.com/RabbitDesigns22/hora-exacta) | real date and time in every message, so nothing lands on the wrong day |
| [hands-on](https://github.com/RabbitDesigns22/hands-on) | the agent does what it can and only asks you for codes, keys and payments |
| [easy-for-them](https://github.com/RabbitDesigns22/easy-for-them) | steps people actually follow: direct link, one action per line |
| [one-answer](https://github.com/RabbitDesigns22/one-answer) | one thought-through answer instead of plan, fix, new plan |
| [never-twice](https://github.com/RabbitDesigns22/never-twice) | a shared error log so no session repeats a known mistake |
| [report-now](https://github.com/RabbitDesigns22/report-now) | status checked live this minute, stamped with the time |
| [sort-me-out](https://github.com/RabbitDesigns22/sort-me-out) | one ordered list of what is urgent, waiting and forgotten |
| [in-the-loop](https://github.com/RabbitDesigns22/in-the-loop) | a live board so parallel sessions know what the others changed |
| [study-first](https://github.com/RabbitDesigns22/study-first) | reads everything in full and answers point by point, no invented details |
| [session-watchdog](https://github.com/RabbitDesigns22/session-watchdog) | wakes the sessions that got stuck mid-task, leaves the rest alone |
| [skill-harvest](https://github.com/RabbitDesigns22/skill-harvest) | reads your sessions and finds the skills you are missing |
| [whatsapp-closer](https://github.com/RabbitDesigns22/whatsapp-closer) | evidence-ranked rules for a WhatsApp sales assistant that closes |
| [whatsapp-number-onboarding](https://github.com/RabbitDesigns22/whatsapp-number-onboarding) | connect a number to the WhatsApp Cloud API in the safe order |
| [proposal-pdf](https://github.com/RabbitDesigns22/proposal-pdf) | short PDF proposals with every price checked against its source |

If one of them saved you a redo, a star helps other people find it.

## License

MIT. Made by [Rabbit Designs](https://github.com/RabbitDesigns22).
