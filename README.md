<h1 align="center">ChatHub</h1>

<p align="center">
  One chat interface across OpenAI, Anthropic, Google and local Ollama models —<br/>
  with tools, web search, custom assistants, and your keys never leaving the browser.
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=mgmFd9FIu7M"><img src="https://img.shields.io/badge/watch%20the%20full%20build-12h%2020m-FF0000?logo=youtube&logoColor=white" alt="Watch the build"></a>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/Ollama-local%20models-000000?logo=ollama&logoColor=white" alt="Ollama">
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=mgmFd9FIu7M">
    <img src="https://img.youtube.com/vi/mgmFd9FIu7M/maxresdefault.jpg" width="720" alt="Build Your AI Chat Platform — the full 12-hour build">
  </a>
</p>

---

## What it does

**Every model, one thread.** GPT-4o, GPT-4 Turbo, Claude 3 Opus / Sonnet / Haiku, Gemini 1.5 Pro and Flash,
and anything served by a local Ollama instance — switched mid-conversation without losing context.

**Your keys stay yours.** API keys are entered in the app and stored in the browser's own IndexedDB.
There is no server-side key store, and no proxy that sees your traffic. The only server credential this
project needs is Supabase.

**Tools the model can actually call.** Web search through DuckDuckGo or Google, a calculator, DALL·E image
generation, and a memory tool that persists facts across sessions. Tools are opt-in per assistant.

**Custom assistants.** Create a named assistant with its own system prompt, model, and enabled tools.
Save it, edit it, switch to it.

**A real editor.** Markdown with syntax-highlighted code blocks, image attachments, voice input via Whisper,
a live token counter, and a prompt library you build up as you go.

**Tunable.** Temperature, top-p, top-k, max tokens, message-history limit and system prompt, all per assistant.

## Stack

| | |
|---|---|
| Framework | Next.js, TypeScript |
| Orchestration | LangChain — `@langchain/openai`, `@langchain/anthropic`, `@langchain/google-genai`, `@langchain/community` |
| Local models | Ollama, default `http://localhost:11434` |
| Persistence | IndexedDB for keys, preferences and sessions; Supabase for the rest |
| UI | Tailwind CSS, Radix UI, Framer Motion, TipTap |

## Running it locally

```bash
git clone https://github.com/kuluruvineeth/chathub.git
cd chathub
npm install
```

Create `.env.local`:

```bash
SUPABASE_URL=
SUPABASE_ANON_KEY=
```

```bash
npm run dev
```

Open <http://localhost:3000>, then add your model API keys in **Settings** — they are stored locally in your
browser. To use local models instead, run `ollama serve` and point the Ollama base URL at it in Settings.

## Watch it being built

**[▶ Build Your AI Chat Platform — full build (12h 20m)](https://www.youtube.com/watch?v=mgmFd9FIu7M)**
· [Condensed version (18m)](https://www.youtube.com/watch?v=KCd_bdnJ1SE)
· [Full playlist, 27 parts](https://www.youtube.com/playlist?list=PLcAVdtHk_JSRQsVk43iGBwo_jHPT5JKAC)

| | |
|---|---|
| [Custom assistants](https://www.youtube.com/watch?v=ZmTY15p_fRg) | [Live web search in chat](https://www.youtube.com/watch?v=-I7ayR3vnv8) |
| [Image generation plugin](https://www.youtube.com/watch?v=stN78YnCS8Y) | [Markdown and code rendering](https://www.youtube.com/watch?v=Tp-VBwI-qR8) |
| [Prompt library](https://www.youtube.com/watch?v=15UthK3aeJI) | [Advanced settings](https://www.youtube.com/watch?v=efq0gnQsaGk) |

ChatHub is also part of [**Open Studio**](https://openstudio.tech), an open AI ecosystem —
[see the changelog](https://www.youtube.com/watch?v=ilusFyzqHQ8).

---

Built by [**@kuluruvineeth**](https://www.youtube.com/@kuluruvineeth) — I build AI products and take them apart on camera.
