# small-budget-ads

**Meta Ads decision rules for small budgets.**

`small-budget-ads` is an agent skill for Claude Code (and any agent that reads `SKILL.md` skills). Most ad skills assume big budgets and clean A/B tests. Small local businesses run 1-5 USD a day per ad set, one ad set per product, with conversations to WhatsApp or Messenger as the result. With so little data, the usual "kill it after 3 days" advice turns off good ads and resets the learning phase for nothing.

`small-budget-ads` gives the agent safe rules: wait for enough data, judge each ad set only against itself, call an ad bad only after it spent 2x its benchmark, never leave an ad set with a single ad, never duplicate to "fix", and always ask the owner before changing anything.

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

## License

MIT. Made by [Rabbit Designs](https://github.com/RabbitDesigns22).
