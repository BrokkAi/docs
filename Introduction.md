**Brokk** (the [Norse god of the forge](https://en.wikipedia.org/wiki/Brokkr?ref=blog.brokk.ai)) is the first code assistant that understands code semantically, not just as chunks of text. Brokk is designed to allow LLMs to work effectively on large codebases that cannot be jammed entirely into working context.

To accomplish this, the Brokk team has broken free of the past forty years of IDE design to rethink how a human engineer can most effectively supervise an AI assistant. With Brokk, your job is not to read and write code a line at a time but to supply the LLM with the appropriate knowledge of the codebase so that it can handle the tactical details of code production.

## How it Works

Unlike other AI tools that treat your source code as plain text, Brokk performs compiler‑grade static analysis to give large‑language‑models (LLMs) **semantic awareness** of classes, methods, call‑graphs, and stacktraces. Brokk mixes that with the ability to understand Git history and even decompiled dependencies to provide more intelligent answers, fewer hallucinations, and higher‑quality edits on very large projects.

![](images/introduction-how-it-works-1.png)

The Brokk Interface

Next: [Quick Start](/documentation/quick-start)