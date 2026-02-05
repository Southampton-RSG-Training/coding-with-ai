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

![Artwork by @allison_horst, CC-BY](fig/i_would_rather_not_behold.png){alt='Cartoon of an instructor gesturing enthusiastically to a screen full of R documentation saying "BEHOLD! An amazing function!" A skeptical looking student looks on, saying "I would rather not behold...'}

This workshop aims to:

- Demonstrate how AI can assist in coding.
- Raise researchers’ awareness of the potential risks associated with AI-assisted coding.
- Provide researchers with the knowledge and understanding to critically assess when it is appropriate to use AI for coding assistance.


### Framing the Question: “What Do We Mean by AI?”

*“Any sufficiently advanced technology is indistinguishable from magic.”* - Arthur C. Clarke, a British science fiction writer, futurist, and inventor (1962)

![Arthur C. Clarke in 1965, ITU Pictures, CC BY 2.0, via Wikimedia Commons](fig/arthur_clarke.jpg){alt='photograph of Arthur C. Clarke in 1965'}

Current AI tools, like ChatGPT and Copilot, can appear almost magical.  They can generate fluent text, write code and respond to conversations in a way that seems almost human. Arthur Clarke's observation is a reminder that this appearance of magic is not evidence of mystery or sentience but of technological complexity.  These systems are built on decades of research in mathematics, statistics and computer science. 

The aim of this episode is to place AI tools in their historical and technical context, clarify what they can and cannot do, and demystify the 'magic' of AI. 

::::::::::::::::::::::::::::::::::::: challenge 

## When you hear the term “artificial intelligence”, what comes to mind?

Write your answer in the shared document.  There are no right or wrong answers!

::::::::::::::::::::::::::::::::::::::::::::::::

"Artificial intelligence (AI) is the capability of a machine or software system to perform tasks that would normally require human intelligence, such as learning from data, recognising patterns, making decisions, or generating outputs." - Merriam-Webster Dictionary.

## History of AI

Artificial intelligence is best understood not as a single capability or system, but as a broad collection of techniques and approaches for solving different kinds of problems. These techniques have been developed over the past 70 years.  Let's consider a timeline of major AI developments to put the current AI tools into historical context:


### 1950s–1970s: Rule-based Approaches

AI research began with rule-based approaches focused on logic. Rule-based systems are deterministic, in other words the same inputs always lead to the same outputs, and the rules governing behaviour are explicitly defined. The systems rely on explicitly encoded rules and struggled with anything outside of those rules. Some key milestones for early AI include Alan Turing’s 1950 paper on “Computing Machinery and Intelligence” and the 1956 Dartmouth Conference, where the term “artificial intelligence” was first introduced.

Rule-based chat AI systems existed.  An AI chatbot ELIZA was introduced in 1966 to act as a psychotherapist among other purposes.  ELIZA processes text inputs and gives a response based on the pre-programmed rules. However, ELIZA differs drastically from the generative AI chatbots we know today such as ChatGPT, because it did not have the capability to respond to any inputs outside of its pre-programmed rules.

![Public domain, via Wikimedia Commons](fig/ELIZA_conversation.png){alt='A conversation with the ELIZA chatbot.'}

### Mid-1990s–2000s: Shift to Data-driven Machine Learning

AI research moves toward statistical and data-driven methods. Rather than following fixed rules, these systems use statistical models to learn patterns from data and make predictions, classifications or risk estimates.  Their outputs support decisions but do not create new content.

One example of a predictive, data-driven system is a machine-learning model trained to automatically label features in microscope images, such as identifying specific cell types or structures.

The model learns from large sets of images that have been annotated by experts, using features like shape and texture to distinguish between categories. Once trained, it can classify new images, allowing researchers to analyse large datasets more efficiently and consistently than manual methods.

![A close-up microscope image of a growth plate, Robert M. Hunt, Public domain, via Wikimedia Commons](fig/micrograph.jpg){alt='Light micrograph of an undecalcified epiphyseal plate that is displaying the hypertrophic zone with its typical chondrocytes, matrix and three zones: maturation (top), degenerative (middle) and provisional calcification (bottom).'}


TODO:Add Deep Blue example


### 2017-Present: The Emergence and Scaling of Generative AI

The transformer model was proposed in 2017, laying the foundation for modern generative AI (Transformer is the 'T' in chatGPT). In 2018, GPT-1 demonstrated that transformer-based models trained on large amounts of text can perform a wide range of language tasks through pre-training and fine-tuning. 

In November 2022, ChatGPT was released by OpenAI and this introduced generative AI to a broad public audience through a conversational interface. Following the public release of ChatGPT, generative AI rapidly became embedded into widely used tools and platforms, including code editors, office software, search engines, and data analysis environments (e.g. AI “copilots”). 

Generative AI systems are designed to produce new outputs that resemble the data on which they were trained. This includes generating text, code, images, or other media. It's important to note that generative AI systems are statistical models that work on probabilities.  Therefore, **the same input will not always produce the same output.** 

![Jernej Furman from Slovenia, CC BY 2.0, via Wikimedia Commons](fig/smartphone_with_chatGPT.jpg){alt='Smartphone with ChatGPT on the US dollar banknotes background'}


## Current AI Landscape

Rule-based, predictive, generative AI systems are all used today and each has strengths and limitations.


| **AI System Type** | **What the system does** | **Strengths** | **Limitations** |
|-------------------|-------------------------|---------------|----------------|
| **Rule-Based & Decision Systems** | Follows clearly defined rules to allow, block, or trigger actions | Predictable and transparent; behaves the same way every time; well suited to safety-critical or regulated settings | Cannot adapt to new situations or handle uncertainty |
|  **Predictive & Analytical Systems** | Uses data to estimate categories, trends, or likelihoods | Can analyse large datasets efficiently; supports consistent analysis and forecasting | Results depend on data quality; outputs are probabilities, not final answers |
| **Generative Systems** | Creates new text, code, images, or other content | Flexible and easy to interact with; useful for drafting, coding, and exploring ideas | Outputs can sound confident but be incomplete or wrong |


**Human Oversight Across AI Systems** 

Human responsibility increases from rule-based to predictive to generative systems because more judgment, interpretation, and accountability must be carried by people rather than the system itself. 

- Rule-based systems behave exactly as specified and therefore the responsibility is mostly in system design, not in day-to-day interpretation.
- Predictive systems give estimates, not decisions and the responsibility lies with humans for interpretation and validation.
- Generative systems require the highest human responsibility at the point of use.  For example, when a researcher uses generative AI to draft text, summarise literature, or generate code, the responsibility for correctness remains entirely with the human.


## Demystifying Generative AI

### What Is GPT?

The model of generative AI that has been widespread in recent years is GPT. GPT is an AI model that can produce coherent and context-aware text, such as explanations, summaries, or responses to questions.

ChatGPT is an application built on top of GPT models. It provides a user-friendly, conversational interface to interact with the GPT model. ChatGPT is one of many tools that use GPT. 

GPT is also integrated into software products such as Microsoft’s Copilot, search engines, and coding environments. 

GPT stands for Generative Pre-trained Transformer:

- **Generative**: GPT is designed to generate new content. Rather than retrieving fixed answers from a database, it produces original outputs, such as text or code.
- **Pre-trained**: it is trained on vast amounts of data before deployment.
- **Transformer**: this refers to the internal design of the neural network that helps the system keep track of context across longer pieces of text.

### Understanding Large Language Models

Systems like GPT belong to a group called Large Language Models (LLMs). An LLM is a program that learns how language works by analysing very large collections of text. It does not store facts in a database or follow pre-programmed rules. Instead, it learns patterns in how words, sentences, and ideas tend to appear together.

LLMs are built using neural networks. In this context, a neural network provides the underlying learning machinery that allows the system to absorb information from large amounts of text and improve its predictions over time.  The type of neural network used by GPT is a transformer. The key strength of the transformer model is the ability to consider context (how different parts of a sequence relate to one another) when processing or generating information.

For example, when interpreting the meaning of a pronoun such as "it", the transformer can look back across the sentence or paragraph to determine which earlier word is most relevant. Consider the sentence "The cat ate the mouse because it was hungry." The transformer model is able to see that "it" refers to "the cat", not "the mouse".  This might seem minor, but this was a major breakthrough in AI generating coherent text.


### Tokens

GPT doesn't simply retrieve pre-written sentences, but instead builds content step by step (or token by token) and this is why it can generate such flexible and novel outputs. When GPT is building content it does so using **tokens**. A token can be a word, part of a word, or a punctuation mark. Tokens are decided on during training by merging frequently occurring character sequences until a fixed vocabulary size is reached.

Consider the sentence:

*“The dataset was cleaned.”*

Internally, the model might split this into tokens such as:`The`| ` data` | `set` | ` was` | ` clean` | `ed` | `.`

Tokens do not necessarily align with meaning or syllables because tokenisation is **statistical**, it's based on which characters tend to appear together, rather than based on any rules of language. This explains why prompts that seem similar to us humans can produce very different outputs. 

Understanding tokenisation allows us to appreciate a key limitation of GPT: the model optimises for what is **likely** to follow, not for what is **correct**, so early token-level errors can influence the rest of the response.

When you enter a prompt into GPT:

1. The model looks at the input text (the prompt) and splits it into tokens.
2. It predicts the probability of each possible next token based on all previous tokens.
3. A token is chosen based on the model’s predicted probabilities. Either the most likely token is selected, or one is sampled from the distribution of probable tokens to allow more varied or creative outputs.
4. The token is added to the growing output sequence.
5. Steps 2–4 repeat until the model produces a complete response.
6. The tokens are decoded back into human-readable text.


### How a GPT Model is Trained

1. **Data collection** - A large amount of text is gathered to train the AI model on.
2. **Model architecture design** - The neural network architecture is designed to best suit the purpose of the AI
3. **Pre-training** - The AI model is trained on the collected text.
4. **Fine-tuning** - Further training the model on specific datasets and tasks related to its purpose e.g. if it is going to be a code assistant it will be trained on tasks related to code generation. 
5. **Alignment** – Guide the model so that its outputs are helpful, safe, and in line with human intentions. This often involves human feedback to encourage responses that are accurate, reliable, and appropriate.
6. **Evaluation and iteration** - Testing the AI in a variety of use cases, getting feedback and iterating the model architecture to improve performance. 

![](fig/model_training_process_cropped.png){alt='Diagram of the 6 steps for training a GPT model'}


## Overview of AI tools that can support research coding

### AI-Assisted Coding Tools


1. **ChatGPT** – A conversational large language model by OpenAI that can generate code, explain programming concepts, assist with debugging, and support data analysis workflows.

2. **GitHub Copilot** – AI-powered coding assistant integrated into code editors, suggesting code completions, functions, and boilerplate across multiple programming languages.

3. **Google Gemini** – Google’s AI platform for research and coding assistance, capable of generating code, providing explanations, and supporting data analysis and workflow tasks.

4. **Claude** – A conversational AI by Anthropic designed to assist with coding, writing, and research tasks, providing explanations, summaries, and code generation support.

5. **Microsoft Copilot** – Integrated into Microsoft tools like Word, Excel, and Visual Studio, this AI assistant helps with code generation, data analysis, and workflow automation.


::::::::::::::::::::::::::::::::::::: callout

## Which tools are most commonly used by researchers?

In a study of 868 scientists who code as part of their research, ChatGPT was by far the most common tool used to assist with research coding, used by 64% of participants, followed by GitHub Copilot, used by 12% of participants. 

(O'Brien, G., Parker, A., Eisty, N., & Carver, J. (2025). More code, less validation: Risk factors for over-reliance on AI coding tools among scientists. arXiv preprint arXiv:2512.19644.)


::::::::::::::::::::::::::::::::::::::::::::::::

### Levels of AI-Assisted Coding

The [Oxford AI Competency Centre](https://oerc.ox.ac.uk/ai-centre/ai-guides/getting-started-with-ai-for-coding) suggest thinking about AI-Assisted Coding as existing in four levels of differing complexity and capability. 

**Level 1: Code Snippets (Copy and Paste)**
A Large Language Model inside a chatbot generates code that you copy and paste into files or environments you manage yourself. Examples: ChatGPT, Claude, Gemini, GitHub Copilot Chat

**Level 2: Canvas and Artifacts (Integrated Execution)** 
LLM writes code inside a chatbot and immediately runs it within the chat interface, creating interactive applications you can use and modify in real-time. Examples: Google Gemini, Claude Artifacts, ChatGPT Canvas

**Level 3: Agentic App Builders (Full Application Development)**
LLM-powered services that plan and execute the entire development process, from concept to deployed application, handling multiple files, frameworks, and deployment automatically. Examples: Lovable, Bolt, v0 by Vercel, Google AI Studio

**Level 4: Agentic IDEs (Professional Development)**
AI-powered development environments that assist with complex, multi-file projects, handling entire codebases, version control, and sophisticated development workflows. Examples: Cursor, GitHub Copilot, Claude Code, Google Colab


This workshop will stick to Level 1. The intermediate-level course 'Developing Research Software with AI Tools' addresses how you would work within Level 4. 



::::::::::::::::::::::::::::::::::::: challenge 

## What is your experience of using AI tools for coding?

Which AI tools have you used to help with coding so far, if any? What are your current impressions of them?

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 

- Artificial intelligence is not as a single capability or system, but as a broad collection of techniques and approaches for solving different kinds of problems.
- AI has evolved from early symbolic, rule-based systems (1950s–1970s), to data-driven machine learning, and deep learning, to modern large language models and generative AI (2017–present), culminating in tools like ChatGPT and AI-integrated software. 
- AI can be grouped into 3 broad categories: Rule-Based and Decision Systems, Predictive and Analytical Systems, and Generative Systems
- GPT (Generative Pre-trained Transformer) is a type of large language model built on transformer neural networks, which use attention to process entire sequences and capture context, enabling coherent, context-aware text or code generation.
- GPT generates content one token at a time, predicting each new token based on all previous tokens to produce fluent, contextually relevant, and novel outputs.
- GPT models are trained in stages: collecting large text datasets, designing the neural network, pre-training on broad data, fine-tuning on task-specific datasets, and iteratively evaluating and improving performance.
- ChatGPT is a user-friendly application built on GPT models, while GPT itself is also integrated into other tools like Microsoft Copilot, search engines, and coding environments.

::::::::::::::::::::::::::::::::::::::::::::::::



## References

- [S.J. Hettrick et al, UK Research Software Survey 2014](https://zenodo.org/records/1183562)
- [He, R., Cao, J., & Tan, T. (2025). Generative artificial intelligence: a historical perspective. National Science Review, 12(5), nwaf050.](https://doi.org/10.1093/nsr/nwaf050)
- [Introduction to Generative AI for Researchers](https://www.lse.ac.uk/DSI/AI/AI-Research/Introduction-to-Generative-AI-for-researchers?entryId=2319c173-7bdc-45d3-9a69-d12fd54340d7&nodeId=e2e64854-5d30-44fa-a289-a5ef76104f3e)
- [O'Brien, G., Parker, A., Eisty, N., & Carver, J. (2025). More code, less validation: Risk factors for over-reliance on AI coding tools among scientists.](https://arxiv.org/abs/2512.19644)
- [AI-assisted Coding with Codium Carpentries Course](https://carpentries-incubator.github.io/gen-ai-coding/)
- [Getting started with AI for Coding by Oxford AI Competency Centre](https://oerc.ox.ac.uk/ai-centre/ai-guides/getting-started-with-ai-for-coding)
- [Olson, P. (2024). Supremacy: AI, ChatGPT, and the Race that Will Change the World. St. Martin's Press.](https://en.wikipedia.org/wiki/Supremacy_(book))

