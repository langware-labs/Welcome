# FOR TESTING

------

# Onboarding Manual for New Team Members

Welcome to the team! This manual will guide you through the initial setup process to get you up and running. Please follow the steps outlined below.

## 1. Install Neo4j as a Database

To install Neo4j, follow the official installation guide for your operating system on the [Neo4j Download Page](https://neo4j.com/download/).

## 2. Test the Connectivity to the Database

After installing Neo4j, ensure that you can connect to your database. You can do this by opening Neo4j Browser and connecting to the database URL, usually `bolt://localhost:7687`. If you're using a Neo4j Desktop, you can test the connection through the application interface.

## 3. Setup Environment

Ensure your development environment is prepared for the project:

- Install Java JDK if required by Neo4j.
- Ensure Python is installed for back-end services.
- Ensure Node.js is installed for front-end services.

## 4. Pip Install from requirements.txt

Navigate to your project directory and run the following command to install Python dependencies:

```bash
pip install -r requirements.txt
```

## 5. Run the Test Suites

To ensure everything is set up correctly, run the test suites for your project:

```bash
python -m unittest discover
```

## 6. Install Node.js

If you haven't already, install Node.js. You can download it from the [official Node.js website](https://nodejs.org/).

## 7. Change Directory to UI Folder and Run npm Install

Navigate to the UI project folder and install the necessary npm packages:

```bash
cd ui
npm install
```

## 8. Run the Test of UI

To run the UI tests, execute:

```bash
npm test
```

## 9. Start Local App

To start the application locally, you may need to start both the backend and the frontend services. For the frontend, you can typically start it with:

```bash
npm start
```

For the backend, the command depends on your setup, but it might look something like this:

```bash
python app.py
```

---

If you encounter any issues, please reach out to your team lead for assistance. Welcome aboard, and happy coding!