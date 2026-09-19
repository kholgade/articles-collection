# Domestic LLM Updates: Weekly Models Arrive — Doubao Seed Evolving and DeepSeek V4 Flash Reviewed

## I.

The hottest topic in domestic models recently has been Kimi K3, released on July 17 — just three weeks ago. In the AI world, though, that is already a long time ago.

Many new domestic models have appeared in that interval:

- July 31: [DeepSeek V4 Flash](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731) stable release
- July 31: Video model [Seedance 2.5](https://seed.bytedance.com/en/seedance2_5) released
- August 3: Open-source video model [MiniMax H3](https://www.minimaxi.com/blog/minimax-h3) released
- Doubao Seed model renamed to [Seed Evolving](https://ark.volcengine.com/region:cn-beijing/promotion/model?agentMode=close&modelName=doubao-seed-evolving)

All four are noteworthy. Today I'll focus on the two general-purpose models: DeepSeek V4 Flash and Doubao Seed Evolving.

[Doubao Seed Evolving](https://ark.volcengine.com/region:cn-beijing/promotion/model?agentMode=close&modelName=doubao-seed-evolving) in particular is, as far as I know, **the world's first weekly-updated model**.

## II.

The large models we are used to carry version numbers, with new versions released periodically.

There is another software release model called "rolling release" — the software is updated continuously, and you always install the latest version without specifying a version number. Several Linux distributions work this way.

Rolling release is actually a great fit for large models. Most users don't care about version numbers; they just want the latest and strongest version at all times. Manually updating model IDs every so often is annoying.

Some big companies' coding plans provide a special ID that always points to the latest model version. But for the model itself, I had not heard of one that updates automatically and always stays current.

Doubao Seed Evolving is exactly that. Its predecessor was Doubao Seed 2.1 Pro. Last month the team suddenly changed course, renamed the model to "Evolving" (as in continuously evolving), dropped the version number, and began updating on a weekly cycle.

When you call this model, you always get the latest version. The official description: "Connect once, upgrade seamlessly, zero migration cost." No more manually updating version numbers; the model itself "keeps evolving in capability."

## III.

Now for DeepSeek V4 Flash. Like Doubao Seed Evolving, it is a general-purpose model capable of a wide variety of tasks.

The key difference: it lacks visual capability and cannot understand images or video natively, whereas the Seed model has vision capability.

DeepSeek V4 Flash is a lightweight member of the V4 series, with 284B parameters and 13B activated parameters. This very small activation size means low compute requirements and relatively easy local deployment.

Despite its small scale, the performance is impressive. A preview was released in April; the stable version on July 31 brought significant improvements. On [Artificial Analysis](https://artificialanalysis.ai/#intelligence), it ranks 12th among all models, on par with GPT 5.6 Luna and Gemini 3.6 Flash.

However, its [per-task cost](https://artificialanalysis.ai/#price-and-cost) is the lowest of any model — roughly 1% of Claude Fable 5. **By that benchmark alone, DeepSeek V4 Flash is the current "strongest lightweight model."**

On the other side, Doubao Seed Evolving is a closed-source model with no public information on parameter count or architecture. It is ByteDance's flagship Seed team model and the backbone of the Doubao app, and it is highly capable.

As a general model it emphasizes three key capabilities: vision (a clear strength — just look at the Seedance family's popularity), coding (including complex repo repair, cross-file modifications, and real feature development), and agent capability (tool use and information retrieval).

Both DeepSeek V4 Flash and Doubao Seed Evolving have a 1M-token context window, strong long-horizon task ability, high token efficiency, and low running cost.

## IV. Web Animation Test — Angry Birds

The first test: generate the 2D web game [Angry Birds](https://github.com/ruanyf/ai-test-case#Case03).

Both implementations worked well — playable with no logic errors, only minor differences in detail. My impression: Doubao Seed Evolving was slightly better in gameplay; DeepSeek V4 Flash had a more polished UI.

Thinking back a year ago when I ran this same test, models performed miserably — either unplayable or visually dreadful. Models that produced a working version in one shot were few and far between. Just one year later, the situation has completely changed. The progress is staggering.

## V. 3D Animation Test

First a simpler test: generate a [3D Rubik's Cube](https://github.com/ruanyf/ai-test-case#case09) on a web page, animated to show automatic scrambling and solving step by step.

Both implementations looked good with little to choose between them. Algorithmic visualization problems are now too easy for modern models.

Next, a harder test: generate a [Doom-style maze scene](https://github.com/ruanyf/ai-test-case#case10) with ceiling, floor, and brick walls, in first-person perspective, navigable with WASD keys.

Both implementations were fairly basic — the maze was rudimentary, and the ceiling, floor, and brick walls weren't convincingly rendered. Complex 3D scenes are not the strong suit of these two general-purpose models.

## VI. Spatial Reasoning

I then asked the models to generate the popular "pelican riding a bicycle" scene, but using GLSL to produce a 3D scene — a test of spatial imagination.

The generated code can be compiled and viewed at [shadertoy.com](https://www.shadertoy.com/).

Seed Evolving's result was unexpectedly excellent — surpassing any model I had tested before, including Fable 5. DeepSeek V4 Flash's result was also decent, though not quite as good.

## VII. Agent Capability

I also tested their agent abilities — their capacity to operate tools.

I found a WordPress [demo site](https://www.softaculous.com/demos/WordPress) where you can try out WordPress features. Admin credentials are shown in the top-right corner of the page.

I asked the model to log into the admin panel and publish an article, with this prompt:

> Write an introductory article about how to use WordPress, then visit the URL below, log into the admin panel using the admin username and password shown on the page, publish the article, and return the published URL. https://www.softaculous.com/demos/WordPress

DeepSeek V4 Flash successfully published the article ([published URL](https://demos2.softaculous.com/WordPressjm7tw1ooni/)).

![](https://cdn.beekka.com/blogimg/asset/202608/bg2026080904.webp)

![](https://cdn.beekka.com/blogimg/asset/202608/bg2026080905.webp)

## Model Summary

**Doubao Seed Evolving** — Coding and Agent capabilities are becoming the core competencies of language models. Starting now, Volcengine provides developers with a continuously updated model card: `Doubao-Seed-Evolving`. The model focuses on Coding and Agent scenarios with high-frequency upgrades. Developers who continuously use Seed Evolving will see visibly rapid model progress.

Key characteristics:
- Continuous capability evolution with weekly iteration rhythm
- Deep optimization for Coding & Agent scenarios
- Connect once, upgrade seamlessly — same Model ID, new versions take effect automatically with zero migration cost

Model page: https://ark.volcengine.com/region:cn-beijing/model/detail?name=doubao-seed-evolving

1M context window; monthly plan ¥9.9
