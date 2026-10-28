# Gligorco Gligorov

Backend & AI engineer. I build systems that run in production, not just in demos: AI pipelines, reliable distributed backends, and email security.

For the past 3.5 years I've been the sole backend engineer at [BrandsGateway](https://brandsgateway.com), a B2B luxury fashion marketplace. I own the pipeline that imports products from 15+ international vendors and runs them through GPT-4 to clean and write content for 10,000+ SKUs a day. It recovers from failures on its own, isolates state per product, keeps versioned rollback on S3, and logs everything to Graylog so I can see what broke before anyone else notices.

That code is private, so what you see here is mostly what I build on the side.

## Featured

**[Inspekt](https://github.com/GligorcoGligorov/inspekt)**: an open-source email threat-analysis service in Go and Python on Redis Streams and MariaDB. It parses raw MIME as hostile input, verifies SPF, DKIM and DMARC itself, detects lookalike domains, display-name spoofing and QR-code phishing, separates hidden text from what the reader sees, and reports instructions aimed at AI email assistants. Every verdict comes with its evidence. Detection is measured on 6,202 public emails with a dev/holdout split: holdout recall 20% → 39% with no new false positives. Async workers with a watchdog and dead-letter queue, Prometheus/Grafana, and CI that fails if detection regresses. `Go` `Python` `Redis Streams` `MariaDB` `Docker` `Prometheus` `Grafana`

**[Signal](https://signal-blond-phi-13.vercel.app)**: AI lead discovery for software founders (live, private beta). Reads 10+ public sources every hour, filters without AI first, then scores buying intent in batches under a shared AI budget, with a heuristic fallback so a run never breaks. Postgres row-level security with tests proving accounts can't see each other's data. `TypeScript` `Next.js 15` `Supabase` `Gemini` `GitHub Actions`

## Selected projects
[Pact](https://github.com/GligorcoGligorov/Pact): habit app for small crews of friends, built in two weeks during the 8x Playmakers trial. Each day everyone checks in with a photo of the habit plus that day's challenge. If one person misses, the chain breaks for the whole crew, and whoever slips pays the stake. It's an Expo app and a Next.js API sharing one Zod contract. Every read and write goes through the server, and day math is computed in each pact's own time zone and DST-safe. An AI judge (Groq, falling back to Gemini) runs in the background, so it never blocks a check-in. `Expo` `React Native` `Next.js 15` `Prisma` `Supabase` `Zod` `Groq` `PostHog`

[FitCheck](https://thefitcheck.vercel.app): AI wardrobe stylist, live in production. A vision model tags each garment once, then the stylist reasons over a compact text catalogue. That cut inference cost about 10×. Garment names come from a closed vocabulary and are composed in code, so there are no hallucinated names in English, German or Macedonian. `Next.js 16` `Prisma` `PostgreSQL (Neon)` `Vercel AI SDK` `Groq` `Zod`

[CodeSensei](https://github.com/GligorcoGligorov/CodeSensei): coding interview prep platform ([live](https://codesensei-three.vercel.app)). A GPT-4 mentor that gives hints based on your code and attempt history, plus a sandboxed in-browser test runner. `React` `TypeScript` `Node.js` `Express` `Supabase` `OpenAI`

[RentEase](https://github.com/GligorcoGligorov/assess): property rental platform ([live](https://assess-xi.vercel.app)). Real-time renter–owner chat over Socket.io, booking conflicts caught with Postgres `OVERLAPS`, JWT refresh token rotation. `React` `Node.js` `PostgreSQL` `Socket.io`

[VitalLink](https://github.com/GligorcoGligorov/VitalLink): remote patient monitoring app. Patient and doctor roles, request/accept connections, live vitals and chat, all secured with Supabase row-level security. `React Native` `Expo` `Supabase Realtime + RLS`

## Stack

- **Backend:** Go, TypeScript / Node.js, PHP / Laravel, Python, Java / Spring Boot
- **Data and queues:** Redis Streams, MariaDB / MySQL, PostgreSQL, SQLite, Prisma
- **Security:** SPF / DKIM / DMARC, MIME parsing, phishing detection, fuzz testing, row-level security
- **Infra:** Docker, GitHub Actions, Prometheus, Grafana, Graylog, AWS (S3, Lambda), Vercel, Railway, Node-RED
- **AI:** OpenAI, Groq, Gemini, Vercel AI SDK, schema-constrained structured output, evaluation on dev/holdout data
- **Frontend / mobile:** React, Next.js, React Native, Expo

## How I like to work

I think about failure modes before features: what happens when the vendor feed is malformed, when the LLM times out, or when the job dies halfway through. I use Cursor and Claude Code every day, and I review, test and measure everything I ship.

## Get in touch

Open to backend and email-security engineering roles: hybrid or on-site in Skopje, or remote in the EU.

[Portfolio](https://gligorcogligorov.vercel.app) · [LinkedIn](https://linkedin.com/in/gligorco-gligorov-11b282289) · ggligorov1709@yahoo.com
