# When Office Suite Meets AI Agent: Introducing the Open-Source Feishu CLI

## I. Introduction

Before this year's Spring Festival, OpenClaw suddenly exploded in popularity, prompting various cloud services to open their APIs for integration.

One very important category of software also opened their APIs during this period, but didn't receive much external attention: office suites.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051409.webp)

Imagine — once office documents achieve AI automation, how much work and processes could be simplified? And what a huge market that would be!

I recently had a need in this area — wanted AI to automate document management in the cloud — so I searched for office suite toolkits that could integrate with Agents.

Here are my findings:

- [Google Workspace CLI](https://github.com/googleworkspace/cli)
- [Feishu CLI](https://github.com/larksuite/cli)
- [DingTalk CLI](https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli)
- [WeCom CLI](https://github.com/WecomTeam/wecom-cli)

These four open-source toolkits all allow users to call APIs from the command line to operate their cloud SaaS services.

Among them, Google Workspace CLI is semi-official — maintained by one of their engineers personally. The other three are all official projects.

Among these three domestic office suite toolkits, [Feishu CLI](https://github.com/larksuite/cli) stands out.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051502.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051501.webp)

As shown above, all three were released around the same time, but Feishu has the most comprehensive features, the largest project scale, and the highest Star count.

I've been using [Feishu CLI](https://github.com/larksuite/cli) for a few days, and it feels great. If you also want to **integrate office suites with Agents for office automation**, it might be the easiest tool among these three to meet your needs. Here's my brief introduction.

## II. Basic Information

First, Feishu CLI is a very new tool, released on March 28 this year — just over 40 days ago.

Its development pace is very active, with 30 versions already released — roughly one new version per working day. If you ask questions or request features in the repository, you get a quick response, which is reassuring.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051401.webp)

Second, this toolkit is quite comprehensive — it can operate almost all of Feishu's existing business domains, with over 100 capabilities.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051402.webp)

The image above shows the 17 business domains it currently supports, covering all aspects of enterprise office work. In my opinion, its biggest selling point is this: you can use the API of a specific business domain or capability right out of the box, or you can deeply orchestrate multiple capabilities to **customize cross-domain workflows** for complex business automation.

Finally, it's a fully open-source international project using the MIT license, with virtually no usage restrictions. There are a significant number of external code contributors — I've seen many external PRs merged into the main branch.

## III. Project Structure and Skill Packaging

Code-wise, this project uses a multi-layer packaging structure.

The bottom layer is [Feishu OpenAPI](https://www.feishu.cn/content/785259988660), showing each specific API interface, including parameters, return values, error types, etc.

The second layer is the command layer, with each command mapping one-to-one to an OpenAPI definition.

The third layer is the shortcut layer, which wraps the command layer, providing default parameters, simplifying call syntax, outputting easy-to-read formats, and being user-friendly with a lower barrier to entry.

Beyond these three layers, there's a separate Skills section — capability extension packages packaged for Agents, including specialized scripts and prompts, greatly facilitating AI calls. It currently has 24 built-in Skills, representing official best practices.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051403.webp)

## IV. AI Agent Integration

This project is developed in Go and packaged as an npm package. [Installation](https://github.com/larksuite/cli#quick-start-human-users) uses npm commands.

```bash
$ npx @larksuite/cli@latest install
```

However, a better and simpler installation method is to [use natural language](https://www.feishu.cn/feishu-cli) and let the Agent install it itself.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051404.webp)

The entire installation process is automatic, but login and authorization need to be done manually.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051406.webp)

After installation, the Agent can control your Feishu account, allowing you to directly assign tasks for AI to execute.

Below is a test example: within Claude Code (or another Agent), ask AI to [summarize recent documents](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647681090&idx=1&sn=70ff1397460421defa4dcbdf85d77012&scene=21&poc_token=HMNHBWqjDq0LhaY45evquLnZK3LfIx2kk6KaoeFk) (shown below).

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051405.webp)

## V. Typical Capabilities

This tool can do many things. Here are a few examples. There's also an official [Feishu CLI's 100+ New Skills](https://bytedance.larkoffice.com/wiki/CLNjwBozvi11IjkeChOcltHinye) capability list for reference.

(1) Document Features: I usually write Markdown documents, but Feishu uses a visual editor. You can submit Markdown source to AI and have it call Skills for formatting and publishing.

> [Prompt]
> Create a Feishu document from this Markdown content, make it look good.

Feishu supports document comments, which we generally use to post revision suggestions. You can have AI automatically modify documents based on comments.

> [Prompt]
> {{document link}} Modify the document based on comments. After modification, use inline comments to mark the changes.

You can also have AI generate revision suggestions for documents.

> [Prompt]
> {{document link}} Read this document and assess whether it's clear and concise enough as a user-facing documentation. Don't modify the document directly — only use inline comments to mark areas for improvement with suggested revisions.

(2) Whiteboard Features: Whiteboards are mainly used for generating editable flowcharts, framework diagrams, sequence diagrams, etc. You can have AI generate corresponding graphics based on document content and insert them.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051407.webp)

(3) Slideshow Features: It provides pre-built Feishu PPT templates, currently over 40 — more than enough. You can specify a template to convert documents into slides.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051408.webp)

(4) Workflows: A workflow is a multi-step operation process spanning multiple business domains — for example, having AI get the participant list of a group chat, check each participant's calendar to find free time, and schedule an online meeting.

> [Prompt]
> Check the calendars of everyone in the [XX] group, then find a time next week when everyone is available for a one-hour discussion meeting.

Another example: having AI check your inbox and forward important unread emails to a discussion group.

> [Prompt]
> Check all my unread emails. Send summaries of important ones to the [XX] project group.

## VI. Conclusion

If you're already a Feishu user, I believe this [Feishu CLI](https://github.com/larksuite/cli) is an essential tool. Paired with an AI agent, it greatly enhances the practicality and convenience of your office suite.

If you haven't used Feishu yet, considering it's free and all its infrastructure is open to agents through this toolkit, it seems a shame not to use it.

It's clear that the official team places great importance on this project, investing heavily and developing intensively to capture the Agent market. I think they'll keep at it long-term.

Additionally, since the project uses the MIT license and can be used commercially, it's also an opportunity to leverage Feishu's infrastructure to develop secondary applications and explore the enterprise office software market.

(End)