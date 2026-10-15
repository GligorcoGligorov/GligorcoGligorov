# Gligorco Gligorov

Backend engineer. I build AI systems that run in production, not just in demos.

For the past 3+ years I've been the sole backend engineer at [BrandsGateway](https://brandsgateway.com), a B2B luxury fashion marketplace. I own the pipeline that imports products from 15+ European vendors and runs them through GPT-4 to clean and write content for 10,000+ SKUs a day. It recovers from failures on its own, isolates state per product, keeps versioned rollback on S3, and logs everything to Graylog so I can see what broke before anyone else notices.

That code is private, so what you see here is mostly what I build on the side.

## Selected projects

**[FitCheck](https://thefitcheck.vercel.app)**: AI wardrobe stylist, live in production.
A vision model tags each garment once, then the stylist reasons over a compact text catalogue. That cut inference cost about 10×. Garment names come from a closed vocabulary and are composed in code, so there are no hallucinated names in English, German or Macedonian.
`Next.js 16` `Prisma` `PostgreSQL (Neon)` `Vercel AI SDK` `Groq` `Zod`

**[CodeSensei](https://github.com/GligorcoGligorov/CodeSensei)**: coding interview prep platform ([live](https://codesensei-three.vercel.app)).
A GPT-4 mentor that gives hints based on your code and attempt history, plus a sandboxed in-browser test runner.
`React` `TypeScript` `Node.js` `Express` `Supabase` `OpenAI`

**[RentEase](https://github.com/GligorcoGligorov/assess)**: property rental platform ([live](https://assess-xi.vercel.app)).
Real-time renter–owner chat over Socket.io, booking conflicts caught with Postgres `OVERLAPS`, JWT refresh token rotation.
`React` `Node.js` `PostgreSQL` `Socket.io`

**[VitalLink](https://github.com/GligorcoGligorov/VitalLink)**: remote patient monitoring app.
Patient and doctor roles, request/accept connections, live vitals and chat, all secured with Supabase row-level security.
`React Native` `Expo` `Supabase Realtime + RLS`

## Stack

- **Backend:** TypeScript / Node.js, PHP / Laravel, Java / Spring Boot, Kotlin
- **Data:** PostgreSQL, MySQL, SQLite, Prisma
- **Infra:** Docker, AWS (S3, Lambda), Vercel, Railway, Graylog, Node-RED
- **AI:** OpenAI, Groq, Vercel AI SDK, schema-constrained structured output
- **Frontend / mobile:** React, Next.js, React Native, Expo

## How I like to work

I think about failure modes before features: what happens when the vendor feed is malformed, when the LLM times out, or when the job dies halfway through. I use Cursor and Claude Code every day, and I still own every line I ship.

## Get in touch

Open to backend and AI engineering roles, remote in the EU or in Switzerland.

[Portfolio](https://gligorcogligorov.vercel.app) · [LinkedIn](https://www.linkedin.com/in/gligorco-gligorov-11b282289) · ggligorov1709@yahoo.com
