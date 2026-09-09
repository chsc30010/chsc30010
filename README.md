# Sarath Chandu Chitti

Product manager. I build the things I spec, mostly AI agents and the harnesses that tell me whether they actually work.

Most agent demos are convincing and most agents are not. What separates them is measurement, so that's where most of my side work has ended up: hand-labelled datasets, failure-mode detectors, and CI gates that fail the build when a scoring change quietly makes things worse.

## Projects

**[customer-support-agent](https://github.com/chsc30010/customer-support-agent)**
Phone, SMS, web chat and email through one pipeline. Answers from a knowledge base with citations, and hands the contact to a human when it shouldn't be the one answering. Graded on 60 hand-labelled contacts: every contact that needed a person reached one, and 88% of the rest resolved from the right article. Deciding *not* to answer turned out to be the hard half.

**[agentic-eval-harness](https://github.com/chsc30010/agentic-eval-harness)**
Evaluates tool-using agents on what they did, not what they said they'd do. Records the full trajectory and runs detectors over it: ignored tool errors, prompt injection through tool output, hallucinated tools, runaway loops, dropped sub-goals. No dependencies, exits non-zero, drops into CI. Ships with a deliberately naive agent so you can watch the detectors catch real failures without an API key.

**[personal-rag](https://github.com/chsc30010/personal-rag)**
Retrieval over your own documents (PDFs, Word, Markdown, code, web pages) with inline citations. Ollama runs the model and embeddings, ChromaDB sits on disk. Nothing leaves the machine, which was the reason to build it rather than use something hosted.

**[llm-eval-pipeline](https://github.com/chsc30010/llm-eval-pipeline)**
Run a JSONL dataset of prompts through a model, score the responses, get a report. Provider-agnostic, so adding one means implementing a single interface.

**[pm-skills](https://github.com/chsc30010/pm-skills)**
65 PM skills and 36 chained workflows covering discovery through launch, built on frameworks from Teresa Torres, Marty Cagan and Alberto Savoia.

Private, but happy to walk through: **agentos**, a multi-agent kernel where no agent touches a tool except through a governance gate that enforces risk tiers, budgets, human approval and a hash-chained audit log. A **job-signal agent** that scouts, ranks and briefs openings, graded at 88.9% band accuracy on 45 labelled postings. A **chief-of-staff agent** with persistent memory for inbox triage and meeting prep. A **PRD-to-deck generator**.

## Otherwise

Discovery, strategy, PRDs, launch, growth. Python and JavaScript when it's faster to build the thing than to describe it.
