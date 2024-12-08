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



