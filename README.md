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

Developing Guidelines with Branch
Step 1: Clone the Repository
Open a folder of your choice and name it project.
Clone this repository by following the steps below.
Find Current Directory in Windows
To locate the current working directory:

Command Prompt:
bash
Copy code
echo %cd%
PowerShell:
bash
Copy code
Get-Location
Step 2: Verify Git Repository
Check If You’re in the Correct Directory
Ensure you’re inside the directory where the repository was cloned:

bash
Copy code
cd C:\Users\Venks\Desktop\Project\Challenge_1
git status
If git status gives the error:
arduino
Copy code
fatal: not a git repository (or any of the parent directories): .git
This means the directory is not a Git repository.
Verify .git Folder
Check if the .git folder exists:

bash
Copy code
dir -Force
Look for a folder named .git. If it’s missing, follow the steps below.

Step 3: Re-Cloning the Repository
If the .git folder is missing, or you’re in the wrong directory:

Navigate to the parent folder:

bash
Copy code
cd ..
Remove the problematic folder:

bash
Copy code
rmdir /s /q Challenge_1
Re-clone the repository:

bash
Copy code
git clone https://github.com/philtaboada/Challenge-with-EXPLOR
Move into the cloned directory:

bash
Copy code
cd Challenge-with-EXPLOR
Check the Git status:

bash
Copy code
git status
Step 4: Open the Repository in VS Code
After confirming the directory is a Git repository:

Open the folder in VS Code:

bash
Copy code
code .
Verify:

Check the bottom-left corner of VS Code. You should see the branch name (e.g., main or feature/checking_features_built).
If it does, you are in the correct directory.
Step 5: Create a New Branch
To work on a new feature or task, create and switch to a new branch:

bash
Copy code
git checkout -b feature/your-branch-name
Example:
bash
Copy code
git checkout -b feature/checking_features_built
Step 6: Make Changes and Commit
Make Changes:

Edit files using VS Code and save your changes.
Check the Status:

bash
Copy code
git status
Stage Changes:

bash
Copy code
git add .
Commit Changes:

bash
Copy code
git commit -m "Added new feature to check built features"
Step 7: Push the Branch to GitHub
Push your branch to the remote repository:

bash
Copy code
git push origin feature/checking_features_built
Step 8: Create a Pull Request (PR)
Go to the GitHub repository in your browser.
You’ll see an option to Create Pull Request for your new branch.
Add a Title, Description, and assign reviewers (if applicable).
Click Submit Pull Request.
Additional Notes
If You Still Face Issues:
Ensure Git is installed and available in your system's PATH.
Verify with:
bash
Copy code
git --version