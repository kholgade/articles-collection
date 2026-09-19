# World Cup AI Companion: Baidu DuMate Hands-On

## I. Introduction

If you've been watching the World Cup recently, you may have noticed that CCTV's live program "Super Green Field" has introduced "AI Match Commentary."

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071101.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071102.webp)

The screenshots above are from the CCTV broadcast I found.

CCTV is using a Baidu AI product called "[DuMate](https://www.dumate.cn/)" to generate match introductions and tactical commentary.

I mention this because Baidu colleagues invited me to attend [WAIC](https://www.shobserver.cn/wx/detail.do?id=1143071) (World Artificial Intelligence Conference) this weekend in Shanghai. Their full-stack AI product matrix "Core Cloud Model Body" will be showcased at the conference, with the "Agent Family" featuring DuMate as a key component.

The colleagues said CCTV is using DuMate for AI match commentary and told me to look out for it during matches. Its momentum has been strong, with daily queries increasing [20-fold](https://www.qbitai.com/2026/07/447681.html).

DuMate was originally an AI office assistant, but during the World Cup, its product slogan has become "Your World Cup companion, also your daily work companion."

I was curious — can it really analyze the World Cup? What would it say?

Below are my tests, exploring how far AI match analysis has come and whether it can replace expert commentary.

## II. AI Match Analysis

I went to the official website [dumate.cn](https://www.dumate.cn/) to download the installation package. It has both desktop and mobile versions, both requiring installation.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071301.webp)

The name clearly conveys its positioning: "du" for Baidu, "mate" for companion — DuMate is Baidu's AI companion.

Note that after installation, it automatically downloads a 1.7 GB sandbox as a virtual environment for code execution, isolating it from the underlying machine for safety.

Here's its user interface:

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071201.webp)

I checked the settings but couldn't find an underlying model option, so I'm not sure which model it uses. However, it gives free daily credits — enough for light use (dozens of queries or fewer than ten simple tasks based on my testing).

I asked it to generate "Tactical analysis and post-match summary of France vs. Morocco on July 10 in the World Cup."

It defaults to searching Baidu for the latest web results.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071202.webp)

Then it generated a text version of the match analysis.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071204.webp)

Reading this much text was tiring, so I asked it to "present the above content in a visual graphical format." Below are the generated visual match overview, formation introduction, data comparison, and key player performance.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071205.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071206.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071207.webp)

I still wasn't fully satisfied — it could be richer. So I asked it to "show the process of the first goal in a tactical board animation."

Below is the generated goal demonstration:

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071208.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071209.webp)

I think the AI match analysis I could imagine is roughly what's shown above.

After the post-match analysis, I asked it to preview an upcoming match: "Provide a visual preview and tactical analysis of the France vs. Spain semi-final."

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071210.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071212.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071213.webp)

My overall feeling is that AI's level of detail and information aggregation has surpassed sports media. With AI, you might not need to read media analyses and predictions anymore. It's probably not far off that AI will commentate matches instead of human hosts.

## III. Baidu DuMate

Going back to DuMate, it's actually a very new product — just over three months old.

After OpenClaw went viral at the beginning of this year, domestic competitors emerged. DuMate was released in March 2026, after the Spring Festival.

Like OpenClaw, it's not just for AI conversations — it can automatically execute various tasks and complete operations autonomously.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071214.webp)

Above is its main menu. As you can see, its main features aren't AI conversation, but task execution, capability extension (i.e., Skills), automation, and device control. **These operational aspects are its focus — it's better suited for office work.**

It can operate your computer. According to the official website, it ranks first in two agent evaluation benchmarks (PinchBench and DeepResearch) and has passed two certifications from the China Academy of Information and Communications Technology (CAICT) — promising capability.

Next, I tested its office operation capabilities.

## IV. Office Operations

Let's start with its Office document processing — everyday tasks that shouldn't be too difficult, just to see the output quality.

### 4.1 Document Generation

First, generating an analysis report.

> Prompt: Generate an in-depth analysis Word document based on CATL's stock price trend since 2024, with both text and images.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071302.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071303.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071306.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071305.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071304.webp)

This document looks quite professional — rich in information with both arguments and evidence.

### 4.2 Spreadsheet Generation

Next, a common office scenario: organizing invoices into an expense report table.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071307.webp)

Assume there's an invoice directory with images like the one above, and ask AI to organize these into an expense report table.

> Prompt: Identify the invoice images in the current directory and organize the invoice content into an electronic spread for reimbursement.

Below is the generated invoice summary list:

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071308.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071309.webp)

This table fully meets the requirements — all invoice details have been extracted, making reimbursement extremely convenient. Very practical.

### 4.3 Slideshow Generation

Test: gather information from the web and generate a PPT.

> Prompt: Look up the 2026 World Cup top 8 and generate an analysis report predicting rankings, made into a PPT.

I'll let the screenshots speak for themselves — you can judge the accuracy of the predictions.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071215.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071216.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071217.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071218.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071219.webp)

The PPT pages seem a bit basic. Adding a page beautification Skill would make them much more attractive.

Next, I tested its Skills — which I consider its strongest selling point.

## V. Baidu Exclusive Skills

DuMate offers many Baidu-exclusive Skills that I find valuable — unavailable elsewhere.

Select "Capability Extension" from the left menu to see the Skill list.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071220.webp)

Baidu's products and services basically all have corresponding Skills: Baidu Search, Baidu Trending, Baidu Cloud, Baidu Tieba, Baidu Digital Human (Baidu Yijing)...

I first tested the "Baidu Cloud" Skill by clicking Install.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071221.webp)

After installation, I entered the prompt:

> Upload the previously generated file "2026 World Cup Top 8 Analysis and Ranking Prediction.pptx" to Baidu Cloud.

Upon receiving the prompt, DuMate first installed the Baidu Cloud command-line client "dupan," then provided a link for me to open in my browser to obtain the Baidu Cloud authorization code (shown below).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071222.webp)

After entering the authorization code back into DuMate, it automatically handled the file upload to Baidu Cloud.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071223.webp)

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071224.webp)

It's quite user-friendly. From now on, I can operate Baidu Cloud entirely through natural language.

## VI. Browser Automation

The final test was browser automation — having DuMate automatically operate a webpage.

I installed the "Baidu Tieba" skill and tried posting automatically on Tieba with the following prompt:

> Convert the file "2026 World Cup Top 8 Analysis and Ranking Prediction.pptx" into a text post and publish it to the "World Cup" section on Baidu Tieba.

DuMate first found the file, converted it to plain text, then requested a Tieba authorization token from a provided link (shown below).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071225.webp)

Below is the page for obtaining the Tieba token:

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071226.webp)

After copying this authorization code to DuMate, it could auto-post. However, it indicated that the system only allows bots to post to four designated discussion areas, not public Tieba sections (shown below).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071229.webp)

Undeterred, I wondered: if the bot simulates clicking the "Post" button on a real logged-in page, can it post?

It followed the prompt, asking me to log into Tieba in the browser first.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071228.webp)

After I logged in, it automatically operated the browser, clicking the "Post" button and filling in the post form. Below is a screenshot (the AI opened this automatically, not me).

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071231.webp)

Just as I thought it was about to succeed, it notified me that my account was blocked due to suspicious activity and couldn't post.

![](https://cdn.beekka.com/blogimg/asset/202607/bg2026071233.webp)

Well, at least this proves it can automate browser operations — the entire workflow was successful.

## VII. Conclusion

After these tests, I find DuMate paired with Skills quite useful — there's a lot it can do, and it can genuinely handle daily work tasks.

Plus, with 1,000 free credits per day, its practical value is solid.

I tested the personal version. If you use the [enterprise version](https://www.dumate.cn/#enterprise), you can also add permission controls to Skills, and all results and assets can be shared and collaborated on within teams — even more valuable for small teams.

Previously, when someone mentioned domestic OpenClaw-like products (AI work assistants), DuMate might not have come to mind. But from now on, if anyone asks about such products, I'd recommend trying [DuMate](https://www.dumate.cn).

(End)