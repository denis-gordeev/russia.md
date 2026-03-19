# Russia.md

An AI-friendly, open-source knowledge atlas about Russia, forked from [`frank890417/taiwan-md`](https://github.com/frank890417/taiwan-md) and rebuilt as a Russia-focused starter project.

## Scope

- 12 category structure preserved from the upstream site
- Russia-specific branding, navigation, and category descriptions
- Starter essays for history, geography, culture, food, art, music, technology, nature, people, society, economy, and lifestyle
- [`SKILLS.md`](./SKILLS.md) covering Gosuslugi, VK, Yandex, DaData, CBR, FNS, banks, and marketplace integrations for LLM agents

## Status

This is a foundation fork, not a finished editorial project. The inherited Taiwan-specific content has been bypassed in favor of a clean Russia corpus under `russia-knowledge/`.

## Development

```bash
npm install
npm run build
```

## Key paths

- `src/` site shell and Astro pages
- `russia-knowledge/` source markdown used by category and article pages
- `public/llms.txt` AI-oriented project summary

## Next work

- Replace remaining inherited Taiwan-only auxiliary pages and datasets
- Add Russia-specific charts and maps
- Expand each category beyond the single starter essay
- Configure a real GitHub remote, domain, and deployment target
