# Is the IDE Dead? Starting from TRAE's Two-in-One Merge

## I. TraeCode and TraeWork Merge

I saw some recent news: TraeWork and TraeCode have merged and been upgraded into the new [TRAE](https://www.trae.cn/) client.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100605.webp)

This surprised me, because TraeWork was originally split off from the TRAE IDE — it feels like only a few months ago — and I did not expect another upgrade so soon.

But on reflection, it makes sense. In the AI era, the product form of the IDE has long been uncertain; rapid change is the norm.

## II. The IDE in the AI Era

Have you noticed that **(traditional) IDEs may already be dead**? This is something I have been thinking about for the past few months.

Hand-coding requires an IDE, but the future is AI coding — you can build software without touching code at all. In that case, the IDE is no longer necessary.

The AI era needs different development tools. Someone has given this new kind of tool a name: ADE, an Agentic Development Environment.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100606.webp)

The problem is that nobody knows yet what an ADE looks like — what interface it should have, what features it should offer. Everyone is still exploring.

Taking this TRAE upgrade as an opportunity, I want to talk about my vision for development tools in the AI era, and what kind of software fits future development needs.

## III. How TRAE's Product Form Has Changed

TRAE was China's first IDE built specifically for AI coding.

Its earliest product form was close to a traditional IDE: a code-file editing window plus AI assistance features such as code generation and code explanation.

In fact, that original form has been kept to this day — only the name has changed to IDE Mode (below).

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100804.png)

The image above shows IDE Mode in the current version. It looks very much like a traditional IDE (such as VS Code), except that there is an AI chat panel on the right.

I consider this **the first form of the ADE: a traditional IDE enhanced with AI**. It still emphasizes code management and suits programmers who still need to read and edit code by hand.

Later, as AI models became more powerful, this form revealed its limitations.

> (1) Besides writing code, AI can generate PRDs, design mockups, tests, documentation, and so on.
>
> (2) AI can break a task down into multiple subtasks and create multiple instances to complete them in sequence.
>
> (3) Multiple AI agents can work in parallel across multiple code repositories.

All of these capabilities are hard to fit into a traditional IDE interface. The IDE needs to change, moving away from a pure code-editing interface to accommodate more functions.

At that point, TRAE added SOLO Mode (below), introducing an entirely new interface. It was one of the earliest domestic development tools to support AI agent coding.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100805.png)

As you can see, SOLO Mode has no code editor by default; the left sidebar is a task list. Based on the steps it is executing, the AI automatically opens the corresponding tool in the right-hand panel.

I call this **the second form of the ADE: the task executor form**. It is task-centric, focused on completing tasks, and no longer foregrounds code features — the editor is just one of its built-in tools.

Up to this point, development tools were still focused on coding and were still code tools. For TRAE, as a leading domestic code tool, it had already built a large user base — but those users were all programmers. It had not yet occurred to anyone that an IDE could also have non-programmer users.

## IV. Agent Mode

Since the beginning of this year, AI has entered a new stage: it can operate external tools to complete all kinds of tasks — for example, ordering milk tea in a delivery app or sending a message in Feishu.

Suddenly, all kinds of AI assistants appeared. The IDE naturally had to follow the trend and began transforming into a tool assistant.

TraeWork was launched against this backdrop. Positioned as an office assistant for ordinary users, it automatically calls various tools to complete office tasks.

Although TraeWork has now been merged into TRAE, its interface and basic functions have barely changed — only the name has changed to "Agent Mode".

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100806.png)

The image above shows the latest version of TRAE's "Agent Mode", which looks a lot like the old TraeWork interface. You can think of it as a work assistant that can load various capabilities and connect to various external tools to help you get work done.

I consider this **the third form of the ADE: the tool connection hub form**. It manages various capabilities and external tools, calling them automatically as needed.

## V. Two Products Become One

Although the task executor form and the tool connection hub form can both accept instructions and complete tasks, their purposes and target users are actually somewhat different.

So TraeCode and TraeWork started out as two separate clients aimed at different users: the former at developers, the latter at office users.

Now these two clients have merged into one. Two products becoming one reflects **a major trend in development tools: downplaying code, turning into general-purpose tools, and serving a broader user base**.

The new TRAE is now a single client, but it contains two modes: IDE Mode and Agent Mode, switchable in the top-right corner (below). Inside IDE Mode you can switch to SOLO Mode.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100703.webp)

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100704.webp)

The division of labor between the two modes is clear.

> **IDE Mode**: focused on code editing for a single project; its SOLO Mode emphasizes AI-assisted end-to-end development for a single project.
>
> **Agent Mode**: a global workbench — one window to manage multiple projects, multiple agents, and multiple tools, with end-to-end "from idea to result" management.

In a sentence: **IDE Mode focuses on code and is for programmers; Agent Mode focuses on tasks and work assistance, and can also be used by beginners who do not understand code**.

## VI. Features of Future Development Tools

As China's earliest tool dedicated to AI coding, TRAE's evolution highlights how thinking about development tools has changed in the AI era.

I believe TRAE reveals several characteristics of future development tools.

**(1) A full-chain development platform**

It covers every step upstream and downstream of AI coding; the entire development chain can be completed with it.

Requirement breakdown, solution generation, page generation, demo implementation — it can do all of it. One tool handles documentation, design, code, and testing, effectively closing the development loop.

**(2) Real-time sync across devices**

It offers desktop, web, and mobile clients that sync in real time, making development possible anytime, anywhere.

**(3) A unified workbench**

One workbench manages all projects, schedules multiple agents to handle tasks in parallel, and advances work across projects, with progress visible at a glance. When deep changes are needed, you can switch back to IDE Mode with one click.

For example, TRAE has a "My Artifacts" page (below) where web pages, slides, documents, spreadsheets, videos, images, and other outputs from various projects can be managed in one place — whether the artifacts are local or in the cloud.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100707.webp)

**(4) Capability extension interfaces**

It provides various channels for extending capabilities and can connect to external services or data. TRAE, for instance, has a plugin marketplace where you can load skills, MCP, and external services.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100705.webp)

For instant messaging apps, it offers a "My Assistant" feature: once connected, you can invoke the AI remotely just by "@Trae".

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100706.webp)

It also provides a template library, with document templates and automation task templates that can be used directly.

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100708.webp)

![](https://cdn.beekka.com/blogimg/asset/202610/bg2026100709.webp)

## VII. Summary

I think the traditional IDE has probably reached its end. With the development of general AI capabilities, **development tools will become less and less code-centric and start turning into general task management tools**.

TRAE shows signs of this: its desktop version still distinguishes between Code and Work modes, while the mobile version no longer does — whatever the task, there is only one entry point.

The target users of development tools will also change drastically.

Professional developers can still use them to boost development efficiency, while small teams and individuals will use them for "full-chain development". Many former "domain tools" will be replaced: project management, design, testing, operations, documentation, PPT, and so on.

More importantly, many ordinary people will start using them too. They do not understand code, but they understand business and products, and they want to build the tools they need. Development tools will use built-in AI agents to help them develop without code and produce demos — doing things that previously required a programmer.

(End)
