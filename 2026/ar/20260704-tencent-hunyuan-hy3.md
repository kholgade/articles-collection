# Tencent Hunyuan Hy3 + WorkBuddy Hands-On: A 300B Model Challenging GLM 5.1 and DeepSeek V4 Flash

## I. Introduction

This week, Tencent released its new [Hunyuan large model Hy3](https://mp.weixin.qq.com/s/X2x1GF09bFbTzc3M1981BQ).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070603.webp)

Hunyuan, as Tencent's self-developed flagship model, has only released two versions in the past three years: version 1.0 in September 2023 and version 2.0 in December 2025.

Now, the third version has finally arrived, naturally drawing attention. Moreover, this new version has undergone major adjustments, with a changed model positioning (details below) — plenty to examine.

Tencent clearly has high expectations for it. A preview version [Hy3-preview](https://www.tencent.com/zh-cn/articles/2202320.html) was released in April for public testing. According to the release announcement, the official version's coding and Agent capabilities have significantly improved over the preview.

Additionally, Tencent launched a companion tool [WorkBuddy](https://www.codebuddy.cn/work/) in March this year.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070508.webp)

WorkBuddy is officially positioned as a "desktop AI native workspace," supporting various AI usage scenarios. It's somewhat like Claude Code's domestic version, and combined with the Hy3 model, it's said to be a cost-effective choice for most tasks.

Using Hy3 within WorkBuddy gives you a [two-week free trial](https://mp.weixin.qq.com/s/UzRYk8udfpMH8es0s5cwLw).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070602.png)

The image above shows the available models built into WorkBuddy.

I used this free trial period to test the Hy3 + WorkBuddy combination to see if it's as good as advertised.

For comparison, I selected GLM 5.1 and DeepSeek V4 Flash from WorkBuddy's built-in models to compete against.

Let me explain why I chose these as competitors rather than newer, stronger models — it relates to Hy3's model positioning.

## II. Model Positioning

The first thing you need to understand about Hy3 is that **it's only a medium-sized model — even a small-scale model** — definitely not one of those ultra-large models.

It uses a Mixture of Experts (MoE) architecture with 295B total parameters, 21B activated parameters, and a 256K context length.

This parameter scale is relatively small, indicating that its internal computation must also be small — certainly incomparable to those massive SOTA models with enormous computational requirements.

Yet according to Tencent's published test scores, its scores aren't that low.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070601.webp)

The far left of the image above shows Hy3's SWE-bench Pro score — roughly in the middle of the pack.

The release announcement states: "It demonstrates **intelligence significantly stronger than models of the same size**, comparable to larger flagship models, greatly enhancing practical value across various products and productivity tasks."

Let me translate that. Tencent believes Hy3's value lies in its superior performance compared to similarly sized (i.e., small to medium) models. Additionally, because it has relatively fewer parameters, it requires less computation, costs less, and runs faster — making it more valuable for practical use.

To verify this claim, I selected two domestic models of similar scale for comparison: GLM 5.1 and DeepSeek V4 Flash.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070561.webp)

In terms of parameter count, GLM 5.1 has the highest computation, followed by Hunyuan Hy3, then DeepSeek V4 Flash.

My actual testing experience confirmed this: DeepSeek V4 Flash was fastest, Hunyuan Hy3 second, and GLM 5.1 slowest.

This shows that Hunyuan Hy3's design philosophy isn't to pursue raw performance, but to balance performance with cost/speed — a model with decent performance, low cost, and fast speed that can be used as a daily workhorse.

Below are the five rounds of testing I conducted. Spoiler alert: Hunyuan Hy3's performance was impressive — you'd never guess it's a small-to-medium-sized model.

## III. BridgeBench Test Suite

My test questions mainly come from the [BridgeBench test suite](https://www.bridgebench.ai/), currently the hottest benchmark, claiming to be "the world's number one vibecoding benchmark."

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070506.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070507.webp)

It consists of over 170 questions, specifically designed to test models' coding capabilities.

Its running methodology and scoring method haven't been made public, but [some test questions](https://www.bridgebench.ai/test-prompts) are. I selected some questions and ran all three models to see which performed best.

However, these questions are relatively complex — sometimes taking an hour per question. So for the first two simple rounds, I used [my own test suite](https://github.com/ruanyf/ai-test-case).

All tests below were completed within WorkBuddy. I only switched models and working directories; all other conditions remained unchanged.

## IV. Web UI Test

The first test was the simplest — checking the model's ability to generate web UI by refactoring a webpage into an attractive, effective business website landing page ([prompt](https://github.com/ruanyf/ai-test-case#case01)).

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070541.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070542.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070543.webp)

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070547.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070548.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070549.webp)

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070544.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070545.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070546.webp)

Clearly, all three models performed well — I'd say there's no discernible gap.

For large models, generating web UI is probably a solved problem — no longer sufficient to test model capabilities. I probably won't need to test this again. I'm just showing the style and aesthetics of the generated pages here.

The only criticism is that they all clearly used Tailwind templates or Skills, making them look too similar and lacking personality. Fine for business websites, but too bland for personal sites.

## V. Web 2D Game: Angry Birds

The second test was generating a web version of Angry Birds ([prompt](https://github.com/ruanyf/ai-test-case#case03)). This test is actually quite challenging, especially the bird's flight and collision effects.

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070550.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070551.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070552.webp)

This is among the best results I've tested — the page closely matches the original UI, the game is fully playable, the bird's flight and collision effects are realistic, the bird bounces on the ground, and bricks disappear upon collision.

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070553.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070554.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070555.webp)

This result is also decent. While the UI differs from the original (no pigs), the bird's flight effect is well done, especially the glass shattering effect upon collision — very nice.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070556.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070557.webp)

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070558.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070559.webp)

This result is playable but clearly inferior to the other two models, both in UI and animation effects.

As for the comparison between Hunyuan Hy3 and GLM 5.1, I personally think Hy3 is better — it more faithfully recreates the original.

## VI. 2D Pool Game

This test required using Python to generate a 2D pool/billiards game ([prompt](https://www.bridgebench.ai/prompts/c4541e6f-be24-4b0b-ad5e-9ae5b8cfc1b7)).

The requirement was to use only `pygame-ce` and `numpy` — the former for the game window, the latter for pool ball collision math.

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070515.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070516.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070518.webp)

This result was surprisingly good — beautiful graphics, fully playable game, realistic collision effects, and balls can be pocketed one by one.

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070519.webp)

This result was a complete failure. The pool balls are just flat circles inside black squares — the corners aren't even rounded.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070520.webp)

Moreover, the game is unplayable — no matter how I tried, I couldn't hit the white ball with the cue.

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070521.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070522.webp)

This result is acceptable and playable. However, the break is wrong — the balls break horizontally — and it's difficult to control, requiring mouse aiming and Space key to shoot (left mouse button doesn't work).

Clearly, the winner of this round is Hunyuan Hy3.

## VII. 3D Pelican Riding a Bicycle

This test required using GLSL shader language to generate a 3D "pelican riding a bicycle" scene ([prompt](https://www.bridgebench.ai/prompts/64269eb6-6691-4d05-9489-91fb7f4ddf08)).

The model generates a GLSL script that can be pasted into [shadertoy.com](https://www.shadertoy.com/) for online compilation to see the rendered result.

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070513.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070514.webp)

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070511.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070512.webp)

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070509.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070510.webp)

In this round, none of the three models' results were very good. Hunyuan Hy3 was relatively better, but the bicycle looks more like a balance bike. Since the prompt uses "Bicycle" in English, I'm not sure if this includes two-wheeled balance bikes — otherwise, it's hard to explain the shape.

GLM 5.1's bicycle is even stranger — the wheels have become horizontal turntables. Is this a water bicycle? As for DeepSeek V4 Flash, it didn't generate a pelican at all.

## VIII. Large 3D Web Game

The final and most difficult test required the model to generate a large, complex web game.

First, I tested generating Minecraft, with all code contained in a single HTML file ([prompt](https://www.bridgebench.ai/prompts/e3aca9dc-5d6d-4002-ab9c-76267f9689b2)).

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070524.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070529.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070525.webp)

While the graphics are basic and incomplete, the game elements are intact. You can tell it's Minecraft — an open dynamic world for unlimited exploration, moving with WASD keys.

You can even chop trees to collect materials.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070526.webp)

In comparison, the other two models' results are rather sorry.

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070527.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070528.webp)

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070530.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070531.webp)

Though both are poor, GLM 5.1 at least generates a 3D world you can move through. DeepSeek V4 Flash produces a black screen — nothing to see, nothing to interact with.

I wondered if the test process was flawed, so I tested generating the 3D open world "Vice City" ([prompt](https://www.bridgebench.ai/prompts/709d9a91-7406-4240-8b23-ef4a456c385c)).

**Hunyuan Hy3**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070532.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070534.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070535.webp)

I think this city's visual effect is quite good — you can explore infinitely from a first-person perspective with a real-time map in the upper right.

There are pedestrians on the street, and you can press a button to fire bullets with sound effects.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070536.webp)

**GLM 5.1**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070537.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070538.webp)

**DeepSeek V4 Flash**

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070539.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026070540.webp)

GLM 5.1 gives a black screen. DeepSeek V4 Flash runs, but the scene doesn't look like a city at all. Confirmed: both models are weak in 3D web game capabilities.

## IX. Conclusion

After these tests, Hunyuan Hy3's performance was eye-opening. It handles simple tasks without issue and can produce acceptable results for complex tasks as well.

Its (300B model) performance is clearly better than DeepSeek V4 Flash, and in many cases, also better than the much larger GLM 5.1 (750B) — at least not worse.

Given Hy3's smaller size, faster speed, and lower cost — its API pricing is 1 yuan / 4 yuan per million tokens for input/output — it's truly a cost-effective model.

At a small model's price, it delivers above-grade performance, with balanced capabilities suitable as a daily primary programming/Agent model.

Plus, using Hy3 through [WorkBuddy](https://www.codebuddy.cn/work/) is currently free — definitely worth trying.

(End)