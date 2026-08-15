# AI Agent Engineering Bootcamp

A free, self-paced, 14-day bootcamp for backend engineers, solutions architects, and developers moving into **enterprise AI agent engineering**. It treats the topic as an engineering discipline — architecture, security, distributed systems, reliability, and real implementation trade-offs — rather than another prompt-engineering primer.

**[Live site →](https://ai-agent-engineering-bootcamp-production.up.railway.app)**

## Why this exists

Most "AI agents" content stops at prompting and demos. This bootcamp is built around the questions that actually come up when you have to **design, build, and operate** an agent inside a real company: How do you scope a tool safely? What happens when the LLM provider is down? How do you evaluate an agent in production? When does Saga beat a distributed transaction? When do you reach for Go or Rust instead of Python?

Each day connects a new AI concept to something you likely already know from backend, cloud, or distributed systems — the goal is to translate existing engineering judgment into this new domain, not to start from zero.

## What's inside

- **14 daily modules** (3 weeks) — LLM/agent fundamentals, agent architecture, enterprise integration, security & prompt injection, production reliability, System Design framework, distributed systems, cloud architecture (AWS), an ambiguous-problem framework, product thinking, technical communication, behavioral storytelling, and full mock interview sessions.
- **Diagrams and code** — every architecture-heavy day includes a hand-drawn SVG diagram and a working Python implementation sketch (rate limiters, circuit breakers, Sagas, idempotency, consistent hashing, and more).
- **Interactive quizzes and checklists** — self-check your understanding as you go; progress is saved locally in your browser (`localStorage`), nothing is sent anywhere.
- **Reference pages** — a filterable glossary, a reusable mock-interview question bank, dense one-page cheat sheets per track, a page on algorithms behind each architectural pattern (with Big-O complexity), and a language-selection guide (Python vs. Go vs. Rust vs. C++ vs. Java) for different layers of an agent system.

## Structure

```
public/
  index.html              hub — progress tracker + links to every module
  day-01.html … day-14.html
  glosario.html            searchable glossary
  mock-bank.html           reusable mock-interview question bank
  cheatsheets.html         5 dense one-pagers by track
  referencia-extra.html    voice, software engineering, data, DevOps
  algoritmos.html          algorithms by stage, with complexity + Python
  stack-tecnologico.html   language selection guide by architecture layer
server.js                  minimal Express static server
package.json
```

## Running locally

```bash
npm install
npm start
```

Then open `http://localhost:3000`.

Since this is a static HTML/CSS/JS site, you can also just open `public/index.html` directly in a browser, or serve the `public/` folder with any static file server.

## Deployment

Deployed on [Railway](https://railway.app) as a minimal Node/Express static server. Any static host works equally well (Netlify, Vercel, GitHub Pages) — `server.js` exists only because Railway's Nixpacks builder expects a runnable process.

## Design notes

Every page shares a small hand-built design system (no CSS frameworks, no build step) — a "blueprint/engineering notebook" aesthetic: a serif display face for headings, monospace for labels and data, a warm amber accent, and light/dark themes driven entirely by CSS custom properties. All diagrams are hand-authored inline SVG, no diagramming libraries.

## License

MIT — see [LICENSE](LICENSE). Use it, adapt it, teach with it.

## Contributing

This started as a personal study project and is offered as-is. If you spot an error or want to suggest a topic, open an issue or a PR.
