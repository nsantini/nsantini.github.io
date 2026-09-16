---
title: Vibe Coding Experiment
date: 30-05-2025
feed: show
img: vivecoding.jpg
---
## Intro

Watching this [How I AI](https://www.lennysnewsletter.com/p/a-3-step-ai-coding-workflow-for-solo) video was very inspiring to try something new. The key idea is to follow a repeatable process, that resembles what we would do in a "normal" SDLC, and use *instruction files* to guide the AI to do each step.

The process is:
- Generate a PRD with the idea, whether is a brand new project or an addition to an existing one.
- Create a comprehensive list of tasks to meet the PRD.
- And finally execute the tasks linearly.

Not too shabby, but quite effective as it turns out. The key is to make sure to take our time in between steps to evaluate the outcome and amend them as required. So not quite "100% vived", but more like a supervised vive.

## Application

The video shows how to use Cursor on Agent mode to accomplish this process. Now, I don't have a Cursor license to do the same. But I do have access to some API Keys, and the Cline extension on VS Code does pretty much the same.

So, after copying the author's instruction files in the right location for Cline, I was able to start the experiment.

I wanted to try a few different models. So the first thing to do was to come up with an idea/request that I could repeat consistently on step 1. That way I would be able to compare results after each iteration.

The idea was:

>Create a simple note taking application, that stores individual notes as markdown files in the server, and uses Material UI to create a modern looking interface.

Simple, but with enough nuance to make it a good small experiment.

## Execution

### Test 1

For the first test I used OpenAI's o3 for all the steps. It did the job, but the outcome did not include Material UI; instead, it was a "plain" html UI. But it worked.

I tried to iterate on it by creating a new PRD that would refactor the application to include Material UI. But it did not work as expected. I still have some tricks to learn for working with existing codebases, however small they were.

### Test 2

On the second test I decided to try something different. I took the PRD and gave it to Vercel's V0 (free version) to do the work. The outcome was indeed a lot better. Clean and modern UI.

So I downloaded the generated code, opened it in VS Code, and tried to run it. No luck :(.

I had to "fix" some of the conflicting dependencies regarding React's version to get `npm i` to work.

Then I kept getting this obscure error about Client Components not being able to be feed Functions directly

`Error: Functions cannot be passed directly to Client Components unless you explicitly expose it by marking it with "use server".`

After some browsing, I've found that I needed to make the `Layout` be a client component. And stop relying on some of the server side magic from NextJS. And we were off to the races.

It was mostly functional. Just needed some tweaks.

### Test 3

With the V0 version 80% there, I decided to try to use Cline to iterate over it. I generated a new PRD to present the notes using a Markdown library, rather than the raw file. I used Open AI o3-mini to do this step, and the task generation step.

Then, when it came time to execute the tasks and generate the code, I switched to Gemini 2.5-pro-preview. And it worked surprisingly better than o3. Tho this was the most expensive step in the whole experiment, $4 to do the refactoring.

The surprising thing was, Cline used an embedded browser to test its work. It even navigated around the app and created notes to test. Although it needed help to click on the "view" button to confirm that the note was being rendered as expected. So I ended up skipping that step in the end.

Finally, I used Cline to run some refactoring. Like splitting the page into individual components, and some other tidy ups.

## Conclusion

Overall it was a good learning experience. Showcased what could be done with a small amount of effort on my behalf. But that the effort is required.

Also, it showed me that the tooling landscape is still very fluid. There are no clear winners. And that we might need to try different approaches with different tools to get the desired outcome.

Now, was this less effort than just doing it myself? Hard to tell. I think its a good approach to bootstrap an idea. But certainly requires knowledge and handy work to get a great outcome out of it.

I can see the appeal of this approach for people with product but not coding knowledge. They can get a lot done this way. But how far can this applications really go. Are they production ready? I doubt it.

Regardless, it was important to me to test the approach and learn its potential. Whether to apply it, or to argue against it, hands on experience is what will make a difference.

## Footnote

I will write another post going through the details of setting up the tools, and posting the code outcomes. This was more of a reflection brain dump while it was fresh in my mind.