# Tech Enthusiast Weekly (Issue 404): AI Memory Knowledge You Need to Know

This weekly newsletter shares noteworthy tech content, published every Friday.

This magazine is [open source](https://github.com/ruanyf/weekly), and [submissions](https://github.com/ruanyf/weekly/issues) are welcome. There is also a ["Who's Hiring"](https://github.com/ruanyf/weekly/issues/10517) service for posting programmer job openings. For cooperation, please [email](mailto:yifeng.ruan@gmail.com) (yifeng.ruan@gmail.com).

## Cover Image

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071603.webp)

A "SpongeBob" exhibition currently being held at a shopping mall in Shanghai. ([via](https://m.thepaper.cn/newsDetail_forward_33450995))

## AI Memory Knowledge You Need to Know

When running AI models at home, you have two hardware options.

One is a discrete graphics card. Currently, the top-tier consumer graphics card is NVIDIA's RTX 5090, with 32GB of VRAM, priced at around 30,000 RMB.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071511.webp)

The other is a home computer using an onboard chipset (CPU + onboard GPU + onboard memory), such as a mini PC with AMD's Strix Halo chipset (specific model Ryzen AI Max+ 395), which comes with 128GB of memory and costs around 20,000 RMB.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071512.webp)

I ask everyone, which hardware is better?

Most people might instinctively choose the discrete graphics card, after all, the computing power of a discrete GPU far exceeds that of an onboard chipset.

According to the information I found, here are the single-precision 32-bit floating-point (FP32) computing power of the two:

> - Discrete GPU (RTX 5090): **104.8 TFLOPS**
> - Onboard Chipset (AMD Ryzen AI Max+ 395): **14.8 TFLOPS**

As you can see, the discrete GPU's computing power is a full 7 times that of the onboard chipset. For lower-precision floating-point calculations (like FP16 and FP4), the gap is even larger.

However, I tell you that the correct answer is actually "it depends." In many cases, a mini PC with an onboard chipset is actually a better solution for local AI models.

The reason is simple: for most AI models (as long as the parameter count is slightly large), the RTX 5090 simply cannot run them.

The problem lies in its 32GB VRAM, which is too small. For a 70B parameter model, if each parameter uses 4-bit precision, reading all parameter weights into memory requires about 32.6GB of memory, which exceeds the RTX 5090's VRAM capacity, so it simply won't run.

In contrast, the AMD mini PC's onboard memory has 128GB, so loading the model is no problem. **The memory of the onboard chipset is shared between the GPU and CPU, hence it's called "unified memory."** Its advantage is that it can allocate as much memory as possible to a single processor, thus handling AI models with large memory consumption.

Apple's M-series chips have always used this "unified memory" architecture, and other manufacturers are now following suit. AMD's Strix Halo, NVIDIA's DGX Spark, Intel's Core Ultra, and Qualcomm's Snapdragon X all adopt this architecture. Besides large memory capacity, its price is also lower than discrete GPUs.

At this point, you might ask, since the onboard chipset has these advantages, is it still necessary to buy a discrete GPU?

The answer is that memory has two metrics: besides capacity, there is also "memory bandwidth." **The weakness of the onboard chipset is precisely memory bandwidth.**

"Memory bandwidth" refers to the speed at which memory transfers data to the processor. Although the RTX 5090 has limited VRAM, its memory bandwidth is enormous, reaching 1792GB/s, while AMD's memory bandwidth is only 256GB/s.

Every time an AI model generates a Token, the processor needs to read the entire model from memory and perform calculations. If the memory bandwidth is 256GB/s, then for a 40GB model, the processor can only read it 6 times per second (256 divided by 40), meaning it can only generate 6 Tokens per second (theoretical value, actual may be even lower). Who can tolerate such a slow speed?

Even the Apple M3 Ultra chip, which has the largest memory bandwidth at 819GB/s, can generate 20 Tokens per second, far less than the RTX 5090's 1792GB/s.

Therefore, both memory size and memory bandwidth are bottlenecks for AI models. This is also why High Bandwidth Memory (HBM) prices have gone crazy.

If you choose a mini PC with an onboard chipset, you need to mentally prepare for very slow Token generation speeds.

Fortunately, to reduce computational load, the "Mixture of Experts (MoE)" architecture has emerged. **When computing a Token, it does not need to read all parameters, only activate a portion of them.**

Take the Qwen3-30B-A3B model as an example. It contains 30B parameters, but only activates 3B parameters each time. Therefore, the amount of data to read per Token is not 20GB, but 2GB. On an AMD mini PC, this theoretically allows generating over 100 Tokens per second, which is quite decent.

So, if you use a "unified memory" mini PC, choose an MoE model.

Additionally, mini PCs have another major drawback, unrelated to memory, but related to their slow computing power.

We know that the model must first process the user's prompt before generating Tokens. Because the mini PC's computing power is slow, it also processes prompts slowly.

According to [actual measurements](https://vettedconsumer.com/unified-memory-explained-why-mini-pcs-can-run-70b-models-a-big-gpu-cant-and-where-they-slow-down/), an AMD mini PC using a 70B model has a prompt processing speed of 95 Tokens per second. So, if a user submits a document of 4000 tokens, it takes about 40 seconds to process before outputting the first Token.

You can imagine that once the user stuffs more content into the context window, just processing the prompt can become minutes to tens of minutes.

In short, at this stage, running large models on a local computer, whether with a discrete GPU or an onboard chipset, has drawbacks. At best, you can run some medium-sized MoE models, and the prompts cannot be very long.

## How to Name Boolean Variables

Legend has it that there are two hard problems in programming: cache invalidation and variable naming.

Among them, boolean variables are particularly hard to name. How can you aptly express that this variable represents a boolean value of "true" or "false"?

I recently read an article [The Art of Naming Boolean Variables](https://thatamazingprogrammer.com/posts/stop-naming-your-variables-flag-the-art-of-boolean-prefixes/), which suggests that using four prefixes can correctly name boolean variables. I found it very insightful.

(1) **is-**: Describes the state of something, followed by an adjective, e.g., isActive, isDeleted, isEmpty.

(2) **has-**: Describes ownership or containment, followed by a noun, e.g., hasAccess, hasChildren, hasValidationErrors.

(3) **can-**: Describes ability or permission, e.g., canEdit, canDelete, canRetry.

(4) **should-**: Describes intention or logic, e.g., shouldRetry, shouldCacheResponse.

Besides these four prefixes, there is another rule for naming: never use negative words in boolean variable names.

For example, instead of using isDisabled, use `isEnabled = false`.

## Tech News

1. [OpenAI Keyboard](https://openai.com/zh-Hans-CN/supply/co-lab/work-louder/)

OpenAI has just launched a convenient keyboard to facilitate operating AI agents.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071601.webp)

The bottom of the keyboard has a row of shortcut keys for approval, rejection, voice input, etc. The top has a row of RGB lights indicating the current status of the AI agent (thinking, running, waiting, completed).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071602.webp)

This thing costs $230, looks unoriginal, and may not be more convenient than a regular keyboard.

Famous designer Jony Ive, after leaving Apple, is now responsible for OpenAI's hardware design. Everyone hoped he would come up with a smart hardware product that would impress, but this small keyboard that debuted first is disappointing.

2. [Asteroid 2016HO3](https://www.cnsa.gov.cn/n6758823/n6758838/c10760422/content.html)

The Tianwen-2 probe was launched in May 2025 and, after about 400 days of flight, finally reached its target—asteroid 2016HO3—and sent back photos.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071501.webp)

This asteroid is about 20 meters in length, only slightly larger than half a standard basketball court. It has an irregular shape with sharp corners, indicating it is likely debris from a collision rather than formed by cooling lava.

When Tianwen-2 took the photo, it was 20 kilometers from the asteroid. Next, as planned, it will collect rock samples from this asteroid and return them to Earth.

The difficulty lies in the fact that Tianwen-2's wingspan reaches 15 meters, only slightly smaller than the asteroid itself. Sampling might alter the asteroid's orbit.

3. [Wind Knitting Machine](https://www.merelkarhof.nl/work/wind-knitting-factory)

A Dutch designer has invented a home wind knitting machine that can be installed on a balcony or rooftop.

![](https://cdn.beekka.com/blogimg/asset/202507/bg2025070405.webp)

Wind drives the blades, which on a circular knitting turntable, knit yarn into a scarf.

![](https://cdn.beekka.com/blogimg/asset/202507/bg2025070406.webp)

When the wind is strong, the knitting speed is very fast. It appears to be a purely mechanical device, not using wind power generation.

![](https://cdn.beekka.com/blogimg/asset/202507/bg2025070407.webp)

The designer's original intention was to show people that wind power can also be utilized in urban buildings.

![](https://cdn.beekka.com/blogimg/asset/202507/bg2025070408.webp)

## Articles

1. [Machine Learning PhD Job Search Guide](https://silviasapora.github.io/blog/ml-interviews.html) (English)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071509.webp)

The author is a US machine learning PhD graduate who has joined DeepMind. This article is a review and summary of the job search process.

There is another [similar article](https://alisawuffles.github.io/blog/job-search/).

2. [Using DNS for ACME Challenges](https://hsm.tunnel53.net/article/dns-for-acme-challenges/) (English)

![](https://cdn.beekka.com/blogimg/asset/202509/bg2025092405.webp)

Free HTTPS certificates are issued via the ACME protocol. The protocol requires domain ownership verification. One verification method uses DNS. This article explains how it works.

3. [The Predicament of Go](https://www.andrewvittiglio.com/thoughts/go-killed-arenas) (English)

![](https://cdn.beekka.com/blogimg/asset/202512/bg2025120608.webp)

This article argues that Go's position is awkward and its future is not promising. "As slow languages become faster and hard languages become easier, the middle ground that Go occupies will cease to exist."

4. [JavaScript Hashing Speed Comparison](https://lemire.me/blog/2025/01/11/javascript-hashing-speed-comparison-md5-versus-sha-256/) (English)

![](https://cdn.beekka.com/blogimg/asset/202501/bg2025011918.webp)

MD5 and SHA256 are both commonly used hashing algorithms. This article explores which of these two hashing algorithms is faster in JavaScript. The answer might be different from what you think.

5. [Terminal Control Characters Cheat Sheet](https://jvns.ca/blog/2024/10/31/ascii-control-characters/) (English)

![](https://cdn.beekka.com/blogimg/asset/202411/bg2024110405.webp)

The author created a diagram (above) listing the control character shortcuts available in the command line (e.g., Ctrl-C terminates the current command), totaling 33.

6. [Richard Feynman Joins My Startup](https://longnow.org/ideas/richard-feynman-and-the-connection-machine/) (English)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071605.webp)

The author recalls the famous physicist Richard Feynman joining his startup to develop a supercomputer, with many interesting anecdotes.

## Tools

1. [WhatCable](https://github.com/darrylmorley/whatcable)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071510.webp)

A macOS menu bar app that displays the characteristics of the USB-C cable currently plugged into the computer.

2. [amber](https://amber-lang.com/)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071401.webp)

A new language that simplifies Bash syntax. Its scripts can be compiled into Bash.

3. [Ant](https://antjs.org)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071402.webp)

A lightweight JS/TS language runtime, seemingly written from scratch, with a binary file size of only 8MB.

4. [Screen Translator](https://github.com/ciddwd/overlay-translator)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071404.webp)

An open-source Android app for real-time screen translation. ([@ciddwd](https://github.com/ruanyf/weekly/issues/10701) submission)

5. [TurboOCR](https://turboocr.com/)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071406.webp)

A tool for high-speed text recognition (OCR) using GPU. ([@nataell95](https://github.com/ruanyf/weekly/issues/10706) submission)

There is also a purely local text recognition library [light-ocr](https://github.com/arcships/light-ocr) providing JS/C++ API. ([@eric8810](https://github.com/ruanyf/weekly/issues/10714) submission)

6. [Visprex](https://visprex.com/)

![](https://cdn.beekka.com/blogimg/asset/202411/bg2024111013.webp)

This website allows you to upload CSV data files and automatically generate visualizations.

7. [Loro](https://www.loro.dev/)

![](https://cdn.beekka.com/blogimg/asset/202311/bg2023111321.webp)

An open-source CRDT synchronization algorithm library for real-time multi-user state synchronization.

8. [File Wizard](https://github.com/LoredCast)

![](https://cdn.beekka.com/blogimg/asset/202510/bg2025100202.webp)

A self-hosted, web-based service for converting common file formats, also supporting image OCR and audio-to-text.

## AI Related

1. [Oh My HuggingFace](https://github.com/oh-my-hf/ohmyhf)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071405.webp)

An unofficial open-source cross-platform Hugging Face client for browsing and downloading models, datasets, etc. ([@fzlzjerry](https://github.com/ruanyf/weekly/issues/10705) submission)

2. [pi-auto-approval](https://github.com/Europa2061/pi-auto-approval)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071403.webp)

A plugin for the Pi agent programming agent that automatically approves low-risk permission confirmations, while high-risk ones are still left for user confirmation. ([@Europa2061](https://github.com/ruanyf/weekly/issues/10669) submission)

3. [GPT Crawler](https://github.com/BuilderIO/gpt-crawler)

This tool crawls the content of a specified website into a JSON file, then uploads it to ChatGPT, thereby generating a chatbot for that website, allowing you to chat with it.

4. [Tokenwiz](https://github.com/1rgs/tokenwiz)

![](https://cdn.beekka.com/blogimg/asset/202311/bg2023111305.webp)

An open-source implementation that mimics OpenAI's tokenization of input text.

## Resources

1. [Goto Onion](https://gotoonion.site/)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071506.webp)

A gateway for Tor .onion websites, allowing regular browsers to access Onion URLs.

2. [Fading Maize](https://www.fadingmaize.com/)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071507.webp)

A very interesting website. A US college band recorded an album in 2001 and then disbanded.

Now, they have AI re-record the original recordings in a 2026 style. The website plays both recordings simultaneously for comparison.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071508.webp)

Music is truly magical. Music from over 20 years ago shows no trace of time; the guitar sounds as if it were yesterday.

3. [Maze Algorithms](https://www.jamisbuck.org/mazes/)

![](https://cdn.beekka.com/blogimg/asset/202601/bg2026012505.webp)

This website collects various maze generation algorithms.

## Images

1. [Undersea Roundabout](https://visitfaroeislands.com/en/plan-your-stay/getting-around/world-first-under-sea-roundabout)

Roundabouts are usually at busy intersections, but in the Faroe Islands in the Atlantic Ocean, there is a world-unique undersea roundabout.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071502.webp)

The image above is a schematic of the Faroe Islands' undersea tunnel. At the yellow circle, the tunnel splits into two, leading to two different islands. An undersea roundabout was built here.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071503.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071504.webp)

To attract drivers' attention, the government hired artists to paint it in the shape of a jellyfish.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071505.webp)

## Digest

1. [AI Was Supposed to Save Time and Reduce Workload](https://decrypt.co/357527/ai-save-time-instead-created-new-kind-burnout)

People thought AI would save time and reduce workload, but a survey by the University of California found the opposite. AI increases workload, makes work more intense, and leads to burnout.

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026021615.webp)

**Why hasn't AI reduced work, but instead increased it?** The reasons might include the following.

**(1) Expanded Scope of Job Responsibilities.** Product managers now write code, researchers maintain servers. People's job responsibilities are no longer clear-cut but become blurred. Employees start handling work outside their scope, and AI makes this shift feasible.

This creates a chain reaction. Engineers suddenly find themselves needing to review, correct, and guide code written by non-programmer colleagues, because those colleagues are "vibe coding."

People who automate work outside their own expertise actually create more work for others.

**(2) Blurred Work/Life Boundaries.** AI's conversational interface makes work easy and convenient. There's no more helplessness facing a blank page, nor a daunting learning curve.

Therefore, employees start sending "quick prompts" before leaving their desks (e.g., before going to the bathroom), letting AI handle some trivial tasks while they are away. Many even input prompts during off-hours to let AI run. The cumulative use of AI during non-work hours leads to reduced rest time and significantly increased working hours.

**(3) Surge in Multitasking.** Because AI creates the illusion that tasks can be handled in the background, employees are asked to manage multiple workflows simultaneously.

This may superficially boost productivity, but in practice often translates into constant attention switching and longer to-do lists.

**(4) Self-Reinforcing Cycle of the Above Factors.** AI makes things easier, so employees do more, leading to greater reliance on AI to simplify those things. This cycle repeats, eventually leading to burnout.

Researchers point out: "Some participants said that although they felt more productive, they didn't feel less stressed; instead, they felt busier than before."

**(5) Solutions.** Researchers suggest that to address AI-induced burnout, companies should develop deliberate countermeasures to regulate how employees use AI.

1. Pause current work before making important decisions.
2. Prioritize tasks to reduce context switching.
3. Reserve time for genuine interpersonal interaction.

## Quotes

1.

If you are the sun, I am the black hole.

— [Stephen Hawking](https://geohot.github.io//blog/jekyll/update/2026/05/03/punk-or-why-i-dont-stream.html)

2.

The world of AI models is like a city with five corporate headquarters districts and a Chinatown.

— [The Singularity Is Nearer](https://geohot.github.io//blog/jekyll/update/2026/05/03/punk-or-why-i-dont-stream.html)

3.

AI is a complete black box, which means so-called "AI engineering" or "prompt engineering" is a complete scam. Any claim to be able to manipulate the black box in some clever way is false.

You cannot explore AI's operational logic; it's just a machine-implemented "trust me, bro."

— [AI Is a Bad Tool](https://bytecode.news/posts/2026/07/user-submission-ai-is-a-bad-tool)

4.

I have a bread machine that does almost everything: kneading, proofing, baking. I pour in the ingredients, press a button, and three hours later, bread is ready.

Well, in three years, I've probably used that machine only twice. Instead, I buy a pre-sliced loaf from the supermarket every week.

This explains why, even though AI can easily generate code, SaaS companies are far from decline.

— [Why Convenience Always Wins, and Why SaaS Won't Die](https://www.joanwestenberg.com/p/the-bread-paradox-why-convenience)

## Previous Issues

[The Game of Stablecoins](https://www.ruanyifeng.com/blog/2025/07/weekly-issue-357.html) (#357)

[Don't Value Product Hunt Too Much](https://www.ruanyifeng.com/blog/2024/07/weekly-issue-307.html) (#307)

[Jensen Huang's Nvidia Story](https://www.ruanyifeng.com/blog/2023/06/weekly-issue-257.html) (#257)

[The Peak of the Automotive Industry May Have Passed](https://www.ruanyifeng.com/blog/2022/05/weekly-issue-207.html) (#207)

(End)