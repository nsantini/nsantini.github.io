---
title: Vibe Coding Part Deux
date: 2025-06-07
---
## Context

Back to experimenting with AI Agents for coding, following up from my [[Vibe Coding Experiment]] post.

This time I wanted to start testing an idea: Using AI Agents for coding seem to be very straightforward for green fields and small codebases. What if we use the concepts of `microservices` and `micro frontends` to achieve our bigger goals?

The idea is this: create a micro frontend application, where I can then use AI Agents to code new features/tools that get registered and run as part of the larger application. If we manage to modularise and encapsulate each feature/tool, then we should be able to get the most benefit from the AI coding tools.

## Process

I followed the same approach as with my previous experiment. Using a three steps process: generate PRD, generate task list, execute task list.

For record keeping, I added the exported Cline tasks to the [project repo](https://github.com/nsantini/vibe-micro-frontend/tree/main/tasks)

### PRD

This time my PRD prompt was:

>Create a PRD for the feature I want to build: I want to establish the foundation for a microfrontend application. Where in the future I will creating multiple features, each feature will be implemented as a microfrontend application. The goal of this PRD is to establish the foundation for the microfrondend architecture.  
>We will be using NextJS to build each feature. And Material UI for the presentation layer.

I ran this on GitHub Copilot using GPT-4.1. The follow up questions were:

	To create a thorough PRD for establishing the foundation of a microfrontend application using Next.js and Material UI, I need to ask a few clarifying questions:
	
	1. What is the main problem or pain point you want the microfrontend architecture to solve? (e.g., independent deployment, team autonomy, scalability, etc.)
	2. Who are the primary users or stakeholders of this foundation? (e.g., developers, product teams, end-users)
	3. What are the key actions or capabilities you expect from the foundation? (e.g., routing between microfrontends, shared authentication, design system integration)
	4. Can you provide a few user stories from the perspective of developers or teams who will use this foundation?
	5. What are the acceptance criteria for considering the foundation "successfully implemented"?
	6. Are there any specific things that should be out of scope for this initial foundation (e.g., no cross-app state management, no SSR for all microfrontends)?
	7. What kind of data or configuration will the foundation need to support or expose?
	8. Are there any existing design mockups, architecture diagrams, or UI guidelines to follow for the shell or shared components?
	9. Are there any technical constraints or dependencies to consider (e.g., deployment platform, monorepo vs. polyrepo, CI/CD requirements)?
	10. Are there any edge cases or error conditions you want to highlight (e.g., what happens if a microfrontend fails to load)?
	
	Once you answer these, I’ll draft a detailed PRD for you.

To which I answered:

	1. I want to be able to use AI Agents to help me build each feature, but avoid the complexity of an ever growing code base to add each feature on.
	2. Developers
	3. Should provide all the scafolding code, routing for features to be registered to, and navigation. With a simple "home page" microfrontend to show how to use it
	4. As a developer, I want to be able to easily create and integrate a new microfrontend into the application
	
	That's all we need for now

The outcome PRD can be seen [in this md file](https://github.com/nsantini/vibe-micro-frontend/blob/main/tasks/prd-microfrontend-foundation.md)

### Tasks

Generating the tasks was straightforward, the outcome is [this md file](https://github.com/nsantini/vibe-micro-frontend/blob/main/tasks/tasks-prd-microfrontend-foundation.md). 
The file [`cline_task_jun-7-2025_9-20-24-am.md`](https://github.com/nsantini/vibe-micro-frontend/blob/main/tasks/cline_task_jun-7-2025_9-20-24-am.md) Shows the task list generation prompt.

### Execution

Here is where things get more interesting. You can browse the whole agent history in [`cline_task_jun-7-2025_9-46-07-am.md`](https://github.com/nsantini/vibe-micro-frontend/blob/main/tasks/cline_task_jun-7-2025_9-46-07-am.md)

Things worked mostly well. But I encountered a couple of issues.

First, while trying to install Jest for unit testing, we ran into dependency version issues. For the sake of brevity I decided to skip the unit testing steps. But that's something that would have to be ironed out for a non-toy project.

Second, because I asked to use NextJS, the micro frontend registration process didn't work on the first go. The issue was that the registration code was being called from the Layout component. But NextJS executes this code in the backend, part of its "out of the box" SSR. So the Navigation was not showing me the Home sample application.

So I asked the Agent to solve this issue, as seen in [`cline_task_jun-7-2025_10-36-52-am.md`](https://github.com/nsantini/vibe-micro-frontend/blob/main/tasks/cline_task_jun-7-2025_10-36-52-am.md). All that had to be done was moving the registration call from the Layout to the Navigation component, that was registered to only run in the client with `"use client"`.

## Conclusion

It was a good first step for my larger experiment. I now have a working micro frontend application.

The next step is to start generating micro frontends with features/tools. And have the Agent integrate them.

The goal is to prove the idea that by splitting the work this well, the Agent will be able to better handle the work.