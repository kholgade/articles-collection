# Tech Enthusiast Weekly (Issue 398): Token Costs Are Hard to Bear

Here records the weekly tech content worth sharing, published on Fridays.

This magazine is [open source](https://github.com/ruanyf/weekly), and [submissions](https://github.com/ruanyf/weekly/issues) are welcome. There is also a [Who's Hiring](https://github.com/ruanyf/weekly/issues/9815) service, posting programmer recruitment information. For cooperation, please [contact via email](mailto:yifeng.ruan@gmail.com) (yifeng.ruan@gmail.com).

## Cover Image

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052803.webp)

The Anji Cultural and Art Center in Anji County, Zhejiang Province, opened last year. The area is rich in bamboo, and the roofs are designed in the shape of bamboo leaves. ([daemin_kg@ig](https://www.instagram.com/p/DYKVQBKiBG1/?img_index=1))

## Token Costs Are Hard to Bear

Last week, Peter Steinberger, founder of OpenClaw (Lobster), posted his [Token usage](https://x.com/steipete/status/2055346265869721905).

He wasn't deliberately showing off how many Tokens he used, but rather to introduce the tool [CodexBar](https://codexbar.app/). This menu bar widget can count your Token usage and calculate the corresponding cost.

Guess how many Tokens he used?

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051701.webp)

According to the screenshot, he sent 7.6 million requests in one month, consuming 603 billion Tokens. Based on the preset rate, these Tokens are worth $1.3 million!

That means **his AI programming costs an average of over $40,000 per day**.

Of course, this number is not actual expenditure. Because he is an employee of OpenAI, he can use the company's Tokens for free without limit. So, this money is not a real expense.

However, his Token usage is real. Most companies need to purchase Tokens externally. Using his example, everyone can calculate: if a programmer uses hundreds of billions or even trillions of Tokens per month, how much would the company have to pay?

One person, one month, $1.3 million, equivalent to nearly 9 million RMB, **over 100 million RMB per year!** That's the cost for a company to allow unrestricted use of top-tier models.

If switching to cheaper models, the cheapest domestic open-source model costs about 1/30 to 1/50 of foreign flagship models, then the annual cost would be 2 to 3 million RMB.

The conclusion is: **if unlimited usage is allowed, a programmer will cost at least 2 to 3 million RMB per year in Token fees**. If using US flagship models, the cost quickly rises to tens of millions or even hundreds of millions of RMB.

To reduce costs, companies have two methods: one is to purchase monthly subscription packages, but they are insufficient for large projects; the other is to set up their own open-source models, saving external purchase costs, but hardware costs are not cheap, and the strongest models are currently not open source.

Weighing the options, I suspect **companies will almost certainly set restrictions, not allowing programmers unlimited use of external models**. Otherwise, the huge Token costs are unbearable. Programmers' salaries are already high, plus at least several million RMB per person per year in Token fees, the company's development costs will explode.

Can anyone tell me if there is a company that provides unlimited API calls to external models for programmers? I haven't heard of any.

In fact, I know a few examples where companies have tightened AI programming due to high Token costs.

For instance, ride-hailing giant [Uber](https://www.forbes.com/sites/janakirammsv/2026/05/17/uber-burns-its-2026-ai-budget-in-four-months-on-claude-code/) spent its entire $3.4 billion AI budget for 2026 in the first four months and had to restrict AI usage.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052405.webp)

Another example, [Microsoft](https://aiweekly.co/alerts/microsoft-drops-claude-code-after-budget-overrun) also dropped Claude Code due to budget overruns and switched to its own hosted OpenAI model.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052406.webp)

If giants like Uber and Microsoft can't bear the huge Token costs, then probably no company can.

In short, although AI programming sounds great, the moment the bill arrives, the company wakes up: **AI programming is much more expensive than human programmers**.

So, will AI replace programmers? For companies with large software projects, I think there won't be large-scale replacement because of the cost. At least for now. If Token costs drop significantly in the future, it's hard to say.

## The End of Bug Bounty Programs

[Turso](https://turso.tech) is an open-source cloud database, with code on GitHub.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052804.webp)

It had a bounty program, giving $1,000 to people who found vulnerabilities. It was working well, but since large models could be used to find vulnerabilities, things went wrong.

The PR page (external code submissions) of its repository has become like this.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051606.webp)

People submitting vulnerabilities are flooding in, all aiming for the bounty. The so-called vulnerabilities are often deliberately injected garbage bytes or configuration errors, naturally unable to run.

The development team is exhausted and overwhelmed. Sometimes, when closing these PRs, the submitter will argue with you, using AI-generated [long-winded arguments](https://github.com/tursodatabase/turso/pull/6257#issuecomment-4216531987) telling the development team "I'm not wrong, you're wrong," which is ridiculous.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051607.webp)

Eventually, the development team had to announce the [termination of the bounty program](https://turso.tech/blog/the-wonders-of-ai), and submitting vulnerabilities and PRs will no longer receive bounties.

> People who churn out garbage content might take just a minute to submit, but we spend hours reading, understanding, and responding. And the generation rate of such content is almost unlimited.
>
> Although automated scripts can be set up to filter PRs, because bounties are involved, the motivation to submit AI code is too great. There are always people endlessly arguing, reopening the same PR, etc.

This tells us that traditional bug bounty programs are likely unworkable in the AI era. In the future, finding vulnerabilities may not come with a bounty. I wonder if this will lead to an increase in online attacks.

## Tech News

1、[Weight and Temperature](https://news.yale.edu/2026/05/20/warmer-temps-heavier-owl-monkeys-climate-linked-weight-gain-primates)

A Yale University expedition team found that owl monkeys in Argentina are heavier than 25 years ago. The average weight of monkeys in 2023 was 50 grams heavier than in 1999, an increase of about 4%.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052103.webp)

Scientists believe this is related to rising temperatures. The average daily temperature in Argentina in 1999 was 22.2°C, rising to 23.8°C in 2023.

Higher temperatures reduce the energy monkeys expend on thermoregulation, allowing extra calories for weight gain.

This theory also seems applicable to humans, meaning global warming may increase the number of obese people.

2、[Artificial Eggshell](https://www.nationalgeographic.com/science/article/artificial-egg-colossal-chickens-moa-dodo)

US biotech company Colossal has created an "artificial eggshell" and successfully hatched 26 chicks.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052403.webp)

Its shell is a sturdy hexagonal cup-like structure for support; the inner wall is a semi-permeable membrane material that allows oxygen to pass through easily while retaining moisture.

Researchers placed chick embryos into the "artificial eggshell" and successfully hatched them in an incubator.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052404.webp)

In the image above, the top of the eggshell is transparent, allowing observation of the interior.

Colossal's purpose in creating this device is to revive the extinct dodo bird. Otherwise, even if dodo cloning embryos are made, they would still need to be bred inside other animals (like ostriches).

3、[Artistic Protest](https://p26.bg/news/dupkite-po-ul-chiprovci-v-sofiya-se-prevarnaha-v-ulichna-galeriya-snimki-4310news.html)

In Sofia, the capital of Bulgaria, there was a small pothole on the road that the city government had not repaired for a long time.

Two artists were dissatisfied and painted an angry face on the pothole.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051702.webp)

The bright pattern made it easier for drivers and pedestrians to notice, reducing accidents. It also sparked public interest, with news media reporting widely, and the pothole was quickly repaired.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026051703.webp)

This tells us that dissatisfaction should be expressed; it can drive solutions, and expressing it in an artistic form is more effective and easier for people to accept.

## Articles

1、[Why Memory Prices Are Rising](https://davidoks.blog/p/ai-is-killing-the-cheap-smartphone) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052301.webp)

Memory manufacturers produce three types of memory: DDR (for desktop computers), LPDDR (low-power memory for phones), and HBM (high-bandwidth memory for AI data centers).

Due to surging demand for HBM from AI companies, which offer high prices, manufacturers have shifted production capacity to HBM, reducing output of DDR and LPDDR, leading to memory shortages and price increases for consumer electronics.

2、[I'm Getting Into Reticulum](https://www.jonaharagon.com/posts/im-getting-into-mesh-networks-meshtastic-meshcore-and-reticulum/) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052801.webp)

Reticulum is a project for self-organizing networks, allowing virtual networks to be set up on top of various physical networks (WiFi, wired, radio, LoRa, etc.). This article is an introduction.

3、[Warm Up Your MacBook](https://z3ugma.github.io/2019/11/18/warm-up-your-macbook/) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052802.webp)

A cool article. The Mac system has a `stress` command to put CPU under load. This article suggests using it to warm up the cold metal shell of a MacBook in winter.

4、[Why I'm Against Boolean Logic](https://abuseofnotation.github.io/boolean-thinking/) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052302.webp)

A philosophical article. Boolean logic has only two values (true and false). The author argues that this leads to black-and-white binary thinking. The real world is non-Boolean, full of uncertainty and non-uniqueness.

5、[Why the Central Limit Theorem Is Everywhere](https://www.quantamagazine.org/the-math-that-explains-why-bell-curves-are-everywhere-20260316/) (English)

![](https://cdn.beekka.com/blogimg/asset/202603/bg2026031915.webp)

A popular science article introducing the history and meaning of the Central Limit Theorem. This theorem discovered the distribution pattern of sample means, making it extremely important.

Sample means follow a normal distribution, but there are two caveats: first, each sample must be independent; second, sometimes outliers are more important than the mean.

## Tools

1、[DOCX Editor](https://github.com/eigenpal/docx-editor)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052202.webp)

An open-source WYSIWYG web editor for docx files.

2、[DvnIP](https://dynip.dev/)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052601.webp)

A dynamic IP service, free for personal users.

3、[Graphite](https://editor.graphite.rs/)

![](https://cdn.beekka.com/blogimg/asset/202410/bg2024101704.webp)

A vector graphics web application, [open source](https://github.com/GraphiteEditor/Graphite).

4、[Hindsight](https://github.com/chaosprint/hindsight)

![](https://cdn.beekka.com/blogimg/asset/202601/bg2026010203.webp)

A command-line tool that scans local git repositories and generates a GitHub-style personal contribution heatmap.

5、[NyaTerm](https://github.com/nyakang/nyaterm)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052201.webp)

A cross-platform desktop application that brings SSH, terminal sessions, remote files, authentication information, port forwarding, and configuration backup into one workspace. ([@nyakang](https://github.com/ruanyf/weekly/issues/10021) contributed)

6、[diving-rs](https://github.com/wagoodman/dive)

A command-line tool that displays the file list of each layer inside a Docker image. ([@vicanso](https://github.com/ruanyf/weekly/issues/10037) contributed)

7、[CanvasCast](https://github.com/nine19een/CanvasCast)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052401.webp)

A whiteboard recording web application for drawing, presenting, and recording whiteboard-style content directly in the browser. ([@Hao4Wang](https://github.com/ruanyf/weekly/issues/10055) contributed)

8、[Echo Loop](https://github.com/echo-loop/Echo-Loop)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052704.webp)

An open-source English listening and speaking training app. ([@echo-loop](https://github.com/ruanyf/weekly/issues/10082) contributed)

9、[Vue TUI](https://github.com/Simon-He95/vue-tui)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052705.webp)

A Vue-based terminal component library, can be used to develop agents. ([@Simon-He95](https://github.com/ruanyf/weekly/issues/10083) contributed)

10、[witr](https://github.com/pranshuparmar/witr)

![](https://cdn.beekka.com/blogimg/asset/202601/bg2026010313.webp)

A command-line tool that shows which command corresponds to each process, can be queried by command name or port number.

## AI Related

1、[DeepSeek Reasonix](https://github.com/esengine/DeepSeek-Reasonix)

A terminal AI programming agent designed specifically for DeepSeek, fully utilizing the cache mechanism to greatly reduce costs. Only supports DeepSeek's paid API.

2、[FunASR](https://github.com/modelscope/FunASR)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052402.webp)

An industrial-grade speech recognition toolkit open-sourced by Alibaba Tongyi Lab, recently launched a desktop voice input method tool. ([@LauraGPT](https://github.com/ruanyf/weekly/issues/10056) contributed)

Two derivative tools based on it:

- [FunClip](https://github.com/modelscope/FunClip): Intelligent video clipping tool. Input keywords or sentences, automatically locate corresponding segments in the video, and clip and export with one click. ([@LauraGPT](https://github.com/ruanyf/weekly/issues/10057) contributed)
- [SenseVoice](https://github.com/FunAudioLLM/SenseVoice): Speech understanding tool, can recognize speech, language, emotion, and sound events. ([@LauraGPT](https://github.com/ruanyf/weekly/issues/10058) contributed)

3、[Codex Mate](https://github.com/SakuraByteCore/codexmate)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052706.webp)

An all-in-one local AI programming agent management panel. Unified management of Codex, Claude Code, Gemini CLI, CodeBuddy, OpenClaw, Gemini CLI. ([@ymkiux](https://github.com/ruanyf/weekly/issues/10088) contributed)

## Resources

1、[Calculus Made Easy](https://github.com/KeyAI/calculusmadeeasy-zh)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052407.webp)

An unofficial Chinese translation of the famous textbook "Calculus Made Easy", an easy-to-read introductory calculus book. Can be [read online](https://keen-ginger-62hw.here.now/). ([@KeyAI](https://github.com/ruanyf/weekly/issues/10065) contributed)

2、[Xiaoxitian 3D Panorama](https://funes.world/apps/the-hanging-sculptures-of-the-xiaoxitian)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052104.webp)

A web-based 3D panoramic tour of Xiaoxitian in Xi County, Shanxi Province.

3、[C Language Quiz](https://stefansf.de/c-quiz/) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052304.webp)

A set of C language syntax multiple-choice questions.

## Images

1、[Pocket Calculator Museum](https://www.calculators.de/)

There is an online museum in Germany dedicated to collecting various pocket calculators, including some unusual electronic calculators.

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052205.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052206.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052207.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052204.webp)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052203.webp)

## Digest

1、[Behavioral Economics Decoy](https://www.sina.cn/news/detail/5279286413232198.html)

Behavioral economist Dan Ariely was browsing The Economist website one day.

On the subscription page, he saw three options:

> A. Digital Edition – $59.
> B. Print Edition – $125.
> C. Print + Digital Edition – $125.

He was stunned.

B and C were the same price. One gives only print, the other gives both print and digital. Who would choose B?

No one, right? But Ariely didn't laugh; he immediately realized it was a brilliant design.

He took these three options into a classroom at MIT and conducted an experiment, asking 100 students to choose among them.

Results: 16% chose A, 0% chose B, 84% chose C. Total subscription revenue: $11,444.

As expected, no one chose B.

Then Ariely did a small thing: he removed B, leaving only A and C.

Logically, something that no one ever chose, removing it shouldn't affect the result, right?

Results: 68% chose A, 32% chose C. Total subscription revenue plummeted to $8,012.

That's the role of option B. It was never chosen, never sold a single copy, but secretly helped the most expensive option C sell 52% more.

Just by its "existence," it made the magazine an extra $3,432. This is the famous "decoy effect" in behavioral economics.

The principle is simple: humans are not good at judging the "absolute value" of something, but extremely good at making "relative comparisons."

When there are only two options, $59 and $125, your brain compares "cheap vs expensive," and most choose cheap.

But when the decoy "$125 for print only" appears, your brain stops comparing A and C; it starts comparing B and C.

Same price, C gives an extra digital edition. Wow, it's a steal! So you happily choose C.

Unaware that you just spent an extra $66 on a print magazine you might never open.

This trick is everywhere now. The medium cup price at coffee shops is just to make the large cup seem "more worthwhile." The monthly card for video sites is expensive to make the annual card seem "a must-buy."

At phone launches, there is always a "high price, low spec" model whose only mission is to make the flagship model next to it look like "great value."

When you feel you've gotten a bargain, chances are someone has carefully placed a decoy to lead you willingly through the more expensive door.

The option no one chooses is the real star of the show.

## Quotes

1、

Many people can't see the potential of AI to change the world because they don't understand that everything is an algorithm.

Specifically, they don't realize that societies and companies are just collections of algorithms.

-- [Companies Are Just Graphs of Algorithms](https://danielmiessler.com/blog/companies-graph-of-algorithms)

2、

To deal with "software package poisoning," the current popular approach is to set a cooling-off period for newly released packages. Ordinary users need to wait until the "cooling period" is over before they can install the package.

This mechanism can effectively defend against supply chain attacks, but it has a tricky problem: it relies on others to install the package first. Where do you find people to try every newly released package immediately?

-- [Software Packages Should Be Rolled Out in Phases](https://illegalcode.net/rfcs/phased_rollouts.html)

3、

AI can provide one-on-one customized education, which is more effective. Universities will become worthless for many people.

-- [Sam Altman](https://fortune.com/2025/07/24/sam-altman-college-not-working-great-stanford-dropout/), CEO of OpenAI

4、

Non-technical middle managers who have never written a line of code now feel that the biggest obstacle to success has disappeared.

They no longer have to deal with those annoying programmers. They can change web page styles and user experience without programmers, and implement certain functions themselves. Moreover, AI won't complain, won't form unions, and won't protest; it only obeys any command.

-- [Where Will AI Lead Us?](https://pop.rdi.sh/where-does-next-token-prediction-leave-us/)

5、

One reason I like PHP is that its variables are identified by the dollar sign ($), which reminds you what you're using it for.

-- [PHP's Oddities](https://flowtwo.io/post/php's-oddities)

## Past Issues

[GitHub Issues (Almost) Is the Best Note App](https://www.ruanyifeng.com/blog/2025/06/weekly-issue-351.html) (#351)

[OpenAI's Library Cubicle](https://www.ruanyifeng.com/blog/2024/05/weekly-issue-301.html) (#301)

[Domestic Single-Board Computers Worth Recommending](https://www.ruanyifeng.com/blog/2023/04/weekly-issue-251.html) (#251)

[China Needs to Establish a Semiconductor Department](https://www.ruanyifeng.com/blog/2022/04/weekly-issue-201.html) (#201)

(End)