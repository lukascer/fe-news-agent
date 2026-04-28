# 📰 FE News Agent

Automatický AI agent pro denní skenování frontend novinek a publikování na Slack.

## Co to dělá

Každý pracovní den v 8:30 agent:

1. 🔍 Prohledá web pro novinky z React/Next.js, CSS, JS tooling, npm security, prohlížečů
2. 📖 Přečte historii Slack kanálu `#frontend-news`
3. 🆕 Porovná a pošle jen nové věci
4. 💬 Publikuje formátovanou zprávu v češtině na Slack

## Nastavení

Tento repo slouží jako konfigurace pro **Claude Code Routine**:

1. Připoj tento repo v [claude.ai/code](https://claude.ai/code) → Settings → GitHub
2. Jdi na [claude.ai/code/routines](https://claude.ai/code/routines)
3. Klikni **New Routine**
4. Vyber tento repo
5. Jako prompt zadej: `Proveď denní FE news scan podle instrukcí v CLAUDE.md`
6. Nastav trigger: **Weekdays v 8:30**
7. Připoj **Slack** connector

## Konfigurace

Veškerá konfigurace agenta je v souboru `CLAUDE.md`:

- Sledované oblasti (React, CSS, JS, Security, Browsers)
- Formát zpráv (emoji, odsazení, struktura)
- Jazyková pravidla (přirozená čeština, anglické tech termíny)
- Deduplikační logika
- Slack kanál ID
