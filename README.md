# Agasthiya Nexus — Educational AI Expo Website

A Next.js educational chatbot with a hosted Groq AI backend. Visitors can access the deployed site in Chrome without VS Code or Ollama.

## Local setup

1. Install Node.js LTS.
2. Create a free account at https://console.groq.com and create an API key.
3. Copy `.env.example` to `.env.local` and replace the placeholder with your Groq API key. Never share or commit this key.
4. Run `npm install` then `npm run dev`.
5. Open http://localhost:3000.

## Public deployment (Vercel + GitHub)

1. Create a GitHub repository and upload project files (not `.env.local`, `node_modules`, or `.next`).
2. Visit https://vercel.com/new and import your GitHub repository.
3. Under Environment Variables, add `GROQ_API_KEY` with your private key and `GROQ_MODEL` with `openai/gpt-oss-20b`.
4. Deploy. Vercel supplies a public HTTPS URL. If changing variables later, redeploy.
5. Open the URL on a second computer and test educational and unrelated questions.

## Important limitations

- The Groq free tier has per-model and per-account request/token limits; it is not unlimited.
- Vercel Hobby is for personal, non-commercial use and has usage caps.
- The educational intent classifier is AI-based, not guaranteed to be perfect.
- The in-memory IP rate limit is best-effort only on serverless instances. For a heavily shared public site, add a persistent rate limiter and abuse controls.
- Voice recognition depends on browser support and may require internet connectivity.
- The chat is not streamed; it displays the response once completed.
- There is no paid AI API requirement if usage stays within the provider's free tier.
- Never put your Groq key in browser-side code or commit it to GitHub.
