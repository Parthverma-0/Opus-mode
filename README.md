# 🧠 Opus Mode

**Make any AI think like Claude Opus.**

A tiny set of copy-paste prompts that reshape how ChatGPT, Gemini, Cursor, Antigravity, or any other model *behaves* - so it reasons before it answers, tells you the truth instead of flattering you, and writes like a sharp human instead of a content mill.

No install. No API key. No extension. Copy one block, paste it where your AI takes instructions, done.

---

## ⚡ 30-second start

1. Pick your tool below.
2. Copy the prompt.
3. Paste it into your model's system prompt / custom instructions / rules file.
4. Watch it stop saying *"Certainly! I'd be happy to help with that!"*

| Tool | Where it goes | File |
|------|---------------|------|
| ChatGPT | Settings → Personalization → Custom Instructions | [`prompts/chatgpt.md`](prompts/chatgpt.md) |
| Gemini | Create a Gem → Instructions | [`prompts/gemini.md`](prompts/gemini.md) |
| Cursor / Antigravity | `.cursorrules` / rules file in repo root | [`prompts/cursor-antigravity.md`](prompts/cursor-antigravity.md) |
| Anything else | System prompt / first message | [`prompts/system-prompt.md`](prompts/system-prompt.md) |

---

## 🪞 Before / After

**You:** *Is it fine to store JWTs in localStorage?*

**Default assistant:**
> Great question! Storing JWTs in localStorage is a common approach with several advantages. Here are some considerations: 1) **Convenience** ✅ ... 2) **Persistence** ✅ ... 3) **Simplicity** ✅ ... Ultimately, it depends on your use case!

**Opus Mode:**
> Usually no. localStorage is readable by any JavaScript on the page, so one XSS bug hands an attacker your token. Prefer an httpOnly, Secure, SameSite cookie so the token is never exposed to JS. The exception is if you're not in a browser at all (e.g. a native app) — then the XSS surface doesn't exist and localStorage-equivalent storage is fine. What's your client?

Same model. Different behavior.

---

## 🤔 The honest part

This does **not** turn GPT-4 or Gemini *into* Opus. You can't swap the underlying model with a paragraph of text — capability is baked into the weights.

What it **does** do is steer *behavior*, which is where most of the "Opus feels different" reaction actually comes from:

- **Think first.** Reason through the problem instead of pattern-matching to a familiar-looking answer.
- **Honest > agreeable.** Say what's true, not what's flattering. Push back when you're wrong. Admit "I don't know."
- **Write like a human.** Natural prose over bullet soup, bold-everything, and emoji headers. Cut the hype and the *"Certainly!"* throat-clearing.
- **Calibrated length.** Short question, short answer. No padding.
- **Respect the reader.** Assume the person is smart. Warm, never sycophantic.
- **One good question** when something's genuinely ambiguous — instead of guessing or interrogating.

You're not cloning the model. You're cloning the *manners.* That turns out to be most of it.

---

## 🧩 The principles, in full

The complete prompt lives in [`prompts/system-prompt.md`](prompts/system-prompt.md). Everything else here is a trimmed-to-fit version of that same core for a specific tool.

---

## 🛠️ Contributing

Got a variant that works better on a specific model? A condensed version that fits a tighter character limit? A killer before/after example? PRs welcome. Keep prompts original (no leaked/proprietary system prompts) and keep the tone the prompts themselves preach: tight, honest, no fluff.

MADE BY PARTH ❤️

## 📄 License

MIT - do whatever you want with it. A ⭐ is appreciated but never required.
