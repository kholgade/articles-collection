# I Used Doubao Seed 2.1 Pro to Generate a Digital West Lake

## I. Introduction

Recently, ByteDance friends invited me to beta-test their latest foundation model, [Doubao Seed-2.1-Pro-0915](https://mp.weixin.qq.com/s/Fp_mgF6wxMk0bkUVBqOKqA).

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091613.webp)

Regular followers may know Seed 2.1 Pro has been out for a while. What most people don't know is that its release model changed (explained below).

The new version now includes a release date: **Seed-2.1-Pro-0915** is the latest version launched on September 15, 2026.

To test its multimodal coding capability, I used it to generate an interactive 3D digital West Lake. I lived in Hangzhou for several years and know the lake well — a good benchmark for how accurately a large model can reconstruct it.

Bottom line: I was impressed. See the video below.

I've published the code on [GitHub](https://github.com/ruanyf/seed-westlake); you can open the site directly [here](https://ruanyf.github.io/seed-westlake/).

## II. The Shift in Development Model

Before diving in, a brief explanation of how this Doubao Seed 2.1 Pro model works.

The model formally launched in June 2026. Normally the next version would be Seed 2.2. But the team made a major decision: change the release model.

On top of Seed 2.1 Pro, they launched another foundation model, **[Doubao Seed Evolving](https://ark.volcengine.com/region:cn-beijing/model/detail?name=doubao-seed-evolving)**. The code base is identical; the only difference is that **Seed Evolving carries no version number**.

Seed Evolving is a continuously-updating model — just a name, no version number. You call it by name without specifying a version and it always resolves to the latest. As far as I know, this is the first large model with no version number.

It updates at high frequency — two to three releases per month — distinguished only by release date, no artificially imposed version number.

The primary reason: most users **don't care about version numbers; they just want the latest, strongest code**. Without a version number, users never need to update manually; the model silently updates in the background and you always call the latest version. It's also simpler for the developers, who no longer need to maintain old versions.

The model is called Seed *Evolving* precisely because "evolving" means continuous progress.

Seed 2.1 Pro and Seed Evolving share the same codebase; **every time Seed Evolving releases a major version, Seed 2.1 Pro updates to match**. Seed-2.1-Pro-0915 is therefore the September Seed Evolving version.

## III. Three Core Capabilities

Doubao Seed 2.1 Pro as a foundation model emphasizes three strengths: **Coding, Agent (tool use), and VLM (vision)**.

All three are reportedly very strong and well-balanced, with no obvious weakness — befitting the model that powers the Doubao app.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091614.webp)

The 0915 release improves all three:

> **(1) Coding**: reads very complex large software projects; stronger multimodal code generation from images.
>
> **(2) Agent**: improved reliability, more accurate search results, fewer hallucinations, more stable on complex long-horizon tasks.
>
> **(3) VLM**: stronger multimodal understanding, reasoning from video, handling 3D objects and dense text-image content.

## IV. Digital West Lake

My prompt:

> Based on maps available online, create a 3D panoramic tourist map of West Lake that is interactive — scroll to zoom, drag to rotate, click a location to automatically fly to it.

The project was complex enough that it ran for 2 hours and 15 minutes, costing ¥28 in API fees.

The first result already had the interface and all requested features: scroll to zoom, drag to rotate, click a landmark and fly to it with a 360-degree auto-revolving view.

One shot achieving this level exceeded my expectations. Of course there were some imperfections — let me walk through the details.

First, the 3D West Lake panorama:

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091003.webp)

The "Ten Scenes of West Lake" are correctly labeled and positioned. White Causeway and Su Causeway are connected in the rendering; in reality there is a small stretch of water between them.

Next, Leifeng Pagoda and Liuhe Pagoda:

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091005.webp)

Both towers are nestled in mountain hollows — matching reality, as they both sit at the foot of the hills around West Lake.

Small lively details: boats on the water, and the boats are moving.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091007.webp)

The proportions are off though — the boats and lakeside pavilions are oversized relative to the lake area.

Overall: from a single prompt, all the basic requirements were correctly implemented. Quite impressive.

## V. Enhancements

I refined the initial version in a few passes to make the 3D map more practical.

**(1) Scale correction**

> [Prompt] Adjust building proportions to match realistic scale.

After the fix, the map closely resembles the actual terrain, and the Su Causeway and White Causeway positions are now accurate.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091008.webp)

Liuhe Pagoda is now more subdued, surrounded by hills.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091009.webp)

The model's reasoning output included actual height data:

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091010.webp)

**(2) Landmark photos**

The initial version shows an info popup when you click a landmark name.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091011.webp)

I requested a real photo of each landmark in the popup, with a click-to-enlarge option:

> [Prompt] In the info popup that appears when clicking a landmark name, add a real photo of that landmark. Clicking the photo should display a large version.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091012.webp)

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091013.webp)

**(3) Transport information**

> [Prompt] Label the major roads around West Lake with their names, and mark the major metro stations with their names.

![](https://cdn.beekka.com/blogimg/asset/202609/bg2026091014.webp)

Hangzhou Metro Line 1, Yan'an Road, and West Lake Avenue were added.

After these refinements, the 3D interactive West Lake map became genuinely usable. The total time investment was one afternoon and a few dozen yuan.

All results were one-shot generations — I essentially did not ask Seed 2.1 Pro to revise anything. Each of the three modifications took more than 20 minutes and filled the entire 1M-token context window.

All code is on [GitHub](https://github.com/ruanyf/seed-westlake); the hosted version is [here](https://ruanyf.github.io/seed-westlake/).

## VI. Summary

The "Digital West Lake" project demonstrates that Seed-2.1-Pro-0915 is impressively capable — handling a complex 3D web project in one shot, which fits its billing as the strongest foundation model in the Seed series.

And since Seed Evolving continues to publish new releases, the model will keep improving.

Going forward, when I discuss tier-1 domestic models, I will include Seed 2.1 Pro (or Seed Evolving).

(End)
