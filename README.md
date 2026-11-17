# dAIgest

**An India-first news experience with concise story briefs and article-grounded conversational Q&A.**

[Open dAIgest](https://daigest.xyz)

dAIgest brings current headlines into a category-based feed, creates short story briefs, and lets readers ask follow-up questions about a selected article. When the selected story does not provide enough context, the app can retrieve related global reporting and include citations.

## Features

- **News feed:** latest headlines with category navigation and search
- **Story briefs:** concise, story-specific summaries and starter questions
- **Ask dAIgest:** conversational answers grounded in the selected story, with related-news retrieval when needed
- **Fallback content:** sample stories remain available when live news is unavailable

## Tech

- **News:** Currents API
- **Language model:** Gemini 3.5 Flash-Lite for category validation, starter questions, and conversational answers
- **Application:** React, Next.js-compatible app stack, TypeScript, and Vinext
- **Data/backend options:** Supabase, Drizzle ORM, and optional Cloudflare D1 support in the starter

## Run locally

**Requirements:** Node.js `>=22.13.0` and pnpm (the repository's package manager).

```bash
pnpm install
cp .env.example .env.local
pnpm dev
```

Set the following server-side environment variables in `.env.local` to enable live functionality:

- `CURRENTS_API_KEY`
- `GEMINI_API_KEY`

Keep API keys out of source control. The application reads them in server-side routes; do not expose them to the browser.

## Key areas

- `app/` — application pages and routes
- `components/` — reusable UI components
- `lib/` — shared application utilities
- `public/` — static assets
- `.env.example` — environment variable template

## Notes

The repository includes additional Sites/Vinext runtime and deployment configuration. For deployment-specific setup, use the hosting environment's configuration and keep generated runtime state and secrets out of Git.

---

Built by [Gairik Chakraborty](https://github.com/gairikzzz) · [Portfolio](https://gairik.tech) · [LinkedIn](https://www.linkedin.com/in/gairikchakraborty)
