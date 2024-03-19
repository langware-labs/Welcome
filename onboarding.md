# Welcome to Flowpad!

🚀 **Embark on your Flowpad journey!** Flowpad is here to navigate you through the setup process, ensuring you have everything you need to get started. Once set up, you'll dive into your first tasks, equipped with guidance, executable code snippets, and scripts—all at your fingertips. Engage with our chatbot in each section for interactive learning and instant code solutions.

For a seamless experience, please tick the checkbox after completing each section. It's crucial to keep moving forward without backtracking for the smoothest user journey.

## Setup Your Development Environment

Let's kick things off by enhancing Flowpad with some powerful extensions! These tools are designed to supercharge Flowpad, offering you the ability to run code directly from the interface.

👉 Click the **Add Extension** button at the top of this page and introduce the URLs provided below—one at a time. These extensions are key to unlocking a more dynamic coding experience within Flowpad.

** Extensions to Add:**

- **Code Snippet Extension**: Allows you to execute code snippets seamlessly.
  ```url
  https://raw.githubusercontent.com/langware-labs/components/main/code-snippet/src/extensionConfig.json
  ```

- **Shell Script Extension**: Enables the execution of shell scripts directly.
  ```url
  https://raw.githubusercontent.com/langware-labs/components/main/shell-script/src/extensionConfig.json
  ```

Dive in and let Flowpad transform your coding workflow into an adventure! 🌟

### 1. Python

Python and pip installed on your system (Python 3.10 or newer is recommended).
**NOTE: run the command below to check if python is installed on your system.**

```bash
python --version
```

### 2.1. Git

If you haven't already, install Git. Git is required for cloning repositories and version control. Visit
the [official Git website](https://git-scm.com/downloads) to download and install Git for Windows or macOS.
**NOTE: run the command below to check if git is installed on your system.**

```bash
git --version
```

### 2.2. GitHub CLI
If you haven't already, install GitHub CLI tool. It streamlines the work with git. Visit
their [official GitHub website](https://cli.github.com/) to download and install GitHub CLI for Windows or macOS.
**NOTE: run the command below to check if GitHub CLI is installed on your system.**

```bash
gh --version
```

Once you have the GitHub CLI instaled, use it for authentication.
Open terminal and run the following command:

```
gh auth login
```

### 3. Node and NPM

Node.js installed on your system.** You can download it from the [official Node.js website](https://nodejs.org/).
Installing Node.js is crucial for FlowPad to run correctly.

**NOTE: run the command below to check if Node.js is installed on your system.**

```bash
node --version
```

### 4. Clone Flowpad Repository

```bash
git clone https://github.com/langware-labs/FlowPad.git
```

### 5. Environment Variables

To create a copy of the enviornment variables example, run:

```bash
cp FlowPad/flowpad/hub/.env.local.example FlowPad/flowpad/hub/.env.local
```

Note: Use your `OPENAI_API_KEY` If you don't have an OpenAI API key, you can get
one [here](https://platform.openai.com/account/api-keys).

Now go to your `.env.local` file and fill in the values.

**Configuration Table example**

When deploying the application, the following environment variables can be set:

- NOTE: Below are the necessary configuration settings for the project. All settings are required.

| Setting                   | Description                        | Required |
|---------------------------|------------------------------------|----------|
| `NEO4J_DATABASE_USERNAME` | Your Neo4j database username.      | Yes      |
| `NEO4J_DATABASE_PASS`     | Your Neo4j database password.      | Yes      |
| `NEO4J_DATABASE_DB_NAME`  | Your Neo4j database name.          | Yes      |
| `NEO4J_DATABASE_HOST`     | Your Neo4j database host address.  | Yes      |
| `NEO4J_DATABASE_PORT`     | Your Neo4j database port.          | Yes      |
| `OPENAI_API_KEY`          | Your OpenAI API key.               | Yes      |
| `DEVELOPMENT`             | `True` for dev.                    | Yes      |

Ensure you replace the placeholders with your actual configuration values before running the project.
Do not use special characters in DB_NAME.
**DB_NAME should be anything BUT `neo4j`**. e.g. `local`

~### 6. Change directory to the Flowpad folder and list the contents and create a virtual environment~

~```bash~
~cd FlowPad~
~python -m venv venv~
~source venv/bin/activate~
~ls -la~
~```~

### 7. Install Dependencies

Install the necessary packages from the requirements.txt file:

```bash
cd FlowPad
pip install -r requirements.txt
```

Navigate to the UI project folder and install the necessary npm packages:

```bash
cd Flowpad/flowpad/ui
npm install
cd -
```

### 8. Run Tests

To run the backend tests, execute:

```bash
cd FlowPad
python -m unittest flowpad/hub/tests/api/test_suite.py
python -m unittest flowpad/hub/tests/units/test_suite.py
```

To run the UI tests, execute:

```bash
cd Flowpad/flowpad/ui
npm test
```

### Congrats. You have a working environment.

### 9. Start Local App

We currently do not support opening dev environemt inside this environment.
So, for now, open a terminal.
To start the application locally, you may need to start both the backend and the frontend services. For the frontend,
you can typically start it with:

```
cd Flowpad/flowpad/ui
npm run build
npm run dev
```

For the backend, the command depends on your setup, but it might look something like this:

```
cd Flowpad
python -m flowpad.app
```

# First Tasks

Welcome to the team! We're thrilled to have you on board and excited to guide you through the initial steps to get you
up and running. This manual is designed to streamline your onboarding process, so please follow the outlined steps
carefully.

## Task 1: Obtain Counter App Code

Your first assignment involves acquiring the code for a counter app directly from our chatbot. This task is your gateway
to understanding the foundational elements of our project's ecosystem. Engage with our chatbot, request the counter app
code, and familiarize yourself with our automated systems.

## Task 2: Code to Count Langware's Tokens

As part of your integration, you are tasked with developing a script that counts all of Langware's code tokens. You
should get both our backend code and frontend code, seprately.
Frontent is in /ui, backend is all the rest.

## Task 3: Automate Source Code Documentation

Core part of Langware system is maintaining organization knowledge graph, a database which holds up to date company and
product "truth", constantly and automatically maintaining it. we call this princple "0 cost of truth". Code changes are
often representing the ground truth, i.e. none debateable status of our products, apps and system. relflecting these
changes back into our knowledge base (and hence to our arcitecture, documentation, communication) automatically is
critical knowldge transfer which will allow non-technical members stay up to date.
We would like to believe the future of just putting the entire codebase into a model and asking for architecture docs is
not that far wawy as Gemini 1.5 pro already support 1M tokens, yet for now we would like to get such decription of
flowpad, even if not complete.
The biggest challenge now is how to scan and gradually build the code documentaiton where we are likly to be limited by
context window size. we are exepcted to endup with many pieces of code docs which will rise the question how good LLMs
are in consolidating them all into one document with low effort.
your task is to write a code in python, which is completely independent to flowpad and outputs documentaiton folder, to
documentation is an architectualt documentation and should be friendly to joniors, product and program manager. The
outpuy may containing one or mode md files and the activation function signature is:

```python
def gen_doc(repo_root_folder: str, outputfolder: str | None = None):
    # if output folder is None place docs under docs subfolder of repo folder.
    pass
```

---

This manual is not just a set of tasks but a journey into our collaborative environment. Each task is designed to
enhance your understanding of our operations and prepare you for the exciting work ahead. Should you face any
difficulties, we are always ready to assist. Welcome aboard, and happy coding!
