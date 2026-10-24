# RAG Playground

An interactive, single-page simulator that shows step by step how **RAG (retrieval-augmented generation)** works, using a support assistant for an online booking and payments app.

**▶ Try it:** https://indhu-natarajan.github.io/my_rag_simulator/rag-simulator-stripe.html

Built by Indhu Natarajan as part of the HelloPM AI Product Management program.

---

## Why I built it

Many AI products answer questions from a company's own documents. As a product manager I wanted to understand what happens between a customer's question and the answer, so I can make better product decisions about it. I chose a help-centre for an online booking and payments app because that is the domain I worked in (bookings, rescheduling, deposits, refunds, card on file).

## What you can do

1. **Edit the knowledge base:** change the help-centre articles or paste your own text.
2. **Chunk it:** move the chunk-size slider and see how the text is split into searchable pieces.
3. **See embeddings:** each chunk gets a (simplified) numeric representation.
4. **Ask a question:** type a customer question, choose how many chunks to retrieve, and see the match scores.
5. **See the prompt:** the retrieved chunks are inserted into the final prompt sent to the AI model.
6. **Get a grounded answer:** the answer cites the chunk it came from, and if the articles don't cover the question, the assistant says it doesn't know instead of guessing.

## What I learned as a PM

- **Chunk size is a trade-off:** smaller chunks are more precise, larger chunks keep more context.
- **Retrieval quality decides answer quality:** if the right chunk isn't found, the AI can't answer well.
- **"I don't know" is a feature:** a trustworthy assistant must refuse to guess when the knowledge base has no answer.
- **Citations build trust:** showing where an answer came from lets users and support teams check it.

## Note

This is a learning simulator. Embeddings, match scores and answers are **simplified and simulated in the browser**; no real AI model is called.

## Versions

I iterated on this from a basic walkthrough to an interactive tool:

| Version | Design inspiration | What changed |
|---|---|---|
| [**v3: RAG Playground** (latest)](https://indhu-natarajan.github.io/my_rag_simulator/rag-simulator-stripe.html) | Stripe | Fully interactive: editable knowledge base, chunk-size slider, own questions, top-K, prompt view, "I don't know" handling |
| [v2](https://indhu-natarajan.github.io/my_rag_simulator/rag-simulator-google-studio.html) | Google Studio | Same walkthrough as v1, trying a different design |
| [v1](https://indhu-natarajan.github.io/my_rag_simulator/rag-simulator.html) | Apple | Step-by-step walkthrough with Back / Next |

Each version is a single HTML file (HTML, CSS and JavaScript), built with AI assistance.
