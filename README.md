# Welcome to Langware Labs

---
<details>
<summary>Installing Python on Windows and macOS</summary>

# Installing Python on Windows and macOS

This guide will walk you through the steps to install Python on your Windows or macOS computer.

<details>
<summary>For Windows Users</summary>

### Step 1: Download Python

1. Go to the official Python website at [python.org](https://python.org).
2. Hover over the `Downloads` menu, then click on `Windows`.
3. Click on the `Download Python` button (choose the version you wish to install, typically the latest version is
   recommended).

### Step 2: Install Python

1. Open the downloaded `.exe` file to start the installation.
2. Check the box next to `Add Python X.X to PATH` at the bottom of the installation window. This step is crucial as it
   allows you to run Python from the Command Prompt.
3. Click `Install Now` and follow the on-screen instructions to complete the installation.

### Step 3: Verify Installation

- Open Command Prompt and type the following command then press Enter:
  ```
  python --version
  ```
- If the installation was successful, you should see the Python version number.

</details>

<details>
<summary>For macOS Users</summary>

macOS's users have two options for installing Python: directly from the Python website or using Homebrew, a package
manager for macOS.

### Option 1: Install Python with Homebrew

#### Step 1: Install Homebrew

- Open Terminal.
- Paste the following command and press Enter:
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
- Follow the on-screen instructions to complete the Homebrew installation.

#### Step 2: Install Python

- Once Homebrew is installed, you can install Python by running:
  ```
  brew install python
  ```
- This command installs the latest version of Python.

#### Step 3: Verify Installation

- To check if Python was successfully installed, type the following command and press Enter:
  ```bash
  python3 --version
  ```
- If the installation was successful, you should see the Python version number.

### Option 2: Install Python from the Official Website

#### Step 1: Download Python

1. Go to the official Python website at [python.org](https://python.org).
2. Hover over the `Downloads` menu, then click on `macOS`.
3. Click on the `Download Python` button (choose the version you wish to install, typically the latest version is
   recommended).

#### Step 2: Install Python

1. Open the downloaded `.pkg` file to start the installation.
2. Follow the on-screen instructions to complete the installation, agreeing to the license agreement when prompted.

#### Step 3: Verify Installation

- Open Terminal and type the following command then press Enter:
  ```
  python3 --version
  ```
- If the installation was successful, you should see the Python version number.

</details>

**NOTE: This document is designed to help users install Python smoothly and efficiently on their operating systems.
Remember, Python's official documentation and the Homebrew website provide additional help and resources if you
encounter any issues during installation.**

</details>

***

<details>
<summary>Install Neo4j</summary>

### 1. Setup Environment

Ensure your development environment is prepared for the project:

- Install Java JDK if required by Neo4j.

### 2. Download and Install Neo4j

To install Neo4j, follow the official installation guide for your operating system on
the [Neo4j Download Page](https://neo4j.com/download/).

### 3. Test Connectivity to Neo4j Locally

After installing Neo4j, ensure that you can connect to your database. You can do this by opening Neo4j Browser and
connecting to the database URL, usually `bolt://localhost:7687`. If you're using a Neo4j Desktop, you can test the
connection through the application interface.

<details>
<summary>Testing Connectivity to Neo4j Locally</summary>

### Testing Connectivity to Neo4j Locally

To test the connectivity to a Neo4j database locally without the use of development languages, you can use either the
Neo4j Browser or Neo4j Desktop. These methods are straightforward and do not require programming knowledge.

### Using Neo4j Browser

The Neo4j Browser is a web-based interface that allows for querying and visualizing graph data.

1. **Access Neo4j Browser**:
   Open a web browser and navigate to `http://localhost:7474`. This assumes Neo4j is running locally with default
   settings.

2. **Login**:
   You will be prompted to enter your database connection details. The default credentials are:
    - **Username:** neo4j
    - **Password:** neo4j (you will be asked to change this upon your first login).

3. **Test Connectivity**:
   Run a simple Cypher query to verify connectivity. In the command input, type and execute:
   ```cypher
   RETURN 'Hello, World!' AS message
   ```

### Using Neo4j Desktop

Neo4j Desktop provides a convenient development environment for managing Neo4j databases.

1. **Launch Neo4j Desktop**:
   Start the Neo4j Desktop application. If you haven't installed it yet, download it from
   the [Neo4j website](https://neo4j.com/download/).

2. **Manage Databases**:
    - You can **create a new database** or **start an existing database** directly from the Neo4j Desktop.

3. **Access Neo4j Browser**:
    - Open the Neo4j Browser from within the Neo4j Desktop to connect to your database without entering connection
      details manually.

4. **Test Connectivity**:
    - Like in the web version of the Neo4j Browser, you can test the connectivity by running:
      ```cypher
      RETURN 'Hello, World!' AS message
      ```

These methods allow you to quickly verify that your local Neo4j instance is operational and accessible without needing
to write any code.

--- 

</details>

</details>


---


<details>
<summary>Install FlowPad</summary>

# FlowPad Installation Guide

FlowPad is an innovative tool designed to streamline your workflow. Follow the steps below to install and start using
FlowPad.

## Prerequisites

Before installing FlowPad, ensure you have the following prerequisites met:

- Python installed on your system (Python 3.6 or newer is recommended).
- `pip` for installing Python packages.
- Git, for cloning repositories from GitHub.

## Environment Configuration

Before running FlowPad, you must configure the following environment variables:

Note: Use your `OPENAI_API_KEY` If you don't have an OpenAI API key, you can get one [here](https://1password.com/).

<details>
<summary>For Windows</summary>
<ul>
<details>
<summary>Windows Command Prompt</summary>

```cmd
set NEO4J_DATABASE_USERNAME=<YOUR_NEO4J_DATABASE_USERNAME>
set NEO4J_DATABASE_PASS=<YOUR_NEO4J_DATABASE_PASS>
set NEO4J_DATABASE_DB_NAME=neo4j
set NEO4J_DATABASE_HOST=localhost
set NEO4J_DATABASE_PORT=7687
set OPENAI_API_KEY=<YOUR_OPEN_API_KEY>
```

</details>

<details>
<summary>Windows PowerShell</summary>

```powershell
$env:NEO4J_DATABASE_USERNAME=<YOUR_NEO4J_DATABASE_USERNAME>
$env:NEO4J_DATABASE_PASS=<YOUR_NEO4J_DATABASE_PASS>
$env:NEO4J_DATABASE_DB_NAME=neo4j
$env:NEO4J_DATABASE_HOST=localhost
$env:NEO4J_DATABASE_PORT=7687
$env:OPENAI_API_KEY=<YOUR_OPEN_API_KEY>
```

</details>
</ul>

</details>

<details>
<summary>For macOS and Linux</summary>

```bash
export NEO4J_DATABASE_USERNAME=<YOUR_NEO4J_DATABASE_USERNAME>
export NEO4J_DATABASE_PASS=<YOUR_NEO4J_DATABASE_PASS>
export NEO4J_DATABASE_DB_NAME=neo4j
export NEO4J_DATABASE_HOST=localhost
export NEO4J_DATABASE_PORT=7687
export OPENAI_API_KEY=<YOUR_OPEN_API_KEY>
```

</details>

## Create virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

## Installation Steps

1. **Install FlowPad**:

   Open a terminal or command prompt and execute the following command to install FlowPad directly from its GitHub
   repository:

   ```bash
   pip install git+https://github.com/langware-labs/flowpad.git@v0.0.6#egg=flowpad        
   ```

   This command uses `pip` to install FlowPad using the Git protocol. It clones the repository and installs it as a
   package in your Python environment.

2. **Start FlowPad**:

   After the installation completes and the environment variables are set, you can start FlowPad by running:

   ```bash
   flowpad start
   ```

   This command initializes FlowPad and opens its user interface, allowing you to begin organizing your projects and
   tasks immediately.

## Post-Installation

After starting FlowPad, you can access its features through the user interface. Explore the documentation and tutorials
available on the FlowPad website to get the most out of your new workflow tool.

</details>

