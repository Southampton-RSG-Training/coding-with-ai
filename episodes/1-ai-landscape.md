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

Software is increasingly critical to research - the national Software Sustainability Institute found that more than 92% of academics use research software, and 56% develop their own software. 

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

- **2017: Transformer architecture introduced**: The transformer model is proposed, enabling more effective handling of long-range context in language tasks and laying the foundation for modern large language models (Transformer is the 'T' in chatGPT)

- **2018: GPT-1 and the emergence of large language models**: GPT-1 demonstrates that transformer-based models trained on large text corpora can perform a wide range of language tasks through pre-training and fine-tuning, influencing subsequent research and development.

- **2020–2021: Scaling of large language models**: Models such as GPT-3 show that increasing model size and training data leads to qualitatively new capabilities, including few-shot learning and more fluent text generation.

- **2022: ChatGPT and mainstream adoption of generative AI**: ChatGPT introduces large language models to a broad public and professional audience through a conversational interface

- **2023–2024: Integration of generative AI into mainstream software and research infrastructure**: Following the public release of ChatGPT, large language models are rapidly embedded into widely used tools and platforms, including code editors, office software, search engines, and data analysis environments (e.g. AI “copilots”). This period marks a shift from experimental or standalone use of generative AI to routine, workflow-integrated assistance in research, coding, writing, and analysis.


## Current Landscape of AI

In recent years, one particular type of AI system, generative AI, has dominated public and professional interaction with artificial intelligence. While highly visible, generative AI represents only one approach within a much broader AI landscape. Most AI systems are designed for specific purposes, and understanding what a system is built to do is more useful than understanding its internal technical details.

At a high level, today’s AI systems can be grouped into three broad categories:

1. **Rule-Based and Decision Systems**: These systems operate using explicitly defined rules, logic, or constraints. Their behaviour is deterministic and transparent, which makes them reliable in stable, well-defined environments. Rule-based systems are still widely used in areas such as compliance, governance, and safety-critical decision-making. However, they are limited in their ability to handle ambiguity, novelty, or rapidly changing conditions.

For example, a laboratory safety interlock is an example of a rule-based system. It monitors the state of critical variables, such as door positions, pressure levels, temperature, radiation shielding, or airflow, and allows an action only if all safety conditions are met. For example, a high-power laser system may be physically prevented from firing unless the enclosure door is closed, warning lights are active, and emergency stops are disengaged. If any condition is violated, the system immediately shuts down or blocks operation.

These systems are deterministic and transparent, in other words the same inputs always lead to the same outcome and the rules governing behaviour are explicitly defined. Unlike learning-based AI systems, laboratory safety interlocks do not adapt or infer, they exist to enforce safety rules reliably, even in the presence of human error.


2. **Predictive and Analytical Systems**: These systems learn patterns from data to make predictions, classifications, or risk estimates. Rather than following fixed rules, they use statistical models to answer questions such as What category does this belong to? or How likely is this outcome? Predictive AI systems are common in research and operational settings, including data analysis, diagnostics, and forecasting. Their outputs support decisions but do not create new content.

One example of a predictive AI system is a machine-learning model trained to automatically label features in microscope images, such as identifying specific cell types or structures.

The model learns from large sets of images that have been annotated by experts, using statistical patterns like shape, texture, and intensity to distinguish between categories. Once trained, it can rapidly classify new images, allowing researchers to analyse large datasets more efficiently and consistently than manual methods.

The system provides probabilities, rather than definitive answers, as outputs and does not generate new content or biological insight. The results must be validated and interpreted by researchers, as the model's performance depends heavily on the quality of the training data and imaging conditions.

3. **Generative Systems**: Generative AI systems are designed to produce new outputs that resemble the data on which they were trained. This includes generating text, code, images, or other media. GPT and ChatGPT fall into this category, specializing in language and code generation. These systems are optimized for producing fluent and contextually appropriate responses, not for verifying truth or making authoritative decisions.

Large language models (LLMs) are examples of generative AI systems.  They are designed to process and generate human-like language by learning patterns from vast amounts of text.

They are trained to predict the next word or token in a sequence, which allows them to produce coherent text, answer questions, summarize documents, and generate code. LLMs do not possess understanding or intent. Instead, they rely on statistical associations learned during training to generate outputs. As a result, their outputs can be fluent and convincing while still being incomplete, outdated, or incorrect.

LLMs are powerful tools for supporting research tasks such as drafting, coding, and exploration of ideas, but their outputs must always be interpreted and validated by humans, particularly in contexts where accuracy, reproducibility, and accountability matter. We'll talk a lot more about this throughout this workshop. 


Most AI systems in use today are narrow, task-specific tools. Some are designed to enforce rules, others to analyze data and make predictions, and a smaller but increasingly visible group, generative systems, are designed to produce new content. Generative AI systems are powerful and influential, but they are not representative of AI as a whole. Understanding these broad categories helps researchers set appropriate expectations and prepares us to examine generative AI in more detail.


## Demystifying Generative AI

### What Is GPT?

GPT is a type of Large Language Model (LLM). This is a neural network trained on massive amounts of text data to predict and generate human-like language.

GPT stands for Generative Pre-trained Transformer:

- **Generative**: GPT is designed to generate new content. Rather than retrieving fixed answers from a database, it produces original outputs, such as text or code.
- **Pre-trained**: it is trained on vast amounts of data before deployment.
- **Transformer**: it uses a neural network architecture optimised for understanding context and sequence.

::::::::::::::::::::::::::::::::::::: callout

## What is a transformer?

A transformer is a type of neural network architecture designed specifically to work with sequences, such as sentences, paragraphs, or lines of code. Its key strength is the ability to consider context, that is, how different parts of a sequence relate to one another—when processing or generating information.

Traditional language-processing systems handled text one word at a time, in order. This made it difficult for them to keep track of long-range relationships, such as how a word at the start of a sentence relates to one at the end. Transformers address this limitation by processing all parts of a text sequence simultaneously, allowing the model to identify patterns and relationships across an entire passage at once.

The central mechanism that enables this is called attention. Attention allows the model to assign different levels of importance to different words in a sentence depending on the context. For example, when interpreting the meaning of a pronoun such as “it,” the transformer can look back across the sentence or paragraph to determine which earlier word is most relevant. This makes the model far more effective at handling complex language structures. For example, consider the sentence "The cat ate the mouse because it was hungry." Attention helps the model see that “it” refers to “the cat”, not “the mouse,” by focusing on the most relevant word in the sentence.

In practical terms, the transformer architecture is what enables systems like GPT to produce fluent, context-aware text, maintain coherence over long responses, and adapt their output to different tasks using the same underlying model. However, despite their apparent sophistication, transformers do not reason or understand language; they identify and reproduce patterns based on statistical relationships learned during training.

::::::::::::::::::::::::::::::::::::::::::::::::


GPT generates content token by token (or one piece at a time) rather than producing an entire sentence all at once.  A token can be a word, part of a word, or a punctuation mark. When you enter a prompt into GPT:

1. The model looks at the input text (the prompt) and calculates the probability of what the next token should be.
2. It selects the most likely next token.
3. That token is added to the growing output.
4. The model then considers the updated sequence, including the new token, and predicts the following token.
5. Steps 2–4 repeat until the model produces a complete response.

This sequential token generation allows GPT to produce coherent and contextually relevant text because each new token is generated based on all previous tokens in the sequence. It’s like writing a sentence one word at a time, making sure each word fits with everything written before it.

This is why GPT can generate flexible and novel outputs, rather than just retrieving pre-written sentences, it literally builds the content step by step.


### How a GPT Model is Trained

1. **Data collection** - A large amount of text is gathered to train the AI model on.
2. **Model architecture design** - The neural network architecture is designed to best suit the purpose of the AI
3. **Pre-training** - The AI model is trained on the collected text.
4. **Fine-tuning** - Further training the model on specific datasets and tasks related to its purpose e.g. if it is going to be a code assistant it will be trained on tasks related to code generation. 
5. **Evaluation and iteration** - Testing the AI in a variety of use cases, getting feedback and iterating the model architecture to improve performance. 



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

- [O'Brien, G., Parker, A., Eisty, N., & Carver, J. (2025). More code, less validation: Risk factors for over-reliance on AI coding tools among scientists.](https://arxiv.org/abs/2512.19644)
-[S.J. Hettrick et al, UK Research Software Survey 2014](https://zenodo.org/records/1183562)
