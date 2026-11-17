# dAIgest

**An India-first news experience with concise story briefs and article-grounded conversational Q&A.**

[Open dAIgest](https://daigest.xyz)

dAIgest brings current headlines into a category-based feed, creates short story briefs, and lets readers ask follow-up questions about a selected article. When the selected story does not provide enough context, the app can retrieve related reporting and include citations.

## Features

- **News feed:** headlines with category navigation and search
- **Story briefs:** concise, story-specific summaries and starter questions
- **Ask dAIgest:** conversational answers grounded in the selected story, with related-news retrieval when needed
- **Fallback content:** sample stories remain available when live news is unavailable

## Tech stack

- **News ingestion:** Currents API
- **AI:** DeepSeek LLM for conversational, context-aware answers
- **Frontend:** React, TypeScript, and a Next.js-compatible app built with Vinext
- **Backend integration:** Supabase, with an optional external Ask API

## Run locally

**Requirements:** Node.js `>=22.13.0` and pnpm.

```bash
pnpm install
cp .env.example .env.local
pnpm dev
```

Configure the values in `.env.local`:

- `NEXT_PUBLIC_SUPABASE_URL` — Supabase project URL
- `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` — Supabase publishable key
- `NEXT_PUBLIC_ASK_API_BASE` — optional base URL for the Ask dAIgest API; omit it when the API is served from the same origin

The DeepSeek integration and news-provider credentials belong in the protected backend environment, not in the browser-facing frontend configuration. Never commit API keys or secrets.

## Key areas

- `app/` — application pages and client-side experience
- `components/` — reusable UI components
- `lib/` — shared utilities and Supabase client
- `public/` — static assets
- `.env.example` — local environment template

## Notes

The repository also contains Sites/Vinext runtime and deployment configuration. Keep generated runtime state and secrets out of Git. Configure protected API credentials in the backend hosting environment.

---

Built by [Gairik Chakraborty](https://github.com/gairikzzz) · [Portfolio](https://gairik.tech) · [LinkedIn](https://www.linkedin.com/in/gairikchakraborty)
