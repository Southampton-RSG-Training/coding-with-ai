---
title: "The AI Landscape"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- Where does generative AI fit within the broader historical and technical landscape of AI systems?
- How do large language models generate text, code, or explanations without understanding meaning in a human sense?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Recall key milestones in the historical development of artificial intelligence
- Describe where ChatGPT and similar large language models fit within the broader AI landscape.
- Explain, at a conceptual level, what generative AI and ChatGPT are.
- Summarize the primary functions and intended use cases of common AI coding assistants.

::::::::::::::::::::::::::::::::::::::::::::::::
## Introduction

Software is critical to research - the Software Sustainability Institute's UK Research Software Survey found that more than 92% of academics use research software, and 56% write their own code. 

For many researchers, writing code for data analysis or software development can be boring, frustrating, or intimidating.  Most researchers would rather be thinking about and researching their subject matter rather than spending lots of time learning a programming language and writing code. Therefore, with easy access to AI tools, it can be very tempting to ask AI to write your research code for you.

This workshop aims to:

- Demonstrate how AI can assist in coding.
- Raise researchers’ awareness of the potential risks associated with AI-assisted coding.
- Provide researchers with the knowledge and understanding to critically assess when it is appropriate to use AI for coding assistance.


### Framing the Question: “What Do We Mean by AI?”

“Any sufficiently advanced technology is indistinguishable from magic.” - Arthur C. Clarke, a British science fiction writer, futurist, and inventor (1962)

Current AI tools, like ChatGPT and Copilot, can appear almost magical.  They can generate fluent text, write code and respond to conversations in a way that seems almost human. Arthur Clarke's observation is a reminder that this appearance of magic is not evidence of mystery or sentience but of technological complexity.  These systems are built on decades of research in mathematics, statistics and computer science. 

The aim of this episode is to place AI tools in their historical and technical context, clarify what they can and cannot do, and demystify the 'magic' of AI. 

::::::::::::::::::::::::::::::::::::: challenge 

## When you hear the term “artificial intelligence”, what comes to mind?

Write your answer in the shared document.  There are no right or wrong answers!

::::::::::::::::::::::::::::::::::::::::::::::::

"Artificial intelligence (AI) is the capability of a machine or software system to perform tasks that would normally require human intelligence, such as learning from data, recognising patterns, making decisions, or generating outputs." - Merriam-Webster Dictionary.

## History of AI

Artificial intelligence is best understood not as a single capability or system, but as a broad collection of techniques and approaches for solving different kinds of problems. These techniques have been developed over the past 70 years.  Let's consider a timeline of major AI developments to put the current AI tools in historical context:


- **1950s–1970s: Symbolic AI and early expert systems**: AI research begins with symbolic, rule-based approaches focused on logic, search, and reasoning. Key moments include Alan Turing’s 1950 paper “Computing Machinery and Intelligence” and the 1956 Dartmouth Conference, where the term “artificial intelligence” was coined. Systems relied on explicitly encoded rules and struggled outside narrowly defined domains.

- **1980s–early 1990s: Expert systems and the first AI boom (and bust)**: Rule-based expert systems are adopted in industry (e.g. medical diagnosis, configuration systems). Progress stalls due to high development costs, limited scalability, and lack of data, leading to periods known as “AI winters”.

- **Mid-1990s–2000s: Shift to data-driven machine learning**: AI research moves toward statistical and data-driven methods. Machine learning models learn patterns from data rather than relying on hard-coded rules. Common applications include classification, prediction, clustering, and recommendation systems. Increased availability of digital data and improved computing infrastructure drive adoption.

- **2010–2015: Deep learning resurgence**: Advances in neural networks, combined with GPUs and large labelled datasets, lead to major breakthroughs in computer vision, speech recognition, and natural language processing. Deep learning becomes the dominant paradigm for many AI tasks.

- **2017-2021: The emergence and scaling of large language models**: The transformer model is proposed in 2017, laying the foundation for modern large language models (Transformer is the 'T' in chatGPT). In 2018, GPT-1 demonstrates that transformer-based models trained on large text corpora can perform a wide range of language tasks through pre-training and fine-tuning.  In 2020, more fluent text generation.

- **2022-present: ChatGPT and mainstream adoption of generative AI**: In November 2022, ChatGPT introduces large language models to a broad public and professional audience through a conversational interface. Following the public release of ChatGPT, large language models are rapidly embedded into widely used tools and platforms, including code editors, office software, search engines, and data analysis environments (e.g. AI “copilots”). 

![](fig/timeline.png){alt='timeline of key events in AI development'}

## Current Landscape of AI

In recent years, one particular type of AI system, generative AI, has dominated public and professional interaction with artificial intelligence. While highly visible, generative AI represents only one approach within a much broader AI landscape. Most AI systems are designed for specific purposes, and understanding what a system is built to do is more useful than understanding its internal technical details.

At a high level, today’s AI systems can be grouped into three broad categories:

1. **Rule-Based and Decision Systems**: These systems operate using explicitly defined rules, logic, or constraints. Their behaviour is deterministic and transparent, which makes them reliable in stable, well-defined environments. Rule-based systems are still widely used in areas such as compliance, governance, and safety-critical decision-making. However, they are limited in their ability to handle ambiguity, novelty, or rapidly changing conditions.

For example, a laboratory safety interlock is an example of a rule-based system. It monitors the state of critical variables, such as door positions, pressure levels, temperature, radiation shielding, or airflow, and allows an action only if all safety conditions are met. For example, a high-power laser system may be physically prevented from firing unless the enclosure door is closed, warning lights are active, and emergency stops are disengaged. If any condition is violated, the system immediately shuts down or blocks operation.

These systems are deterministic and transparent, in other words the same inputs always lead to the same outcome and the rules governing behaviour are explicitly defined. Unlike learning-based AI systems, laboratory safety interlocks do not adapt or infer, they exist to enforce safety rules reliably, even in the presence of human error.

Rule-based chat AI systems existed.  An AI chatbot ELIZA was introduced in 1966 to act as a psychotherapist.  ELIZA processes inputted text and gives a response based on the pre-programmed rules. However, for real-world applications there will always be situations outside the pre-designed rules, which a rule-based AI will not have the capability to respond to. 



2. **Predictive and Analytical Systems**: These systems learn patterns from data to make predictions, classifications, or risk estimates. Rather than following fixed rules, they use statistical models to answer questions such as 'What category does this belong to?' or 'How likely is this outcome?' Predictive AI systems are common in research and operational settings, including data analysis, diagnostics, and forecasting. Their outputs support decisions but do not create new content.

One example of a predictive AI system is a machine-learning model trained to automatically label features in microscope images, such as identifying specific cell types or structures.

The model learns from large sets of images that have been annotated by experts, using statistical patterns like shape, texture, and intensity to distinguish between categories. Once trained, it can rapidly classify new images, allowing researchers to analyse large datasets more efficiently and consistently than manual methods.

The system provides probabilities, rather than definitive answers, as outputs and does not generate new content or biological insight. The results must be validated and interpreted by researchers, as the model's performance depends heavily on the quality of the training data and imaging conditions.

3. **Generative Systems**: Generative AI systems are designed to produce new outputs that resemble the data on which they were trained. This includes generating text, code, images, or other media. The current AI systems that we are familiar with, such as ChatGPT, fall into this category. These systems are optimised for producing fluent and contextually appropriate responses, not for verifying truth or making authoritative decisions.

Large language models (LLMs) are examples of generative AI systems.  They are designed to process and generate human-like language by learning patterns from vast amounts of text.

They are trained to predict the next word or token in a sequence, which allows them to produce coherent text, answer questions, summarize documents, and generate code. LLMs do not possess understanding or intent. Instead, they rely on statistical associations learned during training to generate outputs. As a result, their outputs can be fluent and convincing while still being incomplete, outdated, or incorrect.

LLMs are powerful tools for supporting research tasks such as drafting, coding, and exploration of ideas, but their outputs must always be interpreted and validated by humans, particularly in contexts where accuracy, reproducibility, and accountability matter. We'll talk a lot more about this throughout this workshop. 

Most AI systems in use today are narrow, task-specific tools. Some are designed to enforce rules, others to analyze data and make predictions, and a smaller but increasingly visible group, generative systems, are designed to produce new content. Generative AI systems are powerful and influential, but they are not representative of AI as a whole. Hopefully, understanding these broad categories helps us to set appropriate expectations for AI and prepares us to examine generative AI in more detail.

| **AI System Type** | **What the system does** | **Strengths** | **Limitations** |
|-------------------|-------------------------|---------------|----------------|
| **Rule-Based & Decision Systems** | Follows clearly defined rules to allow, block, or trigger actions | Predictable and transparent; behaves the same way every time; well suited to safety-critical or regulated settings | Cannot adapt to new situations or handle uncertainty |
|  **Predictive & Analytical Systems** | Uses data to estimate categories, trends, or likelihoods | Can analyse large datasets efficiently; supports consistent analysis and forecasting | Results depend on data quality; outputs are probabilities, not final answers |
| **Generative Systems** | Creates new text, code, images, or other content | Flexible and easy to interact with; useful for drafting, coding, and exploring ideas | Outputs can sound confident but be incomplete or wrong |


**Human Oversight Across AI Types** 

Human responsibility increases from rule-based to predictive to generative systems because more judgment, interpretation, and accountability must be carried by people rather than the system itself. 

- Rule-based systems behave exactly as specified and therefore the responsibility is mostly in system design, not in day-to-day interpretation.
- Predictive systems give estimates, not decisions and the responsibility lies with humans for interpretation and validation.
- Generative systems require the highest human responsibility at the point of use.  For example, when a researcher uses generative AI to draft text, summarise literature, or generate code, the responsibility for correctness remains entirely with the human.



## Demystifying Generative AI

### What Is GPT?

GPT is a computer model designed to work with written language. It can produce text that reads as coherent and context-aware, such as explanations, summaries, or responses to questions.

Systems like GPT belong to a group called Large Language Models (LLMs). An LLM is a program that learns how language works by analysing very large collections of text. It does not store facts in a database or follow pre-programmed rules. Instead, it learns patterns in how words, sentences, and ideas tend to appear together.

LLMs are built using neural networks. In this context, a neural network provides the underlying learning machinery that allows the system to absorb information from large amounts of text and improve its predictions over time.

::::::::::::::::::::::::::::::::::::: callout

## What is a neural network?

A neural network is a type of computational model inspired by how the human brain processes information. The name comes from its loose resemblance to brain cells (called neurons), but it is not a biological model of the brain.

Instead, a neural network is built from many simple processing units, called neurons, that pass information to one another in stages. Each neuron receives inputs, applies a simple rule to transform them, and then passes the result forward. By stacking many of these stages on top of each other, the system can learn complex patterns in data.

Learning in a neural network happens gradually as the network adjusts how strongly the neurons influence each other so that its outputs become more accurate over time.

::::::::::::::::::::::::::::::::::::::::::::::::

GPT stands for Generative Pre-trained Transformer:

- **Generative**: GPT is designed to generate new content. Rather than retrieving fixed answers from a database, it produces original outputs, such as text or code.
- **Pre-trained**: it is trained on vast amounts of data before deployment.
- **Transformer**: this refers to the internal design of the neural network that helps the system keep track of context across longer pieces of text.

::::::::::::::::::::::::::::::::::::: callout

## What is a transformer?

A transformer is a type of neural network architecture designed specifically to work with sequences, such as sentences, paragraphs, or lines of code. Its key strength is the ability to consider context, that is, how different parts of a sequence relate to one another—when processing or generating information.

Traditional language-processing systems handled text one word at a time, in order. This made it difficult for them to keep track of long-range relationships, such as how a word at the start of a sentence relates to one at the end. Transformers address this limitation by processing all parts of a text sequence simultaneously, allowing the model to identify patterns and relationships across an entire passage at once.

The central mechanism that enables this is called attention. Attention allows the model to assign different levels of importance to different words in a sentence depending on the context. For example, when interpreting the meaning of a pronoun such as “it,” the transformer can look back across the sentence or paragraph to determine which earlier word is most relevant. This makes the model far more effective at handling complex language structures. For example, consider the sentence "The cat ate the mouse because it was hungry." Attention helps the model see that “it” refers to “the cat”, not “the mouse,” by focusing on the most relevant word in the sentence.

In practical terms, the transformer architecture is what enables systems like GPT to produce fluent, context-aware text, maintain coherence over long responses, and adapt their output to different tasks using the same underlying model. However, despite their apparent sophistication, transformers do not reason or understand language; they identify and reproduce patterns based on statistical relationships learned during training.

::::::::::::::::::::::::::::::::::::::::::::::::


GPT generates content **token by token**, rather than producing an entire sentence all at once. A token can be a word, part of a word, or a punctuation mark. When you enter a prompt into GPT:

1. The model looks at the input text (the prompt) and splits it into tokens.
2. It predicts the probability of each possible next token based on all previous tokens.
3. A token is chosen based on the model’s predicted probabilities. Either the most likely token is selected, or one is sampled from the distribution of probable tokens to allow more varied or creative outputs.
4. The token is added to the growing output sequence.
5. Steps 2–4 repeat until the model produces a complete response.
6. The tokens are decoded back into human-readable text.

This sequential token generation allows GPT to produce coherent and contextually relevant text because each new token is generated in the context of all previous tokens. It’s like writing a sentence one word at a time, making sure each word fits with everything written before it.

As you can now understand, GPT doesn't simply retrieve pre-written sentences, but instead builds content step by step and this is why it can generate such flexible and novel outputs. 

::::::::::::::::::::::::::::::::::::: callout

## What is a token?

A **token** is the basic unit of text that a GPT model processes and generates. Tokens are not always whole words. They may be a full word (e.g. `data`), part of a word (e.g. `clean` + `ed`), numbers, symbols, or punctuation (e.g. `.`, `,`, `(`).

Consider the sentence:

*“The dataset was cleaned.”*

Internally, the model might split this into tokens such as:`The`| ` data` | `set` | ` was` | ` clean` | `ed` | `.`

Large language models do not decide how to split words dynamically. Instead, tokenisation is fixed in advance by a tokeniser created before training. Most GPT-style models use subword tokenisation methods such as Byte Pair Encoding (BPE) or similar approaches, which merge frequently occurring character sequences until a fixed vocabulary size is reached.

Common words are typically single tokens (e.g. `data`), while less common or more complex words are split into subword tokens (e.g. `token` + `isation`). This allows the model to handle new or rare words by recombining familiar pieces rather than requiring a unique token for every word.

Tokens do not necessarily align with meaning or syllables because tokenisation is **statistical** rather than **linguistic**. This explains why prompts that seem similar to us humans can produce very different outputs. 

Understanding tokenisation allows us to appreciate a key limitation of GPT: the model optimises for what is **likely** to follow, not for what is **correct**, so early token-level errors can influence the rest of the response.

::::::::::::::::::::::::::::::::::::::::::::::::


### How a GPT Model is Trained

1. **Data collection** - A large amount of text is gathered to train the AI model on.
2. **Model architecture design** - The neural network architecture is designed to best suit the purpose of the AI
3. **Pre-training** - The AI model is trained on the collected text.
4. **Fine-tuning** - Further training the model on specific datasets and tasks related to its purpose e.g. if it is going to be a code assistant it will be trained on tasks related to code generation. 
5. **Alignment** – Guide the model so that its outputs are helpful, safe, and in line with human intentions. This often involves human feedback to encourage responses that are accurate, reliable, and appropriate.
6. **Evaluation and iteration** - Testing the AI in a variety of use cases, getting feedback and iterating the model architecture to improve performance. 



### ChatGPT vs GPT

ChatGPT is an application built on top of GPT models. It provides a user-friendly, conversational interface to interact with the GPT model. 

ChatGPT is one of many tools that use GPT. 

GPT is also integrated into software products such as Microsoft’s copilot, search engines, and coding environments. 


## Overview of AI tools that can support research coding


1. **ChatGPT** – A conversational large language model by OpenAI that can generate code, explain programming concepts, assist with debugging, and support data analysis workflows.

2. **GitHub Copilot** – AI-powered coding assistant integrated into code editors, suggesting code completions, functions, and boilerplate across multiple programming languages.

3. **Google Gemini** – Google’s AI platform for research and coding assistance, capable of generating code, providing explanations, and supporting data analysis and workflow tasks.

4. **Claude** – A conversational AI by Anthropic designed to assist with coding, writing, and research tasks, providing explanations, summaries, and code generation support.

5. **Microsoft Copilot** – Integrated into Microsoft tools like Word, Excel, and Visual Studio, this AI assistant helps with code generation, data analysis, and workflow automation.


The [Oxford AI Competency Centre](https://oerc.ox.ac.uk/ai-centre/ai-guides/getting-started-with-ai-for-coding) suggest thinking about AI-Assisted Coding as existing in four levels of differing complexity and capability. 

**Level 1: Code Snippets (Copy and Paste)**
A Large Language Model inside a chatbot generates code that you copy and paste into files or environments you manage yourself. Examples: ChatGPT, Claude, Gemini, GitHub Copilot Chat

**Level 2: Canvas and Artifacts (Integrated Execution)** 
LLM writes code inside a chatbot and immediately runs it within the chat interface, creating interactive applications you can use and modify in real-time. Examples: Google Gemini, Claude Artifacts, ChatGPT Canvas

**Level 3: Agentic App Builders (Full Application Development)**
LLM-powered services that plan and execute the entire development process, from concept to deployed application, handling multiple files, frameworks, and deployment automatically. Examples: Lovable, Bolt, v0 by Vercel, Google AI Studio

**Level 4: Agentic IDEs (Professional Development)**
AI-powered development environments that assist with complex, multi-file projects, handling entire codebases, version control, and sophisticated development workflows. Examples: Cursor, GitHub Copilot, Claude Code, Google Colab


This workshop will stick to Level 1. Our intermediate course 'Developing Research Software with AI Tools' addresses how you would work within Level 4. 


::::::::::::::::::::::::::::::::::::: callout

## Which tools are most commonly used by researchers?

In a study of 868 scientists who code as part of their research, ChatGPT was by far the most common tool used to assist with research coding, used by 64% of participants, followed by GitHub Copilot, used by 12% of participants. 

(O'Brien, G., Parker, A., Eisty, N., & Carver, J. (2025). More code, less validation: Risk factors for over-reliance on AI coding tools among scientists. arXiv preprint arXiv:2512.19644.)


::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: challenge 

## Which AI tools have you used so far, if any? What are your current impressions of them - what worked well, and what challenges or limitations did you notice?

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 

- Artificial intelligence is not as a single capability or system, but as a broad collection of techniques and approaches for solving different kinds of problems.
- AI has evolved from early symbolic, rule-based systems (1950s–1970s), to data-driven machine learning, and deep learning, to modern large language models and generative AI (2017–present), culminating in tools like ChatGPT and AI-integrated software. 
- AI can be grouped into 3 broad categories: Rule-Based and Decision Systems, Predictive and Analytical Systems, and Generate Systems
- GPT (Generative Pre-trained Transformer) is a type of large language model built on transformer neural networks, which use attention to process entire sequences and capture context, enabling coherent, context-aware text or code generation.
- GPT generates content one token at a time, predicting each new token based on all previous tokens to produce fluent, contextually relevant, and novel outputs.
- GPT models are trained in stages: collecting large text datasets, designing the neural network, pre-training on broad data, fine-tuning on task-specific datasets, and iteratively evaluating and improving performance.
- ChatGPT is a user-friendly application built on GPT models, while GPT itself is also integrated into other tools like Microsoft Copilot, search engines, and coding environments.

::::::::::::::::::::::::::::::::::::::::::::::::



## References

-[S.J. Hettrick et al, UK Research Software Survey 2014](https://zenodo.org/records/1183562)
- [He, R., Cao, J., & Tan, T. (2025). Generative artificial intelligence: a historical perspective. National Science Review, 12(5), nwaf050.](https://doi.org/10.1093/nsr/nwaf050)
- [Introduction to Generative AI for Researchers](https://www.lse.ac.uk/DSI/AI/AI-Research/Introduction-to-Generative-AI-for-researchers?entryId=2319c173-7bdc-45d3-9a69-d12fd54340d7&nodeId=e2e64854-5d30-44fa-a289-a5ef76104f3e)
- [O'Brien, G., Parker, A., Eisty, N., & Carver, J. (2025). More code, less validation: Risk factors for over-reliance on AI coding tools among scientists.](https://arxiv.org/abs/2512.19644)
- [AI-assisted Coding with Codium Carpentries Course](https://carpentries-incubator.github.io/gen-ai-coding/)
- [Getting started with AI for Coding by Oxford AI Competency Centre](https://oerc.ox.ac.uk/ai-centre/ai-guides/getting-started-with-ai-for-coding)
- [Olson, P. (2024). Supremacy: AI, ChatGPT, and the Race that Will Change the World. St. Martin's Press.](https://en.wikipedia.org/wiki/Supremacy_(book))

