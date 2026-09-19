## Tests Are the New Moat

[Next.js](https://nextjs.org) is currently the number one JS framework. I'd estimate that half of the JS full-stack apps you encounter are built with it.

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022808.webp)

Two weeks ago, this framework was upended by a news story.

A Cloudflare engineer [announced](https://blog.cloudflare.com/vinext/) that **he re-implemented Next.js with AI in just one week**, naming it [vinext](https://vinext.io/).

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022809.webp)

In fact, the product prototype was generated in one day; the following days were just refinement.

> "I actually started on February 13. By that evening, the basic functionality was implemented. By the afternoon of the second day, 10 out of 11 routers were done. On the third day, it was already deployed to our servers with full client-side hydration.
>
> The following days were mainly spent on security hardening: fixing edge cases, expanding the test suite, and raising API coverage to 94%."

This new implementation actually outperforms the original Next.js.

> "In early benchmarks, build speed improved by 4x, client-side bundle size shrank by 57%, and production Next.js applications are already running directly on it."

The vinext [code](https://github.com/cloudflare/vinext) has been released.

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022810.webp)

I think **this is a huge blow to Next.js**.

Next.js is a Vercel product backed by a large development team with massive annual investment over a full 10 years. Although it's open source, the enterprise version, cloud services, plugins, and themes all cost money — last year's revenue reached $200 million.

**This seemingly unbreachable moat crumbled before AI.** One engineer, in one week, replicated the work of a large team over ten years. Existing web applications, without changing a single line of code, can be dropped onto it and run. Every feature of the original is supported.

Do you know how much it cost? Just $1,100 in token fees!

How can Vercel justify further investment in Next.js development? How can customers be willing to pay premium fees for a particular feature?

By extension, all commercial software has been severely impacted. **The code moat no longer exists. With just a small investment of money, AI can replicate large-scale software.**

So, to protect themselves, software companies will next need to prevent AI replication.

How? **The key is test cases**.

The reason the Cloudflare engineer succeeded this time is that Next.js has comprehensive documentation, a vast community of articles, and a complete test suite. Every API that AI simulates can be confirmed as 100% compatible as long as it passes the original interface tests.

Without access to test cases, who knows if the code behavior is consistent? Who would dare to run it in production?

It's conceivable that to prevent replication, large software projects will protect their test cases. **Tests are the new moat.**

![](https://cdn.beekka.com/blogimg/asset/202603/bg2026030601.webp)

The world's most popular database, [SQLite](https://sqlite.org), has 156,000 lines of code itself, but its test cases total [92.05 million lines](https://sqlite.org/testing.html) — 590 times larger!

Among them, the core test suite [TH3](https://sqlite.org/th3.html) is closed-source and not publicly released. It primarily tests extreme cases and edge scenarios for critical industries like aviation and healthcare, forming core technology assets. It's precisely these confidential test cases that make SQLite difficult to replicate.

Coincidentally, just two days ago, another open-source project, [tldraw](https://github.com/tldraw/tldraw/issues/8082), also announced plans to close-source its test suite.

![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022811.webp)

To be honest, keeping test suites confidential is certainly not conducive to the development of open-source projects. But developers need to protect their interests. In the face of increasingly powerful AI, more and more software may choose to do this.

## Copyright Issues with AI Replication

AI software replication also raises copyright issues, which have stirred [significant controversy](https://tuananh.net/2026/03/05/relicensing-with-ai-assisted-rewrite/).

![](https://cdn.beekka.com/blogimg/asset/202603/bg2026030602.webp)

Next.js uses the most permissive MIT license, so replication has no copyright issues. However, when someone replicated a project called [chardet](https://github.com/chardet/chardet), it became highly controversial.

chardet originally used the more restrictive LGPL license. After replication, it was changed to the MIT license, sparking protests from the original author.

Online opinions were divided.

Supporters said that AI only replicated the functionality and interface — the code was completely different, so changing the license was perfectly fine.

Opponents said that GPL requires all derivative works to maintain the same license. AI replication, they argued, qualifies as a derivative work.

More troublingly, US law states that AI-generated output has no copyright and belongs to the public domain. This means **AI-replicated software cannot have a license; any license attached is invalid**.

Under this law, software licenses become largely meaningless. Regardless of your license, anyone can bypass it through AI replication. AI-implemented versions would all be copyright-free.

---

https://saewitz.com/tests-are-the-new-moat

https://blog.cloudflare.com/vinext/

https://vinext.io/

https://github.com/cloudflare/vinext

SQLite code is open source, but its test suite is closed source, preventing anyone from replicating SQLite.