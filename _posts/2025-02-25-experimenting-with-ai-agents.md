---
title: Experimenting with AI Agents
date: 2025-02-25 20:45 +1300
---

## Context and the experiment

After getting the [DeepSeek reasoning models running locally](https://blog.santini.nz/2025/01/31/experimenting-with-r1-locally), I wanted to go further in my hands-on understanding of AI Agents.

Now, there are a lot of AI Agent frameworks coming out of the wood works left, right, and center. So choosing one to experiment with is not an easy task. So I made the choice to go with one that seemed to be growing in popularity in the online circles I frequent. [LlamaIndex](https://www.llamaindex.ai/).

I have to say that it was a breeze to get started. Their learning tutorials were quite good. And in little time I had a few things going.

First, I created an embedding index with my blog posts (markdown files), and was able to ask questions about them. Then, I took it a step further and made that index (the basics for a RAG system) part of an Agent's toolset. It kept on working. Finally, I added one of their Agent Tools to the list, a DuckDuckGo search tool. And it all started to work together as I expected it to.

I took the experiment a bit further by putting the Agent behind a simple API, to run my tests using PostMan. With the idea that it would be the basis for creating a simple web application. And it was at this point that many things started to become very clear to me.

## Realizations and insights gained

1.  The state of tooling around Large Language Models is such that it makes it very easy and accessible for teams to not only experiment, but to develop and deliver features in their products. All this without requiring special skill sets, like what we came to know as Data Scientists or Machine Learning Engineers. And it will only become easier as time passes. Not only to use LLMs, but going Multi Modal too.
2.  The biggest hurdle to clear is to have a clear use case to apply this technology to. An actual problem for which GenAI is a good solution to apply. With that as a starting point, then it's a matter of applying true and tested software development practices.
3.  The biggest challenge to implementation is not coding, but delivering a useful UX that actually adds value to the intended audience. And solves the problem in an accessible way. It's very important that we keep [good principles](https://blog.santini.nz/2025/02/11/building-good-ux-in-ai-products) in mind when developing such features.
4.  There is no need to "move fast and break things". There is enough AI slop out there already. We can actually think things through and avoid falling into FOMO. Start with why.

## Conclusion

It was fun to get deep in the weeds and gain a working understanding of how easy or hard implementing AI Agents has become. To be able to discern where the attention needs to be placed on. And what will be the most important aspects to consider when developing solutions using this technology.

The hype is still very high around all this. And there is a lot of snake oil salesman poisoning the well of knowledge. It is therefore super important to experiment and gain first hand experience with this technology. So that we can make better informed decisions. And also help educate those around us about it.