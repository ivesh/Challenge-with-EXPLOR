## agents.py
This file contains the definition of custom agents.
To create a Agent, you need to define the following:
1. Role: The role of the agent.
2. Backstory: The backstory of the agent.
3. Goal: The goal of the agent.
4. Tools: The tools that the agent has access to (optional).
5. Allow Delegation: Whether the agent can delegate tasks to other agents(optional).

    [More Details about Agent](https://docs.crewai.com/concepts/agents).

## task.py
This file contains the definition of custom tasks.
To Create a task, you need to define the following :
1. description: A string that describes the task.
2. agent: An agent object that will be assigned to the task.
3. expected_output: The expected output of the task.

    [More Details about Task](https://docs.crewai.com/concepts/tasks).

## crew (main.py)
This is the main file that you will use to run your custom crew.
To create a Crew , you need to define Agent ,Task and following Parameters:
1. Agent: List of agents that you want to include in the crew.
2. Task: List of tasks that you want to include in the crew.
3. verbose: If True, print the output of each task.(default is False).
4. debug: If True, print the debug logs.(default is False).

    [More Details about Crew](https://docs.crewai.com/concepts/crew).

---


# Developing Guidelines with Branch

A brief description of how to work on this project together simultaneously.

## Sections in This Guide
- [Clone the Repository](#clone-the-repository)
- [Verify Git Repository](#verify-git-repository)
- [Re-Cloning the Repository](#re-cloning-the-repository)
- [Open the Repository in VS Code](#open-the-repository-in-vs-code)
- [Create a New Branch](#create-a-new-branch)
- [Make Changes and Commit](#make-changes-and-commit)
- [Push the Branch to GitHub](#push-the-branch-to-github)
- [Create a Pull Request (PR)](#create-a-pull-request-pr)

## Clone the Repository
To clone the repository:


1. Open a folder of your choice and name it `project`.
    ```bash
    git clone https://github.com/philtaboada/Challenge-with-EXPLOR

2. Run the following commands to find your current directory:

   **Windows Command Prompt:**
   ```bash
   echo %cd%
-    
    **PowerShell:**
    ```bash
    Get-Location

**Re-Cloning the Repository:**
If the .git folder is missing or you’re in the wrong directory:

- **Navigate to the parent folder:**
    ```bash
        Copy code
        cd ..
        
        
- **Remove the problematic folder:**
    ```bash
    Copy code
    rmdir /s /q Challenge_1

- **Re-clone the repository:**
    ```bash
    Copy code
    git clone https://github.com/philtaboada/Challenge-with-EXPLOR

- **Move into the cloned directory:**
    ```
    bash
    Copy code
    cd Challenge-with-EXPLOR

- **Check the Git status:**
    ```bash
    Copy code
    git status
    Open the Repository in VS Code
    After confirming the directory is a Git repository:

- **Open the folder in VS Code:**
    ```bash
    Copy code
    code .
Verify by checking the bottom-left corner of VS Code. You should see the branch name (e.g., main or feature/checking_features_built).
If it’s visible, you are in the correct directory.

- **Create a New Branch**:
To work on a new feature or task, create and switch to a new branch:
    
    ```bash
    Copy code
    git checkout -b feature/your-branch-name
    Example:
    Copy code
    git checkout -b feature/checking_features_built
    Make Changes and Commit
    Make Changes:
    Edit files using VS Code and save your changes.

- **Check the Status:**
    ```bash
    Copy code
    git status
    
- **Stage Changes:**
    ```bash
    Copy code
    git add .

- **Commit Changes:**
    ```bash
    Copy code
    git commit -m "Added new feature to check built features"
    Push the Branch to GitHub

- **Push your branch to the remote repository:**
    ```bash
    Copy code
    git push origin feature/checking_features_built
- **Create a Pull Request (PR)**
1. Go to the GitHub repository in your browser.
2. You’ll see an option to Create Pull Request for your new branch.
3. Add a Title, Description, and assign reviewers (if applicable).
-Click Submit Pull Request.

-Additional Notes
-If you still face issues: Ensure Git is installed and available in your system’s PATH.

- **Verify with:**
    ```bash
    Copy code
    git --version
If not installed, download Git from the official website.
Ensure the directory was cloned from GitHub and is not a manually copied folder.

--

You're absolutely right! Understanding the distinction between the **original repository** and the **cloned repository** (or forked repository) is critical for team collaboration. Let me add a **dedicated section** to explain this distinction and update the steps for clarity.

---

# Developing Guidelines with Branch
A comprehensive guide for team members to collaborate on this project.

---

## **Understanding the Original and Cloned Repository**

### What Is the Original Repository?
The **original repository** is the main project repository hosted on GitHub, owned by the project maintainer or organization. In this guide, the original repository is:
```
https://github.com/philtaboada/Challenge-with-EXPLOR
```
This is the **source of truth** where all approved changes will eventually be merged.

### What Is a Cloned Repository?
A **cloned repository** is a local copy of the original repository on your computer. Each team member clones the original repository to their machine to work on it locally. 

### Important Notes:
1. **You cannot directly edit the original repository** unless:
   - You are working locally on a cloned repository and pushing your changes.
   - You have been granted write access to the original repository.
2. **Changes are merged into the original repository through pull requests.**

---

## Sections in This Guide

1. [Clone the Repository](#clone-the-repository)
2. [Verify Git Repository](#verify-git-repository)
3. [Re-Cloning the Repository](#re-cloning-the-repository)
4. [Open the Repository in VS Code](#open-the-repository-in-vs-code)
5. [Create a New Branch](#create-a-new-branch)
6. [Make Changes and Commit](#make-changes-and-commit)
7. [Push the Branch to GitHub](#push-the-branch-to-github)
8. [Create a Pull Request (PR)](#create-a-pull-request-pr)
9. [Sync Your Repository with the Original Repository](#sync-your-repository-with-the-original-repository)
10. [Additional Notes](#additional-notes)

---

## Clone the Repository

1. **Open a folder** of your choice and name it `project`.
2. Clone the original repository to your local machine:
   ```bash
   git clone https://github.com/philtaboada/Challenge-with-EXPLOR
   ```

3. Navigate into the cloned directory:
   ```bash
   cd Challenge-with-EXPLOR
   ```

4. **Verify your Git setup**:
   ```bash
   git remote -v
   ```
   Expected Output:
   ```
   origin  https://github.com/philtaboada/Challenge-with-EXPLOR.git (fetch)
   origin  https://github.com/philtaboada/Challenge-with-EXPLOR.git (push)
   ```
   This confirms your cloned repository is connected to the original repository.

---

## Verify Git Repository

1. Run the following command to confirm the directory is a Git repository:
   ```bash
   git status
   ```
2. If the output shows:
   ```
   fatal: not a git repository (or any of the parent directories): .git
   ```
   This means the `.git` folder is missing. Follow the **Re-Cloning the Repository** steps below.

---

## Re-Cloning the Repository

1. Navigate to the parent directory:
   ```bash
   cd ..
   ```

2. Remove the problematic folder:
   ```bash
   rmdir /s /q Challenge_1
   ```

3. Re-clone the repository:
   ```bash
   git clone https://github.com/philtaboada/Challenge-with-EXPLOR
   ```

4. Navigate into the cloned directory:
   ```bash
   cd Challenge-with-EXPLOR
   ```

5. Confirm the repository is set up correctly:
   ```bash
   git status
   ```

---

## Open the Repository in VS Code

1. Open the cloned repository in VS Code:
   ```bash
   code .
   ```

2. Verify:
   - Check the bottom-left corner of VS Code. You should see the branch name (e.g., `main` or `feature/checking_features_built`).

---

## Create a New Branch

1. To work on a new feature or task, create and switch to a new branch:
   ```bash
   git checkout -b feature/your-branch-name
   ```

2. Push the branch to the remote repository:
   ```bash
   git push origin feature/your-branch-name
   ```

---

## Make Changes and Commit

1. **Make changes** to project files using VS Code.
2. Check the status of your changes:
   ```bash
   git status
   ```

3. Stage the changes:
   ```bash
   git add .
   ```

4. Commit your changes with a descriptive message:
   ```bash
   git commit -m "Added feature: user authentication"
   ```

---

## Push the Branch to GitHub

Push your changes to your feature branch:
```bash
git push origin feature/your-branch-name
```

---

## Create a Pull Request (PR)

1. Go to the **original repository** on GitHub.
2. Navigate to the **Pull Requests** tab and select **New Pull Request**.
3. Select:
   - **Base branch**: `main` (original repository)
   - **Compare branch**: Your feature branch
4. Add a **Title** and **Description** for the PR.
5. Submit the pull request for review.

---

## Sync Your Repository with the Original Repository

To ensure your local repository stays up-to-date with the latest changes in the original repository:

1. Add the original repository as an **upstream remote**:
   ```bash
   git remote add upstream https://github.com/philtaboada/Challenge-with-EXPLOR
   ```

2. Fetch the latest changes from the original repository:
   ```bash
   git fetch upstream
   ```

3. Merge updates from the original repository into your local `main` branch:
   ```bash
   git checkout main
   git merge upstream/main
   ```

4. Push the updated `main` branch to your fork:
   ```bash
   git push origin main
   ```

---

## Additional Notes

### Distinction Between Local, Forked, and Original Repositories
- **Local Repository**: Your Git clone on your computer.
- **Original Repository**: The main repository on GitHub (source of truth).
- **Remote Repository**: A GitHub-hosted repository you cloned or forked.

---

By adding these steps and clarifying the relationship between the original and cloned repositories, your team will better understand the process. Let me know if further adjustments are needed! 😊

