# Jude Caldwell

Computer Science at the College of William & Mary. Expected graduation: May 2028. Monroe Scholar. Vienna, VA.

In summer 2024 I replaced the room reservation policy at a 10,000-student campus. It's still the system they run on. Most of what I've built since has been the same shape — tools and infrastructure that someone uses on an ordinary weekday.

jcaldwell@wm.edu · [LinkedIn](https://www.linkedin.com/in/jude-caldwell-1a66562ab)

---

## ChainOpt

**[chain-opt.vercel.app](https://chain-opt.vercel.app)** · Python SDK and CLI · March 2026 – present · sole engineer

Static analysis for LLM agent pipelines built on LangChain, LangGraph, or raw SDK calls. Langfuse and Helicone tell you what you spent. ChainOpt tells you what to change.

The SDK patches the httpx transport layer to intercept outbound LLM calls, so it runs against an existing pipeline with no changes to that pipeline's code. The CLI maps the call graph and infers what each call is for — extraction, routing, summarization, validation — then produces an HTML cost report backed by the actual prompts and responses rather than aggregate counters.

Shipped today: **model-oversizing detection**, flagging calls running on a more expensive model than the task requires. Parallelization, redundancy and semantic overlap, and context-bloat detection are roadmap, not product.

## Campus room reservation system — George Mason University

A.I. Algorithms Lab · Summer 2024

GMU allocated rooms first-come-first-served, so whoever clicked fastest won. A four-person study group could take a lecture hall while a fifty-person section got turned away.

I designed two things. An online policy, since requests arrive one at a time and you have to decide without knowing what's coming: Follow-the-Leader selecting among three heuristics — room popularity, spatial density, and current reservation load. And an offline linear program minimizing rejected requests, which gave me a ceiling to measure the online policy against. Without that benchmark I'd have had no way to tell whether the heuristics were good or merely better than nothing.

I also built and deployed the full-stack Node.js/React interface to campus servers. It is the university's primary reservation system.

## ICEBREAKR — Geospatial Evaluation and Observation Lab, W&M

December 2025 – present · 6-person team

A political wargaming simulation platform. Human-playable first; the RAG-backed agent layer came after.

I built the MCP server that exposes simulation state and legal actions as callable tools to LLM agents, and designed the pipeline that processes a single game turn. Agent-driven runs finish in minutes where the human version takes hours or days, and scenarios can now run in parallel.

## Tool-augmented LLM security — Monroe Scholar research

W&M Department of Computer Science · advised by Prof. Yue Xiao · July 2026 – present

Can a tool-using LLM agent be hijacked by the pages it reads?

I built an autonomous research agent in Python with headless-browser, protected-file, and note-writing tools, and a repeatable harness that plants hidden instructions in the content that agent retrieves — CSS-hidden text, DOM metadata, fake system delimiters, poisoned agent notes, multi-page payloads. Every tool call is logged, so the question becomes measurable: how often does the agent follow attacker text over its own instructions?

The design spans 12 injection techniques across 6 page archetypes, run on the same architecture against OpenAI, Anthropic, and Google models to isolate provider-specific failures. Roughly 1,000 trials, scored on unauthorized data access, instruction-hierarchy violation, and multi-step exploit success, using the SAFE-MCP attack taxonomy.

**This work is in flight. Those are the planned parameters, not results — I have no findings to report yet.**

## District demographics platform — W&M Department of Sociology

May 2026 – present · 3-person team

An interactive geospatial analysis tool covering every U.S. legislative district, built in React/Vite, Mapbox GL, FastAPI, and PostgreSQL.

I modeled and normalized roughly 200 demographic and population fields per district into a queryable Postgres schema, and implemented the multi-field filtering that lets researchers compare district composition against redistricting-fairness measures interactively.

## Marine species classifier

1st place, W&M AI Case Competition ($1,000) · October 2025

A YOLO model classifying 11 marine species in non-sequential ocean-floor imagery at 95.6% validation accuracy, with a web interface for bulk upload and result tracking so researchers could work through large unordered image sets in one pass. Scoped for the Virginia Institute of Marine Science.

## Hackathons

**Sales automation platform** — Y Combinator Full Stack Hackathon, January 2026. Django/React platform that classifies inbound sales messages with an LLM and auto-generates contextual replies across a managed pipeline.

**EcoLens** — &Hacks. Best Use of MongoDB.

---

## Tools

**Languages** — Python, TypeScript, JavaScript, Java, SQL

**Frameworks** — React, Vite, Node.js, FastAPI, Django, LangChain, MCP, YOLO/Ultralytics

**Infrastructure** — PostgreSQL, MongoDB, MySQL, Docker, Linux, Git, Mapbox GL, Vercel

## Elsewhere

Public Relations chair for ACM at William & Mary — digital communications for 500+ members, 5–7 weekly office hours tutoring and advising students, and a student–faculty research networking event that drew over 100 people.

Assistant swim coach at Vienna Aquatic Club, summer 2026 — practices and meet operations for a 200-athlete program, ages 5 to 18, across a 10-week season.

---

Much of the work above lives in lab or private repositories, so the public repos here don't represent it. ChainOpt is live at [chain-opt.vercel.app](https://chain-opt.vercel.app). Happy to walk through any of it — jcaldwell@wm.edu.
