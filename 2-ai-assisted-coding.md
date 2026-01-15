---
title: "AI-Assisted Coding"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- How can AI be used effectively as a reference or learning aid rather than a substitute for problem-solving?
- What types of coding tasks benefit most from AI assistance?
- How should developers evaluate and validate AI-generated code, explanations, or fixes?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explain why delegating full software development to AI without understanding the solution introduces technical, ethical, and reliability risks.
- Describe appropriate roles for AI tools as assistants rather than autonomous developers.
- Use ChatGPT as a reference tool to locate, summarize, and clarify technical information more precisely than traditional search methods.
- Apply AI tools to explain unfamiliar code to support learning.
- Use AI-generated suggestions to debug code and resolve errors, while validating the proposed fixes.
- Generate boilerplate code and perform basic refactoring tasks using AI assistance.
- Use AI tools to draft technical documentation.
- Translate code between programming languages using AI assistance.
- Evaluate AI-generated code and explanations for correctness, efficiency, and alignment with project requirements.
- Analyze when AI assistance enhances productivity versus when it may obscure understanding or introduce errors.


::::::::::::::::::::::::::::::::::::::::::::::::

## Why Understanding Still Matters: The Limits of AI-Driven Software Development
(Why you shouldn't delegate the whole software development to AI without fully understanding the solution)

Scenario

You've collected some data on the animal species found within plots of land at a study site.  Your colleague wants some plots of the data as quickly as possible so that she can present them at an upcoming seminar.  You know that matplotlib is a plotting library in python but you're not quite sure how to use it, so you decide to ask AI to make the plot for you. 

Open an AI chat interface and prompt the AI to 'Generate some code to create a plot of hindfoot_length vs weight, colour by species_id. Include only species with over 100 observations. The data is in a csv file called animals.csv.  Use python and matplotlib.' 

Open anaconda navigator and launch jupyter notebooks. 

::::::::::::::::::::::::::::::::::::: callout

TODO: where this data comes from

::::::::::::::::::::::::::::::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: challenge 

Think about problems with this approach and write them in the shared document.

::::::::::::::::::::::::::::::::::::::::::::::::

Artificial intelligence tools can generate code quickly and often convincingly. For researchers who are new to programming, this can be appealing: it may seem efficient to delegate the entire task of software development to an AI system. However, doing so without understanding the solution introduces significant technical, ethical, and reliability risks.

### Technical Risks 
AI-generated code may appear correct but can contain subtle errors. These errors are particularly dangerous because:

- They may not cause obvious failures.
- They can produce plausible but incorrect results.
- They may only appear under specific conditions or data sets.

Without understanding how the code works, a researcher cannot:

- Verify that the implementation matches the intended analysis.
- Detect incorrect assumptions or inappropriate methods.
- Adapt or debug the code when results look suspicious.

In a research context, this undermines the validity and reproducibility of results.

### Reliability and Reproducibility Risks
AI systems do not reason about your research goals in the way a human collaborator would. They generate outputs based on patterns in training data, not on an understanding of your experiment, theory, or domain constraints.

As a result:

- The same prompt may produce different solutions at different times.
- Generated code may rely on undocumented assumptions.
- Dependencies, versions, or defaults may change without warning.
- If you cannot explain how your software works, you cannot reliably defend or reproduce your findings, an essential requirement of research.

### Ethical and Academic Integrity Risks 

Researchers remain fully responsible for the work they submit, publish, or use to inform decisions. Delegating development entirely to AI raises several ethical concerns:

- **Accountability**: You cannot attribute errors or misconduct to an AI system.
- **Transparency**: Reviewers and collaborators may expect you to explain your methods.
- **Misrepresentation**: Using code you do not understand may amount to overstating your expertise or control over the research process.

Relying heavily on AI may also conflict with institutional policies on research integrity or responsible use of AI.


### Appropriate Roles for AI when Writing Research Code

AI tools can be highly valuable when used correctly, as a tool to assist you with your research. The key principle is that they should function as assistants, not autonomous developers.

Appropriate uses of AI include:

- Explaining unfamiliar concepts, terminology or programming frameworks.
- Helping you to spot bugs (problems) in your code and suggesting possible fixes.
- Helping to translate ideas into a starting implementation
- Writing boilerplate code (standard structures for functions, modules etc.)
- Supporting you to write technical documentation. 

In the rest of this episode, we'll walk through these ways that AI can assist you with coding. 

## Using AI to Understand Code and Technical Concepts 

AI tools like ChatGPT can serve as an interactive reference and tutor, helping researchers understand unfamiliar coding constructs, libraries, or data analysis techniques. Unlike traditional search engines, AI can summarize and clarify technical information in context, tailored to your specific dataset, code, or research question.

### Use AI as a Reference Tool

- **Locate technical information quickly**: Instead of reading through multiple documentation pages, you can ask AI to find the relevant function, argument, or method for your task.
- **Summarize key concepts**: AI can condense long documentation into concise, understandable explanations.
- **Clarify ambiguous points**: You can follow up iteratively, asking AI to rephrase explanations, provide examples, or highlight potential pitfalls.



### Use AI to Explain Unfamiliar Code

- **Code comprehension**: Paste code generated by AI or colleagues and ask for line-by-line explanations.
- **Contextual learning**: Ask why certain functions or methods are used, what alternatives exist, and best practices.


Using AI to explain code and programming concepts can be beneficial as it can:

- Help you to access and summarise technical information faster than traditional web searches.
- Help you to learn new coding techniques by having unfamiliar code explained in context.
- Reduce cognitive load when learning new techniques by explaining code and library functions in clear, step-by-step terms, tailored to your code and dataset. 


::::::::::::::::::::::::::::::::::::: challenge 

## Up-skill rather than De-skill with AI

1. Rather than asking AI to actually generate the code for the weight vs hindfoot length plot, instead ask for a step-by-step explanation of how you would do it with your preferred technologies and packages. 
e.g. “Explain how to filter a DataFrame in Python to include only species with more than 100 observations, and then plot hindfoot_length vs weight colored by species using MatplotLib.”

2. Take the code generated in the our example (plotting hindfoot_length vs weight) and ask AI:
“Explain what each line of this Python code does and why it is needed.”
Try iteratively refining questions: if a term or method is still unclear, ask AI to provide an example, an analogy, or reference documentation.

::::::::::::::::::::::::::::::::::::::::::::::::


## Debugging and Error Analysis



## Code Generation and Refactoring

In which situations can is it appropriate for AI to generate code.


## Using AI to Support Technical Documentation

Write a docstring for the function


## Translating Code with AI

Translate from python to R

## Integrating AI Tools into IDEs

Brief paragraph on how AI tools can be integrated into IDEs and the benefits of this.  To learn more about this you can take the training on developing research software with AI.
