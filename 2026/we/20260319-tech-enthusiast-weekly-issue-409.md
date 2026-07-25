# Tech Enthusiast Weekly (Issue 409)

## Tools

1. [Bython](https://pypi.org/project/Bython/)

This tool uses curly braces instead of Python's indentation, suitable for programmers who don't like pressing Tab at the beginning of each line.

1. [Gitu](https://github.com/altsem/gitu)

![](https://cdn.beekka.com/blogimg/asset/202406/bg2024061705.webp)

A terminal-based Git client.

1. [Dbmate](https://github.com/amacneil/dbmate)

A lightweight database migration tool that supports various mainstream databases.

1. [lnav](https://lnav.org/)

![](https://cdn.beekka.com/blogimg/asset/202406/bg2024061901.webp)

A terminal-based log file viewer that supports searching, filtering, and querying log files.

1. [NetVentory](https://github.com/RamboRogers/netventory)

![](https://cdn.beekka.com/blogimg/asset/202412/bg2024122610.webp)

A network scanning tool that can be seen as a GUI version of nmap.

1. [Speech Note](https://github.com/mkiol/dsnote)

![](https://cdn.beekka.com/blogimg/asset/202409/bg2024091301.webp)

A Linux desktop software that can transcribe lecture audio into text and translate it into other languages.

1. [Rustpad](https://github.com/ekzhang/rustpad)

![](https://cdn.beekka.com/blogimg/asset/202409/bg2024091810.webp)

An open-source online text editor that supports real-time collaborative editing of the same document by multiple users on the web.

1. [Speed-Test](https://github.com/openspeedtest/Speed-Test)

![](https://cdn.beekka.com/blogimg/asset/202312/bg2023121002.webp)

An open-source network speed testing tool that supports all platforms. Since it can be self-hosted, it can also test intranet speeds.

1. [Wave Terminal](https://www.waveterm.dev/)

![](https://cdn.beekka.com/blogimg/asset/202403/bg2024031202.webp)

A modern, open-source terminal emulator supporting macOS and Linux.

1. [Ayllu](https://ayllu-forge.org/)

![](https://cdn.beekka.com/blogimg/asset/202312/bg2023121101.webp)

A web UI for Git repositories, used for self-hosting Git repos.

1. [Don't Fuck With Paste](https://github.com/aaronraimist/DontFuckWithPaste)

![](https://cdn.beekka.com/blogimg/asset/202403/bg2024031006.webp)

An open-source browser extension that makes input fields that block copy-paste become copy-pasteable.

9. [Timelock](https://timelock.dev/)

![](https://cdn.beekka.com/blogimg/asset/202403/bg2024031201.webp)

An open-source online tool for encrypting messages that can only be decrypted at a specified time.

## Resources

1.  [Flexport Atlas](https://www.flexport.com/atlas/)

    ![](https://cdn.beekka.com/blogimg/asset/202603/bg2026030205.webp)

    This website shows the real-time positions of large cargo ships on a map.

2.  [Plugs and Sockets Museum](https://plugsocketmuseum.nl)

    ![](https://cdn.beekka.com/blogimg/asset/202602/bg2026022701.webp)

    This website collects information about plugs and sockets from around the world.

3.  [Cure Dolly](https://kellenok.github.io/cure-script/1-the-basic-types-of-sentences.html)

    ![](https://cdn.beekka.com/blogimg/asset/202506/bg2025061601.webp)

    An English-language Japanese tutorial.

4.  [Web Browser Engineering](https://browser.engineering/index.html)

    ![](https://cdn.beekka.com/blogimg/asset/202410/bg2024101603.webp)

    A free English e-book explaining how browsers work, using Python scripts as examples to implement a simple browser.

## Images

2. [The Longest Terms of Service](https://mastodon.mit.edu/@Eggfreckles/114825126857396420)

Commercial software or websites usually have terms of service. These agreements are extremely lengthy, and no one reads them carefully.

What is the longest terms of service you have ever seen for a piece of software?

![](https://cdn.beekka.com/blogimg/asset/202509/bg2025092004.webp)

A netizen posted an image online showing that the Mac version of Slack, a group chat software, has a terms of service document that is 15.2 MB and 272,516 lines long. Is there anything longer than this?

1. [The World's Most Famous Motorcycle Photo](https://en.wikipedia.org/wiki/Rollie_Free)

In 1948, an American motorcycle racer set the world speed record on a motorcycle.

![](https://cdn.beekka.com/blogimg/asset/202504/bg2025041105.webp)

To minimize wind resistance, he wore only a helmet and swim trunks, and kept his body as horizontal as possible.

![](https://cdn.beekka.com/blogimg/asset/202504/bg2025041106.webp)

![](https://cdn.beekka.com/blogimg/asset/202504/bg2025041107.webp)

He set a record of 150.313 miles per hour. The current world record is 376.363 miles per hour, but that motorcycle has an enclosed cockpit, so the rider doesn't have to strip down.

## Abstract

1. [Why numbering should start at zero](https://www.cs.utexas.edu/~EWD/transcriptions/EWD08xx/EWD831.html)

Author: Edsger W. Dijkstra (famous computer scientist)

Consider a sequence of natural numbers from 2 to 12, which we can write as 2, 3, ..., 12.

To express this sequence in a program, we do not use the three-dot ellipsis, but rather inequalities. There are four possible ways:

> - a) 2 ≤ i < 13
> - b) 1 < i ≤ 12
> - c) 2 ≤ i ≤ 12
> - d) 1 < i < 13

Which one is better?

The answer is that a and b are better than c and d. The reason is that in a and b, the difference between the bounds equals the length of the sequence. If there is a subsequent sequence, the upper bound of one sequence equals the lower bound of the other.

Between a and b, which one is better?

Considering that there exists a smallest natural number, the lower bound can be inclusive. Therefore, a is the better choice, as it can start from the smallest natural number.

The next question is: when dealing with a sequence of length N, we want to index its elements. What subscript value should be assigned to the first element?

Following the convention of a, if we start with subscript 1, the subscript range is 1 ≤ i < N+1. However, starting from 0 gives a more precise range: 0 ≤ i < N, where the upper bound is exactly equal to the length.

Therefore, let the numbering of the sequence start from zero, so that the ordinal (subscript) of an element equals the number of elements preceding it.

## Quotes

1.

Imagine two very similar companies. They have similar revenue and produce similar software products. The only difference between these two companies is that Company A uses 1 million lines of code, while Company B uses 100,000 lines of code. Which company performs better?

Obviously, the company with fewer lines of code is better. Fewer lines of code means it can be understood and modified faster.

-- [Code is Debt](https://tornikeo.com/code-is-debt/)

1.

I let a Claude Code instance run for 24 hours, handling unexpected situations. It essentially became a 24/7 on-call engineer.

-- [An Autonomous Monitoring Agent](https://denislavgavrilov.com/p/clopus-watcher-an-autonomous-monitoring)

1.

Large models will transform you from a programmer who writes code into a programmer who manages context, eliminates irrelevant information, and writes detailed prompts.

-- [Liz Fong-Jones](https://simonwillison.net/2025/Dec/30/liz-fong-jones/)

1.

A founder who assembled the right team but built the wrong product in 2024 will, by 2027, be able to assemble a battle-hardened team to build the right product. The experience of failure is stored like nutrients in the roots, waiting for the next season, not wasted.

-- [AI Won't Crash, But It Will Go Through a Storm](https://ceodinner.substack.com/p/the-ai-wildfire-is-coming-its-going)

1.

We have become accustomed to believing in tech magic, letting GPS guide us and algorithms decide what we watch. But if GPS is wrong, I'll quickly notice the location is off; if Netflix recommends a bad movie, I'll just stop watching.

AI is different. The more advanced it is, the harder it is to know if it's wrong. We will use AI for tasks where we cannot verify them. We can only keep summoning the wizard, hoping the spell works. Welcome to the age of wizards.

-- [On Working with Wizards](https://www.oneusefulthing.org/p/on-working-with-wizards)