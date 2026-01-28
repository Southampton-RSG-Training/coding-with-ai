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

**Scenario**: Imagine, your research team has collected some data on the animal species found within plots of land at a study site.  

Download the data from here: [animals.csv](data/animals.csv)

The dataset is stored as a comma separated value (CSV) file. You can open the csv file in excel or a similar spreadsheet tool and have a look at the data. You'll see the variable names in the top row of the spreadsheet.   Each row holds information for a single animal, and the columns represent:


| Column           | Description                        |
| ---------------- | ---------------------------------- |
| record\_id       | Unique id for the observation      |
| month            | month of observation               |
| day              | day of observation                 |
| year             | year of observation                |
| plot\_id         | ID of a particular plot            |
| species\_id      | 2-letter code                      |
| sex              | sex of animal (“M”, “F”)           |
| hindfoot\_length | length of the hindfoot in mm       |
| weight           | weight of the animal in grams      |
| genus            | genus of animal                    |
| species          | species of animal                  |
| taxon            | e.g. Rodent, Reptile, Bird, Rabbit |
| plot\_type       | type of plot                       |

::::::::::::::::::::::::::::::::::::: callout

## Where does the data come from?

The data we're working with comes from the [Portal Project](https://portal.weecology.org/), a long-term ecological study being conducted near Portal, Arizona. Since 1977, the site has been used to study interactions between rodents, ants and plants.

For this scenario, we use a CSV file that is a subset of the teaching-focused Portal dataset. This version has been simplified by removing some of the complexities of the full dataset, making it more suitable for computational training and learning exercises.

::::::::::::::::::::::::::::::::::::::::::::::::

Your colleague wants some plots of the data as quickly as possible so that she can present them at an upcoming seminar.  You know that matplotlib is a plotting library in python but you're not quite sure how to use it, so you decide to ask AI to make the plot for you. 

Open an AI chat interface (such as ChatGPT or Microsoft CoPilot) and prompt the AI to:

'Generate some code to create a plot with weight on the x axis and hindfoot_length on the y axis, colour by species_id. Include only species with over 100 observations. The data is in a csv file called animals.csv.  Use Python and Matplotlib.' 

- Open anaconda navigator and launch jupyter notebooks. 
- Navigate to the folder where you will save your Jupyter notebook.
- Drag and drop animals.csv into this folder.
- Create a new jupyter notebook in this folder.
- Paste the AI-generated code into a code chunk in the Jupyter notebook and run the code.

We could even go one step further and upload the dataset to the AI chat so that the analysis can actually be run within the AI tool (depending on the features that you have access to with your AI tool). 

![](fig/animals_plot_chatgpt.png){alt="Screenshot of uploaded csv, chatGPT prompt, and generated plot"}

::::::::::::::::::::::::::::::::::::: challenge 

Think about problems with getting an AI tool to write your research code for you. 

Which additional problems are introduced when you also use AI to run the code?

:::::::::::::::::::::::: solution 

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

### Additional Problems with AI also Runs the Code

- When AI runs code for you, the execution environment (hardware, operating system, library versions) may be opaque, making results hard to interpret or reproduce.
- The AI can hide warnings, errors, or suspicious behavior, increasing the likelihood that flawed results go unnoticed.
- Uploading data or running code through AI systems can reduce your control over how data is handled, including where it is stored, whether it is logged or reused, and how long it is retained. Without clear guarantees, data may persist beyond its intended use, whether temporarily in memory, in logs, or in backups, creating risks for confidentiality, compliance, and ethical oversight.
- When AI both generates and executes code, researchers may be more likely to trust outputs uncritically, reducing independent verification and scrutiny.
:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::




### Appropriate Roles for AI when Writing Research Code

AI tools can be highly valuable when used correctly, as a tool to assist you with your research. The key principle is that they should function as assistants, not autonomous developers.

Appropriate uses of AI include:

- Explaining unfamiliar concepts, terminology or programming frameworks.
- Helping you to spot bugs (problems) in your code and suggesting possible fixes.
- Writing boilerplate code (standard structures for functions, modules etc.)
- Supporting you to write technical documentation. 
- Helping to translate ideas into a starting implementation or prototype

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

Scenario
A researcher has written the following Python code to plot weight vs hindfoot length by species using Matplotlib. When they try to run it, the code fails with an error.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv("animals.csv")

# Count observations per species
species_counts = df["species_id"].value_counts()

# Keep only species with >100 observations
valid_species = species_counts[species_counts > 100].index
df_filtered = df[df["species_id"].isin(valid_species)]

# Create the plot
plt.figure(figsize=(10, 6))

for species, group in df_filtered.groupby("species_id"):
    plt.scatter(
        group["weight"],
        group["hindfoot_lenght"],
        label=species,
        alpha=0.7
    )

plt.xlabel("Weight")
plt.ylabel("Hindfoot Length")
plt.title("Hindfoot Length vs Weight (Species with >100 Observations)")
plt.legend(title="Species ID")
plt.tight_layout()
plt.show()

```

```output
KeyError: 'hindfoot_lenght'
```

Rather than asking AI to “fix the code,” the researcher could use it as a debugging assistant. 

For example, the researcher could enter the prompt “I am getting a KeyError: 'hindfoot_lenght' when running the following Python code that uses pandas and matplotlib. Can you help me understand what this error means and how to diagnose it?”

This wording of the prompt will result in explanation rather than just a correction and substitution of the code and will help the researcher learn how to diagnose similar problems in future rather than becoming reliant on AI. 

In this example, AI might explain that:

- A KeyError in pandas means a column name does not exist
- The issue is likely a mismatch between the dataset’s column names and those referenced in the code

At this point, the researcher should verify this claim independently by:
- Inspecting df_clean.columns
- Comparing column names visually
- Checking for spelling inconsistencies

::::::::::::::::::::::::::::::::::::: challenge 

## AI as a Dubugging Assistant

The code below contains a different bug. Use AI to help you debug the code, then apply the fix and verify that the code runs as expected. 

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv("animal.csv")

# Count observations per species
species_counts = df["species_id"].value_counts()

# Keep only species with >100 observations
valid_species = species_counts[species_counts > 100].index
df_filtered = df[df["species_id"].isin(valid_species)]

# Create the plot
plt.figure(figsize=(10, 6))

for species, group in df_filtered.groupby("species_id"):
    plt.scatter(
        group["weight"],
        group["hindfoot_length"],
        label=species,
        alpha=0.7
    )

plt.xlabel("Weight")
plt.ylabel("Hindfoot Length")
plt.title("Hindfoot Length vs Weight (Species with >100 Observations)")
plt.legend(title="Species ID")
plt.tight_layout()
plt.show()

```
:::::::::::::::::::::::: solution 

```output
FileNotFoundError: [Errno 2] No such file or directory: 'animal.csv'
```

Prompt: I am getting the error: FileNotFoundError: [Errno 2] No such file or directory: 'animal.csv'. Can you help me understand what this error means and how to diagnose it?

The AI's output may include:
- This error is raised by Python when your code attempts to open a file that the operating system cannot locate at the specified path.
- The most common causes - the file is not in the current working directory, the filename is misspelled, the file path is incorrect, the file has not been created.

In this case the filename is misspelled as 'animal.csv' rather than 'animals.csv'.  


:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::


## Code Generation


### Boilerplate

AI can be particularly useful for some coding tasks that are tedious and repetitive such as writing boilerplate code, restructuring code into functions, and generating code documentation.

Boilerplate code is a term used to describe standard code structures that are repeated in multiple places with little variation. Examples of boilerplate code across a few different contexts include:

- Templates for function/class definitions
- Bash script skeleton
- Web page structure in HTML
- Functional component in React
- Unit test template

Using AI to generate boilerplate code can save researchers time with minimal risk, allowing them to spend their time and effort focusing on the intent of the analysis rather than the programming language's syntax. 

For example:
"Generate boilerplate code for a scatterplot using Matplotlib"

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [5, 4, 3, 2, 1]

# Create scatter plot
plt.scatter(x, y, color='blue', marker='o', label='Data Points')

# Add labels and title
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Scatter Plot Example')

# Show legend
plt.legend()

# Display the plot
plt.show()
```

After generating the boilerplate, researchers should:

- Change the variable names to match their dataset
- Confirm that they understand what the code is doing and check it matches their intent
- Treat the generated code as a starting point to build on, not a final solution



### Refactoring

Code refactoring describes restructuring existing source code, making small, incremental changes to improve its internal design, readability, and maintainability, without changing its external behaviour or functionality.

For example, once the hindfoot length vs weight plotting code is working, the researcher may notice opportunities to improve it. At the moment our code filters the data to include only species with over 100 observations.  If the researcher wanted to change the threshold for observations, the would have to edit the script directly, which is problematic for reusability of the code and reproducibility of the outputs.  Instead, they could extract the filtering code into it's own function. 

Recognising these opportunities for refactoring is a human judgment task. AI is only applied after the goal is clear.

Rather than asking ChatGPT to “rewrite the code,” you have more control over the output if you use a prompt that's specific and constrained, for example:

“Can you refactor this code to move the species-filtering logic into a small function, without changing its behaviour?”

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv("animals.csv")

# Function to filter species by minimum count
def filter_species_by_count(df, species_col, min_count=100):
    """
    Returns a DataFrame containing only species with at least min_count observations.
    
    Parameters:
        df (pd.DataFrame): Input DataFrame
        species_col (str): Name of the column containing species IDs
        min_count (int): Minimum number of observations required for a species to be kept
    
    Returns:
        pd.DataFrame: Filtered DataFrame
    """
    species_counts = df[species_col].value_counts()
    valid_species = species_counts[species_counts > min_count].index
    return df[df[species_col].isin(valid_species)]

# Filter the DataFrame
df_filtered = filter_species_by_count(df, "species_id", min_count=100)

# Create the plot
plt.figure(figsize=(10, 6))

for species, group in df_filtered.groupby("species_id"):
    plt.scatter(
        group["weight"],
        group["hindfoot_length"],
        label=species,
        alpha=0.7
    )

plt.xlabel("Weight")
plt.ylabel("Hindfoot Length")
plt.title("Hindfoot Length vs Weight (Species with >100 Observations)")
plt.legend(title="Species ID")
plt.tight_layout()
plt.show()
```

### Using AI to Support Technical Documentation

You may have noticed that when the AI generated the filter_species_by_count function, it also included documentation (a docstring) for the function. A **docstring** in Python is a short note written at the start of a function that explains what it does, what inputs the function takes, and what the function outputs.

Writing thorough code documentation can be time-consuming, which is why many scripts are left undocumented and can be hard to understand later, either by others or by yourself. AI can help by generating documentation automatically, making it faster to produce clear, understandable explanations of your code.

However, just as with any other AI-generated output, it's important to check the generated documentation.

We can evaluate the correctness of an AI-generated output using **triangulation**, the practice of verifying something with multiple sources of evidence or methods. For AI-generated code or documentation, this means cross-checking outputs in several ways to ensure they match your expectations and requirements.  

In this example, triangulation could involve:  

- Asking: *"Does the docstring accurately describe what the function actually does?"*  
- Checking that the listed parameters match the function’s arguments.  
- Confirming that any descriptions of functionality align with the actual code logic.  

Triangulation is a simple but powerful way to catch errors that have been introduced by AI misinterpretation or by subtle bugs in the code. Treat an AI-generated docstring as a guide, not a guarantee, and always verify before relying on it.  After all, it's better to have no documentation than incorrect documentation!

In short, triangulation is about **not relying on a single source of truth**, in this case the AI, but instead evaluating the results from multiple angles to reduce errors and improve reliability.  

For example, if we extract plotting code into a function like `plot_species_scatter`, we can use AI to generate a docstring, then manually check that it correctly reflects the function’s behaviour before using it.


```python
def plot_species_scatter(df, species_col="species_id", x_col="weight", y_col="hindfoot_length", min_count=100):
    df_filtered = filter_species_by_count(df, species_col, min_count)
    
    plt.figure(figsize=(10, 6))
    
    for species, group in df_filtered.groupby(species_col):
        plt.scatter(
            group[x_col],
            group[y_col],
            label=species,
            alpha=0.7
        )
    
    plt.xlabel(x_col.capitalize())
    plt.ylabel(y_col.replace("_", " ").capitalize())
    plt.title(f"{y_col.replace('_', ' ').capitalize()} vs {x_col.capitalize()} (Species with >{min_count} Observations)")
    plt.legend(title=species_col)
    plt.tight_layout()
    plt.show()
```



::::::::::::::::::::::::::::::::::::: challenge 

## Generate a Docstring

Use AI to generate a docstring for the 'plot_species_scatter' function.

If you know Python, verify that the docstring accurately represents what the code does.  If you don't know Python, read through the docstring and use it to help you understand what the function does.  

- Ask: "Does the docstring accurately describe what the function actually does?"
- Check that the listed parameters match the function’s arguments.  
- Confirm that any descriptions of functionality align with the actual code logic.  

:::::::::::::::::::::::: solution 

Prompt: Generate a docstring for the following function: 

```python
def plot_species_scatter(df, species_col="species_id", x_col="weight", y_col="hindfoot_length", min_count=100):
    df_filtered = filter_species_by_count(df, species_col, min_count)
    
    plt.figure(figsize=(10, 6))
    
    for species, group in df_filtered.groupby(species_col):
        plt.scatter(
            group[x_col],
            group[y_col],
            label=species,
            alpha=0.7
        )
    
    plt.xlabel(x_col.capitalize())
    plt.ylabel(y_col.replace("_", " ").capitalize())
    plt.title(f"{y_col.replace('_', ' ').capitalize()} vs {x_col.capitalize()} (Species with >{min_count} Observations)")
    plt.legend(title=species_col)
    plt.tight_layout()
    plt.show()
```

Example AI - generated docstring:

```python
    """
    Creates a scatter plot of two numerical variables for species with a minimum number of observations.
    
    The function filters the input DataFrame to include only species that have more than `min_count`
    observations, then plots `x_col` vs `y_col` for each species as separate scatter points with a legend.

    Parameters:
        df (pd.DataFrame): The input DataFrame containing the data.
        species_col (str, optional): Column name representing species IDs. Defaults to "species_id".
        x_col (str, optional): Column name for the x-axis values. Defaults to "weight".
        y_col (str, optional): Column name for the y-axis values. Defaults to "hindfoot_length".
        min_count (int, optional): Minimum number of observations required for a species to be included. Defaults to 100.

    Returns:
        None. Displays a matplotlib scatter plot.
    
    Example:
        >>> plot_species_scatter(df, species_col="species_id", x_col="weight", y_col="hindfoot_length", min_count=50)
    """
```


:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

### Code Generation for Rapid Prototyping

AI can allow you to generate first drafts or prototypes of code very quickly.  You can treat these as a starting point but make sure to validate everything and handcraft the final product carefully. 

It's important to write prompts that are specific and context-rich. Clearly define your requirements, including any libraries, frameworks, or constraints.

AI coding tools lack human intuition and situational awareness, so they can only produce the intended results when given detailed, explicit instructions.

It can be helpful to use an iterative process when generating code with AI tools to ensure you get the most relevant output.  This process may include:

- Breaking your task down into steps
- Creating a specific prompt
- Generating the code
- Reviewing the generated code
- If you’re not happy with the code, editing the prompt and repeating steps 3-5


::::::::::::::::::::::::::::::::::::: challenge 

## Generating code prototypes specifically and iteratively

Imagine you'd like to explore the animals dataset by visualising some other variables of your data.  You could use AI to generate first drafts of these plots quickly, before spending more time investigating the variables of interest. 

Using the animals data, create a line plot of the number of observations per year for each genus. (note: the relevant column names are `year` and `genus`).

Generate the code for a first draft of this plot.  Remember:

- Break the task down into steps.
- Craft a specific prompt including all your requirements and the libraries you want to use. 
- Review the code and run it.  
- If necessary, edit the prompt and re-generate. 

:::::::::::::::::::::::: solution 

**Break the task down into steps**

- Load the data
- Count the number of observations of each genus in each year
- Produce a line plot of the data

**Create a specific prompt**

"Generate code in Python, using the packages Pandas and MatplotLib, that will do the following: Load the data from animals.csv which is in the same folder as the code. Count the number of observations of each genus in each year. The names of these columns are 'genus' and 'year'. Produce a line plot of the number of observations of each genus, with year on the x axis and number of observations on the y axis. Each line should represent a different genus and should be differently coloured, according to a colourblind-friendly colour palette. Show the plot."

**Review and run the code**

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data from the CSV file in the same directory
df = pd.read_csv("animals.csv")

# Count the number of observations for each genus in each year
counts = (
    df.groupby(["year", "genus"])
      .size()
      .unstack(fill_value=0)
      .sort_index()
)

# Create the plot
plt.figure(figsize=(10, 6))

# Use a colorblind-friendly palette (matplotlib's 'tab10')
color_cycle = plt.get_cmap("tab10").colors

for i, genus in enumerate(counts.columns):
    plt.plot(
        counts.index,
        counts[genus],
        label=genus,
        color=color_cycle[i % len(color_cycle)]
    )

# Add labels, title, and legend
plt.xlabel("Year")
plt.ylabel("Number of Observations")
plt.title("Number of Observations per Genus by Year")
plt.legend(title="Genus")

# Improve layout
plt.tight_layout()

# Save the plot as a PNG image
plt.savefig("observations_by_genus_over_time.png", dpi=300)

# Show the plot
plt.show()

```

![](fig/observations_by_genus_over_time.png){alt="Line plot of observations by genus over time"}

The plots looks good but I'd like to save it as well.

**Edit the prompt and re-generate**

'Generate code in Python, using the packages Pandas and MatplotLib, that will do the following: Load the data from animals.csv which is in the same folder as the code. Count the number of observations of each genus in each year. The names of these columns are 'genus' and 'year'. Produce a line plot of the number of observations of each genus, with year on the x axis and number of observations on the y axis. Each line should represent a different genus and should be differently coloured, according to a colourblind-friendly colour palette. Show the plot and **also save the plot as a .png image**.'

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::



### Translating Code with AI

**Scenario**: A collaborator would like to build on the weight vs hindfoot length plotting code but he works primarily using the programming language R. Translating the code manually from python to R could be a time-intensive and error-prone task.  This is another instance where AI could be used with massive time-saving benefits:

Prompt: 'Translate this code from Python to R.'

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv("animals.csv")

# Count observations per species
species_counts = df["species_id"].value_counts()

# Keep only species with >100 observations
valid_species = species_counts[species_counts > 100].index
df_filtered = df[df["species_id"].isin(valid_species)]

# Create the plot
plt.figure(figsize=(10, 6))

for species, group in df_filtered.groupby("species_id"):
    plt.scatter(
        group["weight"],
        group["hindfoot_length"],
        label=species,
        alpha=0.7
    )

plt.xlabel("Weight")
plt.ylabel("Hindfoot Length")
plt.title("Hindfoot Length vs Weight (Species with >100 Observations)")
plt.legend(title="Species ID")
plt.tight_layout()
plt.show()

```

However, there are a few important factors to bear in mind when using AI to translate code:

1. AI might suggest a translation using a package you are unfamiliar with. Verify that it is appropriate and installed.
2. Differences in data structures can lead to subtle errors. For example, pandas.DataFrame indexing differs from R’s data.frame. Check that filters, groupings, and calculations (e.g., counting observations per species) give the same results in R as in Python.
3. Avoid blindly copying the AI output. Make sure you understand the translation so that you can troubleshoot, extend, or adapt it safely for future analyses.
4. To maintain reproducibility, keep track of both the original Python code and the AI-generated R translation. Document any changes or assumptions made during translation.
5. Be aware of AI limitations - AI can only translate syntax and structure, it cannot verify the scientific correctness of the analysis.


TODO: Challenge - which tasks will you use AI tools for when you next have to write some code for data analysis or software development?


## Integrating AI Tools into IDEs

In this episode, we have used seperate interfaces to interact with AI and to run our code.  As of 2025 this was the most common way that researchers interacted with AI for coding assistance.  However, it is also possible to integrate AI into an environment you use to write and run code (known as an Integrated Development Environment or IDE).  For example, an AI assistant called GitHub Copilot can be integrated IDEs such as Visual Studio Code.  There are some advantages and disadvantages to this integrated approach: 

### Advantages of using an IDE-Integrated AI Assistant

- **Context awareness**: Integrated AI can access the files and project structure in your IDE, making suggestions that are relevant to your current codebase.
- **Immediate feedback and autocompletion**: As well as the AI chat tool that we've been using in this session, IDE-integrated AI also offers autocompletion and code suggestions as you're typing. 
- **Seamless workflow**: You don't have to switch between windows or copy-paste code. Everything happens in one environment, which can reduce cognitive load.

### Disadvantages of using an IDE-Integrated AI Assistant

- **Limited explanation**: Unlike a standalone AI like ChatGPT, IDE-integrated AI often provides suggestions without detailed reasoning. This can reduce researchers' understanding of AI-generated code
- **Potential over-reliance**: It can be very tempting to accept AI code suggestions that appear to work, without fully understanding them, and this can lead to errors or misunderstandings about what your code does.
- **Privacy and security risks**: The AI may send code snippets to cloud services for processing. Sensitive data or unpublished research could be exposed if this is not carefully managed.


For training on IDE-integrated AI assistants see 'Developing Research Software with AI Tools'[link to course materials].  

::::::::::::::::::::::::::::::::::::: keypoints 
- Delegating full software development to AI without understanding the code introduces technical, ethical, and reliability risks.  
- AI tools should function as assistants, not autonomous developers, supporting learning, debugging, and code generation.  
- AI can be used as a reference tool to locate, summarise, and clarify technical information more efficiently than traditional search.  
- Researchers can use AI to explain unfamiliar code line by line, helping them understand programming constructs and libraries.  
- AI can assist with debugging by explaining errors and suggesting possible fixes, but researchers should independently verify solutions.  
- AI is useful for generating boilerplate code, performing basic refactoring, and drafting technical documentation, saving time on repetitive tasks.  
- AI can translate code between programming languages, but outputs must be reviewed for correctness, compatibility, and reproducibility.  
- Integrating AI into IDEs offers contextual suggestions and autocompletion, but carries risks of over-reliance, limited explanation, and potential privacy concerns.

::::::::::::::::::::::::::::::::::::::::::::::::
