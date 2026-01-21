---
title: "Ethics, Reliability and Security Considerations"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are some risks of biased, inaccurate, or unreliable AI-generated outputs?
- How can the use of AI tools compromise data privacy, security, or confidentiality in research and software development?
- What intellectual property and authorship issues emerge when AI contributes to code or written work?
- What are the long-term consequences of researchers relying on AI without developing core coding skills?
- What best practices can ensure that AI is used responsibly, ethically, and transparently in research workflows?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Describe common sources of bias, inaccuracy, and unreliability in AI-generated outputs.
- Explain data privacy, confidentiality, and security risks associated with using AI tools in coding and research contexts.
- Summarize intellectual property, authorship, and citation considerations related to AI-generated code and text.
- Analyze the potential long-term consequences of researchers relying on AI tools without developing foundational coding skills.
- Examine ethical challenges introduced by AI-assisted research, including accountability, transparency, and reproducibility.
- Assess the appropriateness of AI tool usage in specific research or coding scenarios.
- Apply best practices to mitigate ethical, security, and skills-related risks when using AI in research.
- Develop personal or team-level guidelines for responsible and ethical AI use in coding and data analysis workflows.

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: callout

When using AI for coding assistance, you can imagine an AI tool as being like a fresh computer science graduate with so much enthusiasm they will never say ‘I can’t do it’, but no practical experience or broad understanding. 

::::::::::::::::::::::::::::::::::::::::::::::::

## Accuracy and Reliability of AI-Generated Code

For researchers, relying on AI-generated code carries significant risks. Incorrect code can lead to flawed results, which may compromise the validity of your research, damage your professional reputation, and even necessitate a paper retraction.

AI coding assistants can produce both random and systematic errors, threatening the reliability and reproducibility of your work. For instance, a [study conducted by researchers at Bilkent University](https://arxiv.org/pdf/2304.10778) found that GitHub Copilot generated correct code only 46.3% of the time. This underscores the danger of depending solely on AI tools for critical research tasks without careful review.

**Outdated Results**
If the AI model's training data does not contain recent developments, AI-generated code can be outdated. This can be particularly problematic in fields such as software development and scientific research, where current knowledge is critical.

For example, an AI might suggest a function from an open-source library that hasn't been well-maintained over the past few years. If the library has unpatched security flaws, these could propagate into the project.

**Unreliable Results**
AI models sometimes “hallucinate” information.  In the absence of relevant training data, a GPT model will fabricate information rather than saying it doesn't know. 

For example, an artificial intelligence might suggest an optimisation that causes a memory leak or a system crash that, if unchecked by the developer, could lead to serious system failures in production environments.

**Transparency and Explainability**: Many AI coding assistants function as “black boxes,” offering code suggestions without explaining the reasoning behind them. Without this insight, researchers may find it difficult to verify or trust the proposed solutions, increasing the risk of undetected errors propagating into experimental results.

This lack of transparency has direct implications for research reproducibility. If the logic behind AI-generated code is unclear, other researchers may be unable to replicate your methods or results, even if the code appears to run correctly. There may be subtle errors or undocumented assumptions embedded in AI-generated solutions, which can lead to inconsistencies across experiments or datasets, leading to different results and undermining confidence in your findings.


While AI can accelerate coding, researchers must critically evaluate every output, verify results against established methods, and remain vigilant to subtle errors that could compromise both research validity and professional credibility.


::::::::::::::::::::::::::::::::::::: callout

## Vibe Coding

Vibe Coding is a term used to describe AI-assisted coding without a structured plan, proper design, or architectural considerations. Decisions are made on the fly, often based on intuition or immediate needs rather than a thoughtful development strategy.

This can be fantastic for developing a quite prototype or trying out an idea. However, coding in this way can also lead to some major problems:

- Without planning the structure of your code at the start, programs are likely to become messy and confusing, and this can introduce mistakes into the code.
- Outputs are likely to appear mostly correct and, while obvious errors are usually caught, the subtle mistakes are easy to miss.
- This approach is likely to lead to problems being discovered only during the build or runtime phase instead of during design, which makes them more time-consuming and costly to fix.  

::::::::::::::::::::::::::::::::::::::::::::::::

## Data Privacy, Security Risks, and Confidentiality

**Data Privacy and Confidentiality**

AI tools such as chatGPT process and may retain user inputs.  Therefore, it's really important to be cautious that you don't accidentally share confidential code, sensitive datasets or proprietary research methods. Depending on the settings of your AI tool, the information you enter may be reused to improve the AI model and/or could resurface in future outputs, creating risks around intellectual property leakage, confidentiality breaches, or non-compliance with data protection regulations.

When AI tools run in the cloud, your code or data may be transmitted to external servers. This increases the risk of exposure during transfer or through storage breaches. Even if data is anonymised, code structure and comments can still reveal sensitive details about research methods or system design.

**Insecure AI-Generated Code**

AI assistants learn from large volumes of existing code—both good and bad. As a result, they may suggest insecure or outdated practices. A [2023 Stanford University study](https://arxiv.org/pdf/2211.03622) found that programmers who used AI assistants often produced less secure code but at the same time, felt more confident that it was secure - a risky combination!

For example, an AI tool might generate code that fails to properly validate user input, leaving the system open to issues like SQL injection or cross-site scripting. Because the code “looks right,” these problems can be missed.

**Hidden Dependencies and Security Gaps**

AI tools will often generate code that includes external libraries or frameworks without checking whether they are secure and appropriate for your use case. This could lead to vulnerabilities in your code, licensing issues, or compatibility problems, which can cause problems later and be difficult to untangle or debug. 

**Adversarial Attacks**

AI systems can also be targets for people with bad intentions. Attackers may try to influence training data or how the AI interprets user inputs so that AI tools suggest insecure patterns.  If these patterns are reused across many projects, insecure practices can spread quickly.



## Intellectual Property, Authorship, and Citation of AI-Generated Code and Text



## Ethical Considerations in AI-Assisted Research



## De-skilling and Overdependence on AI in Research Computing




## Mitigating Risks: Best Practices for Responsible AI Use in Research




## References
- [AI-Assisted Coding with Codium, Ethical and Security Considerations](https://carpentries-incubator.github.io/gen-ai-coding/3-ethical-and-security-considerations.html)
- [Perry, N., Srivastava, M., Kumar, D., & Boneh, D. (2023, November). Do users write more insecure code with ai assistants?. In Proceedings of the 2023 ACM SIGSAC conference on computer and communications security (pp. 2785-2799)](https://arxiv.org/pdf/2211.03622)
- [Yetiştiren, B., Özsoy, I., Ayerdem, M., & Tüzün, E. (2023). Evaluating the code quality of ai-assisted code generation tools: An empirical study on github copilot, amazon codewhisperer, and chatgpt. arXiv preprint arXiv:2304.10778.](https://arxiv.org/pdf/2304.10778)

