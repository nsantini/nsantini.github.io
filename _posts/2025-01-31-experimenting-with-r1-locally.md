---
layout: post
title: Experimenting with DeepSeek R1 Locally
date: 2025-01-31 13:38 +1300
---

After reading a few posts, in particular [Simon Willison’s DeepSeek-R1 and exploring DeepSeek-R1-Distill-Llama-8B](https://simonwillison.net/2025/Jan/20/deepseek-r1/), I took the plunge to install and run DeepSeek R1 on my local machine.

Following instructions from Simon's post and [How to Use DeepSeek R1 in Visual Studio Code with Cline](https://apidog.com/blog/free-deepseek-r1-vscode-cline/), I managed to get everything running this way on my terminal:

1. Install Ollama:

Download it from ollama.com, or install via homebrew like I did, to manage local AI models.

`brew install ollama`

2. Run Ollama:

`ollama serve`

3. Download the model

I went for the 14B model, that seems to be a good enough model to run locally. But there are other options: 1.5B, 8B, 14B, 32B, and 70B. Pick what's best for your use case.

- 1.5B: The smallest and lightest, great for testing or machines with limited resources.
- 8B: A good balance of performance and resource usage, a solid starting point for most users.
- 14B: Stepping up in capability, offering improved performance for more demanding tasks.
- 32B: Getting into the larger, more powerful models, requiring more GPU power.
- 70B: The largest and most intelligent, designed for top-tier performance but needs significant GPU resources.

`ollama pull deepseek-r1:14b`

4. Install LLM Ollama plugin

Using Simon's approach and open source tool, [LLM](https://llm.datasette.io/en/stable/), that I like.

`llm install llm-ollama`

5. Run the LLM chat interface

`llm chat -m 'deepseek-r1:14b'`

6. Profit!

That's it. DeepSeek R1 14B running locally in chat mode!
