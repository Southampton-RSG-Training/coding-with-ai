---
title: "Setup"
---

A practical introduction to using AI to support coding in research. This course will help researchers understand how to use AI to help them write code effectively and responsibly. This course is designed for researchers with little to no experience coding.  The course provides clear, hands-on guidance for using AI to write, debug, and understand code, while addressing key ethical, security, and reliability considerations in research contexts.


## Data Sets

Download the dataset we will work with by clicking here: [animals.csv](../episodes/data/animals.csv)

Save it to your desktop or another easily accessible location. 

::::::::::::::::::::::::::::::::::::: callout

## Where does the data come from?

The data we're working with comes from the [Portal Project](https://portal.weecology.org/), a long-term ecological study being conducted near Portal, Arizona. Since 1977, the site has been used to study interactions between rodents, ants and plants.

For this workshop, we use a CSV file that is a subset of the teaching-focused Portal dataset. This version has been simplified by removing some of the complexities of the full dataset, making it more suitable for computational training and learning exercises.

::::::::::::::::::::::::::::::::::::::::::::::::

## Software Setup

### AI Tool

You need to be able to access an AI Chat tool such as [ChatGPT](https://chatgpt.com/) or Microsoft CoPilot.

### Anaconda Navigator

To run the code examples used in this workshop, you will need a way to execute Python code on your computer.

The instructor will be using **Jupyter Notebooks via Anaconda Navigator**. Unless you already have a preferred Python setup, we recommend installing **Anaconda Navigator** and running the examples using **Jupyter Notebooks** from within it. This provides a simple, self-contained environment with all required tools pre-installed.  Instructions to install Anaconda Navigator on University of Southampton computers and personal computers are in the blocks below:


:::::::::::::::: spoiler

### University of Southampton Computers

If you are using a computer provided by the University of Southampton, please use the 'Software Center' icon to download Anaconda Navigator. This icon is on the desktop of all university-managed laptops, desktops and CLS workstations used by students and staff. You can install the most common software types from this shortcut.

::::::::::::::::::::::::


:::::::::::::::: spoiler

### Personal Computers

Follow these steps to install **Anaconda Navigator** on your personal computer. The process is similar on Windows, macOS, and Linux.

### Step 1: Go to the Anaconda Website
1. Open a web browser.
2. Visit: https://www.anaconda.com/products/distribution

### Step 2: Choose the Installer
1. Click **Get Started**.
2. Select the **Anaconda Distribution** installer for your operating system:
   - **Windows**
   - **macOS**
   - **Linux**
3. Choose the **64-bit graphical installer** unless you have a specific reason to use another option.

### Step 3: Download the Installer
1. The installer file will begin downloading automatically.
2. Wait for the download to complete (this may take a few minutes).

### Step 4: Run the Installer
- **Windows**
  1. Double-click the downloaded `.exe` file.
  2. Click **Next** through the welcome screens.
  3. Accept the license agreement.
  4. Choose **Just Me** when prompted.
  5. Use the default installation location.
  6. Click **Install**.

- **macOS**
  1. Double-click the downloaded `.pkg` file.
  2. Follow the on-screen instructions.
  3. Accept the license agreement.
  4. Use the default installation settings.
  5. Click **Install** (you may be asked for your computer password).

- **Linux**
  1. Open a terminal.
  2. Navigate to the folder containing the downloaded `.sh` file.
  3. Run the installer: `bash Anaconda3-*.sh`
  4. Follow the on-screen prompts and accept the defaults.

### Step 5: Launch Anaconda Navigator
1. After installation completes, open **Anaconda Navigator**:
   - On Windows or macOS: search for *Anaconda Navigator* in your applications.
   - On Linux: run `anaconda-navigator` from the terminal.
2. Wait for the Navigator interface to load.

### Step 6: Verify Installation
1. In Anaconda Navigator, find **Jupyter Notebook**.
2. Click **Launch**.
3. If Jupyter opens in your web browser, the installation was successful.

If Anaconda Navigator does not open or you encounter issues, restarting your computer often resolves initial setup problems.


::::::::::::::::::::::::



