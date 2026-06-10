# Why Epistemology Matters for an AI Engineer 🍵

> A short learning report on why knowledge theory is core engineering knowledge, not abstract philosophy. Built from my reading of Jennifer Nagel's *Knowledge: A Very Short Introduction* and my own responsible-AI and RAG notes.

**Live page:** anp-exe.github.io/knowledge-in-ai/

![status](https://img.shields.io/badge/status-complete-e4548f)
![topic](https://img.shields.io/badge/topic-epistemology%20%C3%97%20AI-a855f7)
![made with](https://img.shields.io/badge/made%20with-plain%20HTML%20%2B%20CSS-f7c6dd)

## The thesis

An LLM emits claims but has no concept of truth. Hallucinations come from next-word sampling: the model produces plausible text with no fact-checker. Plausibility is not truth. So if a model cannot tell a justified true belief from a lucky guess from a confident fabrication, the engineer has to build the part that does. Epistemology is the field that already worked that out.

The core idea I keep coming back to: when you ground a model on unlabelled web data, you pour in fact, knowledge, and opinion all wearing the same clothes. A tokeniser cannot tell them apart. To make a model decipher them, you need an explicit theory of what separates them. That theory is epistemology.

## What's inside

| File | What it is |
|------|-----------|
| `epistemology-for-ai-engineers.html` | The interactive report. Berry pink, three live demos. |

Three interactive bits on the page:

- a **JTB switchboard** for flipping Belief / Truth / Justification and watching knowledge appear (with a Gettier warning)
- a **contextualism stakes slider** that walks trust thresholds from film-rec to legal to medical
- a **fact / knowledge / opinion** epistemic-filter diagram

## Three ideas from Nagel, mapped to engineering

- **Gettier** → a true, cited, believed RAG answer can still be right by luck. Faithfulness evaluation rules that out.
- **Testimony** → every retrieved chunk is testimony; a vector DB is a testimony engine. Reductionism is source scoring and reranking.
- **Contextualism** → "know" shifts weight with the stakes, so trust thresholds should too. One principle, three deployment settings.

## Run it locally

It's a single static HTML file, so no build step:

```bash
# clone, then just open the file
open epistemology-for-ai-engineers.html
# or serve it
python3 -m http.server 8000
```

## Deploy on GitHub Pages

1. Push these files to a repo.
2. Settings → Pages → deploy from `main`, root.
3. Rename `epistemology-for-ai-engineers.html` to `index.html` (or keep the name and link to it directly).

## Sources

- Jennifer Nagel, *Knowledge: A Very Short Introduction* (the reading this is built on)
- My responsible-AI and RAG study notes (hallucination, veracity, grounding)

---

Made by Anna · AI & Philosophy 🍵