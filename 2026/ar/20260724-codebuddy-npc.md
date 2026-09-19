# Tencent Cloud's New Play: AI Becomes an NPC to Help You Write Code

## I.

I once imagined that NPCs (non-player characters) in future games would be AI — entities you could interact with and even command to do tasks for you.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072501.webp)

What I never expected was that the first to realize this idea would be Tencent Cloud — but not for gaming. Instead, it uses NPCs to write code and do development.

They launched a [major upgrade](https://www.oschina.net/news/477664) to their AI coding tool CodyBuddy, called **CodeBuddy NPC**.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072502.webp)

Once you log into the platform, you can direct a group of NPCs (various AI models) to carry out tasks.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072503.webp)

The screenshot above shows [four NPCs summoned simultaneously](https://cnb.cool/npc/CodeBuddy/-/issues/57), each assigned the same task — four runs in total.

Each NPC's name is followed by the token count and cost for that run, as if reminding you not to go over budget.

Although the official description doesn't explicitly invoke game metaphors — calling it the developer's **"cloud-based AI teammate"** — I think it is essentially an open-world cloud environment. You log in, play the "coding game," and can summon NPCs at will.

It is also a "cloud game": everything runs in the cloud, independent of your local machine and environment. You can brief your NPCs and then walk away from your computer entirely, checking progress from any device later.

After trying it out, I found this to be the simplest AI development solution available today. **No setup or installation needed — just a browser** — and the cloud functionality is comprehensive. **If you choose free models, it costs nothing.**

## II.

Using CodeBuddy NPC currently requires Tencent Cloud's [CNB platform](https://cnb.cool/).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072504.webp)

CNB stands for "Cloud Native Build," but don't worry about the name — it is essentially Tencent Cloud's GitHub alternative for code hosting.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072505.webp)

Above is [its repository homepage](https://cnb.cool/yifeng.ruan/codebuddy-test-webpage) — it looks nearly identical to GitHub.

Tencent reportedly uses this platform internally. It has now been opened up with a public version for external use.

It may not have been as powerful as GitHub before, but with CodeBuddy NPC added, I think it is at least better in the AI department. The examples below will show I'm not exaggerating.

**CodeBuddy NPC effectively lets you use natural language to operate all functions of the underlying code platform**: committing code, managing issues, merging PRs, continuous builds, and more. It will completely change the way you use a code platform.

## III.

CodeBuddy NPC uses natural language to summon an NPC, requiring a place to enter prompts. A repository's issue tracker is the natural entry point.

Here is the simplest Hello World example. Create an empty repository on the web, go into it, open a new issue, and write your intent — for example, "Create a website introducing Beijing tourism."

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072601.webp)

Then assign an NPC to complete the task.

The system includes multiple built-in NPCs (AI models). Just type `@` and a popup will list the available NPCs.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072602.webp)

The official programming assistant `CodyBuddy` is currently available for free.

There is also an `npc/CodeBuddy` group containing various domestic models.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072603.webp)

Tencent's Hy3 is free; others list their pricing. Let's pick the free Hy3.

After selecting the NPC, submit the issue. The NPC runs automatically and, once finished, posts a reply to the current issue explaining what it did.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072605.webp)

The underlined section shows token consumption and cost. Clicking in shows the NPC's detailed logs.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072606.webp)

At this point, the [generated code files](https://cnb.cool/yifeng.ruan/codebuddy-test-webpage) have already been committed to the repository automatically.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072607.webp)

The whole process requires only opening a new issue — everything else is handled automatically. If needed, a deployment script can also be generated to publish the result. Could it be any simpler? And all of it is free.

## IV.

The CNB platform integrates multiple capabilities alongside CodeBuddy to cover almost any need without requiring other tools.

In the top-right corner of the repository homepage there is a "Cloud-Native Dev" button that provides an IDE environment for manually reading or modifying code.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072608.webp)

Clicking it shows a dialog.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072610.webp)

The dialog has three rows: Web IDE (manual), Cloud Agent (AI-operated), and external IDE apps (CodeBuddy IDE / VSCode / Cursor).

Selecting "Web IDE" opens an online editor similar to VSCode.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072611.webp)

There is a preview button in the top-right corner (not shown in the screenshot). Clicking it opens a new browser window to preview the generated result.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072612.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072613.webp)

## V.

CodeBuddy NPC can handle a wide variety of tasks. Essentially, any common operation you do on GitHub can be delegated to an NPC.

**(1) Permissions**

When posting an issue, there is a "Work on my behalf" toggle in the menu bar.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072614.webp)

It defaults to on, meaning the NPC uses your permissions to act for you. If you have commit access, the generated result is committed directly to the repository.

Turning it off causes the result to be submitted as a PR instead (see below), requiring manual approval before merging.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072615.webp)

**(2) Code conflicts**

After a PR is submitted, merge conflicts may arise. You can simply ask the NPC to resolve them.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072618.webp)

**(3) Feature development**

You can open an issue requesting new features and have the NPC implement them.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072619.webp)

**(4) Team collaboration**

Multiple NPCs can divide and conquer work together — see [this example repository](https://cnb.cool/examples/twine-team-demo).

It defines 8 NPCs that collaborated to complete a game.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072620.webp)

The key role is the "Project Manager," which automatically breaks down the PRD from the issue into subtasks, assigns them to other roles, and triggers each NPC via system events until all tasks are complete.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026072621.webp)

The kanban view shows real-time progress on all subtasks.

## VI.

After two days of use, I think CodyBuddy NPC is very creative. Using AI as NPCs is a fitting metaphor — it really does feel like a virtual teammate for developers, evolving from an assistant tool to independently handling development tasks.

More importantly, **it is deeply integrated with the CNB code hosting platform, elevating development automation to a whole new level**. Nearly all major GitHub functions — development, Git operations, issues, PRs, CI/CD — can be triggered through natural language.

CodeBuddy NPC automatically treats the current repository as context, submits it to the model, and runs everything in an isolated sandbox. According to the official documentation, a built-in token optimization tool compresses the repository context as much as possible to control token usage.

Try this latest form of "cloud game" and experience what it feels like to command NPCs.

(End)
