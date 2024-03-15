# Setup development environment

To add the required extensions for using Flowpad, you'll need to incorporate specific configuration details from the
provided JSON files. These configurations pertain to code snippets and shell script components, enabling enhanced
functionality in your Flowpad environment.

For detailed JSON configurations and to implement these extensions directly into your Flowpad setup, please refer to the
original sources:

- [Code Snippet Extension Configuration](https://raw.githubusercontent.com/langware-labs/components/main/code-snippet/src/extensionConfig.json)

```url
https://raw.githubusercontent.com/langware-labs/components/main/code-snippet/src/extensionConfig.json
```

- [Shell Script Extension Configuration](https://raw.githubusercontent.com/langware-labs/components/main/shell-script/src/extensionConfig.json)

```url
https://raw.githubusercontent.com/langware-labs/components/main/shell-script/src/extensionConfig.json
```

These URLs contain JSON data that defines the extensions, including their titles, descriptions, models, and view
components necessary for integration. simply copy the URLs provided and use them in the "Add Extension" button within
your Flowpad environment. This process will integrate the code snippet and shell script functionalities into your
workspace, enhancing your development capabilities with Flowpad.

Please mark the checkbox for each section after you have successfully completed it.

### 1. Python

Python and pip installed on your system (Python 3.10 or newer is recommended).
**NOTE: run the command below to check if python is installed on your system.**

```bash
python --version
```

### 2. Git

If you haven't already, install Git. Git is required for cloning repositories and version control. Visit
the [official Git website](https://git-scm.com/downloads) to download and install Git for Windows or macOS.
**NOTE: run the command below to check if git is installed on your system.**

```bash
git --version
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

### 5. Change directory to the Flowpad folder

```bash
cd FlowPad
```

### 6. Install Dependencies

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

### 7. Run Tests

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

### 8. Start Local App

To start the application locally, you may need to start both the backend and the frontend services. For the frontend,
you can typically start it with:

```bash
cd Flowpad/flowpad/ui
npm run build
npm run dev
```

For the backend, the command depends on your setup, but it might look something like this:

```bash
cd Flowpad
python python flowpad/app.py
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

The culmination of your onboarding tasks is to establish an automated system for documenting our source code. This
initiative is vital for the maintenance of our codebase's clarity and the ease of onboarding future team members.

---

This manual is not just a set of tasks but a journey into our collaborative environment. Each task is designed to
enhance your understanding of our operations and prepare you for the exciting work ahead. Should you face any
difficulties, we are always ready to assist. Welcome aboard, and happy coding!
