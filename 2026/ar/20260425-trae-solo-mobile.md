# AI on Mobile: Finally Capable of Real Work

## I. Introduction

How do you use AI on your phone?

In my experience, AI mobile clients have always been very limited — only good for chat conversations, nothing else.

Want AI coding? Sorry — previewing and editing code on mobile is a disaster, and executing code is out of the question. You'd have to open the web version to run code generation.

Just when I thought this was the status quo with no good solution, I unexpectedly saw a new approach last week: TRAE SOLO is getting a mobile version.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050601.webp)

This isn't an ordinary AI mobile version — it's a completely new approach: TRAE has [split](https://mp.weixin.qq.com/s/iN0LUDIGsYeetq_wn1Q8FA) into SOLO as an independent client brand, and it's not just one client, but three: web, desktop, and mobile.

## II. Three-End Interconnection

The biggest feature of this approach is "**three-end interconnection**": these three clients — mobile, web, and desktop — are connected.

You can operate the web and desktop versions from your mobile device. **Actions on any one end are visible on the other two.**

Imagine this scenario: an AI task is running on your office computer, but it's time to go home. Previously, you'd have to wait for the task to finish before leaving. Not anymore. Since the mobile and desktop ends are connected, you can check task progress on the office computer from the subway using your phone. If there are results, you can even remotely operate the desktop from your phone.

Similarly, mobile coding is no longer a problem. You can initiate a coding task from your phone, have the web or desktop version run the code, and just return the results to your phone — bypassing the limitation of mobile devices lacking a Linux environment.

This approach suddenly made it click for me: **the mobile client can become a "remote workstation" for the desktop and cloud** — solving all the problems!

If this succeeds, it could become a trend, and future AI mobile clients may all develop in this direction.

## III. SOLO's Positioning

Let me first explain what SOLO is and how it relates to TRAE.

As you know, TRAE is ByteDance's IDE specifically designed for AI coding, similar to VS Code.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050103.webp)

Previously, SOLO was a mode within TRAE IDE — essentially a workspace for AI tasks where you could initiate, view, and manage various AI coding tasks.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050104.webp)

However, IDE has many limitations — it can't attract non-programmer users, and it can't release a mobile version.

So in April this year, the development team split TRAE into two products: TRAE IDE and TRAE SOLO.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050105.webp)

TRAE IDE focuses on the original AI coding IDE functionality, while TRAE SOLO evolves toward a general-purpose AI client, **positioned as something like an "AI programmer + office assistant."**

The new SOLO mobile version has powerful capabilities, fully suitable for real work: operating local computers, dispatching ideas anytime, accessing work anywhere. Below, I'll share my test results.

## IV. Installation and Interface

As mentioned, TRAE SOLO has three clients — web, desktop, and mobile. My recommendation is to [install](https://solo.trae.cn/) both the desktop and mobile versions, since they're interconnected, maximizing the advantage.

The desktop version has Mac and Windows versions; the mobile version has iOS and Android versions.

It also distinguishes between international and domestic versions with identical features, differing only in models — the international version uses foreign models (paid), while the domestic version uses domestic models (free). Though the domestic models are free, there may be queues during peak times. If you have your own model API key, you can switch to your own models.

After installing on mobile, opening it looks like this:

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050106.webp)

It looks similar to most AI mobile clients — a dialog box. At the top, you can switch run modes: MTC (default) and Code.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050107.webp)

Code is programming mode, which I won't discuss here. MTC stands for "More than Coding" — targeting non-programmer users like product managers, designers, and managers.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050108.webp)

In other words, MTC is the general-purpose mode for everyone.

## V. Test Scenario A: Operating a Local Computer

First, I tested connecting my phone to a local computer for remote operation.

Below the dialog box on the mobile app, you can select the connection target. The default is Cloud.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050109.webp)

When in programming mode, the cloud can also be bound to a GitHub repository.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050110.webp)

Since I needed to connect to a local computer, I switched targets by clicking and selecting "Connect Your Computer."

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050111.webp)

The prerequisite for a successful connection is that your computer is online with the SOLO desktop client open, and both the desktop and mobile clients are logged in with the same account. After a successful connection, it looks like this:

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050501.webp)

At this point, it prompts you to "Select a Folder" — a directory that SOLO has read/write permissions for. By default, it's under the documents directory on the local computer. You can create a dedicated work subdirectory.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050502.webp)

After selection, this directory is effectively mounted to your phone, allowing SOLO to read and write this local computer directory from your phone.

For example, if this directory contains a beach image called beach.jpg:

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050503.webp)

I can ask SOLO on my phone to remotely modify this image.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050505.webp)

The modified image is generated on the local computer and can also be viewed on the phone.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050504.webp)

Similarly, you can have the local computer generate programming scripts from your phone.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050506.webp)

The entire conversation and generated output can be seen synchronously on the desktop.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050507.webp)

## VI. Test Scenario B: Dispatching Ideas Anytime

One major advantage of the mobile client is that ideas can be dispatched to AI anytime, without being constrained by time or place.

A typical example is voice input, which is standard on phones but awkward on desktops. SOLO goes a step further with built-in "voice interactive discussion," which I tested specifically.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050203.webp)

It's somewhat like "having a meeting with AI" — you can discuss issues back and forth using voice.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050202.webp)

I "talked" with it for five minutes, asking how to design a conference website.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050204.webp)

After the discussion, it automatically generated content notes (shown above). I find this feature very useful — **suitable for extended voice input**, unlike typical mobile voice input that can only dictate a few sentences.

The verbatim transcript and summary of the mobile discussion are automatically synced to the web and desktop clients.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050205.webp)

After the discussion, you can also dispatch follow-up tasks from your phone, such as generating corresponding Office files or webpages, for further processing on the desktop.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050207.webp)

## VII. Test Scenario C: Accessing Work Anytime

AI mobile clients often lack operational capabilities because mobile devices don't have a local environment — generated scripts can't run, and you can't install Skills or MCP.

Three-end interconnection provides the solution: **install and run scripts on the desktop/web, and remotely call the other ends from your phone.**

This means the phone becomes an extension of your work environment, making office work much more convenient.

I tested operating Feishu Docs from my phone, which requires skills. The skill repository is [Feishu CLI](https://github.com/larksuite/cli). This is a command-line tool for operating Feishu from the command line, with 24 built-in Skills for AI Agent use.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050208.webp)

Among them, the [lark-doc skill](https://github.com/larksuite/cli/tree/main/skills/lark-doc) enables AI to automatically create, edit, and search documents on Feishu.

SOLO comes with this skill pre-installed, saving you the [installation](https://www.feishu.cn/feishu-cli) step. Viewing installed skills (shown below) or installing new ones requires the web or desktop client — the mobile client can only call, not install.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050209.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050211.webp)

With this skill, the phone can generate Feishu documents through the cloud (or local computer). Below, I generated a "Renovation Notes" document from my phone through the desktop client.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050212.webp)

After generation, the document is automatically saved to Feishu's cloud and can be viewed on all three SOLO clients.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050213.webp)

## VIII. Other Features: Scheduled Tasks

Let me also mention a feature I really like — you can **set up scheduled tasks from your phone**, using natural language to have AI run specific prompts in the cloud at scheduled times (e.g., generate a daily AI news summary).

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050214.webp)

However, the mobile client can only set scheduled tasks. Management and viewing must be done on the web or desktop client's "Automation" page.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026050215.webp)

## IX. Conclusion

My experience over the past few days is that SOLO's mobile version is truly impressive.

"Three-end interconnection" makes **the mobile client a fully-featured AI client** capable of handling various tasks and viewing progress on the web and desktop — extremely convenient.

This means you can leave your laptop behind, operate remote computers from your phone, and free yourself from device and location constraints.

I believe this represents the trend for mobile office and AI development. It's exciting to see domestic tools leading the way this time.

When I signed up, an invitation code was required. Now it's fully open to everyone — anyone can use it, and the domestic version is free. Give it a try — having AI coding at your fingertips from your phone is quite an experience.

(End)