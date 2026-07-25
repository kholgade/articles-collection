# Tech Enthusiast Weekly (Issue 399): A Visit to China's AI Giants

Here is a record of tech content worth sharing each week, published on Fridays.

This magazine is [open source](https://github.com/ruanyf/weekly), and [submissions](https://github.com/ruanyf/weekly/issues) are welcome. There is also a [Who's Hiring](https://github.com/ruanyf/weekly/issues/10147) service that publishes programmer job postings. For cooperation, please [email](mailto:yifeng.ruan@gmail.com) (yifeng.ruan@gmail.com).

## Cover Image

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060402.webp)

The Shenzhen International Art Museum opened this week. ([via](https://sa.trip.com/moments/detail/shenzhen-26-146282837?locale=en-SA))

## A Visit to China's AI Giants

In early May this year, a US delegation visited China, touring 14 AI and robotics companies.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060104.webp)

The visited companies included DeepSeek, Moonshot AI, MiniMax, Zhipu AI, ByteDance, Alibaba, Ant Group, Xiaomi, 01.AI, Unitree, ModelScope, and others.

All members were tech analysts. After returning to the US, each wrote their impressions: [Kevin Xu](https://interconnect.substack.com/p/chinai-mood-april-26-may-4-2026), [afra Wang](https://afraw.substack.com/p/mandate-of-ai), [Florian Brand](https://florianbrand.com/posts/china-trip), [Nathan Lambert](https://www.interconnects.ai/p/notes-from-inside-chinas-ai-labs), [Azeem Azhar](https://www.exponentialview.co/p/inside-chinese-ai-labs-efficiency-moat), [Lily Ottinger and Kai Williams](https://archive.md/myA7R), [Jasmine Sun](https://jasmi.news/p/party-in-the-permanent-underclass), [Lingua Sinica](https://linguasinica.substack.com/p/notes-from-a-trip-to-chinas-ai-labs), [Caithrin](https://www.caithrin.com/p/searching-for-amanda-askell-with).

These articles contain many interesting points. I've made some excerpts. To ensure a smooth reading experience, I won't separately note the source for each paragraph.

### 1. The Computing Power Gap

At every company, we heard a common complaint: insufficient computing power. This leads to fewer experiments and smaller model sizes.

China's computing power shortage is mainly caused by US chip export control policies. We were interested in seeing firsthand how local companies are coping.

Although supply is not completely cut off, Chinese companies can still obtain NVIDIA's H100, B200, and B300 GPUs, but the quantity is at least an order of magnitude less than their US competitors.

NVIDIA's latest GB300 NVL72 system (72 of NVIDIA's newest GPUs forming one system) has real-time inference speeds 30 times faster than the H100 cluster from three years ago, with 3.6 times more memory per chip and 25 times lower energy consumption per inference. US companies are ordering these systems in large quantities, while Chinese companies cannot.

Chinese tech companies, especially Huawei, have made significant progress in developing AI chips. But even Huawei's latest chip, the Ascend 950PR, released in March this year, has performance roughly equivalent to the H100 released in 2022. Moreover, shipments of these chips are far lower than the H100. It is estimated that NVIDIA had shipped 7 million Hopper and Blackwell GPUs by October 2025 alone, and the shipment rate is still growing. Huawei plans to ship 750,000 Ascend 950PR chips this year, which is still only about one-tenth of NVIDIA's shipments last year.

The result is that the US has a huge lead in computing power. We estimate that by the end of 2025, the US AI industry's computing power will be about 8 times that of China. The total computing power of Chinese AI companies is roughly equivalent to the US scale in 2023.

We shared with Chinese researchers the number of GPUs per researcher at OpenAI. They were stunned when they heard the number. Yet, we all know that OpenAI researchers, or researchers at all Western AI companies, still complain about having too little computing power.

### 2. Allocation of Computing Power

Most of the computing power in the US is used for model training, not for serving customers. However, the situation in China is different: computing power must be used both for training models and for serving hundreds of millions of consumers and rapidly growing enterprise users.

If half of the computing power is used to serve customers, then the computing power available for model training is reduced.

There is another factor to consider. In the US, computing power is dominated by five companies: OpenAI, Anthropic, Google, Meta, and xAI. In China, major tech companies are all actively developing their own frontier models, further fragmenting the computing power pool.

### 3. Computational Efficiency

If we follow this logic, since China's computing power scale lags behind the US by two years, Chinese models should also lag behind US models by at least two years. But that is not the case.

Many analyses suggest that Chinese models are only a few months behind US models. In fact, in some aspects, the models of the two countries seem to be on par.

The reason is that chip restrictions have instead prompted Chinese companies to improve computational efficiency. We found that the AI intelligence supported per unit of computing power in Chinese companies is 4-7 times that of simple scaling, which compensates for the lack of computing power.

### 4. The Open Source Divide

Currently, the best open-source AI models are released by Chinese companies. However, there is a divide within Chinese companies over whether to open source their models.

The company's financial situation and revenue pressure affect the willingness to open source. Currently, a clear boundary is emerging: model parameter scale reaching one trillion.

Some companies believe that open-sourcing models with one trillion or more parameters is a waste of resources, because no one can run such a large model on a local machine, and the typical use case for open-source models is local machines. A better way to release a trillion-parameter model is to host it on the company's own cloud infrastructure and only release its API for user convenience.

But for other companies, open-sourcing models is almost a belief, and building a trillion-parameter model is the ticket to the open-source community.

### 5. Westernization or Sinicization

Some Chinese AI companies exhibit a typical "Western" style, full of Silicon Valley coolness, even reflected in the promotional merchandise they give away.

Other companies are becoming more "Chinese," making it a top priority to build a flashy showroom. These showrooms are used to receive visitors, usually state-owned enterprise CEOs and local officials. After the visit, a dinner banquet is held.

I think this is both a choice and a necessity, stemming from the founder's background and the type of business the company chooses.

### 6. Views on Other Companies

We found that all Chinese AI companies are in awe of ByteDance's Seed team. It is China's only closed-source AI frontier team. It's like the elephant in the room, but it's dancing. Its Doubao (豆包) almost monopolizes AI user traffic, and their models can be quickly promoted to massive users, something other companies cannot match.

DeepSeek is the most respected company in the industry, increasingly taking on foundational work: architecture, efficiency, inference optimization, and adaptation to the Huawei stack.

### 7. Interns

Many employees at Chinese AI companies are brilliant "interns," with an average age of 25-26. Most are still doctoral students and can easily discuss technical topics in English. They mostly graduated from Chinese universities and have no overseas study experience.

Their internships last one to two years, with full-time employee benefits and complete permissions, allowing them to freely propose ideas and conduct experiments. This is in stark contrast to top Western AI companies. OpenAI, Anthropic, Cursor, etc., do not offer internships at all. Other companies (like Google) nominally offer internships for Gemini but do not assign important tasks.

Chinese companies value "fresh blood" more, as they can bring new ideas and ample brainpower. To improve the final model, interns are more willing to do less glamorous work. Moreover, people new to AI development can be free from the influence of previous paradigms.

From the perspective of Chinese universities, the school's computing resources are simply insufficient to fully develop the talents of outstanding students. It's better to send them to industry companies with richer computing resources, where both sides can collaborate on papers and achieve a win-win.

### 8. Attitudes Toward AI Safety

I asked some young Chinese researchers what they thought about AGI (Artificial General Intelligence). They surprisingly gave the exact same answer: "AGI is when AI can replace me!"

I found that they showed no concern. Not only are they not afraid of being replaced, but they are also curious about whether machines can truly surpass their creators. If that happens, they would gladly go do other things.

This is in stark contrast to their Western counterparts, many of whom are very concerned about AI safety and its social impact. Chinese researchers also value safety; everyone believes AI should not do bad things. But how to ensure this, they all feel it should be left to the government to decide, and the government should be able to solve it.

### 9. Chinese Enterprises' AI Demand

Are Chinese enterprises willing to pay for domestic AI services?

A widely held view is that the Chinese AI market is small because Chinese enterprises are generally unwilling to pay for software, thus unable to support domestic AI companies.

This view only applies to SaaS model software spending, which has historically been small in China. However, China clearly has a huge cloud computing market.

Chinese AI companies are debating whether Chinese enterprises see AI services as SaaS products (smaller scale) or cloud computing (larger scale). Currently, the trend in AI seems to lean more towards cloud computing.

### 10. Data Industry Lags Behind the US

We heard that US AI companies like Anthropic or OpenAI spend over $10 million annually on training data (or reinforcement learning environments), with cumulative spending reaching hundreds of millions of dollars. We were curious if Chinese AI companies do the same.

The answer was that China has almost no data industry, because many AI companies feel that the quality of Chinese data products is poor, so preparing data themselves is often more ideal.

Researchers spend a lot of time building reinforcement learning training environments, while large companies like ByteDance and Alibaba have internal data annotation teams to support this work.

### 11. The Role of Government

Who is the real driving force behind China's AI field? The equivalent of Sequoia Capital and a16z in Silicon Valley.

A friend of mine answered: the municipal governments of Shanghai, Beijing, and Hangzhou. These hardworking yet exhausted government officials, completely driven by "fear of missing out" and competitive anxiety, are desperately pushing the local AI industry.

## [Event] XEngineer College Student Training Camp

Attention college students! In the AI era, how to cultivate your abilities without getting lost in the sea of resumes and written exams? Consider this summer's [XEngineer Training Camp](https://mp.weixin.qq.com/s/Ues5CUilqWqCgWMf3SZAAw?from=singlemessage&scene=1&subscene=93&sessionid=1780549607&clicktime=1780550030&enterid=1780550030&ascene=1&fasttmpl_type=0&fasttmpl_fullversion=8285001-zh_CN-zip&fasttmpl_flag=0&realreporttime=1780550030045).

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060404.webp)

It is initiated by **Xu Shiwei, founder and CEO of the listed company Qiniu Cloud**, targeting college graduates and current students from the classes of 2025–2029. No degree or major restrictions apply. **You only need to submit a work proposal or project outcome to apply.**

It trains students in product and architecture capabilities in the AI era, guiding you to start from real needs, think clearly, and then personally design, implement, and launch a project.

You can experience the real work of an internet company, cultivate your practical skills, and gain job qualifications and offer opportunities.

Visit **hr.qiniu.com** or scan the QR code below to register. The earlier you register, the earlier you secure a spot, until the camp opens in July.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060407.webp)

After registration, you will receive specific topics. You need to submit a work proposal and project outcome within 72 hours. The organizing committee will review, followed by roadshows/discussions. Outstanding works will be selected before the camp opens, with a total prize pool of 200,000 yuan.

After the camp opens, over the two summer months, a team of senior mentors and teaching assistants will guide students to complete a real project.

## Articles

1. [My Experience Using AI to Find Bugs](https://newsletter.semianalysis.com/p/finding-miscompiles-for-fun-not-profit) (English)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026053001.webp)

The author used AI to find compiler bugs and found that the cost of running AI was an order of magnitude higher than his salary. Moreover, paying more could find even more bugs.

For the first time, he felt that AI's value was greater than his own.

2. [Health Checks for Load Balancing Nodes](https://singh-sanjay.com/2026/01/12/health-checks-client-vs-server-side-lb.html) (English)

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022403.webp)

This article introduces how load balancing can be done on the server or the client, and how to check for faulty nodes in both cases.

3. [Four Scenarios Where HTML Replaces JS](https://www.htmhell.dev/adventcalendar/2025/27/) (English)

![](https://cdn.beekka.com/blogimg/asset/202512/bg2025122903.webp)

This article proposes that HTML + CSS is already powerful enough that many scenarios can be implemented without JS, using only HTML, such as modals and overlays.

4. [How to Link Phone Numbers on Web Pages](https://sethmlarson.dev/mobile-browsers-and-telephone-numbers) (English)

![](https://cdn.beekka.com/blogimg/asset/202511/bg2025112601.webp)

When a mobile browser opens a webpage, it automatically adds links to phone numbers found on the page, allowing you to tap to call. This article teaches you how to customize this behavior, including removing the link or tapping to call a different number.

5. [Using Custom HTML Elements](https://maurycyz.com/misc/make-up-tags/) (English)

![](https://cdn.beekka.com/blogimg/asset/202512/bg2025122903.webp)

Web pages can use custom HTML elements instead of `div` to provide better semantics.

6. [How Deep is the Challenger Deep?](https://storymaps.arcgis.com/stories/0d389600f3464e3185a84c199f04e859) (English)

![](https://cdn.beekka.com/blogimg/asset/202511/bg2025112404.webp)

A图文 article that uses vivid images to explain the deepest point on Earth, the Challenger Deep, which is about 11,000 meters deep.

## Tools

1. [Breathe CLI](https://github.com/marekkowalczyk/breathe-cli)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026053103.webp)

A command-line program for Mac that displays a progress bar to guide you through slow breathing, about 6 breaths per minute, to improve heart function.

2. [NMLinux](https://github.com/thongor77/nmlinux)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060201.webp)

A graphical panel for network management on Linux systems.

3. [Penpot](https://github.com/penpot/penpot)

![](https://cdn.beekka.com/blogimg/asset/202404/bg2024041001.webp)

An open-source design tool that can replace Figma, converting visual layout designs into CSS + HTML code.

4. [sky adb](https://github.com/sky22333/skyadb)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052901.webp)

An ADB management tool running on Android phones, managing phones, tablets, and TV boxes via WiFi ADB / Wireless Debugging. ([@sky22333](https://github.com/ruanyf/weekly/issues/10101) submission)

5. [readNeo](https://github.com/extrastu/readneo)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052903.webp)

A WeRead data panel that connects to the WeRead Skill API, visualizing bookshelves, reading statistics, notes, and highlights, with one-click export. ([@extrastu](https://github.com/ruanyf/weekly/issues/10110) submission)

6. [AppPorts](https://github.com/wzh4869/AppPorts)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052904.webp)

An open-source app that migrates macOS applications to external storage while keeping them running normally, with the ability to restore at any time. ([@wzh4869](https://github.com/ruanyf/weekly/issues/10119) submission)

7. [Fight the Landlord](https://github.com/palemoky/fight-the-landlord)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060101.webp)

An open-source terminal card game (Fight the Landlord) implemented in Go, supporting online multiplayer, reconnection, and intelligent bots. ([@palemoky](https://github.com/ruanyf/weekly/issues/10149) submission)

8. [fuckssh](https://github.com/hczs/fuckssh)

A command-line tool that wraps SSH-related commands, providing an interactive wizard for server key configuration. ([@hczs](https://github.com/ruanyf/weekly/issues/10184) submission)

9. [StarGuard](https://github.com/m-ahmed-elbeskeri/Starguard)

This Python tool checks how many stars on a given GitHub repository are fake.

10. [Nginx Proxy Manager](https://github.com/NginxProxyManager/nginx-proxy-manager)

![](https://cdn.beekka.com/blogimg/asset/202505/bg2025051008.webp)

This open-source tool uses a web interface to manage Nginx reverse proxies and automatically enables SSL certificates. See the [introduction article](https://www.xda-developers.com/nginx-proxy-manager-best-reverse-proxy/).

## AI Related

1. [Models.dev](https://github.com/anomalyco/models.dev)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052303.webp)

An open-source database that collects specifications and prices of all AI models.

2. [pixtuoid](https://github.com/IvanWng97/pixtuoid)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026052902.webp)

A creative tool that uses pixel characters to represent AI agents, displaying work progress in terminal animations. ([@IvanWng97](https://github.com/ruanyf/weekly/issues/10105) submission)

3. [Flipbook Canvas](https://github.com/imcuttle/flipbook-app)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060204.webp)

Uses AI to generate clickable albums (a series of related images). Based on the text at the click location, it automatically navigates to the corresponding next page. See the example [2026 World Cup](https://imcuttle.github.io/flipbook-app/3CxOnV76roLd/). ([@imcuttle](https://github.com/ruanyf/weekly/issues/10103) submission)

4. [album-assetizer](https://github.com/SeanWong17/album-assetizer)

![](https://cdn.beekka.com/blogimg/asset/202605/bg2026053101.webp)

A command-line tool that scans personal photo albums and uses AI to generate structured descriptions for each image. Results are saved locally in SQLite and can be exported as JSONL/CSV. ([@SeanWong17](https://github.com/ruanyf/weekly/issues/10140) submission)

## Resources

1. [Complete Collection of Gaokao (College Entrance Exam) Past Papers](https://t.urongda.com/)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060401.webp)

This website collects past Gaokao exam papers from various provinces over the years. Also see this [GitHub repository](https://github.com/deekur/gaokaomath). ([@urongda](https://github.com/ruanyf/weekly/issues/10190) submission)

## Images

1. [Cylindrical Projection](https://liorsinai.github.io/mathematics/2020/08/27/secant-mercator.html)

Drawing a flat map of the Earth essentially involves mapping spherical coordinates to planar coordinates.

One method is to imagine a piece of paper wrapped into a cylinder around the Earth. Then, following the Earth's rotation, each point on the ground is projected onto this cylinder.

![](https://cdn.beekka.com/blogimg/asset/202504/bg2025042106.webp)

## Digest

1. [When Does a Software Engineer Retire?](https://thecodist.com/how-to-know-when-its-time-to-go/)

After a year of consideration, I decided to leave my programmer position and retire.

The reason for retirement is not a lack of ability, but that I no longer want to continue.

Everyone eventually reaches a tipping point where they can no longer do what they have been doing all their lives. This has nothing to do with age; I know people much younger than me who have also given up the programmer profession.

The reasons for retirement I have seen are as follows.

(1) Lack of ability. You can no longer complete the tasks assigned to you, and your abilities are not suitable for the industry's needs.

(2) Lack of desire. You have lost interest in the industry.

(3) Poor job market or employer bankruptcy. You cannot find the next job.

(4) Outdated skills. Your skills are no longer needed.

(5) You find other worthwhile things to do.

(6) You have made a lot of money, then feel exhausted and lack sufficient motivation, finding that you no longer care about the tasks at hand.

All programmers will eventually give up the programmer job for one of the above reasons.

I have also seen people who value salary and will keep working as long as they get paid, regardless of whether they like it. That is also a choice, but I am not willing to do that—working while suffering is not worth it.

I like to make changes and accept challenges to do important things and work. Money is good, but I like to make a difference.

Everyone eventually reaches a moment when a job, employer, industry, or even an entire career ends. Being honest and making wise decisions is much better than falling behind and possibly being forced out.

## Quotes

1.

Why do humans have whites in their eyes? Most mammals (like monkeys and apes) do not have whites in their eyes. One explanation is that it allows us to see where others are looking.

-- [Why Humans Have Whites in Their Eyes](https://www.popsci.com/science/why-humans-have-white-part-eyes/)

2.

One reason for (Microsoft CEO) Nadella's success is that he ended Windows—or more precisely, ended Windows as Microsoft's core product—and focused more on developing software that is everywhere and a cloud platform that covers everything.

-- [Microsoft's AI Strategy](https://stratechery.com/2026/the-nvidia-ai-pc-project-solara-microsoft-ai/)

3.

In 1969, two American doctors established a psychological model to analyze the psychology of terminally ill patients, proposing five stages: denial, anger, bargaining (pleading), depression, and acceptance. This model is now also used to analyze cases of unemployment caused by artificial intelligence.

-- [AI Job Grief](https://jackmaguire.org/blog/ai-job-grief/)

4.

Vibe coding generates code; engineering generates systems. Vibe programming is not engineering.

-- [Vibe Programming Is Not Engineering](https://phroneses.com/articles/build/notes/vibe-coding-is-not-engineering.html)

5.

There are three ways to make a living: (1) Tell lies to those who want to hear lies, and you will get rich. (2) Tell the truth to those who want to hear the truth, and you can make a living. (3) Tell the truth to those who want to hear lies, and you will go bankrupt.

-- [Three Ways to Make a Living](https://jasonzweig.com/three-ways-to-get-paid/)

## Past Reviews

[The Correct Look of a Bug Tracking System](https://www.ruanyifeng.com/blog/2025/06/weekly-issue-352.html) (#352)

[Entrepreneurship is Good, But I Dare Not Recommend It Anymore](https://www.ruanyifeng.com/blog/2024/05/weekly-issue-302.html) (#302)

[Internet Entrepreneurship Has Become Harder](https://www.ruanyifeng.com/blog/2023/04/weekly-issue-252.html) (#252)

[Three Inspiring Learning Methods](https://www.ruanyifeng.com/blog/2022/04/weekly-issue-202.html) (#202)

(End)