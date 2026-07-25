# Tech Enthusiast Weekly (Issue 401): How to Make $1 Billion

Here records the weekly tech content worth sharing, published on Fridays.

This magazine is [open source](https://github.com/ruanyf/weekly), and [contributions](https://github.com/ruanyf/weekly/issues) are welcome. There is also a ["Who's Hiring"](https://github.com/ruanyf/weekly/issues/10147) service for posting programmer job openings. For collaboration, please [email](mailto:yifeng.ruan@gmail.com) (yifeng.ruan@gmail.com).

## Cover Image

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060403.webp)

In southern China, people wear sun-protective masks made from giant lotus leaves. ([via](https://www.sohu.com/a/906763935_121284943))

## How to Make $1 Billion

Paul Graham is the founder of Y Combinator, the largest startup accelerator in the United States. He is widely recognized as a startup mentor and the author of *Hackers and Painters*.

He is now retired, having left Silicon Valley to live in the English countryside.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061503.webp)

On June 10th of this year, he gave [a talk](https://paulgraham.com/earn.html) at the invitation of a student society at Oxford University, with the explosive title "How to Make $1 Billion."

I found the content quite interesting and have excerpted some parts below.

1.

Some people seem to think that making $1 billion is impossible unless you use illegal or unethical means.

In my view, making $1 billion is indeed difficult, but not impossible, and the opportunities are greater than most people imagine.

2.

21 years ago, in 2005, we founded the startup accelerator Y Combinator, and to date we have invested in approximately 6,500 startups.

Among the founders of these companies, about 30 have already become billionaires. Moreover, many more are rapidly approaching that goal.

With 6,500 companies and an estimated 20,000 founders, 30 of whom have made $1 billion—the odds are not that small.

3.

The path they all took to making $1 billion was by founding a successful company.

4.

Recently, I was chatting with a founder. I asked her about her company's growth rate, and she said it was 93% last month. This means her net worth is likely growing at the same rate.

Let's do a simple calculation.

Assume her net worth is currently $2 million, all invested in her own company. Then the company only needs to grow 500 times for her assets to reach the billion-dollar level.

How many months do you think it would take for her company to achieve 500x growth?

5.

Assuming the company can maintain a monthly growth rate of 93%, we just need to calculate the logarithm of 500 with base 1.93, i.e., log(500, 1.93).

The answer is 9.45.

That means, starting from $2 million, **maintaining a monthly growth rate of 93%, it would take only nine and a half months to achieve 500x growth**, thereby making you a billionaire.

Now you understand why, when I meet founders, the first thing I ask is their growth rate.

6.

You might say that a 93% monthly growth rate is unrealistic. Then let's consider a 15% monthly growth rate. After five years, how many times would you have grown?

Let's calculate 1.15 raised to the 60th power (since five years is 60 months). 1.15^60 is approximately 4,384.

That means after five years, your company's revenue would be about 4,384 times its current level.

If your company's current monthly revenue is $10,000, at that growth rate, after five years your monthly revenue would be about $44 million, or $526 million annually. At that point, if you hold company shares like most founders, you would become a billionaire.

In fact, a 15% monthly growth rate corresponds to an annual growth rate of less than 5.5x. Many startups can achieve or exceed this growth rate.

In short, if you start a company in your early twenties and maintain a high growth rate, becoming a billionaire by the time you're thirty is absolutely possible.

7.

The key to maintaining a high growth rate is that you must create a product good enough that people tell others about it, ensuring a steady stream of customers.

This is another reason why I always ask founders about their growth rate first. **The growth rate reflects whether they are building the right product.**

8.

Any idea that you genuinely believe is worth developing, no matter how absurd it sounds, is highly likely to evolve into a good startup idea.

No matter how absurd your idea is, it can't be more absurd than Justin.TV, which we invested in back in 2006.

That company had just one person: founder Justin Kan. He strapped a camera to his head, walked around, and live-streamed everything he experienced.

Later, he built a platform that allowed others to live-stream like him. Eventually, the company did quite well. You may have heard of it—it's now called Twitch.

9.

The key to starting a business is to deeply understand a specific user group so that you can precisely build the product they truly want.

What do users really want? What can you do for them that will significantly improve their lives?

That is the empathy of entrepreneurship, and it's the quality we look for and cultivate in founders.

10.

Making $1 billion through entrepreneurship ultimately comes down to two determining factors: growth rate and the duration of growth.

**Growth rate comes from building a product that users love and are eager to share; duration of growth comes from entering a large market.**

If your startup can grow exponentially and capture a large market, its value will skyrocket, and as a shareholder, you will naturally become wealthy—likely making $1 billion.

## How Speed Testing Websites Make Money

In March, consulting giant Accenture spent [$1.2 billion](https://www.theverge.com/tech/889234/downdetector-ookla-speedtest-sold-accenture) to acquire [Speedtest](https://www.speedtest.net/) and [Downdetector](https://downdetector.com/).

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026060103.webp)

Both are free websites—one for testing internet speed (pictured above), the other for checking if a website is down. This has left many people puzzled: why are free websites so valuable?

According to [insiders](https://news.ycombinator.com/item?id=48339253), Speedtest is actually a very profitable business. Every day, countless visitors from around the world use it to test their speeds, and many software applications integrate it to assess network conditions. As a result, it has a massive trove of real-world speed data, covering different regions and network types.

Speedtest makes money by selling this data. As the world's largest testing website, telecom operators are willing to purchase its data to improve their own networks. Each data set is priced in the six-figure dollar range, and with many clients each year, Speedtest generates substantial profits.

Thus, what Accenture actually acquired was a data business: users generate the data, and the company packages and sells it. Essentially, free websites have only two ways to make money: advertising or selling user-generated or personal data.

## PRs Are Not Free

SQLite author Richard Hipp [explained](https://lobste.rs/s/aqk8vl/pull_requests_are_free_puppies) in [an interview](https://www.youtube.com/watch?v=x8_ZZhRL3YU&t=1733s) why his project never accepts external PRs.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062008.webp)

Suppose you have a PR for SQLite. You come to me and say, "Hey, I've developed a new feature for SQLite, here's my PR."

When you want me to merge it into the codebase, you say, "Oh, it's free."

No, a PR is not free.

What you're actually asking me is: you've developed this great feature, and now you want me to maintain it for you, write documentation for it, test it, and keep maintaining it for the next twenty-five years. That's not free.

Linus once famously said: Free can mean free beer, or free speech. But there's another kind of free: free puppies. "Look, I've got a free puppy for you." You know what I mean?

Submitting a pull request is like someone giving you a puppy. By the end of the day, you've got a puppy in your house. You can't just throw it away—you have a moral obligation to take care of it until it dies of natural causes.

I don't want any free puppies.

## One-Sentence News

(1) A study found that [grip strength](https://join1440.com/r/20950) (how firmly you can grasp an object) is a better predictor of mortality risk than blood pressure.

For adults, every 5 kg decrease in grip strength increases the risk of death by 16%.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062001.webp)

(2) How expensive is storage? Sandisk has launched a [game-specific hard drive](https://games.gg/zh-CN/news/sandisk%E6%96%B0%E6%AC%BEps5-ssd%E5%94%AE%E4%BB%B7%E6%83%8A%E4%BA%BA%E8%B6%85%E8%BF%87%E4%B8%89%E5%8F%B0ps5-pro%E7%9A%84%E6%80%BB%E4%BB%B7/) for the PS5, with a capacity of just 8TB, priced at a staggering $3,000 — three times the cost of the PS5 itself!

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062002.webp)

(3) Greece recently [restored](https://apnews.com/article/greece-acropolis-restoration-parthenon-tourism-da06640fcd747498613d31b64dac369a) the famous Parthenon temple on the Acropolis, replacing the missing marble.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062105.webp)

Below is what the temple looked like before the restoration.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062106.webp)

## Articles

1. [Detailed Explanation of the New HTTP QUERY Method](https://kreya.app/blog/new-http-query-method-explained/) (English)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062505.webp)

HTTP has officially introduced the QUERY method in addition to GET and POST.

It is essentially a GET method with a body, allowing large numbers of parameters to be sent at once, and these parameters are not cached by the server.

2. [Anonymous Token Protocol PACT](https://www.cloudflare.com/press/press-releases/2026/cloudflare-collaborates-with-leading-browsers-to-develop-a-privacy-first-protocol-for-the-global-internet/) (English)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062506.webp)

Cloudflare, together with the three major browsers—Chrome, Firefox, and Edge—has announced the development of a new protocol to identify bot traffic.

The browser adds a token to HTTP requests from real humans, and the server uses this token to determine whether the visitor is a bot. Specific details are not yet clear. For more information, refer to [Mozilla's article](https://hacks.mozilla.org/2026/06/pact-anonymous-credentials-for-the-web/). In theory, this would eliminate the need for CAPTCHA verification codes.

3. [The Rise and Fall of OpenCL](https://www.modular.com/blog/democratizing-ai-compute-part-5-what-about-cuda-c-alternatives) (English)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061502.webp)

A retrospective article. In the early 2000s, some companies began envisioning a general-purpose C++ framework for GPU operations. However, due to conflicting interests among stakeholders, consensus could not be reached in the standards committee, and the effort ultimately failed.

In the end, Nvidia's CUDA framework replaced it, becoming the standard method for GPU operations, and Nvidia consequently became the dominant player in AI hardware.

4. [Stop Using JWT](https://gist.github.com/samsch/0d1f3d3b4745d778f78b230cf6061452) (English)

This article argues that JWT tokens should not be used to maintain user login state—that is the role of cookies. The only appropriate use case for JWT is transferring user state from one machine to another.

5. [I Stored a Website in a Favicon](https://www.timwehrle.de/blog/i-stored-a-website-in-a-favicon/) (English)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062102.webp)

This article presents an interesting trick: the actual content of a web page is hidden inside the favicon file, and then decoded and rendered using a JavaScript script.

## Tools

1、[Lore](https://github.com/EpicGames/lore)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062101.webp)

A version control system open-sourced by the game company EpicGames. Compared to Git, its main feature is version management for binary files.

It splits large binary files into chunks for storage. Each commit only saves the changed chunks.

2、[DNS Pick](https://github.com/palemoky/dnspick)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061602.webp)

A command-line DNS optimization tool that combines average latency and resolution success rate to select the best DNS server balancing speed and stability. (Contributed by [@palemoky](https://github.com/ruanyf/weekly/issues/10311))

3、[GitFolio](https://github.com/azhai/gitfolio)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061603.webp)

A lightweight Git repository management system, similar to Gitea, supporting syncing repository data from GitHub mirrors. (Contributed by [@azhai](https://github.com/ruanyf/weekly/issues/10316))

4、[ssh-at](https://github.com/baerwang/ssh-at)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061604.webp)

A graphical management tool for `~/.ssh/config`. (Contributed by [@baerwang](https://github.com/ruanyf/weekly/issues/10330))

5、[LockIME](https://github.com/oomol-lab/LockIME)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061202.webp)

An input method locking tool for macOS that allows specifying the default input method for different applications. (Contributed by [@BlackHole1](https://github.com/ruanyf/weekly/issues/10279))

6、[Cover Maker](https://github.com/eternityspring/article-tools)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061203.webp)

A web tool for creating cover images. (Contributed by [@Hao4Wang](https://github.com/ruanyf/weekly/issues/10276))

7、[PowerLens](https://github.com/luyangkk/powerlens)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061606.webp)

An Oh-My-Zsh plugin that displays real-time power consumption, battery, CPU, CPU temperature, fan speed, memory, and network traffic in the command prompt. (Contributed by [@luyangkk](https://github.com/ruanyf/weekly/issues/10345))

8、[MyKVM](https://github.com/XxMinor/mykvm)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061802.webp)

A cross-platform KVM software that allows macOS, Windows, and Linux to share a single set of keyboard, mouse, and clipboard on the same local network. (Contributed by [@fc221](https://github.com/ruanyf/weekly/issues/10373))

9、[ai_caption_video](https://github.com/alexchan197611/ai_caption_video)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061901.webp)

An open-source Windows application for generating Chinese short videos with large captions, supporting keyword highlighting, subtitle animations, local TTS dubbing, and voice cloning. (Contributed by [@alexchan197611](https://github.com/ruanyf/weekly/issues/10378))

10、[AnyDrag](https://github.com/XueshiQiao/AnyDrag)

A macOS utility that allows dragging, resizing, maximizing, and tiling windows without holding the title bar. (Contributed by [@XueshiQiao](https://github.com/ruanyf/weekly/issues/10398))

11、[Direct Light](https://github.com/oukeming64-tech/direct-light)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062107.webp)

A web simulation of studio lighting. (Contributed by [@oukeming64-tech](https://github.com/ruanyf/weekly/issues/10404))

12、[JSOS](https://jsos.dev/)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062507.webp)

Based on Webcontainer technology, it runs Node.js applications in the browser, with data and code stored locally. (Contributed by [@jsos-dev](https://github.com/ruanyf/weekly/issues/10410))

## AI Related

1. [Fishword](https://github.com/Chenggou1/fishword)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061607.webp)

A plugin for the programming agent Cursor that displays a vocabulary memorization window while waiting for AI to generate code. (Contributed by [@Chenggou1](https://github.com/ruanyf/weekly/issues/10338))

2. [OnePagent](https://github.com/sligter/OnePagent)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061801.webp)

An open-source, browser-native, single-file AI agent workbench. Just open an HTML file to start performing AI operations. (Contributed by [@sligter](https://github.com/ruanyf/weekly/issues/10363))

3. [SlopGuard](https://github.com/Blue-B/slopguard)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061201.webp)

A GitHub app that automatically scores PRs and issues to filter out low-quality submissions. (Contributed by [@Blue-B](https://github.com/ruanyf/weekly/issues/10275))

4. [TiyGate](https://github.com/tiylabs/tiygate)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062104.webp)

A self-hosted AI gateway that can automatically switch between multiple subscription plans and provides a unified management panel. (Contributed by [@jorben](https://github.com/ruanyf/weekly/issues/10401))

5. [Mediary Scout](https://github.com/fancydirty/mediary-scout)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062508.webp)

An open-source agent for searching TV shows and movies, fetching various resources and saving them to your cloud storage. Requires self-deployment. (Contributed by [@fancydirty](https://github.com/ruanyf/weekly/issues/10412))

## Resources

1.  [Chopping Wood](https://screen.toys/firewood/)

    ![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061501.webp)

    A web mini-game that looks particularly realistic.

2.  [Solar Wanderer](https://github.com/hyqzz/Solar-Wanderer)

    ![](https://cdn.beekka.com/blogimg/asset/202606/bg2026061607.webp)

    Display a real-scale solar system in the browser, including 8 planets, the Moon, and 21 moons. (Contributed by [@hyqzz](https://github.com/ruanyf/weekly/issues/10349))

3.  [PTP Time Synchronization Technical Book](https://github.com/Lularible/ptp-book/tree/main/chapters)

    An open-source technical book that introduces the PTP/IEEE 1588 precision time protocol and LinuxPTP source code analysis in plain language. (Contributed by [@Lularible](https://github.com/ruanyf/weekly/issues/10284))

4.  [Cosmodial](https://killedbyapixel.github.io/Cosmodial/)

    ![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062006.webp)

    A web-based star simulator to explore the universe in the browser.

## Images

1、[Virtual Map](https://www.jerrysmap.com/the-map)

An American artist has a habit of doodling. Whenever he has free time, he casually draws some color blocks on paper.

One day, he suddenly realized that these doodles, when pieced together, looked a lot like a virtual map.

So he began to seriously invest in this project, piecing together over 4,000 doodles into a map of a virtual world.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062501.webp)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062502.webp)

When all the color blocks are combined, this virtual world happens to form a circle.

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062503.webp)

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062504.webp)

## Digest

1. [The History of the Meter](https://www.abc.net.au/news/science/2025-05-20/metre-treaty-anniversary-metric-system-measurement-metrology/105302024)

At the end of the 18th century, the French Revolution broke out.

At that time, France had countless different systems of weights and measures, creating chaos. There was even a unit of length established by King Henry I of England in the 11th century: the distance from the king's nose to the tip of his outstretched arm was defined as one yard.

The French revolutionaries decided to create a completely new, unified system of measurement for the entire country. The new unit of length was called the "meter," defined as one ten-millionth of the distance from the North Pole, through the Paris Observatory, to the equator.

![](https://cdn.beekka.com/blogimg/asset/202505/bg2025052519.webp)

However, no one actually knew how long this ten-millionth part was.

The task of measuring it fell to two astronomers. Seven years later, in 1799, they submitted their final measurements to the French Academy of Sciences, which became the length of the "one meter" we know today.

The French Academy then crafted this length into platinum bars, producing a total of 30, which were sent to various places so that people would know the new standard of measurement—the "meter." These platinum bars were called "meter prototypes."

![](https://cdn.beekka.com/blogimg/asset/202606/bg2026062509.webp)

![](https://cdn.beekka.com/blogimg/asset/202505/bg2025052520.webp)

Modern instruments measuring the preserved platinum bars found them to be quite accurate, only 0.2 millimeters shorter than the current standard length.

This definition of the meter was used until the second half of the 20th century. At that time, scientists proposed that distance could be expressed using the wavelength of light, since the wavelength of light is constant. Thus, the definition of the meter was revised: 1 meter equaled 1,650,763.73 times the wavelength of the red-orange light emitted by krypton atoms when an electric current passed through a lamp filled with krypton gas.

However, this red-orange light wavelength was inconvenient for measuring extremely small distances. In 1983, the definition of the meter was changed again to be expressed in terms of the speed of light: 1 meter equals the distance that light travels in a vacuum in 1/299,792,458 of a second.

## Quotes

1、

Improve yourself by benefiting others. That is what we are after.

-- [Why We Hire Junior Engineers](https://newsletter.kentbeck.com/p/hey-n00b-we-didnt-hire-you-to-complete)

2、

The standard for a livable residence in Europe is that you can see at least three trees from the room, the tree coverage rate of the neighborhood is at least 30%, and there is a park within 300 meters.

-- [Can You See Three Trees?](https://www.not-ship.com/can-you-see-three-trees/)

3、

When I read a book published before 2022, I know that every word was manually entered, manually proofread, manually edited, and manually proofread again. Somehow, this affects me, making me value the book and its content more.

-- [Pre-2022 Books](https://notes.lorenzogravina.com/musings/pre-2022-books)

4、

I found myself in the predicament of many engineers at big companies. My title and salary are only slightly higher than a junior engineer's, but the work I do every day is at the "senior" or "staff" engineer level. I fail every promotion, and I feel like I'm constantly solving problems two levels above my own, with the only reward being more work assigned by my superiors.

-- [Why I Left YouTube](https://zhach.news/how-i-left-youtube/)

## Past Years Review

[What Does an 8000mAh Phone Battery Mean?](https://www.ruanyifeng.com/blog/2025/06/weekly-issue-354.html) (#354)

[The Most Popular Color](https://www.ruanyifeng.com/blog/2024/06/weekly-issue-304.html) (#304)

[Life Is a Longboard Problem](https://www.ruanyifeng.com/blog/2023/06/weekly-issue-254.html) (#254)

[How to Get Through Epidemics, Layoffs, and Wars](https://www.ruanyifeng.com/blog/2022/04/weekly-issue-204.html) (#204)

(End)